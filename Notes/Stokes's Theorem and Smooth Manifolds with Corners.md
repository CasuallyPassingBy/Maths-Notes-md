---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Integration of Differential Forms on Smooth Manifolds]], [[The Fundamental Theorem of Calculus]], [[Green's Theorem and Curl in R2]], [[Line Integral over a Vector Field]], [[Line Integrals of Differential 1-forms]], [[Conservative Fields]], [[Smooth Partitions of Unity for Manifolds]]
# Stoke's Theorem

**Stoke's Theorem:** Let $M$ be an oriented smooth $n$-manifold with boundary, and let $\omega$ be a compactly supported smooth $(n-1)$-form on $M$. Then $$\int_M d\omega = \int_{\partial M} \omega.$$
First, $\partial M$ is understood to have the induced (Stokes) orientation, and the $\omega$ on the right hand side is to be interpreted to be as $\iota_{\partial M}^*\omega$. If $\partial M = \varnothing$, then the right-hand side is to be interpreted as zero. When $M$ is $1$-dimensional, the right-hand integral is just really a finite sum.

**Example:** Let $M$ be a smooth manifold and suppose $\gamma:[a, b] \to M$ is a smooth embedding, so that $S = \gamma[[a, b]]$ is an embedded $1$-submanifold with boundary in $M$. If we give $S$ the orientation such that $\gamma$ is orientation-preserving, then for any smooth function $f\in\mathcal C^\infty(M)$, we get that
$$\int_\gamma df = \int_{[a, b]} \gamma^*df = \int_S df = \int_{\partial S} f = f(\gamma(b))- f(\gamma(a)). $$Thus Stokes's theorem reduces to the fundamental theorem for line integrals. Then Stokes's theorem gives us [[the fundamental theorem of calculus]].

**Integrals of Exact Forms:** If $M$ is a compact oriented smooth manifold without boundary, then the integral of every exact form over $M$ is zero: $$\int_M d\omega = 0 \qquad \text{if }\partial M = \varnothing. $$

**Integrals of Closed Forms over Boundaries:** Suppose $M$ is a compact oriented smooth manifold with boundary. If $\omega$ is closed form on $M$, then the integral of $\omega$ over $\partial M$ is zero: $$\int_{\partial M} \omega = 0 \qquad \text{if }d\omega = 0\text{ on }M. $$
**Cor:** Suppose $M$ is a smooth manifold with or without boundary, $S\subseteq M$ is an oriented compact smooth $k$-dimensional submanifold with or without boundary, and $\omega$ is closed $k$-form. If $\int_S\omega \neq 0$, then both of the following are true:
- $\omega$ is not exact on $M$.
- $S$ is not the boundary of an oriented compact smooth submanifold with boundary in $M$. 

**Cor ([[Green's Theorem and Curl in R2|Green's Theorem]]):** Suppose $D$ is a compact regular domain in $\Bbb R^2$, and $P$, $Q$ are smooth real-valued functions on $D$. Then $$\int_D \left(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y} \right)\; dxdy = \int_{\partial D} P \; dx + Q\; dy. $$

**Cor:** Suppose $M$ is an oriented compact smooth manifold with boundary. There doesn't exist a retraction of $M$ into its boundary.

**Prop:** Suppose $M$ and $N$ are oriented, compact, connected, smooth manifolds, and $F, G: M \to N$ are homotopic diffeomorphism. Then, $F$ and $G$ are both orientation-preserving or both are orientation-reversing. 

**Prop:** The following statements are equivalent.
- There exists a nowhere-vanishing vector field on $\Bbb S^n$.
- There exists a continuous map $V: \Bbb S^n \to\Bbb S^n$ satisfying $V(x)\;\bot \;x$, with respect to the Euclidean dot product, for all $x\in \Bbb S^n$.
- The antipodal map $\alpha: \Bbb S^n\to\Bbb S^n$ is homotopic to $\text{id}_{\Bbb S^n}$.
- The antipodal map $\alpha: \Bbb S^n\to\Bbb S^n$ is orientation-preserving.
- $n$ is odd.

**The Hairy Ball Theorem:** There exists a nowhere-vanishing vector field on $\Bbb S^n$ iff $n$ is odd. 

## Manifolds with Corners

**Def:** Let $\bar{\Bbb R}^n_+$ denote the subset $\Bbb R^n$ where all the coordinates are nonnegative: $$\bar{\Bbb R}^n_+ := \{(x_1,\dots, x_n) \mid \forall 1\le i \le n[x_i \ge 0]\}.  $$
We see that $\bar{\Bbb R}^n_+$ is homeomorphic to the upper half-space $\Bbb H^n$.

**Def:** Suppose $M$ is a topological $n$-manifold with boundary. A *chart with corners* for $M$ is a pair $(U,\varphi)$, where $U\subseteq M$ is open and $\varphi$ is a homeomorphism from $U$ to an open subset $\widehat U\subseteq \bar{\Bbb R}^n_+$. Two charts with corners $(U, \varphi)$, $(V, \psi)$ are smoothly compatible if the composite map $\varphi \circ\psi^{-1}: \psi[U \cap V] \to \varphi[U\cap V]$ is smooth. 

A *smooth structure with corners* on a topological manifold with boundary is a maximal collection of smoothly compatible interior charts and charts with corners whose domain cover $M$. A topological manifold with boundary together with a smooth structure with corners called a *smooth manifold with corners*. Any chart with corners in the given smooth structure with corners is called a *smooth chart with corners* for $M$.

**Example:** Any closed rectangle in $\Bbb R^n$ is a smooth $n$-manifold with corners. 

From a topological point of view there is no difference between manifolds with boundary and manifolds with corners. The difference is in the smooth structure, because in the dimensions greater than $1$, the compatibility conditions for charts with corners is different from that for boundary charts. We see that $\bar{\Bbb R}^1_+ = \Bbb H^1$, so smooth $1$-manifolds with corners are no different from smooth manifolds with boundary.

**Def:** The boundary of $\bar{\Bbb R}^n_+$ in $\Bbb R^n$ is the set of points at which at least one coordinate vanishes. The points of $\bar{\Bbb R}^n_+$ at which more than one coordinate vanishes are called its *corner points*.

**Invariance of Corner Points:** Let $M$ be a smooth $n$-manifold with corner, $n\ge 2$ and let $p\in M$. If $\varphi(p)$ is a corner point for some smooth char with corners $(U,\varphi)$, then the same is true for every chart whose domain contains $p$.

**Def:** If $M$ is a smooth manifold with corners, a point $p\in M$ is called a *corner point* if $\varphi(p)$ is a corner point in $\bar{\Bbb R}^n_+$ with respect to some smooth chart with corners $(U,\varphi)$. Similarly, $p$ is called a *boundary point* if $\varphi(p) \in \partial \bar{\Bbb R}^n_+$ with respect to some such chart. 

Every smooth manifold with or without boundary is also a smooth manifold with corners, but with no corner points. Conversely, a smooth manifold with corners is a smooth boundary with boundary, iff it has no corner points. The boundary of a smooth manifold with corners is in general a smooth manifold with corners. 

**Prop:** If $M_1,\dots, M_k$ are smooth manifolds with corners, then $M_1\times \dots\times M_k$ is also a smooth manifold with corners. This is not true for manifold with boundaries.

**Def:** Let $M$ be an oriented smooth $n$-manifold with corners, and suppose $\omega$ is an $(n-1)$-form on $\partial M$ that is compactly supported in the domain of a single oriented smooth chart with corners $(U, \varphi)$. We define the integral of $\omega$ over $\partial M$ by  $$\int_{\partial M}\omega = \int_{i = 1}^n (\varphi^{-1})^*\omega, $$where $$H_i := \{(x^1,\dots, x^n) \in \bar{\Bbb R}^n_+ \mid x^i = 0\}  $$is given the induced orientation as part of the boundary of the set where $x^i\ge 0$. In other words, we simply integrate $\omega$ in coordinates over the codimension-$1$ portion of the boundary. Finally, if $\omega$ is an arbitrary compactly supported $(n-1)$-form on $M$, we define the integral of $\omega$ over $\partial M$ by piecing together with a partition of unity just as in the case of a manifold with boundary. 

**Integrations Over Parametrizations of the Boundary:** Let $M$ be a compact, oriented, smooth $n$-manifold with corners, and let $\partial M$ denotes its boundary, equipped with the induced orientation. Let $\omega$ be a compactly supported $(n-1)$-form on $\partial M$.  Suppose $D_1, \dots, D_k$ are open domains of integration in $\Bbb R^{n-1}$, and for $i = 1,\dots, k$, we are given smooth maps $F_i: \overline D_i \to M$ satisfying:
- $F_i$ restricts to an orientation-preserving diffeomorphism from $D_i$ onto an open subset $W_i \subseteq\partial M$;
- $W_i \cap W_j = \varnothing$ when $i \neq  j$;
- $\text{supp }\omega \subseteq \bigcup_{i = 1}^k \overline W_i$. 
Then  $$\int_M \omega = \sum_{i = 1}^k \int_{D_i} F^*_i \omega. $$

**Stokes's Theorem on Manifolds with Corners:** Let $M$ be an oriented smooth $n$-manifold with corner, and let $\omega$ be a compactly supported $(n-1)$-form on $M$. Then$$\int_M d\omega = \int_{\partial M} \omega.$$
**Th:** Suppose $M$ is a smooth manifold and $\gamma_0, \gamma_1:[a,b] \to M$ are path-homotopic piecewise smooth curve segments. For every closed $1$-form on $M$, $$\int_{\gamma_0} \omega = \int_{\gamma_1}\omega.$$
**Cor:** On a simply connected smooth manifold, every closed $1$-form is exact.

