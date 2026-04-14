---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Convergence of Random Variables]], [[Important Probability Inequalities]]

# Weak Law of Large Numbers 

Let $X_1, X_2, \dots$ be independent and identically distributed random variables with mean $\mu$. Then $$\frac{1}{n}\sum_{i = 1}^n X_i \stackrel{\Bbb P}{\longrightarrow} \mu$$
# Strong Law of Large Numbers
Let $X_1, X_2, \dots$ be independent and identically distributed random variables with mean $\mu$. Then $$\frac{1}{n}\sum_{i = 1}^n X_i \stackrel{a.s.}{\longrightarrow} \mu$$
# Central Limit Theorem

Let $X_1, \dots$ be a sequence of independent and identically distributed random variables, such that $E[X_n] = \mu$ and $\text{Var}(X_n) = \sigma^2<\infty$. Then $$\frac{X_1+\dots + X_n- n \mu}{\sqrt n \sigma} \stackrel{d}{\longrightarrow} N(0, 1).$$If we consider the averages as $$\bar X_n := \frac{1}{n}\sum_{k = 1}^n X_k.$$
Then we can rewrite it as $$\frac{\sqrt n (\bar X_n - \mu )}{\sigma} \stackrel{d}{\longrightarrow} N(0, 1).$$
# Slutsky's Theorem

Let $X_n, Y_n$ be sequences of random variables. If $X_n \stackrel{d}{\longrightarrow} X$, and $Y_n \stackrel{d}{\longrightarrow} c$ where $c$ is a constant, then
- $X_n + Y_n \stackrel{d}{\longrightarrow} X + c$
- $X_n Y_n \stackrel{d}{\longrightarrow} Xc$
- $X_n/Y_n \stackrel{d}{\longrightarrow} X/c$ provided that $c \neq 0$.

This gives us the following version of the of central limit theorem: $$\frac{\sqrt n (\bar X_n - \mu )}{S_n} \stackrel{d}{\longrightarrow} N(0, 1),$$where $$\bar X_n := \frac1{n}\sum_{k = 1}X_k, \qquad S^2_n := \frac{1}{n-1} \sum_{k = 1}^n (X_k - \bar X_n)^2.$$

# De Moivre-Laplace Theorem

Let $X_1, \dots$ be a sequence of independent and identically distributed random variables with Bernoulli distribution with parameter $p \in (0,1)$. For any two real numbers $a<b$ $$\lim_{n \to \infty} \Bbb P\left(a <\frac{X_1 + \dots+ X_n -np}{\sqrt{np(1-p)}}<b\right) = \frac{1}{2\pi} \int_a^be^{-x^2/2}\, dx$$ 