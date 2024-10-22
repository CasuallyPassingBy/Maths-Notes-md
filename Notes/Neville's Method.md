---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Interpolation and Polynomial Approximation]], [[Lagrange Polynomials]]

Let $f$ be a function defined at $x_0, \dots, x_n$ and suppose that $m_1, \dots m_k$ are $k$ distinct integers, with $0 \le m_i \le n$ for each $i$. The Lagrange polynomial that agrees with $f$ at the $k$ points $x_{m_1}, \dots, x_{m_k}$ is denoted as $P_{m_1, \dots, m_k}(x)$ 

Let $f$ be defined at $x_0, \dots, x_k$ and $x_i$ and $x_j$ are two distinct numbers in the list. Then

$$
P(x) = \frac{(x-x_j)P_{0, \dots, j-1, j+1, \dots, k} -(x-x_i)P_{0, \dots, i-1, i+1, \dots k}(x)}{x_i-x_j}
$$

We can use this result generate recursively polynomial approximations using consecutive points, is called **Neville's Method**. We could use the notation above, but it can be a lot more cumbersome than it needs to be. We can use a table to see how 

| $x_0$ | $P_0$ |  |  |  |  |
| ---- | ---- | ---- | ---- | ---- | ---- |
| $x_1$ | $P_1$ | $P_{0,1}$ |  |  |  |
| $x_2$ | $P_2$ | $P_{1,2}$ | $P_{0,1,2}$ |  |  |
| $x_3$ | $P_3$ | $P_{2,3}$ | $P_{1,2,3}$ | $P_{0,1,2, 3}$ |  |
| $x_4$ | $P_4$ | $P_{3,4}$ | $P_{2,3,4}$ | $P_{1,2,3,4}$ | $P_{0,1,2,3,4}$ |

We can actually simplify the notation used here since we only need two index, we let $Q_{i, j}(x)$ for $0 \le j \le i$, denote polynomial of degree $j$ on the $j+1$ numbers $x_{i-j}, x_{i-j+1}, \dots x_{i}$; that is 
$$
Q_{i, j}  =P_{i- j, i-j+1, \dots, i-1, i}
$$
Thus we can simplify the notation of the table above as 

| $x_0$ | $Q_{0,0}$ |  |  |  |  |
| ---- | ---- | ---- | ---- | ---- | ---- |
| $x_1$ | $Q_{1,0}$ | $Q_{1,1}$ |  |  |  |
| $x_2$ | $Q_{2,0}$ | $Q_{1,2}$ | $Q_{2,2}$ |  |  |
| $x_3$ | $Q_{3,0}$ | $Q_{1,3}$ | $Q_{2,3}$ | $Q_{3,3}$ |  |
| $x_4$ | $Q_{4,0}$ | $Q_{1,4}$ | $Q_{2,4}$ | $Q_{3,4}$ | $Q_{4,4}$ |

In general we get the recursive identity:

$$
	Q_{i, j} (x) = \frac{(x-x_{i-j})Q_{i, j-1}(x)-(x-x_i)Q_{i-1, j-1}(x)}{x_i -x_{i-j}}
$$

```julia
function nevilles_method(x_values, y_values, x)
    n = length(x_values)
    Q = similar(y_values, Float64)  # Initialize the first column of the table with y-values
    
    for j in 2:n
        for i in 1:n-j+1
            Q[i] = ((x - x_values[i]) * Q[i+1] - (x - x_values[i+j-1]) * Q[i]) / (x_values[i+j-1] - x_values[i])
        end
    end
    
    return Q[1]  # The interpolated value is in the top-right corner of the table
end
```

We can use this method to calculate something called [[Iterated Inverse Interpolation]]. 