---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]]

We say that the random variable $X$ has a Bernoulli distribution with paramenter $p$, and denoted as $X\sim\operatorname{Ber}(p)$, if it has the following pmd,

$$ f(x;p) = \begin{cases} p^{x}(1-p)^{1-x} & x = 0,1 \\ 0 & \text{otherwise} \end{cases} $$

with the cdf of the form

$$ F(x;p) = \begin{cases} 0 & x <0\\ p & 0\le x <1\\ 1 & 1 \le x \end{cases} $$

We have that

- $E[X] = p$
- $\operatorname{Var}[X]= p(1-p)$
- $E[X^n] = p$

We have the the probability generating function is

$$ G(t) = 1-p+pt $$

The moment generating function
$$ M(t)=1-p+pe^t $$
The characteristic function $$\phi(t) = 1-p+pe^{it}$$