---
tags:
  - NumberTheory
  - AnalyticNumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Quadratic Congruences]], [[Prime Numbers]]
## The Legendre Symbols

**********Def:********** Let $p$ be an odd prime and let $\gcd(a, p )=1$. The ***************_Legendre symbol $(a/p)$_ is defined by

$$ \left(\frac{a}{p}\right) = \begin{cases} 1 & \text{if $a$ is a quadratic residue of $p$} \\ -1 & \text{if $a$ is not a quadratic residue of $p$} \end{cases} $$

********Th:******** Let $p$ be an odd prime and let $a$ and $b$ be integers that are relatively prime to $p$. Then

- If $a\equiv b \pmod p$, then $(a/p)=(b/p)$
- $(a^2/p ) =1$
- $(a/p) \equiv a^{(p-1)/2} \pmod p$
- $(ab/p) = (a/p)(b/p)$
- $(1/p) = 1$
- $(-1/p) = (-1)^{(p-1)/2}$

**********Cor:********** If $p$ is an odd prime then
$$ (-1/p) = \begin{cases} 1 & \text{if }p \equiv 1 \pmod 4 \\ -1 & \text{if }p \equiv 3 \pmod 4 \\ \end{cases} $$
This results is linked with [[Wilson's Theorem]]

********Th:******** There are infinitely many primes of the form $4k+1$

********Th:******** If $p$ is an odd prime then

$$ \sum_{a = 1}^{p-1}(a/p) =0 $$

Hence, there are precisely $(p-1)/2$ quadratic residues and $(p-1)/2$ quadratic nonresidues of $p$

************Cor:************ The quadratic residues of an odd prime $p$ are congruent modulo $p$ to the even powers of a primitive root $r$ of $p$; the quadratic nonresidues are congruent to the odd powers of $r$

### Gauss’s Lemma

Let $p$ be an odd prime and let $\gcd(a,n) = 1$. If $n$ denotes the number of integers in the set

$$ S= \left\{ a, 2a,3a, \dots, \frac{p-1}{2}a\right\} $$

whose remaineders upon division by $p$ except $p/2$, then

$$ (a/p) = (-1)^n $$

********Th:******** Let $p$ be an odd prime then

$$ (2/p) = \begin{cases} 1 & \text{if } p \equiv 1, 7\pmod 8 \\ 1 & \text{if } p \equiv 3, 5\pmod 8 \\ \end{cases} $$

**********Cor:********** If $p$ is an odd prime then

$$ (2/p) = (-1)^{(p^2-1)/8} $$

****Th:**** If $p$ and $2p+1$ are both odd primes, then the integer $2(-1)^{(p-1)/2}$ is a primitive root of $2p+1$

********Th: T********here are infinitely many primes of the form $8k-1$ ****************

**************Lemma:************** Let $p$ be an odd prime and let $\gcd(a,n) = 1$, then

$$ (a/p) = (-1)^{\sum_{k =1}^{(p-1)/2}\lfloor ka/p\rfloor} $$

## Quadratic Reciprocity Law

If $p$ and $q$ are distinct odd primes, then

$$ (p/q)(q/p) = (-1)^{\frac{p-1}{2}\frac{q-1}{2}} $$

****Cor:**** If $p$ and $q$ are distinct odd primes, then

$$ (p/q)(q/p) = \begin{cases} 1 & \text{if } p \equiv 1 \pmod 4 \text{ or }q \equiv 1 \pmod 4 \\ -1 & p \equiv q \equiv 3 \pmod 4 \end{cases} $$

****Cor:**** If $p$ and $q$ are distinct odd primes, then

$$ (p/q) = \begin{cases} (q/p) & \text{if } p \equiv 1 \pmod 4 \text{ or }q \equiv 1 \pmod 4 \\ -(q/p) & p \equiv q \equiv 3 \pmod 4 \end{cases} $$

********Th:******** If $p \ne 3$ is an odd prime, then

$$ (3/p) = \begin{cases} 1 & p \equiv \pm 1\pmod{12}\\ -1 & p \equiv \pm 5\pmod{12}

\end{cases} $$

Some Legendre symbols are

$$ (-2/p) = \begin{cases} 1 & \text{if } p \equiv 1, 3\pmod 8 \\ 1 & \text{if } p \equiv 5, 7\pmod 8 \\ \end{cases} $$

$$ (-3/p) = \begin{cases} 1 & p \equiv 1\pmod{6}\\ -1 & p \equiv -1\pmod{6}

\end{cases} $$

$$ (5/p) = \begin{cases} 1 & p \equiv \pm 1\pmod{10}\\ -1 & \text{otherwise}

\end{cases} $$

$$ (7/p) = \begin{cases} 1 & p \equiv \pm1, \pm3, \pm9\pmod{28}\\ -1 & \text{otherwise}

\end{cases} $$

**************Th:************** Let $p$ be a prime and $p \equiv 3 \pmod4$ and $x =\pm a^{\frac{p+1}4}$, then $x^2 \equiv a \pmod p$

**************Th:************** Let $p$ be a prime and $p \equiv 5 \pmod8$, then $x^2 \equiv a \pmod p$ has a solution with $x = a^{\frac{p+3}{8}}$ or $x = 2^{\frac{p-1}4}a^{\frac{p+3}{8}}$