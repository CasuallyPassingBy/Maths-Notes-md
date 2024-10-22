---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Interpolation and Polynomial Approximation]],

Let $x_0, \dots, x_n \in [a, b]$ be distinct and let the real numbers $f^{(k)}(x_i)$ be given for all $i \in \{0,\dots, n\}$ and for every $k\in \{0, \dots, m_i\}$. Then there's a unique polynomial of degree $M$, where $M=\sum_{ k = 0}^n m_k+ n$ . 

Let $x_0, \dots, x_n$ be $n+1$ distinct numbers in $[a, b]$, and for $i \in \{0,1\dots, n\}$, let $m_i \in \Bbb N$. Suppose $f\in {\cal C}^m[a,b]$, where $m = \max\limits_{0 \le i \le n}m_i$.
The *osculating polynomial* approximating $f$ is the polynomial with the least degree such that 
$$
\frac{d^k P(x_i)}{dx^k} = \frac{d^k f(x_i)}{dx^k} \qquad \text{for each }i \in\{0, \dots, n\} \quad \text{and for each }k \in \{0, \dots, m_i\}
$$
We can see that when $n =0$, the osculating polynomial approximating $f$ is the $m_0$th [[Taylor Series in R|Taylor polynomial]]. When $m_i = 0$ for each $i$, the osculating polynomial is the $n$th [[Lagrange Polynomials|Lagrange polynomial]] interpolating $f$ on $x_0, \dots, x_n$.

### Lagrange interpolation ++

We are interested when $m_i = 1$ for $i = 0, \dots, n$ meaning we are looking for when the first derivative matches the first derivative of the function.

If $f\in {\cal C}^1[a,b]$ and a $x_0, \dots, x_n \in [a,b]$ are distinct, the unique polynomial of least degree agreeing with $f$ and $f'$ at $x_0, \dots, x_n$ is the *Hermite interpolating polynomial* of degree at most $2n+1$ given by
$$
H_{2n+1}(x) = \sum_{k = 0}^n f(x_k) H_{n, k}(x) +\sum_{k = 0}^n f'(x_k) \hat H_{n, k}(x)
$$
where, for $L_{n, k}(x)$ denotes the $k$th Lagrange coefficient polynomial of degree $n$, we have 
$$
H_{n,k}(x) = [1-2(x-x_k)L_{n,k}'(x)] L_{n, k}^2(x) \quad \text{and} \quad \hat H_{n, k}(x) = (x-x_k)L_{n, k}(x)
$$
Moreover $f\in {\cal C}^{2n+2}[a,b]$, then 
$$
f(x) = H_{2n+1}(x) + \frac{1}{(2x+2)!}\prod_{k = 0}^n (x-x_k)^2f^{(2n+2)}(\xi(x))
$$
for some (generally unknown) $\xi(x)$ in the interval $(a,b)$.  This method is closely related to Lagrange polynomials, and is not that easy to generalise. If we want to do that we are 

### Divided Differences ++

In order to describe this method, we need to change the data points. We replace the set $\{x_i \mid i =0, \dots, m\}$ by the [[Multiset|multiset]] $\{x_0, x_0\dots,x_0, x_1, x_1\dots x_1, \dots, x_n, x_n\dots, x_n \}$ where for $i =0, \dots, n$ the number $x_i$ occurs $m_i +1$ in the multiset. We renumber the indices in terms of the new multiset so that the elements are $\{x_i \mid i = 0, \dots, M\}$. Hence the terms in the new indicate which derivatives are given as data and we have returned to the case where there are $M+1$ data points, so we can apply [[Newton's Divided Difference]]. 

If we try to do it blindly, we see a problem where we end up diving $0/0$. In this case we can make the definition of let $x_j = x_{j+1} = \dots = x_{j + k}$, then we define it
$$
f[x_j , x_{j+1}, \dots, x_{j+k}] = \frac{f^{(k)}(x_j)}{k!}
$$
which is very convenient since the right hand side is already known. Then we can just copy Newton's divided-difference method. 

Let the function value $f$ be given at the points $\{x_i \mid i =0, \dots, M\}$ and if $x_i$ occurs $m+1$ times in the point set, let the derivatives $\{f^{(j)}(x_i)\mid j = 1, \dots, k\}$ be grouped together, and let $p$ a polynomial of degree $M$ be the polynomial that is calculated by the extension of Newton's method. Then the polynomial $p$ interpolates the data.

### Special Case

Let $x_0$ and $x_1$ be distinct points, where the values of $f$ and $f'$ are known, then we can calculate the difference table and get that, the polynomial that interpolates that is of the form
$$
	f[x_0]+ f[x_0, x_0](x-x_0)+ f[x_0, x_0, x_1](x-x_0)^2+ f[x_0, x_0, x_1, x_1](x-x_0)^2(x-x_1)
$$
### Code
This code calculates the Hermite interpolation, given a derivative for each point 

```julia
function hermite_interpolation(x_vals, y_vals, y_prime_vals)
    n = length(x_vals)
    divided_diff_table = zeros(Float64, n, n + 1)

    # Fill in the first two columns of the divided difference table
    divided_diff_table[:, 1] .= x_vals
    divided_diff_table[:, 2] .= y_vals

    # Fill in the first divided differences
    divided_diff_table[:, 3] .= y_prime_vals

    # Calculate higher-order divided differences
    for k in 4:n+1
        for i in 1:n-k+2
            divided_diff_table[i, k] = (divided_diff_table[i+1, k-1] - divided_diff_table[i, k-1]) /
                                       (x_vals[i+k-2] - x_vals[i])
        end
    end

    # Build the Hermite interpolating polynomial
    function hermite_polynomial(x)
        result = divided_diff_table[1, 2]

        for k in 3:n+1
            term = divided_diff_table[1, k]
            for i in 1:k-2
                term *= (x - x_vals[i])
            end
            result += term
        end

        return result
    end

    return hermite_polynomial
end
```

This code calculates the same thing but for arbitrary derivatives:
```julia

function hermite_interpolation_arbitrary_derivatives(x_vals, y_vals, derivative_vals)
    n = length(x_vals)
    divided_diff_table = zeros(Float64, n, n + 1)

    # Fill in the first two columns of the divided difference table
    divided_diff_table[:, 1] .= x_vals
    divided_diff_table[:, 2] .= y_vals

    # Fill in the arbitrary derivatives
    for i in 1:n
        divided_diff_table[i, 3] = derivative_vals[i][1]
    end

    # Calculate higher-order divided differences
    for k in 4:n+1
        for i in 1:n-k+2
            divided_diff_table[i, k] = (divided_diff_table[i+1, k-1] - divided_diff_table[i, k-1]) /
                                       (x_vals[i+k-2] - x_vals[i])
        end
    end

    # Build the Hermite interpolating polynomial
    function hermite_polynomial(x)
        result = divided_diff_table[1, 2]

        for k in 3:n+1
            term = divided_diff_table[1, k]
            for i in 1:k-2
                term *= (x - x_vals[i])
            end
            result += term
        end

        return result
    end

    return hermite_polynomial
end
```