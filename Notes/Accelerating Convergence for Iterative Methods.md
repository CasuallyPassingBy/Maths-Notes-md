---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]], [[Fixed Point Iteration]], [[Newton's Method]], [[Horner and Müller Methods]], [[Secant Method]], [[Method of False Position]]

## Aitken’s $\Delta^2$ Method

Let suppose $(p_n)_{n \in \Bbb N}$ is a linearly convergent sequence to the limit point $p$, then we will define another sequence $\hat p_n$, defined as

$$ \hat p_n = p_n - \frac{(\Delta p_n)^2}{\Delta^2 p_n} $$

This is _Aitken’sn $\Delta^2$ Method_, we are going to use the $\Delta$ notation for differences that is present in [[discrete calculus]]

Let $(p_n)_{n \in \Bbb N}$ is a sequence that converges linearly to the limit point $p$, and that

$$ \lim_{n \to \infty} \frac{p_{n+1}-p}{p_n - p} <1 $$

Then the Aitken’s $\Delta^2$ sequence $(\hat p_n)_{n \in \Bbb N}$ converges faster to $p$ than $(p_n)_{n \in \Bbb N}$ in the sense that

$$ \lim_{n \to \infty}\frac{\hat p_{n+1}-p}{\hat p_n -p} = 0 $$

## Steffensen’s Method

We denote $\{\Delta ^2\}$ indicates the Aitken’s $\Delta ^2$ method, then

$$ p_0^{(0)}, \quad p_1^{(0)} =g(p_0^{(0)}), \quad p_2^{(0)} = g(p_1^{(0)}), \quad p_0^{(1)} =\{\Delta^2\} (p_0^{(0)}) , \quad p_1^{(1)} =g(p_0^{(1)}) $$

********Th:******** Suppose that $x = g(x)$ has a solution $p$ with $g'(p) \ne 1$. If there exist a $\delta >0$ such that ${g \in \cal C^3[p-\delta, p+\delta]}$, then Steffensen’s Method gives quadratic convergence for any ${p_0 \in [p - \delta , p +\delta]}$

```julia
function steffensen_acceleration(f, x0, tol=1e-6, max_iter=1000)
    x_current = x0
    
    for iter in 1:max_iter
        x_next = f(x_current)
        x_next_next = f(x_next)
        
        # Apply Steffensen's acceleration
        x_accelerated = x_current - ((x_next - x_current)^2) / (x_next_next - 2x_next + x_current)
        
        # Check for convergence
        if abs(x_accelerated - x_current) < tol
            println("Converged after $iter iterations.")
            return x_accelerated
        end
        
        x_current = x_accelerated  # Update the approximation
    end
    
    println("Did not converge within the maximum iterations.")
    return x_current
end
```