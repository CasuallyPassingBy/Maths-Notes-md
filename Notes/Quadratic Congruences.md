---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]

**Def:** Let $p$ be an odd prime and $\gcd(a, p) = 1$. If the quadratic congruence $x^2 \equiv a \pmod p$ has a solution, then $a$ is said to be a _quadratic residue_ of $p$. Otherwise, a is called a _quadratic nonresidue_ of $p$.

From the definition, we can interpret it as wether $a$ has a square root. Similary with the real numbers that we can’t take a square root of all real numbers and staying in the reals. This is an analagous requierment.

### Euler’s Criterion

Let $p$ be an odd prime and $\gcd(a, p)=1$. Then $a$ is a quadratic residue of $p$ iff ${a^{(p-1)/2} \equiv 1 \pmod p}$

****************Cor:**************** Let $p$ be an odd prime and $\gcd(a, p) = 1$. Then $a$ is a quadratic residue or nonresidue according to wether

$$ a^{(p-1)/2} \equiv 1 \pmod p \quad \text{ or } \quad a^{(p-1)/2} \equiv -1 \pmod p $$

****Th:**** Let $p$ be an odd prime then among the reduced residue system there are $(p-1)/2$ quadratic residues and non-residues

********Th:******** Let $p$ be an odd prime and $\gcd(a, p ) = 1$. Then the quadratic congruence

$$ ax^2+bx +c \equiv 0 \pmod p $$

is solvable iff $b^2 -4ac$ is either zero or a quadratic residue of $p$

If $n >2$ and $\gcd(a,n ) =1$, then $a$ is called a quadratic residue modulo $n$ whenever there exists an integer $x$ such that $x^2 \equiv a \pmod n.$ If $a$ is a quadratic residue of $n >2$, then ${a^{\phi(n)/2 }\equiv1 \pmod n}$. It is not true in the backwards direction though