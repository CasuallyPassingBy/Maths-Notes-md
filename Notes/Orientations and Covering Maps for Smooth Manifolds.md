---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Orientations of Smooth Manifolds]], [[Smooth Covering Maps]], [[Lie Group Actions]], [[Automorphism Group of a Covering Map]]

**Prop:** If $\pi: E \to M$ is a smooth covering map and $M$ is orientable then $E$ is also orientable.

**Def:** If $G$ is a Lie group smoothly on a smooth manifold $E$, we say that the action is an *orientation preserving action* if for each $g\in G$, the diffeomorphism $x\mapsto g\cdot x$ is orientation preserving. 

**Th:** Suppose $E$ is a connected, oriented, smooth manifold with or without boundary, and $\pi: E \to M$ is a smooth normal covering map. Then $M$ is orientable iff the action of $\text{Aut}_\pi(E)$ on $E$ is orientation-preserving. 

**Example:** For $n \ge 1$, consider the smooth covering map $q: \Bbb S^n\to \Bbb {RP}^n$. The only nontrivial covering automorphism of $q$ is the antipodal map $\alpha(x) :=-x$. We see that $\alpha$ is orientation-preserving iff $n$ is odd, so it follows that $\Bbb {RP}^n$ is orientable iff $n$ is odd. 

**Example:** Let $E$ be the total space of the Möbius bundle. The quotient map $q:\Bbb R^2 \to E$ used to define $E$ is a smooth normal covering map, and the covering automorphism group is isomorphic to $\Bbb Z$, acting on $\Bbb R^2$ by $n\cdot (x,y) := (x+n, (-1)^n y)$. For $n$ odd the diffeomorphism $(x, y)\mapsto n\cdot (x, y)$ of $\Bbb R^2$ pulls the orientation form $dx\wedge dy$ to $-dx\wedge dy$, so the action $\text{Aut}_\pi(E)$ is not orientation preserving. This implies that $E$ is not orientable.

For each $r>0$, the image under $q$ of the rectangle $[0, 1] \times [-r, r]$ is a Möbius band $M_r$. Because $q$ restricts to a smooth covering map from $\Bbb R\times[-r, r]$ to $M_r$, the same argument shows that a Möbius band is not orientable. 

## Orientation Covering

**Def:** If $N$ and $M$ are topological spaces, et us say that a map $\pi: N \to M$ is a *generalised covering map* if it satisfies all the requirements of a covering map except that $N$ might not be connected: this means that $N$ is locally path-connected, $\pi$ is surjective and continuous, and each point $p\in M$ has a neighbourhood that is evenly covered by $\pi$. If in addition $N$ and $M$ are smooth manifolds with or without boundary and $\pi$ is a local diffeomorphism, we say it is a *generalised smooth covering map*.

**Lemma:** Suppose $N$ and $M$ are topological spaces and $\pi: N \to M$ is a generalised covering map. If $M$ is connected, then the restriction of $\pi$ to each component fo $N$ is a covering map. 

**Def:** Let $M$ be a connected, smooth, positive-dimensional manifold with or without boundary, and let $\widehat M$ denote the set of orientations of all tangent spaces to $M$: $$\widehat M := \{(p, \mathcal O_p)\mid p\in M \text{ and }\mathcal O_p \text{ is orientation of }T_p M\}. $$We define the projection $\widehat \pi: \widehat M \to M$ by sending an orientation of $T_p M$ to each point $p$ to itself: $\widehat \pi(p, \mathcal O_p) := p$. Since each tangent space has exactly two orientations, each fiber of this map has cardinality $2$. The map $\widehat \pi: \widehat M \to M$ is called the *orientation covering of $M.$*

**Properties of the Orientation Covering:** Suppose $M$ is a connected, smooth, positive-dimensional manifold with or without boundary, and let $\widehat \pi: \widehat M \to M$ be its orientation covering. Then $\widehat M$ can be given the structure of a smooth, oriented manifold with or without boundary, with the following properties:
- $\widehat \pi: \widehat M \to M$ is a generalised smooth covering map.
- A connected open subset $U \subseteq M$ is evenly covered by $\widehat \pi$ iff $U$ is orientable.
- If $U\subseteq M$ is an evenly covered open subset, then every orientation of $U$ is the pullback orientation induced by a local section of $\widehat \pi$ over $U$. 

**Orientation Covering Theorem:** Suppose $M$ is a connected smooth manifold with or without boundary, and let $\widehat \pi: \widehat M \to M$ be a its orientation covering.
- If $M$ is orientable, then $\widehat M$ has exactly two components, and the restriction of each $\widehat\pi$ to each component is a diffeomorphism onto $M$.
- If $M$ is nonorientable, then $\widehat M$ is connected, and $\widehat\pi$ is a two-sheeted smooth covering map. 

The orientation covering is sometimes called the *oriented double covering of $M$*.

**Uniqueness of the Orientation Covering:** Let $M$ be a nonorientable connected smooth manifold with or without boundary, and let $\widehat\pi: \widehat M \to M$ be its orientation covering. If $\widetilde M$ is an oriented smooth manifold with or without boundary that admits a two-sheeted smooth covering map $\widetilde\pi: \widetilde M \to M$, then there exists a unique orientation-preserving diffeomorphism $\varphi: \widetilde M \to \widehat M$ such that $\widehat \pi \circ\varphi = \widetilde \pi$. 

**Th:** Let $M$ be a connected smooth manifold with or without boundary, and suppose the [[Fundamental Group of a Topological Space|fundamental group]] of $M$ has no subgroup of index $2$. Then $M$ is orientable. In particular, if $M$ is simply connected then it is orientable. 