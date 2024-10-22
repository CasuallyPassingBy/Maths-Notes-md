---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Gamma Distribution]]

We say that a random variable $X$ has $\chi^2$ distribution or (Chi-squared distribution) with parameter $n >0$, written as $X \sim \chi^2(n)$, if the pdf of $X$ is of the form

$$ f(x;n) = \begin{dcases} \frac{1}{\Gamma(n/2)}\left(\frac{1}{2}\right)^{n/2} x^{n/2 -1}e^{-x/2} & x>0\\ 0 & x\le0 \end{dcases} $$

We can calculate the cdf as

$$ F(x; n) = \frac{1}{\Gamma(n/2)}\gamma\left(\frac{n}{2}, \frac{x}{2}\right) = P\left(\frac{n}{2},\frac{x}{2}\right) $$

where again $\gamma(\cdot, \cdot)$ represents the lower incomplete gamma function, and $P(\cdot, \cdot)$ represent the regularized lower incomplete gamma function.

We can actually see that if $X \sim \chi^2(n)$, then

$$ X\sim \Gamma\left(\frac{n}{2}, \frac{1}{2}\right) $$

meaning the $\chi^2$ distribution is a special case of the $\Gamma$ distribution.

We get that

- $E[X] = n$
- $\operatorname{Var}[X] = 2n$
- The mode is $\max\{n-2,0\}$
- The median is approximately $k\left(1-\frac{2}{9n}\right)^3$

An important property, we get that $X \sim N(0,1)$, a standard normal, then

$$ X^2 \sim \chi^2(1) $$

Let $X$ and $Y$ two independet random variables with a distribution $\chi^2(n)$ and $\chi^2(m)$, respectively, then

$$ X + Y \sim \chi^2(n+m) $$

From this we can deduce, that if we have $X_1, \dots, X_n$ be independent random variables that are distributed as standard normals we get that

$$ \sum_{i = 1}^n X_i^2 \sim \chi^2(n) $$

### Cochran's theorem

Let $X_1, \dots, X_n$ be independent random variables each one with a distribution $N(\mu, \sigma^2)$. Then if we define

$$ \bar X = \frac{1}{n}\sum_{i = 1}^n X_i \qquad S^2 = \frac{1}{n-1}\sum_{i = 1}^n(X_i -\bar X)^2 $$

with this we get that

$$ \frac{1}{\sigma^2}\sum_{i =1}^n(X_i-\bar X)^2=\frac{(n-1)S^2}{\sigma^2} \sim \chi^2(n-1) $$

We can calculate the $m$th moments of $X\sim\chi^2(n)$ is of the form

$$ E[X^m]= 2^m \frac{\Gamma(n/2+m)}{\Gamma(n/2)} $$

The moment generating function is

$$ M(t) = \left(\frac{1}{1-2t}\right)^{n/2} $$The characteristic function is $$ \phi(t) = \left(\frac{1}{1-2it}\right)^{n/2} $$