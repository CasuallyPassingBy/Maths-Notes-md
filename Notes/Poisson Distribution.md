---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]]

Let $X$ be a random variable, we say that $X$ has a Poisson distribution with parameters $\lambda >0$, written as $X \sim \operatorname{Poisson}{\lambda}$, if we have that the pmf of $X$ is of the form

$$ f(x; \lambda) = \begin{dcases} e^{-\lambda}\frac{\lambda^x}{x!} & x \in \Bbb N \\ 0 &\text{otherwise} \end{dcases} $$

we can calculate the cdf as

$$ F(x; \lambda) = P(X\le s) = Q(s, \lambda) $$
where $Q(s, \lambda)$ is the [[Gamma Function#Regularized Incomplete Gamma functions|regularized upper incomplete gamma function]]. 
We have that

- $E[X] = \lambda$
- $\operatorname{Var}[X] = \lambda$

**Prop:** Let $X$ and $Y$ be independent random variables with distribution $\operatorname{Poisson}({\lambda_1})$ and $\operatorname{Poisson}({\lambda_2})$ respectively then

$$ X + Y \sim \operatorname{Poisson}({\lambda_1}+{\lambda_2}) $$

### Approximation through binomial distribution

Let $X$ be a random variable with distribution $\operatorname{bin}(n,p)$ such that $p = \lambda/n$ for sufficiently large $n$, and $\lambda>0$ constant. We can see that for $k \in \Bbb N$,

$$ \lim_{n \to \infty} P(X = k) = e^{-\lambda }\frac{\lambda^k}{k!} $$

meaning we if we have a good approximation of the binomial distribution for large $n$, and small $p$. Namely, we can expect a good approximation when $n \ge 20$ and $p \le 0.05$, or if $n \ge100$ and $np \le 10$. Since the binomial distribution is more expensive to calculate than the Poisson one.

We get that the probability generating function is of the form
$$ G(t) = e^{\lambda(t-1)} $$

We can calculate the moment generating function as

$$ M(t) = \exp(\lambda(e^t-1)) $$

and the $n$th moment is

$$ E[X^n] = \lambda\sum_{k = 0}^{n-1} {{n-1}\choose k} E[X^k] $$
The characteristic function is $$\phi(t) =  \exp(\lambda(e^{it}-1))$$
