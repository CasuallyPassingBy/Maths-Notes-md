---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Rings and Fields]], [[Ring Homomorphisms]]

Let $R$ be a unital ring. 

**Def:** The *characteristic* of a ring $R$ is the smallest positive integer such that $1+1+1+\dots + 1 = 0$ in $R$; if no such integer exists the characteristic is said to be $0$. 

**Prop:** The map $\Bbb Z \to R$ defined by $$k \mapsto \begin{cases}
1+1+\dots+1 \; \text{($k$ times)} & k > 0 \\
0 & k = 0 \\
-1-1-\dots-1 \; \text{($k$ times)} & k < 0 
\end{cases} $$is a ring homomorphism whose kernel $n\Bbb Z$, where $n$ is the characteristic of $R$.

**Prop:** If $p$ is prime and if $R$ is a commutative ring of characteristic $p$, then $(a+b)^p = a^p + b^p$ for all $a, b\in R$. 

**Prop:** Every boolean ring has characteristic $2$

**Prop:** Every integral domain has characteristic $p$, where $p$ is prime or $0$. 