---
tags:
  - NumberTheory
  - AnalyticNumberTheory
---
Subjects: [[Elementary Number Theory]], [[Analytic Number Theory]]
Links: [[Multiplicative Functions]]
**Def:** The _Möbius $\mu$-function_ is defined as for a positive integer $n$

$$ \mu(n) = \begin{cases} 1 & \text{if } n= 1 \\ 0 & \text{if }p^2\mid n \text{ for some prime }p \\ (-1)^r & \text{if } n = p_1 p_2 \cdots p_r \text{ where $p_i$ are distinct primes} \end{cases} $$

Similarly we with the use of the Kronecker delta, we can define it as

$$ \mu(n) = \delta_{\omega(n), \Omega(n)} \lambda(n) $$

where $\lambda$ is the Liouville function.

********Th:******** The $\mu$ function is multiplicative.

**Th:** For each integer $n\ge1$

$$ I(n)=\sum_{d\mid n}\mu(d) = (\mu * \operatorname{Id}_0)(n)

$$

In other words we can think of it as

$$ \mu = 1^{-1} $$

as the [[Dirichlet Product|Dirichlet inverse]] of $\operatorname{Id}_0$

### Möbius Inversion formula
Let $F$ and $f$ be arithmetic functions related by

$$ F(n) = (1* f)(n) = \sum_{d\mid n}f(d) $$

then

$$ f(n) = (\mu * F)(n) = \sum_{d\mid n} \mu(d) F\left(\frac{n}{d}\right) $$

********Th:******** the Dirichlet inverse of $\lambda$ [[Additive Functions#Liouville function|Liouville function]], is of the form

$$ \lambda^{-1}(n) = |\mu(n)| = \mu^2(n) $$

and

$$ \lambda(n) = \sum_{d^2\mid n} \mu\left(\frac{n}{d^2}\right) $$

********Th:********

$$ \sum_{d\mid n} |\mu(d)| = 2^{\omega(n)} $$

**Th:** Let $f$ be multiplicative then

$$ \sum_{d\mid n}\mu(d) f(d) = \prod_{p\mid n} (1-f(p)) $$

****************Th:**************** Let $f$ be multiplicative. Then if $f$ is completely multiplicative iff
$$ f^{-1}(n) = \mu(n)f(n) \quad \text{for all }n\ge1 $$

**************Th:************** If $f$ is multiplicative then

$$ \sum_{d \mid n} \mu(d) f(d) = \prod_{p \mid n} (1-f(p)) $$

Another way to define the Möbius $\mu$ function is as follows

$$ \mu(n) = \sum_{\substack{1 \le k\le n \\ \gcd(k,n)=1}} e^{2\pi i\frac{k}{n}} $$
Which is the sum of the primitive nth roots of unity