---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Tensor Bundles]], [[Correlations, Musical Isomorphisms]], [[Embedded Smooth Submanifolds]], [[Local and Global Sections of Vector Bundles]]

**Def:** Let $M$ be a smooth manifold with or without boundary. A *Riemannian metric on $M$* is a smooth symmetric covariant $2$-tensor field on $M$ that is positive definite at each point. A *Riemannian manifold* is a pair $(M, g)$, where $M$ is a smooth manifold and $g$ is a Riemannian metric on $M$. A *Riemannian manifold with boundary* is defined similarly.

If $g$ is a Riemannian metric on $M$, then for each $p\in M$, the $2$-tensor $g_p$ is an inner product on $T_p M$. Because of this we use the notation $\langle v, w\rangle_g$ to denote the real number $g_p(v, w)$ for $v, w\in T_p M$.

In any smooth local coordinates $(x^i)$, a Riemannian metric can be written as  $$g = g_{ij} dx^i \otimes dx^j,$$but we can make use of the symmetric product to get $$g = g_{ij} dx^i \otimes  dx^j = g_{ij} dx^i dx^j. $$
**Def:** The simplex example of a Riemannian metric is the *Euclidean metric* $\bar g$ on $\Bbb R^n$, given in standard coordinates by $$\bar g = \delta_{ij} dx^i dx^j $$

**Def:** If $(M_1, g_1)$ and $(M_2, g_2)$ are Riemannian manifolds, then product $M_1 \times M_2$ has a natural Riemannian metric $g = g_1 \oplus g_2$, called the *product metric*, defined by $$g(X_1 + X_2, Y_1 + Y_2) := g_1(X_1, Y_1) + g_2(X_2, Y_2),$$where $X_i, Y_i \in T_{p_i} M_i$, under the natural identification $T_{(p_1, p_2)}(M_1 \times M_2) = T_{p_1} M_1 \times T_{p_2} M_2$. 

**Obs:** Any local coordinates $(x^1, \dots, x^n)$ for $M_1$ and $(x^{n+1}, \dots, x^{n+m})$ for $M_2$ give coordinates $(x^1, \dots x^{n+m})$ for $M_1 \times M_2$. In terms of these coordinates the product metric has the local expression $g = g_{ij}dx^idx^j$, where $g_{ij}$ is a block diagonal matrix $$(g_{ij}) = \begin{pmatrix}
(g_1)_{ij} & 0 \\ 
0 & (g_2)_{ij} 
\end{pmatrix}$$
**Existence of Riemannian Metrics:** Every smooth manifold with or without boundary admits a Riemannian metric.

We have a few of the geometric constructions that can be defined on a Riemannian manifold $(M, g)$ with or without boundary.
- The *length* or *norm* of a tangent vector $v\in T_p M$ is defined to be $$|v|_g := \langle v, v\rangle_g^{1/2} = g_p(v, v)^{1/2}. $$
- The *angle* between two nonzero tangent vectors $v, w\in T_p M$ is the unique $\theta\in [0,\pi]$ satisfying $$\cos\theta = \frac{\langle v,w\rangle_g}{|v|_g |w|_g}. $$
- Tangent vectors $v, w\in T_p M$ are said to be *orthogonal* if $\langle v, w\rangle_g = 0$.

**Def:** Let $(M, g)$ be a an $n$-dimensional Riemannian manifold with or without boundary. We say that a local frame $(E_1,\dots, E_n)$ for $M$ on an open subset $U\subseteq M$ is an *orthonormal frame* if the vectors $(E_1|_p,\dots, E_n|_p)$ from an orthonormal basis for $T_p M$ at each point $p\in U$, or equivalently if $\langle E_i, E_j \rangle =\delta_{ij}$.

**Prop:** Suppose $(M, g)$ is a Riemannian manifold with or without boundary, and $(X_j)$ is a smooth local frame for $M$ over an open subset $U\subseteq M$. Then there is a smooth orthonormal frame $(E_i)$ over $U$ such that $\text{span}(E_1|_p,\dots, E_j|_p) = \text{span}(X_1|_p,\dots, X_j|_p)$ for each $j = 1,\dots, n$ and each $p\in U$. 

**Existence of Local Orthonormal Frames:** Let $(M, g)$ be a Riemannian manifold with or without boundary. For each $p\in M$, there is a smooth orthonormal frame on a neighbourhood of $p$. 

# Pullback Metrics

**Def:** Suppose $M$, $N$ are smooth manifolds with or without boundary, $g$ is a Riemannian metric on $N$, and $F: M \to N$ is smooth. The pullback $F^*g$ is a smooth $2$-tensor field on $M$. If it is positive definite, it is a Riemannian metric on $M$, calle the *pullback metric* determined by $F$.

**Prop:** Suppose $F: M \to N$ is a smooth map and $g$ is a Riemannian metric on $N$. Then $F^*g$ is a Riemannian metric on $M$ iff $F$ is a smooth immersion. 

**Def:** If $(M, g)$ and $(\tilde M, \tilde g)$ are both Riemannian manifolds, a smooth map $F: M \to \tilde M$ is called a *Riemannian isometry* if it is a diffeomorphism that satisfies $F^*\tilde g = g$. More generally, $F$ is called a *local isometry* if every point $p\in M$ has a neighbourhood $U$ such that $F|_U$ is an isometry of $U$ onto an open subset of $\tilde M$. 

If there exists a Riemannian isometry between $(M, g)$ and $(\tilde M, \tilde g)$, we say that they are *isometric* as Riemannian manifolds. If each point of $M$ has a neighbourhood that is isometruc to an open subset of $(\tilde M, \tilde g)$, then we say that $(M, g)$ is *locally isometric* to $(\tilde M, \tilde g)$. The study of properties of Riemannian manifolds that are invariant under (local or global) isometries is called *Riemannian geometry*.

A Riemannian $n$-manifold $(M, g)$ is said to be a *flat Riemannian manifold*, and $g$ is a *flat metric*, if $(M, g)$ is locally isometric $(\Bbb R^n,\bar g)$. 

**Def:** An isometry $\varphi: (M, g) \to (M, g)$ is called an *isometry* of $M$. the set of isometries of $M$ is a group, called the *isometry group* of $M$; it is denoted $\mathcal I(M)$. 

**Th:** Let $(M, g)$ be a Riemmanian manifold. The following statements are equivalent:
- $g$ is flat. 
- Each point of $M$ is contained in the domain of a smooth coordinate chart in which $g$ has the coordinate representation $g = \delta_{ij} dx^i dx^j$. 
- Each point of $M$ is contained in the domain of a smooth coordinate chart in which the coordinate frame is orthonormal.
- Each point of $M$ is contained in the domain of a [[Lie Derivative#Commuting Frames|commuting orthonormal frame]].

**Lemma:** Suppose $U, V\subseteq \Bbb R^n$ are connected open sets, $\varphi, \psi: U \to V$ are Riemannian isometries, and for some $p\in U$ they satisfy $\varphi(p) = \psi(p)$ and $d\varphi_p = d\psi_p$, then $\varphi = \psi$.

**Prop:** The set of maps from $\Bbb R^n$ to itself given by the action of $\text E(n)$, the [[Euclidean Group]], on $\Bbb R^n$ is the full group of Riemannian isometries of $(\Bbb R^n, \bar g)$. 

**Def:** Let $(M, g)$ be a Riemannian manifold. A smooth vector field $V$ on $M$ is called a *Killing vector field for $g$*, named after the late nineteenth/early twentieth-century German mathematician Wilhelm Killing, if the flow of $V$ acts by isometries of $g$.

**Obs:** We see that a smooth vector field is a Killing vector field iff $\mathcal L_v g = 0$. 

**Prop:** The set of all Killing vectors on $M$ constitutes a Lie subalgebra of ${\frak X}(M)$. 

**Prop:** Let $(M, g)$ be a Riemannian manifold, and $V$ is a smooth vector field on $M$. $V$ is a Killing vector field iff it satisfies the following equation in each smooth local coordinate chart$$V^k \frac{\partial g_{ij}}{\partial x^k} + g_{jk} \frac{\partial V^k}{\partial x^i} + g_{ik} \frac{\partial V^k}{\partial x^j} = 0$$
**Prop:** Let $K\subseteq \mathfrak X(\Bbb R^n)$ denote the Lie algebra of Killing vector fields with respect to the Euclidean metric. Then we see that a vector field is a Killing vector field iff $$\frac{\partial V^i}{\partial x^ j}+ \frac{\partial V^j}{\partial x^i} = 0.$$This means that the following vector fields form a basis for $K$: $$\frac{\partial}{\partial x^i}, \quad 1 \le i \le n; \qquad x^i\frac{\partial}{\partial x^j}- x^j\frac{\partial}{\partial x^i}, \quad 1\le i < j \le n. $$These vector fields represent translation, and rotations. If we consider $K_0\subseteq K$ denote the subspace consisting of fields that vanish at the origin. Then the map $$V \mapsto \left(\frac{\partial V^i}{\partial x^j}(0)\right) $$is an injective linear map from $K_0$ to $\mathfrak{so}(n)$. 

# Submanifolds

Pullback metrics are particularly important for submanifolds.

**Def:** If $(M, g)$ is a Riemannian manifold with or without boundary, every submanifold $S\subseteq M$ automatically inherits a pullback metric $\iota^* g$, where $\iota: S \hookrightarrow M$ is inclusion. We know that $\iota^*g$ is just the restriction of $g$ to pairs of vectors tangent to $S$. With this metric, $S$ is called a *Riemannian submanifold (with or without boundary) of $M$*. 

**Example:** The metric $\dot g = \iota^*\bar g$ induced on $\Bbb S^n$ by the usual inclusion $\iota: \Bbb S^n \hookrightarrow \Bbb R^{n+1}$ is called the *round metric*, or the *standard metric*, on the sphere.

Computations on a submanifold are usually most conveniently carried out in terms a *local parametrization*: this is an embedding of an open subset $U \subseteq \Bbb R^n$ into $N$, whose image is an open subset of $M$. 

**Example:** If $X: U \to \Bbb R^n$ is a parametrization of a submanifold $M \subseteq \Bbb R^n$ with the induced metric, the induced metric in standard coordinates $(u^1, \dots, u^n)$ on $U$ is just $$g = \sum_{i = 1}^n (dX^i)^2 = \sum_{i = 1}^n \left(\frac{\partial X^i}{\partial u^j} du^j\right)^2.$$
**Induced Metrics on Surfaces of Revolution:** Let $C$ be an embedded $1$-dimensional submanifold of the half plane $\{(r, z) \mid r > 0\}$, and let $S_C$ be the surface of revolution generated by $C$ is given by  $$S_C := \left\{(x, y, z) \in\Bbb R^3 \;\left\rvert\; \left(\sqrt{x^2+ y^2}, z\right)\right.\in C\right\}. $$To compute the induced metric on $S_C$, we can choose a smooth local parametrization $\gamma(t) := (a(t),b(t))$ for $XC$, and note that the map $X(t, \theta) = (a(t)\cos \theta, a(t)\sin\theta,b(t))$ yields a smooth local parametrization of $S_C$, provided $(t, \theta)$ is restricted to a sufficiently small open subset of the plane. Then $$\begin{align*}
X^* g &= d((a'(t) \cos\theta \,dt - a(t) \sin\theta \,d\theta)^2 + d((a'(t) \sin\theta dt + a(t) \cos\theta d\theta)^2 + (b'(t) dt)^2 \\
&= (a'(t)^2 + b'(t)^2) dt^2+ a(t)^2d\theta^2.
\end{align*}
$$In particular, if $\gamma$ is a *unit-speed curve*, meaning that $|\gamma'(t)| = 1$, then it reduces to $X^*g = dt^2 + a(t)^2 d\theta^2$. 

**Flatness Criterion for Surfaces of Revolution:** Let $C\subseteq H$ be a connected embedded $1$-dimensional submanifold of the half-plane $H:= \{(r, z) \mid r > 0\}$, and let $S_C$ be the surface of revolution generated by $C$. The induced metric on $S_C$ is flat iff $C$ is part of the a straight line. 

**Cor:** The round or standard metric on $\Bbb S^2$ not flat.

# The Normal Bundle

Suppose $(M, g)$ is an $n$-dimensional Riemannian manifold with or without boundary, and $S\subseteq M$ is a $k$-dimensional submanifold with or without boundary. Just as we did for submanifolds of $\Bbb R^n$, for any $p\in S$ we say that a vector $v\in T_p M$ is *normal to $S$* if $v$ is orthogonal to every vector in $T_p S$ with respect to the inner product $\langle \cdot, \cdot \rangle_g$. The *normal space to $S$ at $p$* is the subspace $N_p S \subseteq T_p M$ consisting of all vectors that are normal to $S$ at $p$, and the *normal bundle of $S$* is the subset $NS \subseteq TM$ consisting of the union of all the normal spaces at points of $S$. The projection $\pi_{NS}:NS \to S$ is defined as the restriction to $NS$ of $\pi: TM \to M$. 

**The Normal Bundle to a Riemannian Submanifold:** Let $(M, g)$ be a Riemannian $n$-manifold with or without boundary. For any immersed $k$-dimensional submanifold $S\subseteq M$ with or without boundary, the normal bundle $NS$ is a smooth rank-$(n-k)$ subbundle of $TM|_S$. For each $p\in S$, there is a smooth frame for $NS$ on a neighbourhood of $p$ that is orthonormal with respect to $g$. 

**Def:** If $S\subseteq M$ is a Riemannian submanifold, we define the *normal bundle* to $S$ as $$NS := \coprod_{p\in S} N_p S. $$
**Existence of Adapated Orthonormal Frames:** Let $S\subseteq M$ be an embedded Riemannian submanifold of a Riemannian manifold $(M, g)$. For each $p\in  S$, there is a smooth adapted orthonormal frame on a neighbourhood $p$ in $M$. 

**Prop:** Suppose $(M, g)$ is an Riemannian manifold and $S\subseteq M$ an immersed $k$-dimensional manifold. The ambient tangent bundle $TM|_S$ is isomorphic to the Whitney sum $TS\oplus NS,$ where $NS \to S$ is the normal bundle.  

**Def:** Suppose $\pi: N \to M$ is a smooth covering map. A *covering transformation*, or *[[Automorphism Group of a Covering Map|deck transformation]]* is a smooth map $\varphi: N \to N$ such that $\pi \circ \varphi = \pi$. If $g$ is Riemannian metric on $M$, then $h := \pi^* g$ is a Riemannian metric on $N$ that is invariant under all covering transformations. In this case $h$ is called a *covering metric*, and $\pi$ is called *Riemannian covering*. 

**Prop:** If $(M, g)$ is a Riemannian $n$-manifold with or without boundary, let $UM \subseteq TM$ be the subset $\{(x, v) \in TM \mid |v|_g = 1\}$, called the *unit tangent bundle of $M$*. Then  $UM$ is a smooth [[Fibre Bundles on Smooth Manifolds|fibre bundle]] over $M$ with model fibre $\Bbb S^{n-1}$. 