---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Expected Value of Random Variables]], [[Random Variables]], [[Probability Functions for Random Variables]]

## Variance
Let $X$ be a random variable, the variance of $X$, denoted as $\text{Var})(X)$, it is defined as
$$
\text{Var}(X) := E[(X-E[X])^2]
$$

Let $X$ be a discrete random variable with a probability mass function $f$. The variance of $X$ is defined as the number

$$ \operatorname{Var}[X] = \sum_x (x-\mu)^2 f(x) $$

when this sum is convergent, and where $\mu$ is the expected value of $X$.

For a continuous random variable $X$ with a probability density function $f$, it is defined as

$$ \operatorname{Var}[X] = \int_\Bbb R (x-\mu)^2 f(x)\, dx $$

when this integral converges.

With this two cases, we can write that

$$ \operatorname{Var}[X] = E[(X-\mu)^2] $$

Properties of the variance. Let $X$ and $Y$ be two random variables with finite variance and $c$ a constant. Then

- $\operatorname{Var}[X]\ge0$
- $\operatorname{Var}[c] = 0$
- $\operatorname{Var}[cX] = c^2\operatorname{Var}[X]$
- $\operatorname{Var}[X+c] = \operatorname{Var}[X]$
- $\operatorname{Var}[X] = E[X^2] -(E[X])^2$
- In general, $\operatorname{Var}[X+Y] \ne \operatorname{Var}[X] + \operatorname{Var}[Y]$
- $\operatorname{Var}[X] \le E[X^2]$
- $\operatorname{Var}[X+Y] = \operatorname{Var}[X] + \operatorname{Var}[Y] +2E[(X-E[X])(Y-E[Y])]$, From this formula we can see that $E[XY]=E[X]E[Y]$ is equivalent to ${\operatorname{Var}[X+Y] = \operatorname{Var}[X]+\operatorname{Var}[Y]}$.

If two random variables $X$ and $Y$ are independent with finite variance, then

$$ \operatorname{Var}[X+Y] = \operatorname{Var}[X] + \operatorname{Var}[Y] $$