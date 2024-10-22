---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Exponential Distribution]]

Let $X$ be a random variable with a gamma distribution with parameters $\alpha >0$ and $\lambda>0$, written ${X \sim \Gamma(\alpha, \lambda)}$, if the pdf is of the form

$$ f(x;\alpha, \lambda) = \begin{dcases} \frac{(\lambda x)^{\alpha-1}}{\Gamma(\alpha)}\lambda e^{-\lambda x} & x >0 \\ \\ 0 & \text{otherwise} \end{dcases} $$

with $\Gamma (\alpha)$ being the gamma function. If $\alpha$ is an integer, we call the distribution the Erlang distribution, and we can simplify somethings.

If we calculate the cdf we get that

$$ F(x; \alpha, \lambda) = \begin{dcases} 0 & x \le 0\\ \frac{\gamma(\alpha, \lambda x)}{\Gamma(\alpha)}=P(\alpha, \lambda x) & x >0 \end{dcases} $$

where $\gamma(\alpha, \lambda x)$, represents the lower incomplete gamma function, and $P(\alpha, \lambda x)$ is the regularized lower incomplete gamma function.

We get that

- $E[X] = \alpha /\lambda$
- $\operatorname{Var}[X] = \alpha/\lambda^2$
- The mode
    - For $\alpha \ge 1$, $\frac{\alpha -1}{\lambda}$
    - For $\alpha < 1$, is $\alpha$
- There’s no formula for the median

**Prop:** Let $X_1, \dots, X_n$ be indepdent random variables each one with a distribution of $\exp(\lambda)$ for $\lambda>0$. Then

$$ \sum_{i = 1}^n X_i \sim \operatorname{\Gamma}(n,\lambda) $$

We can get that the moment generating function is of the form

$$ M(t) = \left(\frac{\lambda}{\lambda-t}\right)^\alpha $$

The characteristic function is $$ \phi(t) = \left(\frac{\lambda}{\lambda-it}\right)^\alpha $$

We can calculate that the $n$th moment of $X$ is

$$ E[X^n] = \frac{\alpha^{\underline n}}{\lambda^n} $$

where $\alpha^{\underline n}$ means the $n$th falling factioral of $\alpha$.

Let $X$ and $Y$ be independent random variables such that $X \sim \operatorname{gamma}(\alpha_1,\lambda)$ and $Y \sim \operatorname{gamma}(\alpha_2,\lambda)$, then

$$ X+Y \sim X \sim \operatorname{\Gamma}(\alpha_1+\alpha_2,\lambda) $$

Let $X$ be a random variable with $\operatorname{gamma}(\alpha, \lambda)$ if $c>0$ a constant then

$$ cX \sim \operatorname{\Gamma}(\alpha,\lambda/c) $$

If we use an Erlang distribution, namely $n \in \Bbb N^+$, and $X\sim \operatorname{gamma}(n, \lambda)$, we can calculate the cdf as

$$ F(x;n, \lambda)=\sum_{k =n}^\infty \frac{(\lambda x)^k}{k!} e^{-\lambda x} $$