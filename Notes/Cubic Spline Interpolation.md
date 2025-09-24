---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Interpolation and Polynomial Approximation]], [[Neville's Method]], [[Newton's Divided Difference]], [[Hermite Interpolation]]

A lot of problems with Hermite interpolation, Newton's divided difference, or Lagrange interpolation is that they are not very stable with a small change in the points, can make really big change in the function. 
## Piecewise-Polynomial Approximation
The simplest piecewise-polynomial approximation is *piecewise-linear* interpolation, which consists of joining a set of data points 
$$
\{(x_0, f(x_0)), (x_1, f(x_1)),\dots, (x_n, f(x_n)) \}
$$
by a series of straight lines. This approach has its problems because it is not really differentiable on the interval $[x_0, x_n]$. 

```julia
function linear_interpolation(x_values, y_values, x; sorted=false)
	n = length(x_values)
	if n != length(y_values)
		error("The input data x_values and y_values have different lengths")
	end

	# Ensure x_values is sorted
	if !sorted
		pairs_of_values = sort(hcat(x_values, y_values), dims=1)
	else
		pairs_of_values = hcat(x_values, y_values)
	end

	# Find the index of the interval where x lies
	index = searchsortedfirst(pairs_of_values[:, 1], x)

	# Perform linear interpolation
	if index == 1
		y = pairs_of_values[1, 2]
	elseif index == n + 1
		y = pairs_of_values[n, 2]
	else
		x0, y0 = pairs_of_values[index, :]
		x1, y1 = pairs_of_values[index + 1, :]
		y = y0 + (y1 - y0) * (x - x0) / (x1 - x0)
	end

	return y
end
```

### Cubic Splines

The most common piecewise-polynomial approximation uses cubic polynomials between each successive pair  of nodes is called *cubic spline interpolation*. A general cubic polynomial involves four constants, so there is enough flexibility in the cubic spline procedure to ensure that the interpolant not only is continuously differentiable on the interval but also has a continuous second derivative. 

**Def:** Given a function $f$ defined on $[a.b]$ and a set of nodes $a= x_0 <x_1< \dots < x_n = b$, a *cubic spline interpolant $S$* for $f$ is a function that satisfies the following conditions:
- $S(x)$ is a cubic polynomial, denoted $S_j(x)$, on the subinterval $[x_j, x_{j+1}]$ for each $0\le j < n$;
- $S_j(x_j) = f(x_j)$ and $S_j(x_{j+1}) = f(x_{j+1})$  for each $0\le j < n$;
- $S_{j+1}(x_{j+1}) = S_j(x_{j+1})$  for each $0\le j < n-1$;
- $S'_{j+1}(x_{j+1}) = S'_j(x_{j+1})$  for each $0\le j < n-1$;
- $S''_{j+1}(x_{j+1}) = S''_j(x_{j+1})$  for each $0\le j < n-1$;
- One of the following sets of boundary conditions is satisfied:
	- $S''(x_0) = S''(x_n) = 0$, *natural or free boundary*.
	- $S''(x_0) = f'(x_0)$ and $S'(x_n) = f'(x_n)$, *clamped boundary*.
When the free conditions occur the spline is called a *natural spline*. 

#### Natural Splines

**Th:** If $f$ is defined at $a = x_0 < x_1 < \dots <x_n = b$, then $f$ has a unique natural spline interpolant $S$ on the nodes $x_0, x_1, \dots, x_n$; that is, a spline interpolant that satisfies the natural boundary conditions $S''(a) = 0$ and $S''(b) = 0$. 

```python
def natural_cubic_spline(x, y):
    """
    Compute natural cubic spline coefficients.

    Parameters:
        x : list or array of x-values (length n+1)
        y : list or array of y-values (length n+1)

    Returns:
        a, b, c, d : lists of spline coefficients for intervals [x[i], x[i+1]]
    """
    n = len(x) - 1
    a = y[:]  # a[i] = f(x[i])

    # Step 1: h
    h = [x[i+1] - x[i] for i in range(n)]

    # Step 2: alpha
    alpha = [0] * (n + 1)
    for i in range(1, n):
        alpha[i] = (3/h[i]) * (a[i+1] - a[i]) - (3/h[i-1]) * (a[i] - a[i-1])

    # Step 3
    l = [1] + [0]*n
    mu = [0]*(n+1)
    z = [0]*(n+1)

    # Step 4
    for i in range(1, n):
        l[i] = 2 * (x[i+1] - x[i-1]) - h[i-1]*mu[i-1]
        mu[i] = h[i] / l[i]
        z[i] = (alpha[i] - h[i-1]*z[i-1]) / l[i]

    # Step 5
    l[n] = 1
    z[n] = 0
    c = [0]*(n+1)
    b = [0]*n
    d = [0]*n

    # Step 6
    for j in range(n-1, -1, -1):
        c[j] = z[j] - mu[j]*c[j+1]
        b[j] = ((a[j+1] - a[j]) / h[j]) - (h[j]*(c[j+1] + 2*c[j]) / 3)
        d[j] = (c[j+1] - c[j]) / (3 * h[j])

    # Output a,b,c,d for each interval [x[i], x[i+1]]
    return a[:-1], b, c[:-1], d

x_points = [0, 1, 2, 3]
y_points = [0, 1, 0, 1]

a, b, c, d = natural_cubic_spline(x_points, y_points)

for i in range(len(a)):
    print(f"Spline segment {i}:")
    print(f"   S(x) = {a[i]} + {b[i]}(x - {x_points[i]}) + "
          f"{c[i]}(x - {x_points[i]})^2 + {d[i]}(x - {x_points[i]})^3")
```

#### Clampled Splines

**Th:** If $f$ is defined at $a = x_0 < x_1 < \dots <x_n = b$, then $f$ has a unique clamped spline interpolant $S$ on the nodes $x_0, x_1, \dots, x_n$; that is, a spline interpolant that satisfies the natural boundary conditions $S''(a) = f'(a)$ and $S''(b) = f'(b)$. 

```python
def clamped_cubic_spline(x, y, FPO, FPN):
    """
    Compute clamped cubic spline coefficients.

    Parameters:
        x   : list or array of x-values (length n+1)
        y   : list or array of y-values (length n+1)
        FPO : derivative f'(x0)
        FPN : derivative f'(xn)

    Returns:
        a, b, c, d : lists of spline coefficients
    """
    n = len(x) - 1
    a = y[:]

    # Step 1: h
    h = [x[i+1] - x[i] for i in range(n)]

    # Step 2: alpha
    alpha = [0]*(n+1)
    alpha[0] = 3 * (a[1] - a[0]) / h[0] - 3 * FPO
    alpha[n] = 3 * FPN - 3 * (a[n] - a[n-1]) / h[n-1]
    for i in range(1, n):
        alpha[i] = (3/h[i])*(a[i+1]-a[i]) - (3/h[i-1])*(a[i]-a[i-1])

    # Step 3
    l = [0]*(n+1)
    mu = [0]*(n+1)
    z = [0]*(n+1)

    l[0] = 2 * h[0]
    mu[0] = 0.5
    z[0] = alpha[0] / l[0]

    # Step 4
    for i in range(1, n):
        l[i] = 2 * (x[i+1] - x[i-1]) - h[i-1] * mu[i-1]
        mu[i] = h[i] / l[i]
        z[i] = (alpha[i] - h[i-1] * z[i-1]) / l[i]

    # Step 5
    l[n] = h[n-1] * (2 - mu[n-1])
    z[n] = (alpha[n] - h[n-1] * z[n-1]) / l[n]
    c = [0]*(n+1)
    c[n] = z[n]

    b = [0]*n
    d = [0]*n

    # Step 6
    for j in range(n-1, -1, -1):
        c[j] = z[j] - mu[j] * c[j+1]
        b[j] = ((a[j+1] - a[j]) / h[j]) - (h[j] * (c[j+1] + 2*c[j]) / 3)
        d[j] = (c[j+1] - c[j]) / (3 * h[j])

    return a[:-1], b, c[:-1], d

x_points = [0, 1, 2, 3]
y_points = [0, 1, 0, 1]
FPO = 1.0   # derivative at x0
FPN = -1.0  # derivative at xn

a, b, c, d = clamped_cubic_spline(x_points, y_points, FPO, FPN)

for i in range(len(a)):
    print(f"Spline segment {i}:")
    print(f"   S(x) = {a[i]} + {b[i]}(x - {x_points[i]}) + "
          f"{c[i]}(x - {x_points[i]})^2 + {d[i]}(x - {x_points[i]})^3")
```


**Th:** Let $f\in \mathcal C^4[a,b]$ with $\max_{a\le x \le b}|f^{(4)}(x)| = M$. If $S$ is the unique clamped cubic spline interpolant to $f$ with respect to the nodes $a = x_0 <x_1 <\dots < x_n = b$, then for all $x\in [a,b]$,  $$|f(x)- S(x) | \le \frac{5M}{384} \max_{0 \le j < n} (x_{j+1}-x_j)^4.$$