---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]]

This might be related to the [[Geometric Distribution]], as the continuous analogue

We say that $X$ is a random variable with exponential distribution with parameter $\lambda>0$, and we write $X \sim \exp(\lambda)$, when the pdf is

$$ f(x; \lambda) = \begin{cases} \lambda e^{-\lambda x} & x >0 \\ 0 & \text{otherwise} \end{cases} $$

We can calculate the cdf as

$$ F(x;\lambda) = \begin{cases} 1-e^{-\lambda x} & x >0 \\ 0 &\text{otherwise} \end{cases} $$

and that $P(X >x ) = e^{-\lambda x}$

We have that

- $E[X] = 1/\lambda$
- $\operatorname{Var}[X] = 1/\lambda^2$
- The mode is $0$
- The median is $\dfrac{\ln 2}{\lambda}$

and the $n$th moment of $X$, we have that

$$ E[X^n] = \frac{n!}{\lambda^n} $$

Let $c>0$ be constant and $X$ be a random variable with distribution $\exp(\lambda)$, we get that

$$ cX \sim \exp(\lambda/c) $$

We can get the moment generating function of $X$

$$ M(t) = \frac{\lambda}{\lambda-t} \qquad t < \lambda $$

The characteristic is $$ \phi(t) = \frac{\lambda}{\lambda-it} \qquad t < \lambda $$

### Memory loss property

Let $X$ be a random variable with exponential distribution with parameter $\lambda>0$. We get that for any $x, y\ge0$,

$$ P(X>x+y\mid X>y) =P(X>x) $$

Let $U$ be a random variable with distribution $\operatorname{unif}(0,1)$ and let $\lambda>0$ be a constant. Then the random variable $X$, defined as

$$ X =-\frac{1}{\lambda}\ln(1-U) $$

Then $X\sim \exp(\lambda)$.