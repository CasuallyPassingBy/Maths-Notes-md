---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Interpolation and Polynomial Approximation]],

Suppose $P_n$ is a polynomial interpolating that agrees with the function $f$ on the points $x_0, \dots x_n$. This polynomial is unique, but we can represent it in a different way. The divided differences of $f$ with respect to $x_0, \dots, x_n$ are used to express $P_n$ in the form

$$
P_n(x) = \sum_{k  = 0}^n a_k\prod_{i =0}^{k-1} (x-x_i)
$$

or 
$$
P_n(x)  = a_0+ a_1(x-x_0)+a_2(x-x_0)(x-x_1)+\dots +a_n(x-x_0)\cdots(x-x_{n-1})
$$
where we need to find the constants $a_0, \dots, a_n$. If we evaluate $P_n$ at $x_0$ we get that 
$$
P_n(x_0) = a_0 = f(x_0)
$$
Then we would find, for $a_1$ that 
$$
	f(x_0)+ a_1(x_1-x_0) = P_n(x_1) = f(x_1)
$$
then we get 
$$
a_1 = \frac{f(x_1)-f(x_0)}{x_1-x_0}
$$
We are going to introduce a piece of notation that seems a bit artificial at the beginning. We call the *zeroth divided difference* of $f$ as 
$$
f[x_i] = f(x_i)
$$
We define the *first divided diffence* of $f$ as
$$
f[x_i, x_{i+1}] = \frac{f[x_{i+1}]-f[x_i]}{x_{i+1}-x_i}
$$
In general after the $(k-1)$*th divided diferences*, 
$$
f[x_i, \dots , x_{i+k-1}] \quad \text{ and } \quad f[x_{i+1}, \dots, x_{i+k}]
$$
have been determined then, the $k$*th divided difference has been determined* relative to $x_i, \dots x_{i+k}$ is 
$$
f[x_i,\dots x_{i+k}] = \frac{f[x_{i+1}, x_{i+2}, \dots, x_{i+k}]- f[x_i, x_{i+1}, \dots, x_{i+k-1}]}{x_{i+k}-x_i}
$$
This process ends when we with the single *$n$th divided difference*

$$
f[x_0, \dots, x_n] = \frac{f[x_1,\dots, x_n]- f[x_0, \dots, x_{n-1}]}{x_n-x_0}
$$
With this we can actually we get that, get the divided difference form of the polynomial of $f$, as 
$$
P_n(x) = \sum_{k  = 0}^n f[x_0, \dots, x_k]\prod_{i =0}^{k-1} (x-x_i)
$$
This actually means that $a_k = f[x_0, \dots, x_k]$. 

Suppose that $f\in {\cal C}^n [a,b]$ and $x_0, \dots, x_n$ are distinct numbers in $[a, b]$. Then the number $c\in (a,b)$ such that
$$
f[x_0,\dots, x_n] = \frac{f^{(n)}(c)}{n!}
$$
We can see that, it is really easy to add points to the data set without throwing away our calculations since, if we add $x_{n+1}$ with its corresponding value we get
$$
P_{n+1}(x) = P_n(x) + f[x_0, \dots, x_n , x_{n+1}]\prod_{k = 1}^n (x-x_k)
$$
then we only need to calculate $f[x_0, \dots, x_n , x_{n+1}]$ 

The code to generate the coefficients and how to update it:
```julia
function update_divided_differences(F, x, y)
    n = length(x)

    # Add new data point
    push!(x, x[end] + 1)
    push!(y, f(x[end]))  # Replace f(x) with the function you're interpolating

    # Update the last column of F
    for i in 1:n
        F[i, end] = (F[i, end-1] - F[i+1, end-1]) / (x[i] - x[end])
    end

    return F
end

function calculate_divided_differences(x, y)
    n = length(x)
    F = zeros(n, n)

    # Initialize the first column with y values
    F[:, 1] .= y

    # Compute divided differences
    for j in 2:n
        for i in 1:n-j+1
            F[i, j] = (F[i+1, j-1] - F[i, j-1]) / (x[i+j-1] - x[i])
        end
    end

    return F
end
```
### Evenly Spaced Points

The formula can be simplified quite a lot with when the points are evenly spaced, then we can define $h = x_{i+1}-x_i$, for each $i =0, \dots, n-1$, and let $x = x_0 +sh$. Then the difference $x-x_i = (s-i)h$. Then the general formula becomes:
$$
P_n(x) =P(x_0+sh) = \sum _{k = 0}^n s^{\underline k} h^k f[x_0, \dots, x_k]
$$
We are using the [[Falling and Rising Factorials and Pochhamer Symbols|Falling Factorial notation]], and since this combine really well with the binomial coefficients we get that 
$$
P_n(x) =P(x_0+sh) = \sum _{k = 0}^n {s\choose k} k!h^k f[x_0, \dots, x_k]

$$
#### Forward Differences

The *Newton forward-difference formula* is constructed by making use of the difference notation $\Delta$. With this notation we get
$$
f[x_0, x_1] = \frac{1}{h} \Delta f(x_0)
$$
and in general we get that
$$
f[x_0, x_1, \dots, x_k] = \frac{1}{k! h^k} \Delta^k f(x_0)
$$
Using this fact we get that the polynomials is of the form
###### Newton's Forward-difference Formula
$$
P_n (x) = P_n(x_0+sh ) = \sum_{k =0}^n {s\choose k} \Delta ^k f(x_0)
$$
Which is deeply related to [[discrete calculus]]
#### Backward Differences

We can rearrange the nodes values of $x_0, \dots, x_n$ to $x_n , x_{n-1}, \dots, x_0$ we can write is 
$$
P_n(x) = \sum_{k = 0}^n f[x_n, \dots, x_{n-k}] \prod_{i = n-k+1}^n (x-x_i) 
$$
Similarly as we did for the forward differences, we can suppose that the points are evenly spaced and $x = x_n +sh$ and $x = x_i +(s+n-i)h$ then
$$
P_n (x) = P_n(x_n+sh) = \sum_{k = 0}^n s^{\overline k} h^k f[x_n, x_{n-1}, \dots, x_{n-k}]
$$
We are using the [[Falling and Rising Factorials and Pochhamer Symbols|Rising factorial]]. If we use the backward difference present in [[discrete calculus]]. We get the result:
$$
f[x_n, \dots, x_{n-k}] = \frac{1}{k! h^k} \nabla ^k f(x_n)
$$
Then we get the polynomial as

##### Newton Backward-difference Formula
$$
P_n (x) = P_n (x_n+sh) = \sum_{k =0}^n {s-k+1\choose k} \nabla^k f(x_n) = \sum_{k =0}^n (-1)^k {-s  \choose k} \nabla ^k f(x_n)
$$
Which i think it does have a [[discrete calculus]] analogue

