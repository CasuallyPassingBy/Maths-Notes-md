---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Embedded Smooth Submanifolds]]

**Def:** Given a smooth vector bundle $\pi: E \to M$, a *smooth subbundle* of $E$ is a subset $D\subseteq E$ with the following properties:
- $D$ is an embedded submanifold of $E$
- For each $p\in M$, the fiber $D_p := D\cap \pi^{-1}\{p\}$ is a linear subspace of $E_p := \pi^{-1}\{p\}$.
- With the vector space structure on each $D_p$ inherited from $E_p$ and the projection $\pi|_D: D \to M$, $D$ is a smooth vector bundle over $M$. 

**Prop:** If $D \subseteq E$ is a smooth subbundle, then the inclusion map $\iota: D \to E$ is a smooth bundle map over $M$. 

**Local Frame Criterion for Subbundles:** Let $\pi: E \to M$ be a smooth vector bundle, and suppose for each $p\in M$ we are given an $m$-dimensional linear subspace $D_p \subseteq E_p$. Then $D :=\coprod_{p \in M} D_p\subseteq E$ is a smooth subbundle iff the following condition is satisfied:
- Each point $p\in M$ has a neighbourhood $U$ on which there are smooth local sections $\sigma_1,\dots,\sigma_m: U \to E$ such that $\sigma_1|_q, \dots, \sigma_m|_q$ forma a basis for $D_q$ at each $q\in U$.

**Example:** Suppose $M$ is any parallelizable manifold, and let $(E_1, \dots, E_n)$ be a smooth global frame form $M$. If $1 \le k \le n$, the subset $D \subseteq TM$ defined by $D_p = \text{span}(E_1,\dots, E_k)$ is a smooth subbundle of $TM$.