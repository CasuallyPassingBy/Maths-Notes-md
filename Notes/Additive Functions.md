---
tags:
  - NumberTheory
  - AnalyticNumberTheory
---
Subjects: [[Elementary Number Theory]], [[Analytic Number Theory]]
Links: [[Multiplicative Functions]]

**Def:** A arithmetic function $f$ is called **********additive********** if

$$ f(mn) = f(m)+f(n) $$

for $\gcd(m,n) = 1$

**Def:** A arithmetic function $f$ is called **********completely additive********** if for any $m, n$

$$ f(mn) = f(m)+f(n) $$

********Th:******** If we have an additive function $f$, then we can get a multiplicative function by

$$ g(n) = b^{f(n)} $$

for a fixed base $b$, and if the function $f$ is completely additive then $g$ will be completely multiplicative.

### Prime Omega functions

If $n = p_1^{k_1}p_2^{k_2}\cdots p_r^{k_r}$ is the prime factorization of $n$, then we the define $\omega(n)$ to be the number of distinct prime factors,

$$ \omega(n) = \sum_{p \mid n} 1 $$

and, $\Omega(n)$ counts the ******total****** number of prime factors of $n$

$$ \Omega(n) = \sum_{p^\alpha\mid n} 1 = \sum_{p^\alpha\parallel n}\alpha = \sum_{i =1}^rk_i $$

Which is completely additive, and has the following properties

$$ \omega(n) \le \Omega(n) $$

### Liouville function

From these two prime counting functions we can get that another important functions called the _Liouville function_ defined as

$$ \lambda(n) = (-1)^{\Omega(n)} $$

it is completely multiplicative.

If we look at the

$$ \sum_{d\mid n}\lambda(d) = \begin{cases} 1 & \text{if $n$ is a perfect square} \\ 0 & \text{otherwise} \end{cases} $$

which is the square number characteristic function.