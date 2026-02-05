---
tags:
  - DifferentialGeometry
  - Topology/AlgebraicTopology
---
Subjects: [[Differential Geometry]], [[Algebraic Topology]]
Links: [[The de Rham Theorem and Stokes's Theorem on Chains]], [[Smooth Singular Homology]], [[Simplicial Complexes]], [[Riemannian Volume Form on Smooth Manifolds]]

**Def:** Let $M$ be a smooth $n$-manifold and suppose $S\subseteq M$ is an oriented compact embedded $p$-dimensional submanifold. A *smooth [[Simplicial Complexes#^dbc61e|triangulation]]* of $S$ is a smooth $p$-chain $c = \sum_i \sigma_i$ in $M$ with the following properties:
- Each $\sigma_i: \Delta_p \to S$ is a smooth orientation-preserving embedding.
- If $i\ne j$, then $\sigma_i[\text{Int}(\Delta_p)] \cap\sigma_j[\text{Int}(\Delta_p)] = \varnothing$.
- $S = \bigcup_i \sigma_i[\Delta_p]$.
- $\partial c = 0$. 
Two oriented compact embedded $p$-dimensional submanifolds $S, S'\subseteq M$ are said to be *homologous* if there exists a triangulation $c$ for $S$ and $c'$ for $S'$ such that $c - c'$ is a boundary. 

**Prop:** For any smooth triangulation $c$ of $S$ and any smooth $p$-form $\omega$ on $M$, we have $$\int_c \omega = \int_S\omega.$$
**Cor:** If $\omega$ is closed and $S, S'$ are homologous, then $$\int_S \omega = \int_{S'}\omega.$$
**Def:** Suppose $(M ,g)$ is a Riemannian $n$-manifold. A smooth $p$-form $\omega$ on $M$ is called a *calibration* if $\omega$ is closed and $\omega_x(v_1,\dots, v_p) \le 1$ whenever $(v_1,\dots, v_p)$ are orthonormal vectors in some tangent space $T_x M$. An oriented embedded $p$-dimensional submanifold $S\subseteq M$ is said to be *calibrated* if there is a calibration $\omega$ such that the pullback $\iota_S^*\omega$ is the volume form for the induced Riemannian metric on $S$. 

**Prop:** Suppose $S \subseteq M$ is a smooth triangulated calibrated compact submanifold, Then the volume of $S$, with respect to the induced Riemannian metric, is less than or equal to any other submanifold homologous to $S$. 