---
tags:
  - Topology
  - DifferentialGeometry
---
Subjects: [[Topology]], [[Differential Geometry]]
Links: [[Hausdorff Spaces]], [[Separable, First and Second Countable Spaces]], [[Continuous Functions and Homeomorphims]], [[Fundamental Group of a Topological Space]], [[Partitions of Unity]], [[Adjunction Topology]]

**Def:** A topological space $M$ is *locally Euclidean of dimension $n$* if every point $p$ in $M$ has a neighbourhood $U$ such that there is a homeomorphism $\phi$ from $U$ onto an open subset of $\Bbb R^n$. We call the pair $(U, \phi: U \to \Bbb R^n)$ a *chart*, $U$ a *coordinate neighbourhood* or a *coordinate open set*, and $\phi$ a *coordinate map* or a *coordinate system* on $U$. We say that a chart $(U, \phi)$is *centred* at $p \in U$ if $\phi(p) = 0$. If the coordinate domain is homeomorphic to a ball in $\Bbb R^n$, then it is called a coordinate ball. 

**Lemma:** A topological space $M$ is locally Euclidean of dimension $n$ iff
- Every point of $M$ has a neighbourhood homeomorphic to an open ball in $\Bbb R^n$.
- Every point of $M$ has a neighbourhood homeomorphic to $\Bbb R^n$. 

**Def:** A *topological manifold* $M$ is a Hausdorff, second countable locally Euclidean space. It is said to be of *dimension* $n$ if it is locally Euclidean of dimension $n$.

A manifold is said to have dimension $n$ if all of its connected components have dimension $n$. A $1$-dimensional manifold is also called a *curve*, a $2$-dimensional manifold a *surface*, and an $n$-dimensional manifold an $n$-manifold

**Prop:** Every open subset of an $n$-manifold is an $n$-manifold.

$(*)$ **Invariance of Dimension:** If $m \neq n$, a nonempty topological space cannot be both an $m$-manifold and an $n$-manifold.

We haven't proved that the dimension is indeed well defined. For that, we would need to know that for $n \neq m$ an open subset of $\Bbb R^n$ is not homeomorphic to an open subset of $\Bbb R^m$. This fact, called the invariance of dimension, is indeed true, but not in the scope right now.

**Prop:** A separable metric space that is locally euclidean of dimension $n$ is an $n$-manifold.

**Obs:** Suppose $(U, \phi: U \to \Bbb R^n)$ and $(V, \psi: V\to \Bbb R^n)$ are two charts of a topological manifold. since $U \cap V$ is open in $U$ and $\phi: U \to \Bbb R^n$ is a homeomorphism onto an open subset of $\Bbb R^n$, the image $\phi(U \cap V)$ will also be an open subset of $\Bbb R^n$. Similarly, $\psi(U \cap V)$ is an open subset of $\Bbb R^n$, and there is a homeomorphism between them, namely $\psi \circ \phi^{-1}$ or $\phi \circ \psi^{-1}$. 

**Def:** An *atlas* on a locally Euclidean space $M$ is a collection of charts $\mathfrak U = \{(U_\alpha, \varphi_\alpha) \mid \alpha < \kappa\}$ that [[Topological Covers|cover]] $M$, i.e. such that $M = \bigcup_{\alpha < \kappa} U_\alpha$. A *complete atlas* is maximal. 

**Lemma:** Every manifold $M$ has a countable basis all of whose elements have compact closure.

**Prop:** Let $M$ be a topological manifold is [[Local Path Connectedness|locally path connected]], and $M$ has at most countably many componentes, each of which is an open subset of $M$ and a connected topological manifold.

**Cor:** Every topological $n$-manifold is homeomorphic to a disjoint union to countable many connected $n$-manifolds.

**Def:** Let $M$ be an $n$-manifold. We say that a coordinate ball $B\subseteq M$ is a *regular coordinate ball* if there is a neighbourhood $B'$ of $\overline B$ and a homeomorphism $\varphi: B' \to B(0, r')\subseteq \Bbb R^n$ that takes $B$ to $B(0, r)$ and $\overline B$ to $\overline B(0, r)$ for some $r' > r > 0$. 

**Lemma:** Let $M$ be an $n$-manifold. If $B'\subseteq M$ is any coordinate ball and $\varphi: B' \to B(0, r')\subseteq \Bbb R^n$ is a homeomorphism, then $\varphi^{-1}[B(0, r)]$ is a regular coordinate ball. 

**Prop:** Every manifold has a countable basis of regular coordinate balls.

**Cor:** Every topological manifold is [[Local Compactness|locally compact]].

**Prop:** Every topological manifold is [[Paracompacteness|paracompact]], and by Smirnov's metrization theorem, we know that every topological manifold is metrizable. 

**Embeddability of Compact Manifolds:** Every compact manifold is homeomorphic toa subset of some Euclidean space.

**Prop:** The fundamental group of any topological manifold is countable.

## Connected Sum

**Def:** Let $M_1$ and $M_2$ be connected smooth manifolds of dimension $n$. For $i = 1, 2$, let $(W_i, \varphi_i)$ be a smooth coordinate domain centred at some point $p_i \in M_i$ such that $\varphi_i[W_i] \subseteq B(0, 2) \subseteq \Bbb R^n$. We define $U_i = \varphi_i^{-1}[B(0, 1)]\subseteq W_i$ and $M'_i := M_i \setminus U_i$. The *connected sum* of $M_1$ and $M_2$, denoted by $M_1 \# M_2$, is the quotient space of $M_1' \sqcup M_2'$ obtained by identifying each $q\in \partial U_1$ with $\varphi_2^{-1}\circ \varphi_1(q)\in \partial U_2$. 

$M_1 \# M_2$ is a connected topological $n$-manifold and has a unique structure such that the restriction of the quotient map to each $M_i'$ is a smooth embedding, where $M_i'$ is considered a smooth manifold with boundary. There are open subsets $U,V \subseteq M_1 \# M_2$ that are diffeomorphic to $M_1 \setminus \{p_1\}$ and $M_2\setminus \{p_2\}$, respectively, and such that $U \cap V$ is diffeomorphic to $B_2(0) \setminus \{0\}$.

If $M_1$ and $M_2$ are compact, then so is $M_1\#M_2$.

# Manifolds with Boundary

Let us consider the closed $n$-dimensional *upper half-space* $\Bbb H^n \subseteq \Bbb R^n$, defined as $$\Bbb H^n := \{(x^1, \dots, x^n) \in \Bbb R^n \mid x^n \ge 0\}.$$We will use $\text{Int}(\Bbb H^n)$ and $\partial \Bbb H^n$ to denote the interior and boundary of $\Bbb H^n$, respectively, as a subset of $\Bbb R ^n$: $$\begin{align*}
\text{Int}(\Bbb H^n) &= \{(x^1, \dots, x^n) \in \Bbb R^n \mid x^n > 0\}, \\
\partial \Bbb H^n &= \{(x^1, \dots, x^n) \in \Bbb R^n \mid x^n = 0\}.
\end{align*}$$
**Def:** An $n$-dimension *topological manifold with boundary* is a second countable Hausdorff space $M$ in which every point has a neighbourhood homeomorphic to an open subset of $\Bbb H^n$. An open subset $U \subseteq M$ together with a homeomorphism $\varphi$ from $U$ to an open subset of $\Bbb H^n$ will be called a chart, just as in the case of manifolds. When it is necessary to make the distinction, we will call $(U, \varphi)$ an *interior chart* if $\varphi[U] \subseteq \text{Int}(\Bbb H^n)$, and *boundary chart* if $\varphi[U] \cap \partial \Bbb H^n \neq \varnothing$.

**Prop:** If $M$ is an $n$-dimensional manifold with boundary, then $\text{Int}(M)$ is an open subset of $M$, which is itself an $n$-dimensional without boundary.

$(*)$ **Invariance of Boundary:** If $M$ is a manifold without boundary, then a point of $M$ cannot be a boundary point and an interior point. Thus $\partial M$ and $\text{Int}(M)$ are disjoint whose union is $M$

**Cor:** If $M$ is a nonempty $n$-dimensional manifold with boundary, then $\partial M$ is closed in $M$, and $M$ is an $n$-manifold iff $\partial M = \varnothing$. 

**Prop:** Let $M$ be a topological manifold with boundary is [[Local Path Connectedness|locally path connected]].

**Cor:** Every topological -manifold with boundary is homeomorphic to a disjoint union to countable many connected -manifolds with boundary.

**The Double of a Manifold with Boundary:** Suppose $M$ is an $n$-dimensional manifold with boundary. if $h: \partial M \to \partial M$ is the identity map the resulting space $M\cup_h M$ is denoted by $D(M)$ and called the *double of $M$*. 

**Prop:** Suppose $M$ is a connected manifold with nonempty boundary, then its double $D(M)$ is connected.

**Def:** If $M$ is an $n$-manifold with boundary, let us say that a subset $B\subseteq M$ is a *regular coordinate half-ball* if there is an open subset $B'$ containing $\overline B$ and a homemorphism from $B'$ to $B(0,r') \cap \Bbb H^n$ that takes $B$ to $B(0, r) \cap \Bbb H^n$ and $\overline B$ to $\overline B(0, r) \cap \Bbb H^n$ for some $0 < r<r'$. 

**Prop:** Every manifold with boundary has countable basis consisting of regular balls and half-balls.

**Prop:** Every topological manifold  with boundary is [[Paracompacteness|paracompact]], and by Smirnov's metrization theorem, we know that every topological manifold is metrizable. 

**Prop:** If $M$ is a compact manifold with boundary, then $D(M)$ is also compact.

**Embeddability of Compact Manifolds with Boundary:** Every compact manifold with boundary is homemorphic to a subset of some Euclidean space.