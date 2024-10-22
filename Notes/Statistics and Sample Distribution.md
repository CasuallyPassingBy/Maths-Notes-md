---
tags:
  - "#Statistics"
---
Subjects: [[Statistics]]
Links: [[Random Variables]], [[Random Vectors]], [[Normal Distribution]], [[Chi-squared Distribution]], [[F-distribution]], [[Student's t-distribution]]

**Def:** A *random sample* is a collection of random variables $X_1, \dots, X_n$ that satisfy that they are independent and the have the same distribution. The number $n$ is called the *sample size*.

**Def:** The *space of samples* or *sample space* is the set of values that can take a random sample $X_1, \dots, X_n$ and it is denoted as $\frak X$ 

**Def:** A *statistic* is any function $T(X_1, \dots, X_n)$ of the random sample that doesn't depend on any hidden parameters. We will use the notation $\underline X$, to refer to the sample, then $T(\underline X)$. We additionally we would like to have that $T: \Bbb R^n \to \Bbb R^k$ be measurable, and statistics are also random variables. 

Since it is a random variable, it can have a pdf/pmf to understand it better the statistic. 
# Important Statistics
Sample mean: $$\overline X := \frac{1}{n} \sum_{k = 1}^n X_k$$
Sample variance: $$S^2:= \frac{1}{n-1} \sum_{k = 1}^nX_k $$

**Prop:** Let $X_1, \dots, X_n$ is a random sample of $f(x; \theta)$ such that $E[X_i] = \mu$ and $\text{Var}(X_i) = \sigma^2$, for all $i$, then $$E[\overline X] = \mu \qquad \text{Var}(\bar X) = \frac{\sigma^2}{n}$$

**Lemma:** Let $X_1, \dots, X_n$ is a random sample of $f(x; \theta)$, then $$\sum_{i = 1}^n (X_i-\mu)^2  =\sum_{i = 1}^n(X_i-\overline X)^n+ n(\overline X-\mu )^2 $$
**Prop**: Let $X_1, \dots, X_n$ is a random sample of $f(x; \theta)$ such that $E[X_i] = \mu$ and $\text{Var}(X_i) = \sigma^2$, for all $i$, then $$E[S^2] = \sigma^2$$
**Cor:** Let $X_1, \dots, X_n$ be a random sample of a population of distribution $N(\mu, \sigma^2)$, then $$\overline X \sim N(\mu, \sigma ^2/n)$$
**Th:** Let $X_1, \dots, X_n$ be independent random variables such that $X_i \sim N(\mu_i, \sigma^2_i)$ for all $i \in \{1, \dots, n\}$. Let $Z_i = \dfrac{X_i - \mu_i}{\sigma_i} \sim N(0, 1)$, then
- $Z_i^2\sim \chi^2(1)$
- $\sum\limits_{i = 1}^n Z_i^2 \sim \chi^2(n)$ 

**Th:** Let $X_1, \dots, X_n$ be a random sample with distribution $N(\mu, \sigma^2)$. Then: 
- $\bar X$ and the vector $(X_1 - \bar X, \dots, X_n - \bar X)$
- $\bar X$ and $S^2$ are independent
- $\dfrac{(n-1)S^2}{\sigma^2} \sim \chi^2(n-1)$ 
- $E[S^2] = \sigma^2$ and $\text{Var}(S^2) = \dfrac{2\sigma^4}{n-1}$ 

**Cor:** Let $X_1, \dots, X_{m+1}$ be a random sample with distribution $N(\mu_X, \sigma^2_X)$ and  $Y_1, \dots, Y_{n+1}$ be a random sample with distribution $N(\mu_Y, \sigma^2_Y)$, then $$\frac{mS_X^2}{\sigma^2_X} \sim \chi^2(m) \qquad \frac{nS^2_Y}{\sigma_Y^2} \sim \chi^2(n)$$
usando propiedades de la distribución $F$ de Fischer, entonces $$\frac{S^2_x/\sigma^2_x}{S^2_Y/\sigma²_Y} \sim F(m , n) $$
**Cor:**  Let $X_1, \dots, X_n$ be a random sample with distribution $N(\mu, \sigma^2)$. Then $$\frac{\overline X -\mu}{S/\sqrt n} \sim t(n-1)$$