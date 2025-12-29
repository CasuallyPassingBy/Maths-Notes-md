---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]]

**Def:** Let $M$ be a smooth manifold of dimension $n$. A function $f: M \to \Bbb R$ is said to be $\mathcal C^\infty$ or *smooth at a point $p$* in $M$ if there is chart $(U, \phi)$ about $p$ in $M$ such that $f\circ \phi^{-1}$ a function on the open subset $\phi[U]$ of $\Bbb R^n$, is $\mathcal C^\infty$ at $\phi(p)$. The function $f$ is said to be $\mathcal C^\infty$ *on $M$, $\mathcal C^\infty$ at every point of $M$.

**Def:** Given a function $f: M \to \Bbb R^k$ and a chart $(U,\varphi)$ for $M$; the function $\hat f: \varphi[U] \to \Bbb R^k$ defined by $\hat f = f\circ \varphi^{-1}$ is called a *coordinate representation of $f$*. By definition, $f$ is smooth iff its coordinate represention is smooth in some smooth chart around each point. 

**Prop:** Let $M$ be a manifold of dimension $n$, and $f:M \to \Bbb R$ a real-valued function $M$. The following are equivalent:
- The function $f: M \to \Bbb R$ is $\mathcal C^\infty$
- The manifold $M$ has an atlas such that for every chart $(U, \phi)$ in the atlas $f\circ \phi^{-1}: \phi[U] \subseteq \Bbb R^n \to \Bbb R$ is $\mathcal C^\infty$.
- For every chart $(V, \psi)$ on $M$, the function $f \circ \psi^{-1}: \psi[V] \subseteq \Bbb R^n \to \Bbb R$. is $\mathcal C^\infty$.

**Def:** Let $F: N \to M$ be a map and $h$ be a function on $M$. The *pullback* of $h$ by $F$, denoted by $F^*h$, is the composite function $F^* h := h \circ F$. 

In this terminology, a function $f$ on $M$ is $\mathcal C^\infty$ on a chart $(U, \phi)$ iff its pullback $(\phi^{-1})^* f$ by $\phi^{-1}$ is $\mathcal C^\infty$ on the subset $\phi[U]$ of Euclidean space.

# Smooth Maps Between Manifolds

**Def:** Let $N$ and $M$ be manifolds of dimension $n$ and $m$, respectively. A continuous map $F: N \to M$ is $\mathcal C^\infty$ *at a point $p$* in $N$ if there are charts $(V, \psi)$ about $F(p)$ in $M$ and $(U, \phi)$ about $p$ in $N$ such that the composition $\psi \circ F \circ \phi^{-1}$, a map of the open subset $\phi[F^{-1}[V] \cap U]$ of $\Bbb R^n$ to $\Bbb R^m$ ar $\phi(p)$. The continuous map $F: N \to M$ is said to be $\mathcal C^\infty$ if it is $\mathcal C^\infty$ at every point of $N$. 

**Prop:** Every smooth map is continuous.

**Prop:** Suppose $F: N \to M$ is $\mathcal C^\infty$ at $p\in N$. If $(U, \phi)$ is any chart about $p$ in $N$ and $(V, \psi)$ is any chart about $F(p)$ in $M$ then $\psi \circ  F \circ \phi^{-1}$ is $\mathcal C^\infty$ at $\phi(p)$. 

**Equivalent Characterisations of Smoothness:** Suppose $M$ and $N$ are smooth manifolds with or without boundaries, and $F: M\to N$ is a map. Then $F$ is smooth iff it either of the following conditions is satisfied:
- For every $p\in M$, there exists smooth charts $(U, \varphi)$ containing $p$ and $(V, \psi)$ containing $F(p)$ such that $U \cap F^{-1}[V]$ is open in $M$ and the composite map $\psi\circ F \circ \varphi^{-1}$ is smooth from $\varphi[U \cap F^{-1}[V]]$ to $\psi[V]$. 
- $F$ is continuous and there are atlases $\mathfrak U$ for $N$ and $\mathfrak V$ for $M$ such that for every chart $(U, \phi) \in \frak U$ and $(V, \psi)\in \frak V,$ the map: $$\psi\circ F \circ \phi^{-1}: \phi[U \cap F^{-1}[V]] \to \Bbb R^m $$is $\mathcal C^\infty$.
- For every chart $(U, \phi)$ on $N$ and $(V, \psi)$ on $M$, the map: $$\psi\circ F \circ \phi^{-1}: \phi[U \cap F^{-1}[V]] \to \Bbb R^m $$is $\mathcal C^\infty$.

**Smoothness is Local:** Let $M$ and $N$ be smooth manifolds with or without boundary, and let $F: M \to N$ be a map.
- If every point $p\in M$ has a neighbourhood such that the restriction $F|_U$ is smooth, the $F$ is smooth.
- Conversely, if $F$ is smooth, then its restriction of every open subset is smooth. 

**Gluing Lemma for Smooth Maps:** Let $M$ and $N$ be smooth manifolds with or without boundary, $\kappa$ some ordinal, and $\{U_\alpha \mid \alpha<\kappa\}$ be an open cover of $M$. Suppose that for each $\alpha <\kappa$, we are given $F_\alpha: U_\alpha\to N$ such that the maps agree on overlaps: $F\alpha|_{U_\alpha\cap U_\beta} = F_\beta|_{U_\alpha\cap U_\beta}$ for all $\alpha<\beta<\kappa$. Then there exists a unique smooth map $F: M \to N$ such that $F|_{U_\alpha} = F_\alpha$ for each $\alpha<\kappa$. 

If $F: M \to N$ is a smooth map, $(U,\varphi)$ and $(V, \psi)$ are any smooth charts for $M$ and $N$, respectively, we call $\hat F = \psi \circ F \circ \varphi^{-1}$ the *coordinate representation of $F$* with respect to the coordinates. It maps the set $\varphi[U\cap F^{-1}[V]]$ to $\psi[V]$. 

**Prop:** Let $M, N$ and $P$ be smooth manifolds with or without boundary.
- Every constant map $c: M \to N$ is smooth. 
- The identity map of $M$ is smooth. 
- If $U \subseteq M$ is an open submanifold with or without boundary, then the inclusion map $U \hookrightarrow M$ is smooth.
- If $F: M \to N$ and $G: N \to P$ are smooth, then so is $G\circ F: M \to P$. 

**Prop:** Let $M$ and $N$ be manifolds and $\pi: M \times N \to M$, $\pi(p, q) = p$ the projection to the first factor. Then $\pi$ is a $\mathcal C^\infty$ map. 

**Prop:** Let $M_1, M_2$ and $N$ be manifolds of dimension $m_1, m_2$ and $n$ respectively. Then a map $(f_1, f_2): N \to M_1 \times M_2$ is $\mathcal C^\infty$ iff $f_i : N \to M_i$, $i \in \{1, 2\}$ are both $\mathcal C^\infty$. 

**Prop:** Let $M$ and $N$ be manifolds and let $q_0 \in N$. Then the inclusion map $\iota: M \to M \times N$ by $\iota(p) = (p, q_0)$. 

# Diffeomorphisms

**Def:** A *diffeomorphism* of manifolds is a bijective $\mathcal C^\infty$ map $F: N \to M$ whose inverse $F^{-1}$ is also $\mathcal C^\infty$. 

**Prop:** If $(U, \phi)$ is a chart on a manifold $M$ of dimension $n$, then the coordinate map $\phi: U \to \phi[U]\subseteq \Bbb R^n$ is a diffeomorphism. 

**Properties of Diffeomorphisms:**
- Every composition of diffoemorphism is a diffeomorphism.
- Every finite product of diffeomorphism between smooth manifolds is a diffeomorphism.
- Every diffeomorphism is a homeomorphism and an open map.
- The restriction of a diffeomorphism to an open submanifold with or without boundary is a diffeomorphism onto its image.
- 'Diffeomorphic' is an equivalence relation on the class of all smooth manifolds with or without boundary.

**Prop:** Let $U$ be an open subset of a manifold $M$ of dimension $n$. If $F:U \to F[U]\subseteq \Bbb R^n$ is a diffeomorphism onto an open subset of $\Bbb R^n$, then $(U, F)$ is a chart in the differentiable structure of $M$. 

**Def:** The set of all diffeomorphisms of the form $\varphi: M \to M$ is called the *diffeomorphism group of $M$* and it is denoted as $\text{Diffeo}(M)$. This related to the [[automorphism group]] in any category.

**Diffeomorphism Invariance of Dimension:** A nonempty smooth manifold of dimension $m$ cannot be diffeomorphic to an $n$-dimensional smooth manifold unless $m= n$. 

# Smoothness in Terms of Components

**Prop:** Let $N$ be a manifold and $F:N \to \Bbb R^m$ a continuous map. The following are equivalent:
- The $F: N \to \Bbb R^m$ is $\mathcal C^\infty$. 
- The manifold $N$ has an atlas such that for every chart $(U, \phi)$ in the atlas, the map $F\circ \phi^{-1}: \phi[U] \to \Bbb R^m$ is $\mathcal C^\infty$. 
- For every chart $(U, \phi)$ on $N$, the map $F\circ \phi^{-1}: \phi[U] \to \Bbb R^m$ is $\mathcal C^\infty$.

**Prop:** Let $N$ be a manifold. A vector-valued function $F: N \to \Bbb R^m$ is $\mathcal C^\infty$ iff if its component functions $F^1, \dots, F^m: N \to \Bbb R$ are all $\mathcal C^\infty$.

**Prop:** Let $F: N \to M$ be a continuous map between two manifolds of dimension $n$ and $m$ respectively. The following are equivalent:
- The map $F: N \to M$ is $\mathcal C^\infty$. 
- The manifold $M$ has an atlas such for every chart $(V, \psi) = (V, y^1,\dots, y^ m)$ in the atlas, the vector-valued function $\psi \circ F: F^{-1}[V] \to \Bbb R^m$ is $\mathcal C^\infty$.
- For every chart $(V, \psi) = (V, y^1, \dots, y^m)$ on $M$, the vector-valued function $\psi \circ F: F^{-1}[V] \to \Bbb R^m$ is $\mathcal C^\infty$.

**Prop:** Let $F: N \to M$ be a continuous map between two manifolds of dimension $n$ and $m$ respectively. The following are equivalent:
- The $F: N \to M$ is $\mathcal C^\infty$. 
- The manifold $M$ has an atlas such for every chart $(V, \psi) = (V, y^1,\dots, y^ m)$ in the atlas, the components $y^i \circ F: F^{-1}[V] \to \Bbb R$ of $F$ is relative to the chart are all $\mathcal C^\infty$. 
- For every chart $(V, \psi) = (V, y^1, \dots, y^m)$ on $M$, the components  $y^i \circ F: F^{-1}[V] \to \Bbb R$ of $F$ is relative to the chart are all $\mathcal C^\infty$. 
