---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Legendre Symbols]], [[Quadratic Congruences]]

Let $a$ and $b$ are relatively prime, $b$ is odd and $b = \prod_{i = 1}^r p_i^{k_i}$, then we define the _****Jacobi symbol****_ as

$$ (a/b) = \prod_{i = 1}^r (a/p_i)^{k_i} $$

********Th:******** If $a$ is a quadratic residue of $b$, then $(a/b) =1$. But the converse is not true, meaning we have a test for quadratic nonresidue of $b$

Let $b$ and $b'$ be positive odd integers, and $\gcd(aa', bb')= 1$, then

- $a \equiv a' \pmod b$ , then $(a/b) = (a'/b)$
- $(aa'/b) =(a/b)(a'/b)$
- $(a/bb') = (a/b)(a/b')$
- $(a^2/b) = (a/b^2) =1$
- $(1/b) =1$
- $(-1/b) = (-1)^{(b-1)/2}$
- $(2/b)= (-1)^{(b^2-1)/8}$

**************************************************Generalized Quadratic Reciprocity Law**************************************************

If $a$ and $b$ are relatively prime positive odd integers, each greater than $1$, then

$$ (a/b)(b/a) =(-1)^{\frac{a-1}{2}\frac{b-1}{2}} $$

## Quadratic Congruences with Composite Moduli

********Th:******** If $p$ is an odd prime and $\gcd(a, p) = 1$, then the congruence

$$ x^2 \equiv a \pmod{p^n} \qquad n \ge1 $$

has a solution iff $(a/p) =1$

********Th:******** Let $a$ be an odd integer. Then

- $x^2 \equiv a \pmod 2$ always has solution
- $x^2 \equiv a \pmod 4$ has a solution iff $a \equiv 1 \pmod 4$
- $x^2 \equiv a \pmod {2^n}$, for $n \ge 3$, has a solution iff $a \equiv 1 \pmod 8$

********Th:******** Let $n =2^{k_0}p_1^{k_1}p_2^{k_2} \cdots p_r^{k_r}$ be the prime factorization of $n >1$ and let $\gcd(a, n) = 1$. Then ${x^2\equiv a \pmod n }$ is solvable iff

- $(a/p_i) =1$ for all $i = 1, 2, \dots, r$
- $a \equiv 1 \pmod 4$, if $4 \,\|\, n$; $a\equiv 1 \pmod 8$ if $8 \mid n$