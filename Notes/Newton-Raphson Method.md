---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]], [[Fixed Point Iteration]]

Suppose $f \in {\cal C}^2[a,b]$. Let $p_0 \in [a,b]$ be an approximation of $p$ such that $f'(p_0) \ne 0$ and ${|p - p_0|}$ is “small”. Then we can use a Taylor approximation about $p_0$ and evaluated at $p$. If we neglect the term with $|p -p _0|^2$ since it is is so small, then we get that

$$ 0= f(p) \approx f(p_0) +(p-p_0)f'(p_0) $$

solving for $p$, we get that

$$ p \approx p_0 -\frac{f(p_0)}{f'(p_0)} $$

Then we can define Newton’s Method, as the following

$$ p_{n+1} = p_n - \frac{f(p_n)}{f'(p_n)} \quad \text{for }n \in \Bbb N $$

### Newton’s Method Code

```python
def newton_method(f, f_prime, x0, tol=1e-6, max_iter=1000, imag_tol=1e-12):
    """
    Newton's method for finding roots of f(x) = 0, supporting complex roots.

    If the imaginary part of the root is smaller than imag_tol, returns the real part only.

    Parameters:
        f (callable): Function whose root we seek.
        f_prime (callable): Derivative of f.
        x0 (float or complex): Initial guess.
        tol (float): Convergence tolerance.
        max_iter (int): Maximum number of iterations.
        imag_tol (float): Threshold below which imaginary parts are ignored.

    Returns:
        x (float or complex): Approximated root.
    """
    x_current = x0

    for i in range(1, max_iter + 1):
        f_val = f(x_current)
        f_prime_val = f_prime(x_current)

        if abs(f_prime_val) < tol:
            print("Derivative close to zero. Newton's method cannot proceed.")
            return x_current

        x_next = x_current - f_val / f_prime_val

        if abs(x_next - x_current) < tol:
            # Return real part if imaginary part is negligible
            if abs(x_next.imag) < imag_tol:
                return x_next.real
            return x_next

        x_current = x_next

    print("Did not converge within the maximum iterations.")
    # Return real part if imaginary part is negligible
    if abs(x_current.imag) < imag_tol:
        return x_current.real
    return x_current
    
f = lambda x: x*x - 2
f_prime = lambda x: 2*x

root = newton_method(f, f_prime, x0 = 1.0)
print(f'Approximate root: {root}')

f = lambda x: x**2 + 1
f_prime = lambda x: 2*x

root = newton_method(f, f_prime, x0=2.0j)
print("Approximate root:", root) 

```

### Convergence Theorem

Let $f \in \mathcal C^2[a,b]$. If $p \in (a,b)$ such that $f(p) = 0$ and $f'(p) = 0$, then there exists a $\delta >0$ such that Newton’s method generates a sequence $(p_n)_{n \in \Bbb N}$ converging to $p$ for any initial approximation $p_0 \in [p - \delta, p +\delta]$

The idea to find this $\delta$ is that if we consider $g(x) = x - \frac{f(x)}{f'(x)}$, then $g'(x) = \frac{f(x)f''(x)}{f'(x)^2}$. Then if $g(p) = p$, and $g'(p) = 0$, this means that $p$ is a super attractive fixed point of $g$. Meaning we if that we can find $\delta >0$, such that it is a contraction on that interval, and thus it converges. But in practice it just means to have a reasonable first guess of the solution, or look it up first with bisection on $f$, and consequently we get closer to the region where $g$ is contraction.

We can calculate the error by using the Taylor’s Expansion, with the hypothesis of the theorem and with $\| f''\|_\infty \le M$

$$ |p _{n+1} - p| = \frac{M}{2|f'(p_n)|}|p - p_n|^2 $$This method can be modified in a bit of ways to get a different results:
- [[Secant Method]]
- [[Method of False Position]]