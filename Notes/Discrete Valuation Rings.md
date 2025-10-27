---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Rings and Fields]]

**Def:** Let $K$ be a field. A *discrete valuation* on $K$ is a function $\nu:K^\times \to \Bbb Z$ satisfying:
- $\nu(ab) = \nu(a) +\nu(b)$,
- $\nu$ is surjective,
- $\min\{\nu(x), \nu(y)\} \le \nu(x+y)$, for all $x, y\in K^\times$ with $x+y\neq 0$. 
The set $R = \{x\in K^\times \mid \nu(x) \ge 0\} \cup \{0\}$ is called the *valuation ring* of $\nu$. 

**Def:** In general, a ring $R$ is called *discrete valuation ring* if there is some field $K$ and some discrete valuation $\nu$ on $K$ such that $R$ is the valuation ring of $\nu$. 

**Obs:** $R$ is a subring of $K$ which contains the identity. 

**Prop:** For each $x\in K^\times$, either $x$ or $x^{-1}$ is in $R$. 

**Prop:** If $x$ is a unit of $R$ iff $\nu(x) = 0$. 

**Prop:** Let $K$ be a field, let $\nu$ be a discrete valuation on $K$ and let $R$ be a valuation ring of $\nu.$ For each integer $k \ge 0$ we define $A_k := \{r \in R\mid \nu(r) \ge k\} \cup \{0\}$.
- $A_k$ is a [[Principal and Generated Ideals|principal ideal]] and $A_0 \supseteq A_1\supseteq A_2 \supseteq \cdots$.
- If $I$ is a nonzero ideal of $R$, then $I = A_k$ for some $k \ge 0$. In particular $R$ is a local ring with unique maximal ideal $A_1$. 

**Cor:** A discrete valuation ring is local. 

**Cor:** A discrete valuation ring is a [[Principal Ideal Domains|principal ideal domain]]. 

**Prop:** A discrete valuation ring is seen to be a [[Euclidean Domains|Euclidean domain]] with respect to the norme defined by $N(0) = 0$ and $N(r) =\nu(r)$ for $r\in R\setminus\{0\}$. 