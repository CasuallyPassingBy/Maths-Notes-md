---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Gamma Function]]

A random variable $X$ has a Weibull distribution with parameters $\alpha>0$ and $\lambda>0$, denoted as ${X \sim \operatorname{Weibull}(\alpha, \lambda)}$, if the pdf is

$$ f(x; \alpha,\lambda) = \begin{cases} \lambda \alpha(\lambda x)^{\alpha-1} e^{-(\lambda x)^\alpha} & x>0 \\ 0 & \text{otherwise} \end{cases} $$

We can calculte the cdf as

$$ F(x; \alpha, \lambda) = \begin{cases} 0 & x\le 0\\ 1-e^{-(\lambda x)^{\alpha}} & x>0 \end{cases} $$

We can get that

- $E[X] = \dfrac{1}{\lambda}\Gamma(1+1/\alpha)$
- $\operatorname{Var}[X] = \dfrac{1}{\lambda^2}(\Gamma(1+2/\alpha)-\Gamma^2(1+1/\alpha))$
- the mode is
    - for $\alpha > 1$, is $\frac{1}{\lambda}(\frac{\alpha -1 }{\alpha}) ^{1/\alpha}$
    - for $\alpha \le 1$, is $0$
- the median is $\dfrac{1}{\lambda }(\ln 2)^{1/\alpha}$

We can calculate the $n$th moment of $X$ as

$$ E[X^n] = \frac{1}{\lambda^n}\Gamma(1+n/\alpha) $$

From this we can calculte the moment generating function

$$ M(t) = \sum_{n = 0}^\infty \frac{t^n}{\lambda^n n !}\Gamma\left(1+\frac{n}{\alpha}\right) $$

we can calculate the Weibull distribution, with $U \sim \operatorname{unif}(0,1)$

$$ \frac{1}{\lambda}(-\ln(1-U))^{1/\alpha} \sim \operatorname{Weibull}(\alpha, \lambda) $$