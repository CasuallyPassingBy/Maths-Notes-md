---
tags:
  - ProbabilityTheory
---

Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]], [[Geometric Distribution]]

We say the $X$ is a random variable with a negative binomial distribution with parameters $r \in \Bbb N^+$ and $p \in [0,1]$, and we write $X \sim \operatorname{bin\, neg}(r,p)$ if the the pmf of $X$ has the form

$$ f(x; r, p) = \begin{dcases} {{r+x-1}\choose x} p^r(1-p)^x& x \in \Bbb N \\ \\ 0 & \text{otherwise} \end{dcases} $$

We can actually use the [[Generalised Binomial Theorem|generalised binomial coefficients]] to get that

$$ {{r+x-1}\choose x} = (-1)^r{{-r}\choose x} $$

We have that

- $E[X] = \dfrac{r(1-p)}{p}$
- $\operatorname{Var}[X] = \dfrac{r(1-p)}{p^2}$

**Prop:** Let $r \in \Bbb N^+$ and let $X_1,X_2,\dots,X_r$ be independent random variables, each one of them with a distribution $\operatorname{geo}(p)$, then

$$ \sum_{i = 1}^r X_i \sim \operatorname{bin \,neg}(r,p) $$

Reciprocitically, each random variable with distribution $\operatorname{bin \,neg}(r,p)$ can be expressed as a sum of the form above.

If we calculate the probabliti generating function of $X \sim \operatorname{bin \, neg}(r,p)$ then we have that

$$ G(t) \left(\frac{p}{1-(1-p)t}\right)^r $$

and the moment generating function is

$$ M(t) = \left(\frac{p}{1-(1-p)e^t}\right)^r\qquad |t|<-\ln(1-p) $$

Using the moment generating function we can see that if $X \sim \operatorname{bin\,neg}(r,p)$ and ${Y\sim{\operatorname{bin\, neg}(s, p)}}$ are independent, then $X+Y \sim \operatorname{bin\, neg}(r+s, p)$

The characteristic function is $$ \phi(t) = \left(\frac{p}{1-(1-p)e^{it}}\right)^r $$
