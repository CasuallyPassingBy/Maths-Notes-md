---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]], [[Sets of Measure Zero in Rn]], [[Immersed Smooth Submanifolds]]

**Def:** We say that subset $A$ of a smooth $n$-manifold $M$ has measure zero if for every chart $(U,\varphi)$ for $M$, the set $\varphi[A\cap U]$ has measure zero in $\Bbb R^n$. It follows that any set of measure zero has dense complement, because if $M\setminus A$ is not dense, then $A$ contains a nonempty open set which would imply that $\psi[A \cap V]$ contains a nonempty open set for a smooth chart $(V, \psi)$. 

**Lemma:** Suppose $A$ is a subset of a smooth $n$-manifold, and for some collection $\{(U_\alpha, \varphi_\alpha)\}$ of smooth charts whose domains cover $A$, $\varphi_\alpha[A \cap U_\alpha]$ has measure zero in $\Bbb R^n$ for each $\alpha$. Then $A$ has measure zero in $M$.

**Prop:** Let $M$ be a smooth manifold with or without boundary, and $A\subseteq M$ has measure zero in $M$. Then $M \setminus A$ is dense in $A$

**Th:** Suppose $M$ and $N$ are smooth $n$-manifolds with or without boundary, $F:M \to N$ is a smooth map, and $A\subseteq M$ is subset of measure zero. Then $F[A]$ has measure $0$ in $N$. 

**Prop:** Let $M$ be a smooth manifold with or without boundary, then a countable union of sets of measure zero in $M$ has measure zero. 

**Sard's Theorem:** Suppose $M$ and $N$ are smooth manifolds with or without boundary and $F: M \to N$ is a smooth map. Then then the set of critical values of $F$ has measure zero in $N$. 

**Cor:** Suppose $M$ and $N$ are smooth manifolds with or without boundary, and $F:M \to N$ is a smooth map. If $\dim M<\dim N$, then $F[M]$ has measure zero in $N$. 

**Cor:** Suppose $M$ is a smooth manifold with or without boundary, and $S\subseteq M$ is an immersed submanifold with or without boundary. If $\dim S <\dim M$, then $S$ has measure zero in $M$. 