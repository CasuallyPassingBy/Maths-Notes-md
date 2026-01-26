---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Orientations of Vector Spaces]], [[Differential Forms on Smooth Manifolds]], [[Local and Global Sections of Vector Bundles]]

**Def:** Let $M$ be a smooth manifold with or without boundary. We define a *pointwise orientation* on $M$ to be a choice of orientation of each tangent space. If $(E_i)$ is a local frame for $TM$, we say that $(E_i)$ is *positively oriented* if $(E_1|_p,\dots, E_n|_p)$ is a positively oriented basis for $T_p M$ at each point $p\in U$. A *negatively oriented* frame is defined analogously. 

A pointwise orientation is said be *continuous* if every point of $M$ is in the domain of an oriented local frame. An *orientation of $M$* is a continuous pointwise orientations. We say that $M$ is *orientable* if there exists an orientation for it, and *nonorientable* if not. An *oriented manifold* is an ordered pair $(M, \mathcal O)$, where $M$ is the orientable manifold and $\cal O$ is a choice of orientation for $M$; an *oriented manifold with boundary* is defined similarly. For each $p\in M$, the orientation of $T_p M$ determined by $\cal O$ is denoted by ${\cal O}_p$.

If $M$ is a zero-dimensional, this definitions just means that an orientation of $M$ is a choice of $\pm 1$ attached to each of its points. 

**Obs:** Suppose $M$ is an oriented smooth $n$-manifold with or without boundary, and $n \ge 1$. Every local frame with connected domain is either positively oriented or negatively oriented.

**The Orientation Determined by an $n$-Form:** Let $M$ be a smooth $n$-manifold with or without boundary. Any nonvanishing $n$-form $\omega$ on $M$ determines a unique orientation of $M$ for which $\omega$ is positively oriented at each point. Conversely, if $M$ is given an orientation, then there is a smooth nonvanishing $n$-form on $M$ that is positively oriented at each point. 

**Def:** If $M$ is a smooth $n$-manifold with or without boundary, any nonvanishing $n$-form on $M$ is called an *orientation form*. If $M$ is oriented and $\omega$ is an orientation form determining the given orientation, we also say that $\omega$ is *positively oriented*. 

**Def:** A smooth coordinate chart on an oriented smooth manifold with or without boundary is said to be *positively oriented* if the coordinate frame $(\partial/\partial x^i)$ is positively oriented, and *negatively oriented* if the coordinate frame is negatively oriented. A smooth altas $\{(U_\alpha,\varphi_\alpha)\}$ is said to be *consistently oriented* if for each $\alpha, \beta$ the transition map $\varphi_\beta\circ\varphi_\alpha^{-1}$ has positive Jacobian determinant everywhere on $\varphi_\alpha[U_\beta \cap U_\alpha]$. 

**The Orientation Determined by a Coordinate Atlas:** Let $M$ be a smooth positive-dimensional manifold with or without boundary. Given any consistently oriented smooth atlas for $M$, there is a unique orientation for $M$ with the property that each chart in the given atlas is positively oriented. Conversely, if $M$ is oriented and either $\partial M = \varnothing$, or $\dim M > 1$, the the collection of all oriented smooth charts is a consistently oriented atlas for $M$. 

**Prop:** Let $M$ be a smooth manifold with or without boundary. Then the total spaces $TM$ and $T^*M$ are orientable. 

**Product Orientations:** Suppose $M_1,\dots, M_k$ are orientable smooth manifolds. There is a unique orientation on $M_1\times \dots \times M_k$, called the *product orientation*, with the property that for each $i =1,\dots, k$, $\omega_i$ is an orientation form for the given orientation on $M_i$, then $\pi_1^*\omega_1\wedge\dots \wedge \pi_n^*\omega_n$ is an orientation form for the product orientation. 

**Prop:** Let $M$ be a connected, orientable, smooth manifold with or without boundary. Then $M$ has two orientations. If two orientations of $M$ agree at one point, they are equal. 

**Cor:** $\Bbb S^ n$ is orientable. 

**Orientations of Codimension-$0$ Submanifolds:** Suppose $M$ is an oriented smooth manifold with or without boundary, and $D\subseteq M$ is a smooth codimension-$0$ submanifold with or without boundary. Then the orientation of $M$ restricts to an orientation of $D$. If $\omega$ is an orientation form for $M$, then $\iota_D ^*\omega$ is an orientation form for $D$.

**Def:** Let $M$ and $N$ be oriented smooth manifolds with or without boundary, and suppose $F: M \to N$ is a local diffeomorphism. If $M$ and $N$ are positive-dimensional we say that $F$ is *orientation-preserving* if for each $p\in M$, the isomorphism $dF_p$ takes oriented bases of $T_pM$ to oriented basses of $T_{F(p)}N$, and *orientation-reversing* if it takes oriented bases of $T_p M$ to negatively oriented bases of $T_{F(p)} N$. If $M$ and $N$ are $0$-manifolds, then $F$ is orientation preserving if for every $p\in M$, the points $p$ and $F(p)$ have the same orientation; and it is orientation-reversing if they have the opposite orientation.

**Prop:** Suppose $M$ and $N$ are oriented positive-dimensional smooth manifolds with or without boundary, and $F: M \to N$ is a local diffeomorphism. Then the following are equivalent.
- $F$ is orientation-preserving.
- With respect to any oriented smooth charts for $M$ and $N$, the Jacobian matrix of $F$ has positive determinant.
- For any positively oriented form $\omega$ for $N$, the form $F^*\omega$ is positively oriented for $M$.

**Obs:** The composition of orientation-preserving maps is orientation-preserving. 

**Prop:** Suppose $M$ and $N$ are are oriented manifolds with or without boundary and $F: M \to N$ is a local diffeomorphism. If $M$ is connected, then $F$ is either orientation-preserving or orientation-reversing. 

**The Pullback Orientation:** Suppose $M$ and $N$ are smooth manifolds with or without boundary. If $F:M \to N$ is a local diffeomorphism and $N$ is oriented, then $M$ has a unique orientation, called the *pullback orientation induced by $F$*, such that $F$ is orientation-preserving. 

**Def:** If $\cal O$ denotes the given orientation on $N$, the pullback orientation on $M$ is denoted by $F^*\cal O$.

**Obs:** Suppose $F: M \to N$ and $G:N \to O$ are local diffeomorphisms and $\cal O$ is an orientation on $P$. Then $(G \circ F)^*{\cal O} = F^*(G^*{\cal O})$.

**Prop:** Every [[Vector Fields on Smooth Manifolds|parallelisable]] smooth manifold is orientable. 

**Prop:** Every Lie group has precisely two left-invariant orientations, corresponding to the two orientation of its Lie algebra. 

**Prop:** Let $\theta$ be a [[Integral Curves, Flows and Flowouts on Smooth Manifolds|smooth flow]] on an oriented smooth manifold with or without boundary. For each $t\in \Bbb R$, $\theta_t$ is orientation-preserving wherever it is defined. 

**Lemma:** Every orientation-reversing diffeomorphism of $\Bbb R$ has a fixed point.

**Classification of Smooth $1$-Manifolds:** Let $M$ be a connected smooth manifold. 
- $M$ admits a nowhere vanishing vector field on $M$, thus it is $M$ orientable.
- Now let $M$ be arbitrary, its universal covering manifold is diffeomorphic to $\Bbb R$.
The smooth structures on both $\Bbb R$ and $\Bbb S^1$ are unique up to diffeomorphism.

**Classification of Smooth $1$-Manifolds with Boundary:** Every connected smooth $1$-manifold with nonempty boundary is diffeomorphic to either $[0, 1]$ or $[0,\infty)$. 

## Orientations on Hypersurfaces

**Prop:** Suppose $M$ is an oriented smooth $n$-manifold with or without boundary, $S$ is an immersed hypersurface with or without boundary in $M$, and $N$ is a vector field along $S$ that is nowhere tangent to $S$. Then $S$ has a unique orientation such that for each $p\in S$, $(E_1,\dots, E_{n-1})$ is an oriented basis for $T_p S$ iff $(N_p, E_1,\dots, E_{n-1})$ is an oriented basis for $T_p M$. If $\omega$ is an orientation form for $M$, then $\iota_S^*(N \; \lrcorner \;\omega)$ is an orientation form for $S4 with respect to this orientation, where $\iota_S: S \hookrightarrow M$ is inclusion. 

When $n = 1$, since $S$ is a $0$-manifold, this proposition should be interpreted as: at each point $p\in S$, we assign the orientation $+1$ to $p$ if $N_p$ is an oriented basis for $T_p M$, and $-1$ if $N_p$ is negatively oriented. 

**Example:** The sphere $\Bbb S^n$ is a hypersurface of $\Bbb R^{n+1}$, to which the vector field $N = x^i \partial/\partial x^i$ is nowhere tangent, so this vector field induces an orientation on $\Bbb S^n$. We define the *standard orientation of $\Bbb S^n$* to be the orientation determined by $N$. 

**Prop:** Let $M$ be an oriented smooth manifold, and suppose $S \subseteq M$ is a regular level set of a smooth function $f: M \to \Bbb R$. Then $S$ is orientable. 

## Boundary Orientations

**Induced Orientation on a Boundary:** Let $M$ be an oriented smooth $n$-manifold with boundary, $n \ge 1$. The $\partial M$ is orientable, and all outward-pointing vector fields along $\partial M$ determined the same orientation on $\partial M$. 

**Def:** The orientation on $\partial M$ determined by the outward-pointing vector field is called the *induced orientation* or the *Stokes orientation* on $\partial M$. 

**Example:** We can determine the induced orientation on $\partial \Bbb H^n$ when $\Bbb H^n$ itself has the standard coordinate orientation from $\Bbb R^n$. We can identify $\partial \Bbb H^n$ with $\Bbb R^n$ under the correspondence $(x^1,\dots, x^{n-1}, 0) \leftrightarrow(x^1,\dots, x^{n-1})$. Since the vector field $-\partial/\partial x^n$ is outward pointing along $\partial \Bbb H^n$, the standard coordinate frame for $\Bbb R^n$ is positively oriented of $\partial \Bbb H^n$ iff $[-\partial/\partial x^n, \partial/\partial x^1,\dots, \partial/\partial x^{n-1}]$ is the standard orientation for $\Bbb R^n$. This orientation satisfies $$[-\partial/\partial x^n, \partial/\partial x^1,\dots, \partial/\partial x^{n-1}] = (-1)^n[\partial/\partial x^1,\dots, \partial/\partial x^{n-1}, \partial/\partial x^n]  .$$Thus the induced orientation on $\partial \Bbb H^n$ is equal to the standard orientation of $\Bbb R^{n-1}$ when $n$ is even, but it is *opposite* to the standard orientation when $n$ is odd. In particular, the standard coordinates on $\partial\Bbb H^n \cong \Bbb R^n$ are positively oriented iff $n$ is even. 

**Lemma:** Let $M$ be an oriented smooth $n$-manifold with boundary. Suppose $U \subseteq\Bbb R^{n-1}$ is open, $a, b$ are real numbers with $a< b$, and $F:(a,b] \times U \to M$ is a smooth embedding that restricts to an embedding of $\{b\}\times U$ into $\partial M$. Then the parametrization $f: U \to \partial M$ given by $f(x) := F(b, x)$ is orientation preserving iff $F$ is orientation preserving for $M$. 

**Example:** Spherical coordinates yield a smooth local paramterization of $\Bbb S^2$ as follows. Let $U$ be the open rectangle $(0, \pi) \times (0, 2\pi) \subseteq\Bbb R^2$, and let $X: U\to\Bbb R^3$ be the following map $$X(\varphi, \theta) := (\sin\varphi \cos\theta, \sin\varphi\sin\theta,\cos\varphi).  $$
We can check whether $X$ preserves or reverses orientatio by using the fact that is is the restriction of the $3$-dimensional spherical coordinate parametrization $F: (0, 1] \times U \to \bar{\Bbb B}^3$ defined by$$F(\rho,\varphi,\theta) =(\rho\sin \varphi\cos\theta,\rho\sin \varphi\sin\theta, \rho\cos\varphi).   $$Because $F(1,\varphi,\theta) = X(\varphi, \theta)$, then the lemma above can be used. By direct computation, the Jacobian determinant of $F$ is $\rho^2\sin\varphi$, which is positive on $(0, 1]\times U$. Then, $X$ is orientation-preserving.

This actually explains why physicists have the notations they have. It is still like dumb that they don't simply change the place of the variables, and rather change what the variables represent.