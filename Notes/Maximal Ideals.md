---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Ring Ideals and Quotient Rings]], [[Axiom of Choice]]

**Def:** An ideal $M$ in arbitrary ring $R$ is called a *maximal ideal* if $M \ne R$ and the only ideals containing $M$ are $M$ and $R$.

**Krull's Theorem:** In a unitary ring every proper ideal is contained in a maximal ideal. This is equivalent to the [[Axiom of Choice]]. 

**Prop:** The ideal $M$ is maximal iff $R/M$ is a simple ring, 

**Cor:** Let $R$ be a commutative ring. The ideal $M$ is a maximal ideal iff the quotient ring $R/M$ is a field. 

**Cor:** If $M$ is an ideal such that $R/M$ is a field, then $M$ is a maximal ideal. 

**Def:** Let $I$ be an ideal of the commutative ring $R$. We define $$\text{Jac }I := \bigcap\{M \le R \mid M \text{ is a maximal ideal and }I \subseteq M\},$$where the convention is that $\text{Jac } R =R$. If $I$ is the zero ideal, $\text{Jac } 0$ is called the *Jacobson radical* of the ring $R$, so $\text{Jac }I$ us the preimage in $R$ of the Jacobson radical of $R/I$.

**Prop:** Let $R$ be a commutative ring and $I$ an ideal of $R$.
- $\text{Jac } I$ is an ideal of $R$ that contains $I$.
- $\text{rad }I \subseteq \text{Jac }I$. 

**Obs:** Additionally, then $(n)$ is equal to $\text{Jac }(n)$ iff $n$ is a product of distinct prime in $\Bbb Z$. 

**Def:** A commutative ring $R$ is called a *local ring* if it has a unique maximal ideal.

**Prop:** If $R$ is commutative local ring with maximal ideal $M$, then every element $R\setminus M$ is a unit. Additionally, if $R$ is a commutative ring with $1$ in which the set of nonunits forms an ideal $M$, then $R$ is a local ring with unique maximal ideal $M$.