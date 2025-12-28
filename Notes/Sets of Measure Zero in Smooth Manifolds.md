---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth or Differentiable Manifolds]], [[Sets of Measure Zero in Rn]]

**Def:** We say that subset $A$ of a smooth $n$-manifold $M$ has measure zero if for every chart $(U,\varphi)$ for $M$, the set $\varphi[A\cap U]$ has measure zero in $\Bbb R^n$. It follows that any set of measure zero has dense complement, because if $M\setminus A$ is not dense, then $A$ contains a nonempty open set which would imply that $\psi[A \cap V]$ contains a nonempty open set for a smooth chart $(V, \psi)$. 

**Lemma:** Suppose $A$ is a subset of a smooth $n$-manifold, and for some collection $\{(U_\alpha, \varphi_\alpha)\}$ of smooth charts whose domains cover $A$, $\varphi_\alpha[A \cap U_\alpha]$ has measure zero in $\Bbb R^n$ for each $\alpha$. Then $A$ has measure zero in $M$.

**Prop:** Let $M$ be a smooth manifold. Show that a countable union of sets of measure zero in $M$ has measure zero. 

**Th:** Let $F: M \to N$ be a smooth map of constant rank. If $F$ is surjective, then it is a submersion.

It is a result that it is proved nicely using the concept of sets of measure zero. 

**Th:** Suppose $M$ and $N$ are smooth manifolds with $\dim M< \dim N$, and $F: M \to N$ is a smooth map. Then $F[M]$ has measure zero in $N$. In particular $N \setminus F[M]$ is dense in $N$. 

**Cor:** If $M$ is a smooth manifold and $N\subseteq M$ is an immersed submanifold of positive codimension, then $N$ has measure zero in $M$. 

**Sard's Theorem:** If $F:M \to N$ is any smooth map of the set of critical values of $F$ has measure zero in $N$. 