---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]], [[Newton-Raphson Method]]

The main problem of using Newton’s method is the need of the derivative of $f$ at each approximation. Sometimes $f'(x)$ can be more complicated to calculate than $f(x)$. If we look at the definition of derivative, we get it as

$$ f(p_{n}) = \lim_{x \to p_{n}} \frac{f(x) -f(p_{n})}{x - p_{n}} $$

If $p_{n-1}$ is close to $p_{n}$, then

$$ f'(p_{n}) \approx \frac{f(p_{n}) -f(p_{n-1})}{p_{n} - p_{n-1}} $$

Using this approximation for $f'(p_{n})$ to Newton’s Method, we get

$$ p_{n+1} = p_n -\frac{f(p_n)(p_n -p_{n-1})}{(f(p_n) - f(p_{n-1}))} $$

This is called the **_Secant method_**

### Secant Method Code

```python
def secant_method(f, x0, x1, tol=1e-6, max_iter=1000):
    """
    Secant method for finding roots of f(x) = 0.

    Parameters:
        f (callable): The function whose root we seek.
        x0 (float): First initial guess.
        x1 (float): Second initial guess.
        tol (float): Tolerance for convergence.
        max_iter (int): Maximum number of iterations.

    Returns:
        float: The approximated root.
    """
    x_prev = x0
    x_current = x1

    for i in range(1, max_iter + 1):
        f_prev = f(x_prev)
        f_current = f(x_current)

        # Check for convergence
        if abs(x_prev - x_current) < tol:
            return x_current

        # Check if the denominator or difference is too small
        if abs(f_current - f_prev) < tol:
            print("Difference between function values close to zero. Secant method cannot proceed.")
            return x_current

        # Update approximation using the secant formula
        x_next = x_current - f_current * (x_current - x_prev) / (f_current - f_prev)
        x_prev, x_current = x_current, x_next

    print("Did not converge within the maximum iterations.")
    return x_current


f = lambda x: x**2 - 2
root = secant_method(f, x0=1.0, x1=2.0)
print("Approximate root:", root)
```

This method is generally slower than Newton’s Method, but also generally cheaper to compute. This method and Newton’s Method is used to refine an answer obtained by another technique, since they already need quite a good approximations but generally converges rapidly.