---
tags:
  - Topology
  - DifferentialGeometry
---
Subjects: [[Topology]], [[Differential Geometry]]
Links: [[Hausdorff Spaces]], [[Separable, First and Second Countable Spaces]], [[Continuous Functions and Homeomorphims]], [[Fundamental Group of a Topological Space]]

**Def:** A topological space $M$ is *locally Euclidean of dimension $n$* if every point $p$ in $M$ has a neighbourhood $U$ such that there is a homeomorphism $\phi$ from $U$ onto an open subset of $\Bbb R^n$. We call the pair $(U, \phi: U \to \Bbb R^n)$ a *chart*, $U$ a *coordinate neighbourhood* or a *coordinate open set*, and $\phi$ a *coordinate map* or a *coordinate system* on $U$. We say that a chart $(U, \phi)$is *centred* at $p \in U$ if $\phi(p) = 0$. 

**Def:** A *topological manifold* $M$ is a Hausdorff, second countable locally Euclidean space. It is said to be of *dimension* $n$ if it is locally Euclidean of dimension $n$.

A manifold is said to have dimension $n$ if all of its connected components have dimension $n$. A $1$-dimensional manifold is also called a *curve*, a $2$-dimensional manifold a *surface*, and an $n$-dimensional manifold an $n$-manifold

We haven't proved that the dimension is indeed well defined. For that, we would need to know that for $n \neq m$ an open subset of $\Bbb R^n$ is not homeomorphic to an open subset of $\Bbb R^m$. This fact, called the invariance of dimension, is indeed true, but not in the scope right now.

**Obs:** Suppose $(U, \phi: U \to \Bbb R^n)$ and $(V, \psi: V\to \Bbb R^n)$ are two charts of a topological manifold. since $U \cap V$ is open in $U$ and $\phi: U \to \Bbb R^n$ is a homeomorphism onto an open subset of $\Bbb R^n$, the image $\phi(U \cap V)$ will also be an open subset of $\Bbb R^n$. Similarly, $\psi(U \cap V)$ is an open subset of $\Bbb R^n$, and there is a homeomorphism between them, namely $\psi \circ \phi^{-1}$ or $\phi \circ \psi^{-1}$. 

**Def:** An *atlas* on a locally Euclidean space $M$ is a collection of charts $\mathfrak U = \{(U_\alpha, \varphi_\alpha) \mid \alpha < \kappa\}$ that [[Topological Covers|cover]] $M$, i.e. such that $M = \bigcup_{\alpha < \kappa} U_\alpha$. A *complete atlas* is maximal. 

**Lemma:** Every manifold $M$ has a countable basis all of whose elements have compact closure.

**Cor:** Every topological manifold is [[Locally compactness|locally compact]].

**Prop:** Let $M$ be a topological manifold:
- $M$ is locally path connected.
- $M$ is connected iff it is path connected.
- The componentes of $M$ are the same as its path connected.
- $M$ has at most countably many componentes, each of which is an open subset of $M$ and a connected topological manifold.

**Prop:** The fundamental group of any topological manifold is countable.

**Lemma:** Every manifold $M$ has a countable increasing sequence of subsets $\overline{V_n} \subseteq V_{n+1}$, with each $V_n$ open and $\overline{V_n}$ compact, such that $M = \bigcup_{n < \omega} V_n$. 

**Th:** A topological manifold is metrizable iff it is paracompact.

**Lemma:** Every topological manifold admits a countable, locally finite cover by precompact sets. 

# Manifolds with Boundary

Let us consider the closed $n$-dimensional *upper half-space* $\Bbb H^n \subseteq \Bbb R^n$, defined as $$\Bbb H^n := \{(x^1, \dots, x^n) \in \Bbb R^n \mid x^n \ge 0\}.$$We will use $\text{Int}(\Bbb H^n)$ and $\partial \Bbb H^n$ to denote the interior and boundary of $\Bbb H^n$, respectively, as a subset of $\Bbb R ^n$: $$\begin{align*}
\text{Int}(\Bbb H^n) &= \{(x^1, \dots, x^n) \in \Bbb R^n \mid x^n > 0\}, \\
\partial \Bbb H^n &= \{(x^1, \dots, x^n) \in \Bbb R^n \mid x^n = 0\}.
\end{align*}$$
**Def:** An $n$-dimension *topological manifold with boundary* is a second countable Hausdorff space $M$ in which every point has a neighbourhood homeomorphic to an open subset of $\Bbb H^n$. An open subset $U \subseteq M$ together with a homeomorphism $\varphi$ from $U$ to an open subset of $\Bbb H^n$ will be called a chart, just as in the case of manifolds. When it is necessary to make the distinction, we will call $(U, \varphi)$ an *interior chart* if $\varphi[U] \subseteq \text{Int}(\Bbb H^n)$, and *boundary chart* if $\varphi[U] \cap \partial \Bbb H^n \neq \varnothing$.

**Prop:** Let $M$ be a topological manifold with boundary:
- $M$ is locally path connected.
- $M$ has at most countably many componentes, each of which is an open subset of $M$ and a connected topological manifold.
- The fundamental group of $M$ is countable 
