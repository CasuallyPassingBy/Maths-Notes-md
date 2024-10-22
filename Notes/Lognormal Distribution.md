---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Change of Variable Theorem for Random Variables]], [[Normal Distribution]]

A random variable $X$ has a lognormal distribution with parameters $\mu\in \Bbb R$, and $\sigma^2>0$, if ${\ln X \sim N(\mu, \sigma^2)}$, and written as $X\sim \operatorname{Lognormal}(\mu, \sigma^2)$ the pdf is

$$ f(x; \mu, \sigma^2) = \begin{dcases} \frac{1}{x\sqrt{2\pi \sigma^2}}\exp\left(-\frac{(\ln x -\mu)^2}{2\sigma }\right) & x>0\\ \\ 0 & x \le 0 \end{dcases} $$

We can calculate the cdf as

$$ F(x; \mu, \sigma^2) = \frac{1}{2}+\frac{1}{2}\operatorname{erf}\left(\frac{\ln x-\mu}{\sqrt{2\sigma^2}}\right) $$

We can see that

- $E[X] = \exp(\mu+ \tfrac{1}{2}\sigma^2)$
- $\operatorname{Var}[X] = [\exp(\sigma^2) -1]\exp(2\mu +\sigma^2)$
- The mode is $\exp(\mu -\sigma^2)$
- The median is $\exp(\mu)$

We can calculate $n$th moment of $X$ as

$$ E[X^n]= \exp\left(n\mu +\frac{1}{2}n^2\sigma^2\right) $$

Let $X_1$ and $X_2$ be independent random variables with $\operatorname{Lognormal}(\mu_1, \sigma^2_1)$ and $\operatorname{Lognormal}(\mu_2, \sigma^2_2)$, respectively, then

$$ X_1X_2 \sim \operatorname{Lognormal}(\mu_1+\mu_2, \sigma^2_1+\sigma^2_2) $$

We also have that if $X \sim \operatorname{Lognormal}(\mu, \sigma^2)$,and let $a>0$ then

$$ \frac{1}{X} \sim \operatorname{Lognormal}(-\mu, \sigma^2) $$

$$ aX \sim \operatorname{Lognormal}(\mu +\ln a, \sigma^2) $$

$$ X^a\sim \operatorname{Lognormal}(a\mu, a^2\sigma^2) $$