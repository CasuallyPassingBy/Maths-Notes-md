---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Sets of Measure Zero in Smooth Manifolds and Sard's Theorem]], [[The Whitney Embedding Theorem]], [[Homotopy]]

**Def:** If $\delta: M \to\Bbb R$ is a positive continuous function, we say that two functions $F, G: M \to \Bbb R^k$ are *$\delta$-close* if $\|F(x)- G(x)\| <\delta (x)$ for all $x\in M$. This notion of $\delta$-close reminds to have a $\delta$-fine partition for the [[Henstock–Kurzweil Integral]].

**Whitney Approximation Theorem:** Let $M$ be a smooth manifold and let $F: M \to \Bbb R^k$ be a continuous function. Given any positive continuous function $\delta: M \to \Bbb R$, there exists a smooth function $\tilde F: M \to \Bbb R ^k$ that is $\delta$-close to $F$. If $F$ is smooth on a closed subset $A\subseteq M$, then $\tilde F$ can be chosen to be equal to $F$ on $A$.

**Cor:** If $M$ is a smooth manifold with or without boundary and $\delta: M \to \Bbb R$ is a positive continuous function then there is a smooth function $e:M \to \Bbb R$ such that $0<e(x) <\delta(x)$ for all $x\in M$. 

If we let $(M, g)$ be a [[Riemannian Metrics on Smooth Manifolds|Riemannian manifold]], we can extend this theorems to work for vector fields.

**Def:** If $\delta: M \to \Bbb R$ is a positive continuous function, we say that two vector fields $X, Y: M \to TM$, in the Riemannian manifold $(M, g)$, if $\|X_p-Y_p\|_g < \delta(p)$ for all $p\in M.$

**Th:** Let $(M, g)$ be a Riemannian manifold and let $X: M \to TM$ be a continuous vector field. Given any positive continuous function $\delta: M \to \Bbb R$, there exists a smooth vector field $Y: M \to TM$ such that is $\delta$-close to $X$. If $X$ is smooth on a closed subset $A\subseteq M$, then $Y$ can be chosen to be equal to $F$ on $A$. 

**Cor:** Let $M$ be a smooth manifold. 
- If there exists a global non-vanishing vector field on $M$, then there exists a global *smooth* non-vanishing vector field. 
- If there exist $k$ independent vector fields on $M$, then there exists $k$ independent *smooth* vector fields.

This corollary also depends on the fact that for every smooth manifold $M$, there exists a Riemannian metric. 

## Tubular Neighbourhoods

**Def:** Let $M\subseteq \Bbb R^n$ be an embedded $m$-dimensional submanifold. At any $x\in M,$ out usual identifications allow us to view the tangent space $T_xM$ as a subspace of $T_x \Bbb R^n$, which inherits the Euclidean dot product courtesy of its canonical identification with $\Bbb R^n$. We define the *normal space* to $M$ at $x$ to be subspace $N_x M \subseteq T_x\Bbb R^n$ consisting of all vectors that are orthogonal to $T_x M$ with respect to the Euclidean dot product. The *normal bundle* of $M$ is the subset $NM \subseteq T\Bbb R^n$ defined by $$NM := \coprod_{x\in M}N_x M := \{(x, v) \in T\Bbb R^n\mid x\in M, v\in N_x M\}. $$There is a natural projection $\pi_{NM}: NM \to M$ defined as the restriction to $NM$ of $\pi: T\Bbb R^n \to \Bbb R^n$, and each fiber $N_xM$ is vector space of dimension $n-m$. 

**Def:** A local frame $(E_1, \dots, E_n)$ for $\Bbb R^n$ on an open set $U\subseteq \Bbb R^n$ is said to be *orthonormal* if the vectors $(E_1|_x, \dots, E_n|_x)$ are orthonormal at each $x\in U$. It is said to be *adapted to $M$* if the first $n$ vectors $(E_1|_x,\dots, E_m|_x)$ span $T_x M$ at each $x\in U \cap M$. 

**Lemma (Existence of Adapted Orthonormal Frames)** Let $M \subseteq \Bbb R^n$ be a an embedded submanifold. For each $p\in M$, there is a smooth adapted orthonormal frame on a neighbourhood $U$ of $p$ in $\Bbb R^n$

**Prop:** For any embedded $m$-dimensional submanifold $M\subseteq \Bbb R^n$, the normal bundle $NM \subseteq T\Bbb R^n$ is a smooth vector bundle of rank $n-m$ over $M$ and an embedded submanifold of $T\Bbb R^n$. 

**Def:** Define a map $E: NM \to \Bbb R^n$ by $$E(x,v) = x+v,$$where we regard a vector $v\in N_x M \subseteq T_x\Bbb R^n$ as an element of $\Bbb R^n$ by means of the usual identification. This just maps each normal space $N_xM$ affinely onto the [[Affine Spaces#Subspaces|affine subspace]] through $x$ orthogonal to $T_x M$. We see that $E$ is smooth.

A *tubular neighbourhood of $M$* is a neighbourhood $U$ of $M$ in $\Bbb R^n$ that is the diffeomorphic image under $E$ of an open subset $V\subseteq NM$ of the form $$V = \{(x, v)\in NM \mid \|v\| <\delta(x)\},$$for some positive continuous function $\delta: M \to \Bbb R$ 

**Tubular Neighbourhood Theorem:** Every embedded submanifold of $\Bbb R^n$ has a tubular neighbourhood. 

**Prop:** Let $M\subseteq \Bbb R^n$ be an embedded submanifold. If $U$ is any tubular neighbourhood of $M$, there exists a unique [[Topological Subspaces#^c8b9b2|retraction]] of $U$ onto $M$

## Smooth Approximation of Maps Between Manifolds

**Whitney Approximation on Manifolds:** Suppose $N$ is a smooth manifold with or without boundary, $M$ is a smooth manifold without boundary, and $F: N \to M$ is a continuos map. Then $F$ is homotopic to a smooth map. If $F$ is already smooth on a closed subset $A\subseteq N$, then the homotopy can be taken to be relative to $A$.

**Extension Lemma for Smooth Manifolds:** Suppose $N$ is a smooth manifold with or without boundary, $M$ is a smooth manifold, $A\subseteq N$ is a closed subset, and $f: A \to M$ is a smooth map. Then $f$ has a smooth extension fo $N$ iff it has a continuous extension to $N$. 

**Def:** If $M$ and $N$ are smooth manifolds with or without boundary, a homotopy $H: N \times I \to M$ is called a *smooth homotopy* if it is also a smooth map, in the sense that it extends to a smooth map on some neighbourhood of $N \times I$ in $N\times \Bbb R$. Two maps are said to be *smoothly homotopic* if there is a smooth homotopy between them. 

**Lemma:** If $N$ and $M$ are smooth manifolds with or without boundary, smooth homotopy is an equivalence relation on the set of all smooth functions from $N$ to $M$.

**Th:** Suppose $N$ is a smooth manifold or without boundary, $M$ is a smooth manifold and $F, G:N \to M$ are smooth maps. If $F$ and $G$ are homotopic then they are smoothly homotopic. If $F$ and $G$ are homotopic relative to some closed subset $A\subseteq N$, then they are smoothly homotopic relative to $A$. 

**Cor:** Any two points in a connected manifold can be joined by a smooth curve segment. 