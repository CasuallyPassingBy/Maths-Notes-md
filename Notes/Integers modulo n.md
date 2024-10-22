---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Greatest Common Divisor]]

Let $a,b \in\Bbb Z$, and $n > 1$, $a$ and $b$ are said to be congruent iff $n\mid b-a$, and is denoted as ${a\equiv b \pmod{n}}$. 

The $\equiv$ relation forms an equivalence relation over $\Bbb Z$, where the equivalence classes are decided by the residue left when a number is divided by $n$.

To a set $\{a_i\}_{i = 1}^n$ is called a complete set of residue mod $n$, if $\Bbb Z = \bigcup_{i = 1}^n [a_i]$, where $[a_i]$ refers to the partition of $\Bbb Z$, where $a_i$ is a member.

### Algebraic Properties

- if $a \equiv b \pmod n$ and $c \equiv d \pmod n$, then $a+c \equiv b+d \pmod n$ and ${ac \equiv bd \pmod n}$
- If $a \equiv b \pmod n$ then $a^k \equiv b^k \pmod n$, for any $k\in \Bbb N$
- If $ac \equiv bc \pmod n$, then $a \equiv b \pmod{n/d}$ where $d = \gcd(n,c)$
    - $ac \equiv bc \pmod n$ and $\gcd(c,n) = 1$, then $a \equiv b \pmod n$

********Th:******** Let $p(x)$ be a polynomial with integer coefficients, if $a \equiv b \pmod n$, then ${p(a) \equiv p(b) \pmod n}$

When considering this algebraic structure, we denote it as $\Bbb Z_n$ 
