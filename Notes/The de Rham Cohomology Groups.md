---
tags:
  - DifferentialGeometry
  - Topology/AlgebraicTopology
---
Subjects: [[Differential Geometry]], [[Algebraic Topology]]
Links: [[Differential Forms on Smooth Manifolds]], [[The Exterior Derivative on Smooth Manifolds]], [[Quotient of Vector Spaces]], [[Homotopy]], [[Stokes's Theorem and Smooth Manifolds with Corners]], [[Fundamental Group of a Topological Space]]

**Def:** Let $M$ be a smooth manifold with or without boundary or corners, and let $p$ be a nonnegative integer. Because $d: \Omega^p(M) \to \Omega^{p+1}(M)$ is linear, its kernel and image are vector spaces. We define $$\begin{align*}
\mathcal Z^p(M) & := \ker(d: \Omega^p(M) \to \Omega^{p+1}(M)) = \{\text{closed }k\text{-form on }M\}, \\
\mathcal B^p(M) & := \text{Im }(d: \Omega^p(M) \to \Omega^{p+1}(M)) = \{\text{exact }k\text{-form on }M\}.
\end{align*}$$By convention, we consider $\Omega^p(M)$ to be the zero vector space when $p <0$ or $p > n = \dim M$, so that $\mathcal B^0(M) = 0$ and $\mathcal Z^n(M) = \Omega^n(M)$.

The fact that every exact form implies that $\mathcal B^p(M) \le \mathcal Z^p(M)$. Thus, it makes sense to define the *de Rham cohomology group in degree $p$ of $M$*, or the *$p$th de Rham group of $M$* to be the quotient vector space$$H_\text{dR}^p (M) = \frac{\mathcal Z^p(M)}{\mathcal B^p(M)}. $$

**Obs:** It is clear that $H_\text{dR}^p (M) = 0$ for $p <0$ or $p > \dim M$, because $\Omega^p(M) = 0$ in those cases. For $0\le p\le n$, the definition that $H_\text{dR}^p (M) = 0$ iff every closed $p$-form on $M$ is exact.

**Def:** For any closed $p$-form $\omega$ on $M$, we let $[\omega]$ denote the equivalence class of $\omega$ in $H_\text{dR}^p (M)$, called the *cohomology class of $\omega$*. If $[\omega] = [\omega']$, we say that $\omega$ and $\omega'$ are *cohomologous.*

**Induced Cohmology Maps:** For any smooth map $F: M \to N$ between smooth manifolds with or without boundary or corners, the pullback $F^*: \Omega^p(N) \to \Omega^p(M)$ carries $\mathcal Z^p(N)$ into $\mathcal Z^p(M)$ and $\mathcal B^p(N)$ into $\mathcal B^p(M)$. It thus decends to a linear map, still denoted by $F^*$, from $H_\text{dR}^p (N)$ to $H_\text{dR}^p (M)$, called the *induced cohomology map*. The induced cohomology map $F^*: H_\text{dR}^p (N)\to H_\text{dR}^p (M)$ is defined in the obvious way: for a closed $p$-form $\omega$, let $$F^*[\omega] = [F^*\omega].  $$ It has the following properties:
- If $G: N \to P$ is another smooth map, the $$(G \circ F)^*= F^*\circ G^*: H_\text{dR}^p (P) \to H_\text{dR}^p (M).  $$
- If $\text{id}$ denotes the identity map of $M$, then $\text{id}^*$ is the identity map of $H_\text{dR}^p (M)$. 

**Functoriality:** For any integer $p$, the assignment $M \mapsto H_\text{dR}^p (M)$, $F\mapsto F^*$ is a contravariant functor from the category of smooth manifolds with or without boundary to the category of real vector spaces.

**Diffeomorphism Invariance of de Rham Cohomology:** Diffeomorphic smooth manifolds with or without boundary have isomorphic de Rham cohomology groups. 
#### Elementary Computations
**Cohomology of Disjoint Unions:** Let $\{M_j\}$ be a countable collection of smooth $n$-manifolds with or without boundary, and let $M := \coprod_j M_j$. For each $p$, the inclusion map $\iota_j: M_j \hookrightarrow M$ induce an isomorphism from $H_\text{dR}^p (M)$ to the direct product space $\prod_j H_\text{dR}^p (M_j)$. Meaning that,  $$H_\text{dR}^p (M) \cong \prod_j H_\text{dR}^p (M_j).$$
**Cohomology in Degree Zero:** If $M$ is a connected smooth manifold with or without boundary, then $H_\text{dR}^0 (M)$ is equal to the space of constant functions and its therefore $1$-dimensional. 

**Cohomology of Zero-Manifolds:** Suppose $M$ is a manifold of dimension $0$. Then $H_\text{dR}^0 (M)$ is a direct product of $1$-dimensional vector spaces, one for each point of $M$, and all other de Rham cohomology groups of $M$ are zero. 

# Homotopy Invariance

Suppose $F, G: M \to N$ are smooth maps, and let us think what it means to prove that $F^* = G^*$. Given a closed $p$-form $\omega$ on $N$, we need to somehow produce a $(p-1)$-form $\eta$ on $M$ such that $$G^*\omega- F^*\omega = d\eta, $$from which it follows that $G^*[\omega] - F^*[\omega] = [d\eta] = 0$. One might hope to construct $\eta$ in systematic way, resulting in a map $g$ from closed $p$-forms on $N$ to $(p-1)$-forms on $M$ that satisfies $$d(h\omega) = G^*\omega- F^*\omega.  $$
Instead of defining $h\omega$ only when $\omega$ is closed, it turns out to be far simple to define a map $h$ from the space of *all* smooth $p$-forms on $N$ to the space of smooth $(p-1)$-forms on $M$. That satisfies $$d(h\omega)- h(d\omega) = G^*\omega- F^*\omega.$$Which simplifies to what we want when $\omega$ is closed. 

**Def:** If $F, G: M \to N$ are smooth maps, a collection of linear maps $h: \Omega^p(N) \to \Omega^{p-1}(M)$ such that $$d(h\omega)- h(d\omega) = G^*\omega- F^*\omega  $$is satisfied for all $\omega$ is called a *homotopy operator between $F^*$ and $G^*$*. The term *cochain homotopy* is used frequently in the algebraic topology literature.

**Prop:** Suppose $M$ and $N$ are smooth manifolds with or without boundary. If $F, G:M \to N$ are smooth maps and there exists a homotopy operator between the pullback $F^*$ and $G^*$, then the induced cohomology maps $F^*, G^*: H_\text{dR}^p (N) \to H_\text{dR}^p (M)$ are the same.

Let $M$ be a smooth manifold with or without boundary, and for each $t\in I$, let $i_t: M \to M\times I$ be the map $$i_t(x) :=(x, t). $$


**Existence of a Homotopy Operator:** For any smooth manifold $M$ with or without boundary, there exists a homotopy operator between the two maps $i_0^*, i_1^*: \Omega^*(M \times I) \to \Omega^*(M)$. 

**Prop:** Suppose $M$ and $N$ are smooth manifolds with or without boundary, and $F, G: M \to N$ are homotopic smooth maps. For every $p$, the induced cohomology maps $F^*, G^*: H_\text{dR}^p (N) \to H_\text{dR}^p (M)$ are equal. 

**Homotopy Invariance of de Rham Cohomology:** If $M$ and $N$ are homotopy equivalent smooth manifolds with or without boundary, than $H_\text{dR}^p (M) \cong H_\text{dR}^p (N)$ for each $p$. The  isomorphisms are induced by any smooth homotopy equivalence $F: M \to N$.

**Topological Invariance of de Rham Cohomology:** The de Rham cohomology groups are topological invariants: if $M$ and $N$ are homeomorphic smooth manifolds with or without boundary, then their de Rham cohomology groups are isomorphic.

## Computations Using Homotopy Invariance

**Def:** A topological space $X$ is said to be *conctractible* if the identity of $X$ is homotopic to a constant map. 

**Cohomology of Contractible Manifolds:** If $M$ is a contractible smooth manifold with or without boundary, then $H_\text{dR}^p (M) = 0$ for $p \ge 1$. 

**Poincaré Lemma:** If $U$ is a star-shaped open subset of $\Bbb R^n$ or $\Bbb H^n$, then $H_\text{dR}^p (U) = 0$ for $p \ge 1$.

**Local Exactness of Closed Forms:** Let $M$ be a smooth manifold with or without boundary. Each point of $M$ has a neighbourhood on which every closed form is exact.

**Cohomology of Euclidean Spaces and Half-Spaces:** For any integers $n \ge 0$ and $p \ge 1$. $H_\text{dR}^p (\Bbb R^n)= 0$ and $H_\text{dR}^p (\Bbb H^n)= 0$.

**Obs:** Suppose $M$ is a connected smooth manifold and $q$ is any point in $M$. Let $\text{Hom}(\pi_1(M, q),\Bbb R)$ denote the set of groups homomorphisms from $\pi_1(M, q)$ to the additive group $\Bbb R$; it is a vector space under pointwise addition of homomorphisms and multiplication by constants. We define a linear map  $\Phi: H_\text{dR}^1 (M)\to \text{Hom}(\pi_1(M, q),\Bbb R)$ as follows: given a cohomology class $[\omega] \in H_\text{dR}^1 (M)$, w define $\Phi[\omega]: \pi_1(M, q) \to \Bbb R$ by $$\Phi[\omega][\gamma] := \int_{\widetilde \gamma} \omega,  $$where $[\gamma]$ is any path homotopy class in $\pi_1(M, q)$ and $\widetilde \gamma$ is any piecewise smooth curve representing the same path class. 

**First Cohomology and the Fundamental Group:** Suppose $M$ is a connected smooth manifold. For each $q\in M$, the linear map $\Phi: H_\text{dR}^1 (M)\to \text{Hom}(\pi_1(M, q),\Bbb R)$ is well defined and injective.

**Cor:** If $M$ is a connected smooth manifold with finite fundamental group, then $H_\text{dR}^1 (M) = 0$. 

**Cor:** If $M$ is a connected smooth manifold whose fundamental group is a torsion group, $H_\text{dR}^1 (M) =0$.