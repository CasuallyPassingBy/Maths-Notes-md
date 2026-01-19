---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Embedded Smooth Submanifolds]], [[Bundle Homomorphisms for Vector Bundles]]

**Def:** Given a vector bundle $\pi_E: E \to M$, a *subbundle of $E$* is vector bundle $\pi_D : D \to M$, in which $D$ is a topological subspace of $E$ and $\pi_D$ is the restriction of $\pi_E$ to $D$, such that for each $p\in M$, the subset $D_p = D \cap E$ is a linear subspace of $E_p$, and the vector space structure on $D_p$ is the one inherited from $E_p$. If $E \to M$ is a smooth bundles, then a subbundle of $E$ is called a *smooth subbundle* if it is a smooth vector bundle and embedded submanifold with or without boundary in $E$.

**Obs:** Given a smooth vector bundle $E \to M$ and a smooth subbundle $D\subseteq E$, then the inclusion map $\iota: D \hookrightarrow E$ is a smooth bundle homomorphism over $M$.

**Local Frame Criterion for Subbundes:** Let $\pi:E \to M$ be a smooth vector bundle, and suppose that for each $p\in M$ we are given a an $m$-dimensional vector subspace $D_p \subseteq E_p$. Then $D := \bigcup_{p\in M} D_p\subseteq E$ is a smooth subbundle of $E$ iff the following condition is satisfied:
- Each point of $M$ has a neighbourhood $U$ on which there exist smooth local sections $\sigma_1,\dots, \sigma_m:U \to E$ with the property that $\sigma_1(q),\dots,\sigma_m(q)$ form a basis for $D_q$ for each $q\in U$. 

**Example:** Suppose $M$ is a smooth manifold with or without boundary and $S\subseteq M$ is an immersed $k$-submanifold with or without boundary. We know that $TS$ is a smooth rank $k$-subbundle of the ambient tangent bundle $TM|_S$. 

**Def:** Suppose $E\to M$ and $E'\to M$ are vector bundles and $F: E\to E'$ is a bundle homomorphism over $M$. For each $p\in M$, the rank of a linear map $F|_{E_p}$ is called the *rank of $F$ at $p$*. We say that $F$ has *constant rank* if its rank is the same for all $p\in M$. 

**Th:** Let $E$ and $E'$ be smooth vector bundles over a smooth manifold $M$, and let $F:E \to E'$ be a smooth bundle homomorphism over $M$. We define subsets $\ker F\subseteq E$ and $\text{im }F\subseteq E'$ by $$\ker F:= \bigcup_{p\in M} \ker(F|_{E_p}), \qquad \text{im }F := \bigcup_{p\in M} \text{im}(F|_{E_p}). $$Then $\ker F$ and $\text{im }F$ are smooth subbundles of $E$ and $E'$, respectively, iff $F$ has constant rank. 

**Orthogonal Complement Bundles:** Let $M$ be an immersed submanifold with or without boundary in $\Bbb R^n$, and $D$ be a smooth rank-$k$ subbundle of $T\Bbb R^n|_M$. For each $p\in M$, let $D_p^\bot$ denote the orthogonal complemente of $D_p$ in $T_p\Bbb R^n$ with respect to the Euclidean dot product, and let $D^\bot \subseteq T\Bbb R^n|_M$ be the subset $$D^\bot := \{(p, v) \in T\Bbb R^n\mid p\in M, v\in D_p^\bot\}. $$Then $D^\bot$ is a smooth rank-$(n-k)$ subbundle $T\Bbb R_n|_M$. For each $p\in M$, there is a smooth orthogonal frame for $D^\bot$ on e neighbourhood of $p$.

**The Normal Bundle to a Submanifold of $\Bbb R^n$:** If $M\subseteq \Bbb R^n$ is an immersed $m$-dimensional submanifold with or without boundary, its normal bundle $NM$ is a smooth rank $(n-m)$ subbundle of $T\Bbb R^n|_M$. For each $p\in M$, there exists a smooth orthonormal frame for $NM$ on a neighbourhood of $p$. 

**Prop:** Suppose $M \subseteq\Bbb R^n$ is an immersed submanifold. The ambient tangent bundle $T\Bbb R^n|_M$ is isomorphic to the Whitney sum $TM\oplus NM$, where $NM \to M$ is the normal bundle.

**Prop:** Suppose $S$ is a properly embedded codimension-$k$ submanifold of $\Bbb R^n$. The following are equivalent.
- There exists a smooth defining function for $S$ on some neighbourhood $U$ of $S$ in $\Bbb R^n$, that is, a smooth function $\Phi:U \to\Bbb R^k$ such that $S$ is a regular level set of $\Phi$.
- The normal bundle $NS$ is a trivial vector bundle. 