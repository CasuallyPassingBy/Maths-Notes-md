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

If we want to control, 