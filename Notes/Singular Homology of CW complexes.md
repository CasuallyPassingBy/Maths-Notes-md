---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Singular Homology]], [[Mayer-Vietoris Theorem for Singular Homology]], [[Singular Homology of Spheres]], [[Fundamental Group of CW Complexes]], [[Cell Complexes and CW Complexes]], [[Chain Complexes and Cochain Complexes]], [[Free Abelian Groups]]

**Homology Effect of Attaching a Cell:** Let $X$ be any topological space, and let $Y$ be obtained from $X$ by attaching a closed cell $D$ of dimension $n \ge 2$ along the attaching map $\varphi: \partial D \to X$: Let $K$ and $L$ denote the kernel and image, respectively, of $\varphi_{n-1}(\partial D) \to\partial_{n-1}(X)$. Then the homology homomorphism $H_p(X) \to H_p(Y)$ induced by the inclusion is characterised as follows.
- if $p <n-1$ or $p> n$, it is an isomorphism. 
- If $p = n-1$, it is a surjection whose kernel is $L$, so there is a short exact sequence$$0 \to L \hookrightarrow H_{n-1}(X) \to H_{n-1}(Y) \to 0.$$
- If $p = n$, it is n injection, and there is a short exact sequence $$0 \to H_n(X) \to H_n(Y) \to K \to 0. $$

**Homology Properties of CW Complexes:** Let $X$ be a finite $n$-dimensional CW complex. ^cf2f30
- Inclusion $X_k \hookrightarrow X$ induces isomorphisms $H_p(X_k) \cong H_p(X)$ for $p \le k-1$.
- $H_p(X) = 0$ for $p >n$.
- For $0\le p \le 0$, $H_p(X)$ is a finitely generated group, whose rank is less than or equal to the number of $p$-cells in $X$.
- If $X$ has no cells of dimension $p-1$ or $p+1$, then $H_p(X)$ is a free abelian group whose rank is equal to the number of $p$-cells. 
- Suppose $X$ has only one cell of dimension $n$, and $\varphi: \partial D \to X_n-1$ is its attaching map. Then $H_n(X)$ is an infinite cyclic group, if $\varphi_*: H_{n-1}(\partial D)\to H_{n-1}(X)$ is the zero map, and $H_n(X) = 0$ otherwise.

**Homology of CW Complexes:**
- Complex projective $n$-space $\Bbb{CP}^n$ has CW decomposition with one cell in each even dimension, $0,\dots, 2n$. It follows from the theorem above that $H_{2k} (\Bbb {CP}^n) \cong \Bbb Z$ for $k = 0,\dots, n$, and the odd-dimensional homology groups vanish.
- Let $M$ be a compact orientable surface of genus $n$. Then $M$ has a CW complex decomposition of $2n$ circles, and has a $1$-skeleton homeomorphic to a wedge sum of $2n$ circles. $H_1(M)$ is isomorphic to the free abelian group $\Bbb Z\{\alpha_1,\beta_1,\dots, \dots,\alpha_n,\beta_n\}$. We also see that $H_2(M) \cong \Bbb Z$. 
- Let $M$ be a compact nonorientable surface of genus $n$. In this case $M$ has a CW decomposition with one $2$-cell, and with the wedge sum of $n$ circles for the $1$-skeleton. so $H_2(M) = 0$. 

In more thorough treatments of homology, one defines a chain complex for each CW complex, whose $k$th chain group is the free abelian group on the $k$-cells, and whose boundary operators reflect the attaching maps. The homology of this complex, called *[[celular homology]]*, is easily computable in most instances, and can be shown to be isomorphic to singular homology. 

**Th:** If $X$ is a finite CW complex $$\chi(X) = \sum_p (-1)^p \text{ rank }H_p(X).  $$Therefore, the Euler characteristic is a homotopy invariant. 

**Def:** For any topological space $X$, the integer $\beta_p(X) = \text{rank }H_p(X)$ (it it is finite) is called the *$p$th Betti number of $X$*. We define the *Euler characteristic of $X$* by $$\chi(X) := \sum_p (-1)^p \beta_p(X)  $$provided that each $\beta_p(X)$ is finite and $\beta_p(X) = 0$ for sufficiently large $p$. It is a homotopy invariant, and the preceding theorem says it can be computed for finite CW complexes as the alternating sum of the the number of cells.

**Prop:** The dimension of a finite-dimensional CW complex is a topological invariant.

**Prop:** Any triangulation of an $n$-manifold has dimension $n$. 
