---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]]

A random variable $X$ has a normal distribution with parameters, $\sigma >0$, and $\mu \in \Bbb R$, we denote it as $X \sim N(\mu , \sigma^2)$, if the pdf is of the form

$$ f(x;\mu, \sigma^2) = \frac{1}{\sqrt{2\pi \sigma^2}}e^{-(x-\mu)^2/2\sigma} $$

and the cdf is

$$ F(x; \mu, \sigma^2) =\int_{-\infty}^x \frac{1}{\sqrt{2\pi \sigma^2}}e^{-(t-\mu)^2/2\sigma}\, dt= \frac{1}{2}+\frac{1}{2}\operatorname{erf}\left(\frac{x-\mu}{\sqrt{2\sigma^2}}\right) $$

We have that

- $E[X] = \mu$
- $\operatorname{Var}[X] = \sigma^2$
- The mode is $\mu$
- The median is $\mu$

Sea $X \sim N( \mu, \sigma^2)$, entonces

$$ Z = \frac{X-\mu}{\sigma} \sim N(0,1) $$

This is called standarisation. We can un-standarize is, if $Z\sim N(0,1)$, and get that

$$ X = \mu +\sigma Z\sim N(\mu, \sigma^2) $$

We can look at the special case of $Z \sim N(0,1)$, ,this is called the standard normal distribiution, then we get that

$$ \Phi(x)=P(Z \le x) = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^x e^{-u^2/2}\, du = \frac{1}{2}+\frac{1}{2}\operatorname{erf}\left(\frac{x}{\sqrt{2}}\right) $$

and we have can see that

$$ \Phi(-x) = 1-\Phi(x) $$

the pdf, is

$$ \phi(x) = \frac{1}{\sqrt{2\pi}} e^{-x^2/2} $$

In this case, we will use $\alpha$ in the inteval $(0,1)$, the number $z_\alpha$ will denote the quantile to the $100(1-\alpha)\%$ of the normal distribution, meaning

$$ \Phi(z_\alpha) = 1 - \alpha $$

We can calculate the get the moment generating function of $X \sim N(\mu, \sigma^2)$, as

$$ M(t) = \exp\left(\mu t+\frac{1}{2}\sigma^2t^2\right) $$

and we get that the $n$th moment is of the form for $X \sim N(0,\sigma^2)$

$$ E[X^n] = \begin{dcases} \frac{n!}{(n/2)!}\left(\frac{\sigma^2}{2}\right)^{n/2} & n \text{ even} \\ 0 & n \text{ odd} \end{dcases} $$

The characteristic function is $$ \phi(t) = \exp\left(\mu it-\frac{1}{2}\sigma^2t^2\right) $$

Let $X_1$ and $X_2$ be independent random variables with distribution $N(\mu_1, \sigma_1^2)$ and $N(\mu_2, \sigma_2^2)$, respectively, then

$$ X_1 + X_2 \sim N(\mu_1 + \mu_2, \sigma_1^2+\sigma_2^2) $$