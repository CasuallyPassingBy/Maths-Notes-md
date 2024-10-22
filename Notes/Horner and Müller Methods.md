---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Solutions of Equations of One Variable]]
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

```julia
function horner_method(coeffs, x)

    """

    Calculate the value of P(x) and P'(x) using Horner's method.

    coeffs: A list of coefficients in descending order, where coeffs[1] is the coefficient of the highest degree term.

            For example, [3, 1, 2] represents 3x^2 + x + 2.

    x: The value at which to evaluate the polynomial.

    Returns:

    Px: The value of the polynomial P(x) at the given point x.

    Px_prime: The value of the derivative of the polynomial P'(x) at the given point x.

    """

    n = length(coeffs)

    Px = coeffs[1]

    Px_prime = 0

    for i in 2:n

        Px = Px * x + coeffs[i]

        Px_prime = Px_prime * x + coeffs[i - 1] * (n - i + 1)

    end

    return Px, Px_prime

end
```

## Müller’s Method

The idea of muller’s method is to create a parabola that passes through three points of the function $(p_0, f(p_0))$, $(p_1, f(p_1))$ and $(p_2, f(p_2))$ like an extension of [[Newton's Method]], using a polynomial of the form

$$ P(x) = a(x-p_2)^2 +b(x-p_2) +c $$

the constants $a$, $b$ and $c$ can be determined from the conditions:

$$ \begin{align*} f(p_0) &= a(p_0-p_2)^2+ b(p_0-p_2)+c \\ f(p_1) &= a(p_1-p_2)^2+ b(p_1-p_2)+c \\ f(p_2) &= c \\

\end{align*} $$

then we get the values, as

$$ \begin{align*} c &= f(p_2) \\ b &= \frac{(p_0 - p_2)^2[f(p_1)-f(p_2)]-(p_1-p_2)^2[f(p_0)-f(p_2)]}{(p_0-p_2)(p_1-p_2)(p_0-p_1)} \\ a &= \frac{(p_1 - p_2)[f(p_0)-f(p_2)]-(p_0-p_2)[f(p_1)-f(p_2)]}{(p_0-p_2)(p_1-p_2)(p_0-p_1)} \\ \end{align*} $$

since we want the zeros of this quadratic, then we use the quadratic formula 2.0, and get that

$$ p_3 -p_2 = \frac{-2c}{b\pm \sqrt{b^2 -4ac}} $$

In Müller’s Method we make it such that the sign of the radical to agree witht the sign of $b$, getting that

$$ p_3 = p_2 -\frac{2c}{b + \operatorname{sgn}(b)\sqrt{b^2-4ac}} $$

Finally, we iterate through and when $b^2-4ac <0$, the method converges to complex roots.

```julia
function mullers_method(f, x0, x1, x2; tol=1e-10, max_iter=1000)
    # f: The function for which to find roots
    # x0, x1, x2: Initial points for the iteration
    # tol: Tolerance for convergence
    # max_iter: Maximum number of iterations

    iter = 0
    while iter < max_iter
        h1 = x1 - x0
        h2 = x2 - x1
        delta1 = (f(x1) - f(x0)) / h1
        delta2 = (f(x2) - f(x1)) / h2
        a = (delta2 - delta1) / (h2 + h1)
        b = a * h2 + delta2
        c = f(x2)

        # Calculate the two candidate roots
        radicand = b^2 - 4a*c
        if abs(b + sqrt(radicand)) > abs(b - sqrt(radicand))
            den = b + sqrt(radicand)
        else
            den = b - sqrt(radicand)
        end

        # Update roots
        x = x2 - 2c / den

        # Check for convergence
        if abs(f(x)) < tol
            return x, iter
        end

        # Update points for the next iteration
        x0, x1, x2 = x1, x2, x
        iter += 1
    end

    error("Müller's method did not converge within the specified number of iterations.")
end
```