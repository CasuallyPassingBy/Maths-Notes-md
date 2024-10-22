---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]]

We say that a random variable $X$ is distributed geometrically with parameter $p$, written as ${X \sim \operatorname{geo}(p)}$ if it has a pmf being

$$ f(x;p) = \begin{cases} p (1-p)^x & x \in \Bbb N \\ 0 & \text{otherwise} \end{cases} $$

and the cdf is of the form

$$ F(x;p) = \begin{cases} 0 & x <0 \\ 1 -(1-p)^{k+1} & k \le x < k+1; \quad k\in\Bbb N \end{cases} $$

We have that

- $E[X] = \dfrac{1-p}{p}$
- $\operatorname{Var}[X]= \dfrac{1-p}{p^2}$

We can calculate the probability generating function of $X \sim \operatorname{geo}(p)$, that is

$$ G(t) = \frac{p}{1-(1-p)t} $$

additionally we can get the moment generating function as
$$ M(t) = \frac{p}{1-(1-p)e^t}\qquad |t|<-\ln(1-p) $$The characteristic function $$\phi(t) = \frac{p}{1-(1-p)e^{it}}$$
