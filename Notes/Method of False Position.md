---
tags:
  - NumericalAnalysis
---
Subject: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]], [[Bisection Method]], [[Newton-Raphson Method]], [[Secant Method]]

It is not a generally recommended method, but it serves to show a concept called _**************Root Bracketing,**************_ meaning that at each iteration we have that $a_n$ and $b_n$ that “bracket” the root $p$.

Then we want to modify slightly the Secant Method, we have that $p_n$, and $p_{n-1}$ bracket the root at every step of the approximation, basically merging bisection and the secant method. It has similar problems, to the Secant Method and Newton’s Method

### The Method of False Position Code

```python
def false_position(f, a, b, tol=1e-6, max_iter=1000):
    """
    False position (regula falsi) method to find a root of f(x) = 0.

    Parameters:
        f (callable): Function whose root is sought.
        a (float): Left endpoint of initial interval.
        b (float): Right endpoint of initial interval.
        tol (float): Tolerance for convergence.
        max_iter (int): Maximum number of iterations.

    Returns:
        float: Approximated root.
    """
    fa, fb = f(a), f(b)
    if fa * fb > 0:
        raise ValueError("Function must have opposite signs at the endpoints.")

    for _ in range(max_iter):
        # False position formula
        x = b - fb * (b - a) / (fb - fa)
        fx = f(x)

        # Convergence checks
        if abs(fx) < tol or abs(b - a) < tol:
            return x

        # Update interval
        if fa * fx < 0:
            b, fb = x, fx
        else:
            a, fa = x, fx

    print("Did not converge within the maximum iterations.")
    return x

f = lambda x: x*x - 2
root = false_position(f, 1, 2)
print("Approximate root:", root)

```
