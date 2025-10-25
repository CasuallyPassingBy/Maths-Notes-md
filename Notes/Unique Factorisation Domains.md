---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Principal Ideal Domains]], [[Integral Domains]]

**Prop:** In an integral domain a prime element is always irreducible.

**Prop:** In a principal ideal domain a nonzero element is prime iff it is prime. 

**Def:** A *unique factorisation domain (UFD)* is an integral domain $R$ in which every nonzero element $r\in R$ which is not a unit has the following two properties:
- $r$ can be written as a finite product of irreducibles $p_i$ of $R$ (not necessarily distinct).
- the decomposition above is *unique up to associates:* namely, if $r = q_1\cdots q_m$ is another factorisation of $r$ into irreducibles, then $m = n$ and there is some renumbering of the factors so that $p_i$ associate to $q_i$ for $i = 1,\dots, n$. 

**Prop:** In a unique factorisation domain a nonzero element is a prime iff it is irreducible. 

**Prop:** Let $a$ and $b$ be two nonzero elements of the unique factorisation domain $R$ and suppose $$ a= up_1^{\alpha_1}\cdots p_n^{\alpha_n}\quad \text{and}\quad b= up_1^{\beta_1}\cdots p_n^{\beta_n}$$ are prime factorisations for $a$ and $b$, where $u$ and $v$ are units, the primes $p_1,\dots, p_n$ are *distinct* and the exponents $\alpha_i$ and $\beta_i$ are $\ge0$. Then the element $$d= p_1^{\gamma_1}\cdots p_n^{\gamma_n},$$where $\gamma_i :=\min\{\alpha_i,\beta_i\}$ for all $i =1,\dots, n$, is the greatest common divisor of $a$ and $b$. 

**Prop:** Let $a$ and $b$ be two nonzero elements of the unique factorisation domain $R$ and suppose $$ a= up_1^{\alpha_1}\cdots p_n^{\alpha_n}\quad \text{and}\quad b= up_1^{\beta_1}\cdots p_n^{\beta_n}$$ are prime factorisations for $a$ and $b$, where $u$ and $v$ are units, the primes $p_1,\dots, p_n$ are *distinct* and the exponents $\alpha_i$ and $\beta_i$ are $\ge0$. Then the element $$m= p_1^{\delta_1}\cdots p_n^{\delta_n},$$where $\delta_i :=\max\{\alpha_i,\beta_i\}$ for all $i =1,\dots, n$, is the least common multiple of $a$ and $b$. 

**Th:** Every principal ideal domain is a unique factorisation domain. In particular, every Euclidean domain is a unique factorisation domain. 

**Cor (Fundamental Theorem of Arithemetic):** The integers $\Bbb Z$ are a unique factorisation domain.

**Prop:** Let $R = \Bbb Z[\sqrt{-n}]$, where $n$ is a a squarefree integer greater than $3$.
- $2$, $\sqrt{-n}$ and $1+\sqrt{-n}$ are irreducible in $R$.
- $R$ is not a unique factorisation domain.

**Cor:** The quadratic integer ring $\cal O$ is not a unique factorisation domain for $D\equiv 2, 3\pmod 4$ and $D<-3$, and thus neither a Euclidean not a principal ideal domain. 