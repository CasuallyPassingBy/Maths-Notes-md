---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]]

This actually comes from the [[Multinomial Theorem|binomial theorem]]. 

We say that $X$ is a random variable has a binomial distribution with parameters $p$ and $n$ , and we write $X \sim \operatorname{bin}(n,p)$. If $X$ has a pmf of the form

$$ f(x;n, p) = \begin{dcases} {n \choose x}p^x (1-p)^{n-x} & x=0,1,2, \dots, n \\ \\ 0 & \text{otherwise} \end{dcases} $$

We have that there’s a simplified form for $F$ being the cdf

$$ F(k; n,p) = P(X \le k) = I_{1-p}(n-k,k+1) = 1-I_p(k+1,n-k) $$

but in simple cases we can just sum over the integers $i \le k$. Where $I_x(a,b)$ represents the regularized incomplete beta function.

We have that
- $E[X] = np$
- $\operatorname{Var}[X]= np(1-p)$

****Prop:**** Let $X_1, \dots, X_n$ be independent random variables each one with a distribution $\operatorname{Ber}(p)$. Then

$$ \sum_{i = 1}^n X_i \sim \operatorname{bin}(n,p) $$

And any random variable with distribution $\operatorname{bin}(n,p)$ can be expressed as the sum above.
This means that any binomial random variable can be thought of as a sum of [[Bernoulli Distribution|Bernulli Random Variables]]

With this we can get the probability generating function, getting that

$$ G(t) = (1-p+pt)^n $$

the moment generating function
$$ M(t)=(1-p+pe^t)^n $$
The characteristic function $$\phi(t) =(1-p+pe^{it})^n$$
**Prop:** Let $X$ and $Y$ be independent random variables, such that $X \sim \operatorname{bin}(n,p)$ and ${Y \sim \operatorname{bin}(m,p)}$. We get that $X+Y \sim \operatorname{bin}(n+m, p)$

**Prop:** Let $X$ be a random variable distributed by $\operatorname{bin}(n,p)$, then $n-X \sim \operatorname{bin}(n,1-p)$