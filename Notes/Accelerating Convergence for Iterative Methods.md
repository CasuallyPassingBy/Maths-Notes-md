---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]], [[Fixed Point Iteration]], [[Newton-Raphson Method]], [[Horner and Müller Methods]], [[Secant Method]], [[Method of False Position]]

## Aitken’s $\Delta^2$ Method

Let suppose $(p_n)_{n \in \Bbb N}$ is a linearly convergent sequence to the limit point $p$, then we will define another sequence $\hat p_n$, defined as

$$ \hat p_n = p_n - \frac{(\Delta p_n)^2}{\Delta^2 p_n} $$

This is _Aitken’sn $\Delta^2$ Method_, we are going to use the $\Delta$ notation for differences that is present in [[Discrete Calculus]]

Let $(p_n)_{n \in \Bbb N}$ is a sequence that converges linearly to the limit point $p$, and that

$$ \lim_{n \to \infty} \frac{p_{n+1}-p}{p_n - p} <1 $$

Then the Aitken’s $\Delta^2$ sequence $(\hat p_n)_{n \in \Bbb N}$ converges faster to $p$ than $(p_n)_{n \in \Bbb N}$ in the sense that

$$ \lim_{n \to \infty}\frac{\hat p_{n+1}-p}{\hat p_n -p} = 0 $$

## Steffensen’s Method

We denote $\{\Delta ^2\}$ indicates the Aitken’s $\Delta ^2$ method, then

$$ p_0^{(0)}, \quad p_1^{(0)} =g(p_0^{(0)}), \quad p_2^{(0)} = g(p_1^{(0)}), \quad p_0^{(1)} =\{\Delta^2\} (p_0^{(0)}) , \quad p_1^{(1)} =g(p_0^{(1)}) $$

********Th:******** Suppose that $x = g(x)$ has a solution $p$ with $g'(p) \ne 1$. If there exist a $\delta >0$ such that ${g \in \cal C^3[p-\delta, p+\delta]}$, then Steffensen’s Method gives quadratic convergence for any ${p_0 \in [p - \delta , p +\delta]}$

```python
def steffensen_acceleration(f, x0, tol=1e-6, max_iter=1000):
    """
    Steffensen's acceleration method for fixed-point iteration.

    Parameters:
        f (callable): Function defining the fixed-point iteration x = f(x).
        x0 (float or complex): Initial guess.
        tol (float): Convergence tolerance.
        max_iter (int): Maximum number of iterations.

    Returns:
        x (float or complex): Approximated fixed point.
    """
    x_current = x0

    for iter_count in range(1, max_iter + 1):
        x_next = f(x_current)
        x_next_next = f(x_next)

        denominator = x_next_next - 2*x_next + x_current
        if denominator == 0:
            print("Denominator is zero. Steffensen's method cannot proceed.")
            return x_current

        # Apply Steffensen's acceleration
        x_accelerated = x_current - ((x_next - x_current)**2) / denominator

        # Check for convergence
        if abs(x_accelerated - x_current) < tol:
            print(f"Converged after {iter_count} iterations.")
            return x_accelerated

        x_current = x_accelerated

    print("Did not converge within the maximum iterations.")
    return x_current

# Fixed-point iteration example: sqrt(2) via g(x) = 0.5*(x + 2/x)
g = lambda x: 0.5 * (x + 2 / x)
root = steffensen_acceleration(g, x0=1.0)
print("Approximate fixed point:", root)

```
