---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
# Sources of Error

There are two sources of error:

- those inherent in the mathematical formulation of the problem
- those incurred in finding the solution numerically

The first of this sources is caused, usually by the replacement of the infinite process by a finite approximation. We shall denote this type of error in all its various froms as _**********truncation error**********_, since it often is the result of truncating an infinite process to get a finite process.

The second type of error is generated the fact that arithmetic calculations can almost never be carried out with complete accuracy. The error we introduce by rounding a number is called **************roundoff error**************.

# Error Definitions and Related Matters

Let the true value of a quanity be $x$ and measured or inferred value $x_0$, then the error is defined as

$$ \Delta x = x-x_0 $$

we can add absolute value to it and get absolute error, defined as

$$ |\Delta x | = |x - x_0| $$

If we want a portion of the error given that $x \ne 0$, then we define the relative error

$$ |\delta x | = \left|\frac{\Delta x}{x}\right| $$

## Significant Digits

The number $p^*$ is said to approximate $p$ to $t$ _******significant digits******_ if $t$ is the largest nonnegative integer for which

$$ \left|\frac{p-p^*}{p}\right| \le 5\times 10^{-t} $$

## Round-off Error and Computer Arithmetic

### Pending

We can obtain a new-ish, formula for calculating the solutions to quadratic polynomials, we get that the roots of $ax^2+bx+c =0$, with $a\ne 0$ are of the form:

$$ x = \frac{-2c}{b\pm\sqrt{b^2-4ac}} $$

## Error Propagation

In ********addition******** and ************substraction,************ the bounds for the **************absolute error************** in the result are given by the sum of the bounds for the absolute errors of the operands

In _**********multiplication**********_ and ********division,******** the bounds for the **************relative error************** in the result are added

### General Error-Propagation Formula

Let $y$ be a function with several variables, and let $x = (x_1, \dots, x_n)$ be the real value, and ${x^*=(x^*_1, \dots, x^*_n)}$ be the calculated values of $x$, then $\Delta x_i = x^*_i - x_i$, and ${\Delta y = y(x^*) - y(x)}$, then

$$ \Delta y \approx \sum_{i = 1}^n \frac{\partial y}{\partial x_i}(x^*) \Delta x_i \quad \text{ and }\quad |\Delta y| \lesssim \left|\sum_{i = 1}^n \frac{\partial y}{\partial x_i} (x^*) \Delta x_i\right| $$

********Th:******** The relative error in a quantity is approximately equal to the absolute error in its natural logarithm, since

$$ \Delta (\ln y) \approx \frac{\Delta y}{y} $$

Let $y = x_1^{m_1}x_2^{m_2} \cdots x_n^{m_n}$, and $x_i \ne 0$, then

$$ \left|\frac{\Delta y}{y}\right| \lesssim \sum_{i = 1}^n \left|m_i\right|\left|\frac{\Delta x_i}{x_i}\right| $$

Assume that $\Delta x_1, \Delta x_2, \dots, \Delta x_n$ are independent random variables with mean zero and standard diviation $\varepsilon_1, \varepsilon_2, \dots, \varepsilon_n$. Then the standard error $\varepsilon$ for $y =y(x_1, \dots, x_n)$ is given by the formula

$$ \varepsilon = \left(\sum_{i = 1}^n \left(\frac{\partial y}{\partial x_i}\right)^2 \varepsilon_i^2\right)^{1/2} $$