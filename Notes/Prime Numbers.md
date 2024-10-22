---
tags:
  - NumberTheory
  - "#AnalyticNumberTheory"
---
Subjects: [[Elementary Number Theory]]
Links: [[Greatest Common Divisor]], [[Lowest Common Multiple]]

A number $p>1$ is _prime_ iff its only positive divisors are $1$ and $p$ itself.

If $p$ is a prime and $p\mid ab$, then $p\mid a \lor p \mid b$

If $p$ is a prime and $p \mid \prod_i^n a_i$, then $\exists 1 \le k\le n[p \mid a_k]$

If $p , q_1, \dots, q_n$ are primes and $p \mid \prod_{i=1}^n q_i$, then $\exists 1 \le k\le n[p = q_k]$

**Primorial:** The $n$th primorial of number, usually denoted as $p_n^\#$ or $p_n\#$ and means:

$$ p_n\# = \prod_{i = 1}^n p_i $$

where $p_i$ are prime numbers in order, and $p_1 = 2$.

For $x >0$, then the primorial of $x$ is defined as:

$$ x\#=\prod_{p \le x} p $$

**Euclid’s Numbers:** There are two kinds of Euclid’s numbers:

Of the first kind: $E_n$ is the $n$th Euclid’s number and $E_n = p_n^\# +1$

Of the second kind: $K_n$ is the $n$th Kummer’s number and $K_n = p_n^\# -1$

**Euclid’s Theorem:** There are infinitely many primes

**Lemma:** The product of two or more integers of the form $4k+1$ is of the same form

**Th:** There are infinitely primes of the form $4k+3$, $3k+2$ and $6k+5$

### Dirichlet’s Theorem
If $a$ and $b$ are relatively prime positive integers, then the arithmetic progression

$$ a, a+b, a+2b, \dots, a+kb, \dots $$

contains infinitely many primes. The proof uses [[Dirichlet L-functions#Dirichlet's Theorem for Arithmetic Progressions|Dirichlet L-functions]]

********Th:******** If all the $n > 2$ terms of the arithmetic progression

$$ p, p+d, p+2d, \dots, p+(n-1)d $$

are prime numbers, then the common difference $d$ is divisible by every prime $q <n$

**Th:** there’s no polynomial $f$ with integer coefficients such that for all $n \in \Bbb N$, $f(n)$ is prime.

# Fundamental Theorem of Arithmetic

Every positive $n > 1$ is either a prime or product of primes; this representation is unique up to rearrangements.

_Corollary:_ every $n > 1$ can be written in _canonical form:_

$$ n = \prod_{i = 1}^\infty p_i^{k_i} $$

where for each $1 \le i \le m$, $p_i$ is a prime number and $p_1 < p_2 < \dots < p_m < p_{m+1} <\dots$

Given this canonical form of the numbers, we can get formulas for $\gcd(a,b)$ and $\operatorname{lcm}(a,b)$ given the canonical form of $a$ and $b$.

Let $a = \prod_{i = 1}^\infty p_i^{\alpha_i}$ and $b = \prod_{i = 1}^\infty p_i^{\beta_i}$, then $\gcd(a,b) = \prod_{i = 1}^\infty p_i^{\min\{\alpha_i, \beta_i\}}$ and ${\operatorname{lcm}(a,b) = \prod_{i = 1}^\infty p_i^{\max\{\alpha_i, \beta_i\}}}$.

# Weird Inequalities

**Euclid’s inequality**: for $n \ge 2$,

$$ p_n \le p_{n-1}\# -1 $$

- Lemmas necessary for Bertrand’s Postulate:
    1. for $n > 0$, then: $$ \frac{4^n}{2n} \le {2n\choose n} $$
    2. For $p$ prime, and the $R = R(p,n) = \nu_p({2n\choose n})$, the $p$-adic measure of ${2n \choose n}$, then ${p^R \le 2n}$
        
    3. If $p$ is odd and $\frac{2n}{3} < p \le n$, then $R(p,n) = 0$
        
    4. If $x \le 3$, then $x^\# < 2^{2x-3}$

**Bertrand’s Postulate**: for $n \ge 2$, there’s a prime $p$ such that

$$ n <p<2n $$

then, for any $n \ge 1$, $p_{n+1} < 2p_n$, iff $p_n < 2^{n+1}$

**Bonse’s Inequality:** Let $n \ge 4$, then $p_{n+1}^2 \le p_n\#$

**Strong Bonse’s Inequality:** For $n \ge 4$, then $p_{n+1}p_{n+2} \le p_n\#$

Then $p_n \le 2^{2^{n-1}}$

Then, there’s at least $n+1$ prime numbers less than $2^{2^n}$

A weirder inequality: $p_{2n} \le \frac{p_n\#}{p_1} -2$

If $n$ is composite, then there’s a prime $p$ such that $p < \sqrt{n}$

# Conjectures about Primes

### Goldbach’s Conjecture
Every even number greater than $2$ can be expressed as the sum of two primes.

Equivalently, every number greater than $6$ can be expressed as the sum of three primes.

### Twin Prime Conjecture
There are infinitely many twin primes.

The best so far is that there are infinitely many primes with a a bounded difference, aka. progress.

### **Hardy–Littlewood conjecture**
There are infinitely many primes that can be represented by the form $n^2+1$