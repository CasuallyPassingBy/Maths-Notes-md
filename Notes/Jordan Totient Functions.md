---
tags:
  - AnalyticNumberTheory
  - NumberTheory
---
Subjects: [[Elementary Number Theory]], [[Analytic Number Theory]]

Links: [[Möbius Function and Inversion Formula]], [[Euler Totient Function]], [[Multiplicative Functions]]

**********Def:********** We can define the Jordan’s totient function for each $k$, as

$$ J_k(n) = n^k \prod_{p \mid n}\left(1-\frac{1}{p^k}\right) $$

it is a multiplicative function, and we can see that $\phi = J_1$.

************Prop:************ Let $n$ be a positive integer then

$$ \sum_{d \mid n } J_k(d) = n^k $$

in the terms of Dirichlet convolution we can simplify it as

$$ J_k * 1 = \operatorname{Id}_k $$

and using the Möbius Inversion formula we get

$$ \sum_{d \mid n} \mu(d) \left(\frac{n}{d}\right)^k = J_k(n) $$

or

$$ \mu * \operatorname{Id}_k = J_k $$

********Th:******** for any $r$ and $s$ and $n >1$, then

$$ \sum_{d\mid n} d^s J_r(d) J_s\left(\frac{n}{d}\right) = J_{r+s}(n) $$

or

$$ (\operatorname{Id}_s J_r)*J_s = J_{r+s} $$