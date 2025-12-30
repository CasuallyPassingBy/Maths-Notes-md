---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Sard's Theorem]], [[Tangent Spaces and Vector Fields on Submanifolds]]

**Def:** Suppose $M$ is a smooth manifold. Two embedded submanifolds $S, S'\subseteq M$ are said to *intersect transversely* if for each $p\in S\cap S'$, the tangent spaces $T_p S$ and $T_p S'$ together span $T_p M$. 

If $F:N \to M$ is a smooth map and $S\subseteq M$ is an embedded submanifold, we say that $F$ is *transverse to $S$* if for every $x\in F^{-1}[S]$, the spaces $T_{F(x)} S and $dF_x [T_xN]$ together san $T_{F(x)} M$. If $F$ is a smooth submersion, then it is automatically transeverse to every embedded submanifold of $M$. Two embedded submanifolds intersect transeversely iff the inclusion of either one is transverse to the other. 

**Th:** Suppose $N$ and $M$ are smooth manifolds and $S\subseteq M$ is an embedded submanifold.
- $F: N \to M$ is a smooth map that is transverse to $S$, then $F^{-1}[S]$ is an embedded submanifold of $N$ whose codimension is equal to the codimension of $S$ in $M$.



**Transversality Theorem:** A $\mathcal C^\infty$ map $\Phi: M \to N$ is transversal to a embedded submanifold $S$ of codimension $k$ in $M$, then $\Phi^{-1}[S]$ is embedded submanifold of codimension $k$ in $N$. 

**Def:** Two embedded submanifold $S_1, S_2 \subseteq M$ are said to be *transverse*, or to *intersect transversly*, if for each $p\in S_1 \cap S_2$, the tangent spaces $T_p S_1$ and $T_p S_2$ together span $T_p M.$ I am going to denote it as $S_1 \pitchfork S_2$. 

**Prop:** If $S_1$ and $S_2$ are transverse, then $S_1\cap S_2$ is en embedded submanifold of $M$ of dimension $\dim S_1 + \dim S_2- \dim M$. 