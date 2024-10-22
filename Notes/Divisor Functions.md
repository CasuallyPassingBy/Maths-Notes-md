---
tags:
  - NumberTheory
  - AnalyticNumberTheory
---
Subjects: [[Elementary Number Theory]], [[Analytic Number Theory]]
Links: [[Prime Numbers]], [[Multiplicative Functions]]

**Def:** Given a positive integer $n$, let $\tau(n)$ or $d(n)$ denote the number of divisors of $n$, and $\sigma(n)$ denote the sum of these divisors.

********Th:******** If $n = p_1^{k_1}p_2^{k_2}\cdots p_r^{k_r}$ is the prime factorization of $n >1$ then the positive divisors of $n$ are of the form

$$ d =p_1^{a_1}p_2^{a_2}\cdots p_r^{a_r} $$

with $0\le a_i \le k_i$ for $i \le r$

********Th:******** If $n = p_1^{k_1}p_2^{k_2}\cdots p_r^{k_r}$ is the prime factorization of $n >1$, then

- $\tau(n) = (k_1+1)(k_2+1)\cdots(k_r+1)$
- $\sigma(n) = \dfrac{p_1^{k_1+1}-1}{p_1-1}\dfrac{p_2^{k_2+1}-1}{p_2-1} \cdots \dfrac{p_r^{k_r+1}-1}{p_r-1}$

********Th:******** The functions $\tau$ and $\sigma$ are multiplicative functions

********Prop:******** For any $n>1$ then we have that 
$$ n^{\tau(n)/2} = \prod_{d\mid n} d $$

- Some properties
    $$ (1*\operatorname{Id}_{-1})(n)=\sum_{d\mid n } \frac{1}{d} = \frac{\sigma(n)}{n} $$
    $$ \prod_{p \mid n} \left(1 - \frac{1}{p}\right) < \frac{n}{\sigma(n)}<1 $$
    for a composite number $n$, then
    $$ n+\sqrt n <\sigma(n) $$
    $$ \tau(n^2) = \sum_{d \mid n} 2^{\omega(n)} $$
    $$ (\tau^3 * 1)(n)=\sum_{d\mid n} \tau(d)^3 = \left(\sum_{d\mid n} \tau(d) \right)^2 =(\tau*1)^2(n) $$
    $$ (\sigma * 1)(n)=\sum_{d\mid n} \sigma(d) = \sum_{d\mid n}\left(\frac{n}{d}\right) \tau(d) = (\operatorname{Id} * \tau)(n) $$
    $$ (\sigma * \operatorname{Id})(n)=\sum_{d\mid n} \left(\frac{n}{d}\right)\sigma(d) = \sum_{d\mid n} d\tau(d) = (\operatorname{Id}\tau *1)(n) $$
    
**Prop:** for any $n \ge 1$, then

$$ 2^{\omega(n)} \le \tau(n) \le 2^{\Omega(n)} $$

**Def:** Some important multiplicative functions are $\operatorname{Id}_s(n)= n^s$, for a fixed $s\in \mathbb{C}$, and we can define

$$ \sigma_s(n) = \sum_{d\mid n} \operatorname{Id}_s(d) = (\operatorname{Id}_s * 1)(n) $$

then it is multiplicative, with the properties that $\sigma_0 = \tau$ and $\sigma_1 = \sigma$

If $n = p_1^{k_1}p_2^{k_2}\cdots p_r^{k_r}$ is the prime factorization of $n$, then

$$ \sigma_s(n) = \prod_{i = 1}^r \dfrac{p_i^{s(k_i+1)}-1}{p_i-1} $$

Let the special case:

$$ \sigma_{-s}(n) = \frac{\sigma_s(n)}{n^s} $$