---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Integers modulo n]], [[Polynomial Ring of a Single Variable]], [[Euler Totient Function]], [[Cyclic Groups]]

**Def:** If $x^n \equiv a \pmod p$ has a solution, then $a$ is called the an $n$th reside modulo $p$. 

**Def:** Let $m$ be a positive integer and $a$ any integer such that $(a, m) = 1$. Let $h$ be the least positive integer such that $a^h \equiv 1 \pmod m$. We say that $a$ has order $h$ modulo $m$. 

**Th:** If $a$ belongs to the exponent $h$ modulo $m$, then $h \mid \phi(m)$. Additionally, if $a^i \equiv a^j \pmod m$ iff $h\mid (i-j)$. 

**Th:** If has $a$ has order $h$ modulo $m$, then $a^k$ has order $h/(h, k)$ modulo $m$. 

**Def:** If $a$ has order $\phi(m)$ modulo $m$, then $a$ is called a *primitive root modulo $m$.*

In the language of group theory, we see that $a$ is a generator of the multiplicative group $(\Bbb Z/m \Bbb Z)^\times$. In particular, there is a primitive root modulo $m$ iff $(\Bbb Z/m \Bbb Z)^\times$ is cyclic. 

**Th:** If $p$ is prime, then there are $\phi(p-1)$ primitive roots modulo $p$. The only numbers that have primitive roots are $p^k$, $2p^k$, $2$ and $4$ with an odd prime $p$. 

**Cor:** Let $p$ be a prime. The multiplicative group $(\Bbb Z/p \Bbb Z)^\times$ of nonzero residue classes $\mod p$ is cyclic. you didnt expect that comment

**Cor:** Let $n \ge 2$ be an integer with factorisation $n = \prod_{k = 0}^\infty p_k ^{\alpha_k}$ in $\Bbb Z$. We have the following isomorphisms of multiplicative groups:
- $(\Bbb Z/n\Bbb Z)^\times \cong \prod_{k = 0}^\infty (\Bbb Z/p^\alpha \Bbb Z)^\times$.
- $(\Bbb Z/2^\alpha\Bbb Z)^\times$ is the product of a cyclic group of order $2$ and a cyclic group of order $2^{\alpha -2}$ for all $\alpha \ge 2$. 
- $(\Bbb Z/p^\alpha \Bbb Z)^\times$ is a cyclic group of order $p^\alpha(p-1)$, for all odd primes $p$. 

**Th:** Suppose that $m$ has a primitive root $g$. Then $g^k \equiv g^j \pmod m$ iff $j \equiv k \pmod{\phi(m)};$ in particular, $g^k \equiv 1\pmod m$ iff $\phi(m) \mid k$. The set $\{g^k \mid k\in\Bbb Z\}$ forms a reduced residue system modulo $m$; i.e., if $(a, m ) = 1$, then there exists $k \in\Bbb Z$ such that $g^k \equiv a \pmod m$. 

**Th:** If $p$ is prime and $(a, p) = 1$, then the congruence $x^n \equiv a \pmod p$ has $(n, p-1)$ solutions, or no solutions according to $$a^{p-1/(n, p-1)} \equiv 1 \pmod p \text{ or } a^{p-1/(n, p-1)} \not\equiv 1 \pmod p.$$
