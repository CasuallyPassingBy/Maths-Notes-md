---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Functions for Random Vectors]]

Let $f(x, y)$ be pdf of a absolutelt continuous random vector $(X, Y)$. We define the marginal pdf of the variable $X$, as the following integral

$$ f_X(x) = \int_\Bbb R f(x,y)\, dy $$

Similarly the marginal pdf of the variable $Y$, is defined as

$$ f_Y(y) = \int_\Bbb R f(x,y) \, dx $$

In the case that $f(x, y)$ is the pmf of a discrete random vector $(X, Y)$. We define the marginal pmf of the variable $X$, as the following sum

$$ f_X(x) = \sum_ y f(x, y) $$

Similarly, the marginal pmf of the variable is defined as

$$ f_Y(y) = \sum_x f(x,y) $$

If we have more variables, and the marginal pdf of $(X_1, X_2)$ given the pdf of the vector $(X_1, \dots, X_n)$,

$$ f_{X_1, X_2}(x_1, x_2) = \int_\Bbb R \cdots \int_\Bbb R f(x_1, \dots, x_n) \, dx_3 \cdots \, dx_n $$

We define the marginal pdf/pmf of a random vector, we are going to define the cdf

Let $(X,Y)$ be a random vector, with a cdf $F(x, y)$. The marginal cdf of the variable $X$ is defined as

$$ F_X(x) = \lim_{y \to \infty} F(x,y) $$

Analogously, the marginal cdf of the variable $Y$ is defined as

$$ F_Y(y) = \lim_{x \to \infty} F(x,y) $$

From this we get the inequality

$$ F_X(x) + F_Y(y) -1 \le F(x,y) \le \sqrt{F_X(x) F_Y(y)} $$