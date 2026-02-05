---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]], [[Smooth Functions on Smooth Manifolds]], [[Submersions, Immersions and Local Diffeomorphism of Smooth Manifolds]]

**Def:** Let $M$ be a smooth manifold. An *immersed submanifold of dimension $k$*, or *immersed $k$-submanifold* of $M$ is a subset $S \subseteq M$ endowed with a $k$-manifold topology together with a smooth structure such that the inclusion map $\iota:S \to M$ is a smooth immersion. As for embedded submanifolds, we define the *codimension of $S$ in $M$* to be $\dim M - \dim S$.

We see that every embedded submanifold is an immersed submanifold, but the converse is not necessarily true. We adopt the convention that the term *smooth submanifold* without further qualification means an immersed one. Similarly, the term *smooth hypersurface* without qualification means an immersed submanifold of codimension $1$. 

Immersed submanifolds arise in a fairly natural way. Let $F: N \to M$ be an injective immersion, we can give the set image $F[N]$ a unique manifold topology and smooth structure such that $F:N \to F[N]$ is a diffeomorphism. We define that a set $U \subseteq F[N]$ is open iff $F^{-1}[U] \subseteq N$ is open, and take the smooth coordinates maps on $F[N]$ to be the maps of the form $\phi \circ F^{-1}$, where $\phi$ is a smooth coordinate map for $N$. Lastly, the map $\iota: F[N] \to M$ is an injective immersion, 

There are also various notions of submanifold in the topological category. If $M$ is a topological manifold, one could define an *immersed topological manifold $M$* to be a subset $S\subseteq M$ endowed with a topology such that it is a topological manifold and such that the inclusion is a topological immersion. It is an *embedded topological submanifold* if the inclusion is a topological embedding. 

**Prop:** Suppose $M$ is a smooth manifold with or without boundary, $N$ is a smooth manifold, and $F: N \to M$ is an injective smooth immersion. If $S = F[N]$, then $S$ has a unique topology and smooth structure such that it is a smooth manifold of $M$ and such that $F:N \to M$ is a diffeomorphism into its image. 

**Prop:** Suppose $M$ is a smooth manifold with or without boundary, and $S\subseteq M$ is an immersed submanifold. If any of the following gold, then $S$ is embedded.
* $S$ has codimension $0$ in $M$.
* The inclusion map $S\subseteq M$ is proper.
* $S$ is compact.

**Prop:** If $M$ is a smooth manifold with or without boundary, and $S\subseteq M$ is an immersed submanifold, then for each $p\in S$ there exists a neighbourhood $U$ of $p$ in $S$ that is an immersed submanifold of $M$. 

**Prop:** Immersed submanifolds are precisely the images of injective immersions. 

**Def:** If $S \subseteq M$ is an immersed $k$-submanifold. A *local parametrisation of $S$* is a continuous map $X: U \to M$ whose domain is an open subset $U\subseteq \Bbb R^k$, whose image is an open subset of $S$, and which, considered as a map into $S$, is a homeomorphism onto its image. If the image of $X$ is all of $S$, it is called a *global parametrisation*. 

**Prop:** Suppose $M$ is a smooth manifold with or without boundary, $S\subseteq M$ is an immersed $k$-dimensional submanifold, $\iota: S \hookrightarrow M$ is the inclusion map, and $U$ is an open subset of $\Bbb R^k$. A map $X: U \to M$ is a smooth local parametrisation of $S$ iff there is a smooth coordinate chart $(V,\varphi)$ for $S$ such that $X = \iota \circ\varphi ^{-1}$. Therefore, every point of $S$ is the image of some local paramatrisation. 

**Th:** Suppose $M$ is a smooth manifold and $S\subseteq M$ is an immersed submanifold. For the given topology on $S$, there is only one smooth structure making $S$ into an immersed submanifold. 

**Th:** Suppose $M$ is a smooth manifold and $S\subseteq M$ is a [[Smooth Maps on and Between Submanifolds#^089be9|weakly embedded]] submanifold. For the given topology on $S$, there is only one smooth structure making $S$ into a weakly embedded submanifold. 