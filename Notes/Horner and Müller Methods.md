---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]], [[Newton-Raphson Method]]
## Horner’s Method

Let

$$ P(x) = \sum_{i =0}^n a_i x^n $$

Define $b_n = a_n$ and

$$ b_k= a_k + b_{k+1}x_0 \qquad 0\le k <n $$

Then $b_0 = P(x_0)$. Morevoer, if

$$ Q(x) = \sum_{i = 1}^n b_i x^{i-1} $$

then

$$ P(x) = (x-x_0) Q(x) +b_0 $$

Finally we get that $P'(x) = Q(x) +(x-x_0) Q'(x)$, and $P'(x_0) = Q(x_0)$

```python
def horner_method(coeffs, x):
    """
    Evaluate a polynomial and its derivative at a point x using Horner's method.

    Parameters:
        coeffs (list or tuple): Polynomial coefficients in descending order.
                                For example, [3, 1, 2] represents 3x^2 + x + 2.
        x (float): Point at which to evaluate the polynomial.

    Returns:
        Px (float): Value of the polynomial at x.
        Px_prime (float): Value of the derivative at x.
    """
    n = len(coeffs)
    Px = coeffs[0]
    Px_prime = 0

    for i in range(1, n):
        Px_prime = Px_prime * x + coeffs[i - 1] * (n - i)
        Px = Px * x + coeffs[i]

    return Px, Px_prime

coeffs = [3, 1, 2]  # Represents 3x^2 + x + 2
x = 2
Px, Px_prime = horner_method(coeffs, x)
print("P(x) =", Px)
print("P'(x) =", Px_prime)
```


## Müller’s Method

The idea of Müller’s method is to create a parabola that passes through three points of the function $(p_0, f(p_0))$, $(p_1, f(p_1))$ and $(p_2, f(p_2))$ like an extension of [[Newton-Raphson Method]], using a polynomial of the form
$$ P(x) = a(x-p_2)^2 +b(x-p_2) +c $$

the constants $a$, $b$ and $c$ can be determined from the conditions:

$$ \begin{align*} f(p_0) &= a(p_0-p_2)^2+ b(p_0-p_2)+c \\ f(p_1) &= a(p_1-p_2)^2+ b(p_1-p_2)+c \\ f(p_2) &= c \\

\end{align*} $$

then we get the values, as

$$ \begin{align*} c &= f(p_2) \\ b &= \frac{(p_0 - p_2)^2[f(p_1)-f(p_2)]-(p_1-p_2)^2[f(p_0)-f(p_2)]}{(p_0-p_2)(p_1-p_2)(p_0-p_1)} \\ a &= \frac{(p_1 - p_2)[f(p_0)-f(p_2)]-(p_0-p_2)[f(p_1)-f(p_2)]}{(p_0-p_2)(p_1-p_2)(p_0-p_1)} \\ \end{align*} $$

since we want the zeros of this quadratic, then we use the quadratic formula 2.0, and get that

$$ p_3 -p_2 = \frac{-2c}{b\pm \sqrt{b^2 -4ac}} $$

In Müller’s Method we make it such that the sign of the radical to agree witt the sign of $b$, getting that

$$ p_3 = p_2 -\frac{2c}{b + \operatorname{sgn}(b)\sqrt{b^2-4ac}} $$

Finally, we iterate through and when $b^2-4ac <0$, the method converges to complex roots.

```python
import cmath

def mullers_method(f, x0, x1, x2, tol=1e-10, max_iter=1000, imag_tol=1e-12):
    """
    Müller's method for finding roots of a function f(x), supporting complex roots.

    If the imaginary part of the root is smaller than imag_tol, returns the real part only.

    Parameters:
        f (callable): Function whose root is sought.
        x0, x1, x2 (float or complex): Initial guesses for the root.
        tol (float): Convergence tolerance.
        max_iter (int): Maximum number of iterations.
        imag_tol (float): Threshold below which imaginary parts are ignored.

    Returns:
        x (float or complex): Approximated root.
        iteration (int): Number of iterations used.
    """
    for iteration in range(max_iter):
        h1, h2 = x1 - x0, x2 - x1
        f0, f1, f2 = f(x0), f(x1), f(x2)
        delta1 = (f1 - f0) / h1
        delta2 = (f2 - f1) / h2
        a = (delta2 - delta1) / (h2 + h1)
        b = a * h2 + delta2
        c = f2

        radicand = b**2 - 4*a*c
        sqrt_rad = cmath.sqrt(radicand)

        den = b + sqrt_rad if abs(b + sqrt_rad) > abs(b - sqrt_rad) else b - sqrt_rad
        if den == 0:
            raise ZeroDivisionError("Denominator became zero during iteration.")

        x = x2 - 2*c / den

        if abs(f(x)) < tol:
            # Return only real part if imaginary part is negligible
            if abs(x.imag) < imag_tol:
                return x.real, iteration + 1
            return x, iteration + 1

        x0, x1, x2 = x1, x2, x

    raise RuntimeError("Müller's method did not converge within the specified number of iterations.")

f = lambda x: x**3 - x - 2
root, iterations = mullers_method(f, 1, 1.5, 2)
print("Root:", root)
print("Iterations:", iterations)

f = lambda x: x**2 + 1  # roots at ±i
root, iterations = mullers_method(f, 0.5, 1, 1.5)
print("Root:", root)
print("Iterations:", iterations)

```
