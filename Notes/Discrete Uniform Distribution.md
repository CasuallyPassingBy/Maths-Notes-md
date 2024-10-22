---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]]
This distribution is the discrete analogue of the [[Uniform Continuous Distribution]]

Let $X$ be random variable with uniform distribution on a set of $n$ numbers $\{x_1, \dots, x_n\}$. This means that each of the members of the set has a probability of $1/n$. We denote it as ${X \sim \operatorname{unif}\{x_1, \dots, x_n\}}$, meaning has a distributive like this one.

$$ f(x) = \begin{dcases} \frac{1}{n} & x \in\{ x_1, \dots, x_n\} \\ \\ 0 &\text{otherwise} \end{dcases} $$

We have that

- $E[X] = \frac{1}{n}\sum_{i =1}^n x_i = \mu$
- $\operatorname{Var}[X]= \frac{1}{n}\sum_{i =1}^n (x_i -\mu)^2$

If we have that $X \sim \operatorname{unif}\{1, \dots,n\}$, then

- $E[X] = (n+1)/2$
- $E[X^2] = (n+1)(2n+6)/6$
- $\operatorname{Var}[X]= (n^2-1)/12$

We have the the Probability Generating function of $X \sim \operatorname{unif}\{1, \dots,n\}$ is

$$ G(t) = \frac{t(1-t^n)}{n(1-t)} $$

and the Moment generating function of $X \sim \operatorname{unif}\{1, \dots,n\}$ is

$$ M(t)= \frac{e^{t}(1-e^{nt})}{n(1-e^t)} $$
If we have that $X \sim \text{unif}{x_1, \dots, x_n}$, then $$G_X (t) = \frac{1}{n} \sum_{i = 1}^n t^{x_i}$$
