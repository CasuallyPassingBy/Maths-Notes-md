---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Sets of Measure Zero in Smooth Manifolds]], [[The Whitney Embedding Theorem]], [[Fundamental Group of a Topological Space]]

**Def:** If $\delta: M \to\Bbb R$ is a positive continuous function, we say that two functions $F, G: M \to \Bbb R^k$ are *$\delta$-close* if $\|F(x)- G(x)\| <\delta (x)$ for all $x\in M$. This notion of $\delta$-close reminds to have a $\delta$-fine partition for the [[Henstock–Kurzweil Integral]].

**Whitney Approximation Theorem:** Let $M$ be a smooth manifold and let $F: M \to \Bbb R^k$ be a continuous function. Given any positive continuous function $\delta: M \to \Bbb R$, there exists a smooth function $\tilde F: M \to \Bbb R ^k$ that is $\delta$-close to $F$. If $F$ is smooth on a closed subset $A\subseteq M$, then $\tilde F$ can be chosen to be equal to $F$ on $A$.

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

**Whitney Approximation on Manifolds:** Let $N$ and $M$ be smooth manifolds, and let $F:N \to M$ be a continuous map. Then $F$ is homotopic to a smooth map $\tilde F: N \to M$. If $F$ is smooth on a closed subset $A\subseteq N$, then the homotopy can be taken relative to $A$. 

**Def:** If $M$ and $N$ are smooth manifolds, two smooth maps $F, G: M \to N$ are said to be *smoothly homotopic* if there is a smooth map $H:M \times [0, 1] \to N$ that is a homotopy between $F$ and $G$. 

**Prop:** If $F, G: M \to N$ are homotopic smooth maps, then they are smoothly homotopic. If $F$ is homotopic to $G$ relative some closed subset $A\subseteq M$, then they are smoothly homotopic relative to $A$. 

**Cor:** Any two points in a connected manifold can be joined by a smooth curve segment. 