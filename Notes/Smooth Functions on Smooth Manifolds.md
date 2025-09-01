---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth or Differentiable Manifolds]]

**Def:** Le t $M$ be a smooth manifold of dimension $n$. A function $f: M \to \Bbb R$ is said to be $\mathcal C^\infty$ or *smooth at a point $p$* in $M$ if there is chart $(U, \phi)$ about $p$ in $M$ such that $f\circ \phi^{-1}$ a function on the open subset $\phi[U]$ of $\Bbb R^n$, is $\mathcal C^\infty$ at $\phi(p)$. The function $f$ is said to be $\mathcal C^\infty$ *on $M$* $\mathcal C^\infty$ at every point of $M$.

**Prop:** Let $M$ be a manifold of dimension $n$, and $f:M \to \Bbb R$ a real-valued function $M$. The following are equivalent:
- The function $f: M \to \Bbb R$ is $\mathcal C^\infty$
- The manifold $M$ has an atlas such that for every chart $(U, \phi)$ in the atlas $f\circ \phi^{-1}: \phi[U] \subseteq \Bbb R^n \to \Bbb R$ is $\mathcal C^\infty$.
- For every chart $(V, \psi)$ on $M$, the function $f \circ \psi^{-1}: \psi[V] \subseteq \Bbb R^n \to \Bbb R$. is $\mathcal C^\infty$.

**Def:** Let $F: N \to M$ be a map and $h$ be a function on $M$. The *pullback* of $h$ by $F$, denoted by $F^*h$, is the composite function $F^* h := h \circ F$. 

In this terminology, a function $f$ on $M$ is $\mathcal C^\infty$ on a chart $(U, \phi)$ iff its pullback $(\phi^{-1})^* f$ by $\phi^{-1}$ is $\mathcal C^\infty$ on the subset $\phi[U]$ of Euclidean space.

# Smooth Maps Between Manifolds

**Def:** Let $N$ and $M$ be manifolds of dimension $n$ and $m$, respectively. A continuous map $F: N \to M$ is $\mathcal C^\infty$ *at a point $p$* in $N$ if there are charts $(V, \psi)$ about $F(p)$ in $M$ and $(U, \phi)$ about $p$ in $N$ such that the composition $\psi \circ F \circ \phi^{-1}$, a map of the open subset $\phi[F^{-1}[V] \cap U]$ of $\Bbb R^n$ to $\Bbb R^m$ ar $\phi(p)$. The continuous map $F: N \to M$ is said to be $\mathcal C^\infty$ if it is $\mathcal C^\infty$ at every point of $N$. 

**Prop:** Suppose $F: N \to M$ is $\mathcal C^\infty$ at $p\in N$. If $(U, \phi)$ is any chart about $p$ in $N$ and $(V, \psi)$ is any chart about $F(p)$ in $M$ then $\psi \circ  F \circ \phi^{-1}$ is $\mathcal C^\infty$ at $\phi(p)$. 

**Prop:** Let $N$ and $M$ be a smooth manifolds, and $F: N \to M$ a continuous map. The following are equivalent:
- The map $F:N \to M$ is $\mathcal C^\infty$. 
- There are atlases $\mathfrak U$ for $N$ and $\mathfrak V$ for $M$ such that for every chart $(U, \phi) \in \frak U$ and $(V, \psi)\in \frak V,$ the map: $$\psi\circ F \circ \phi^{-1}: \phi[U \cap F^{-1}[V]] \to \Bbb R^m $$is $\mathcal C^\infty$.
- For every chart $(U, \phi)$ on $N$ and $(V, \psi)$ on $M$, the map: $$\psi\circ F \circ \phi^{-1}: \phi[U \cap F^{-1}[V]] \to \Bbb R^m $$is $\mathcal C^\infty$.

**Prop:** If $F: N\to M$ and $G: M \to P$ are $\mathcal C^\infty$ maps of manifolds, then the composite function $G \circ F: N \to P$ is $\mathcal C^\infty$. 

**Prop:** Let $M$ and $N$ be manifolds and $\pi: M \times N \to M$, $\pi(p, q) = p$ the projection to the first factor. Then $\pi$ is a $\mathcal C^\infty$ map. 

**Prop:** Let $M_1, M_2$ and $N$ be manifolds of dimension $m_1, m_2$ and $n$ respectively. Then a map $(f_1, f_2): N \to M_1 \times M_2$ is $\mathcal C^\infty$ iff $f_i : N \to M_i$, $i \in \{1, 2\}$ are both $\mathcal C^\infty$. 

**Prop:** Let $M$ and $N$ be manifolds and let $q_0 \in N$. Then the inclusion map $\iota: M \to M \times N$ by $\iota(p) = (p, q_0)$. 

# Diffeomorphisms

**Def:** A *diffeomorphism* of manifolds is a bijective $\mathcal C^\infty$ map $F: N \to M$ whose inverse $F^{-1}$ is also $\mathcal C^\infty$. 

**Prop:** If $(U, \phi)$ is a chart on a manifold $M$ of dimension $n$, then the coordinate map $\phi: U \to \phi[U]\subseteq \Bbb R^n$ is a diffeomorphism. 

**Prop:** Let $U$ be an open subset of a manifold $M$ of dimension $n$. If $F:U \to F[U]\subseteq \Bbb R^n$ is a diffeomorphism onto an open subset of $\Bbb R^n$, then $(U, F)$ is a chart in the differentiable structure of $M$. 

**Def:** The set of all diffeomorphisms of the form $\varphi: M \to M$ is called the *diffeomorphism group of $M$* and it is denoted as $\text{Diffeo}(M)$. This related to the [[automorphism group]] in any category.

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
