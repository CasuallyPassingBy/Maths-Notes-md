---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Simplicial Complexes]]

Simplicial complexes were invented in the hope that they would enable topological questions about manifolds to be reduced to combinatorial questions simplicial complexes.

**Def:** We define an *abstract simplicial complex* to be a collection $\cal K$ of finite sets, subject to only one condition, to be [[Outer Measures#^292706|hereditary]]. 

If $\cal K$ is an abstract simplicial complex, the finite sets that make up $\cal K$ are called *abstract simplices*. Given an abstract simplex $s\in \cal K$, any element of $s$ is called a *vertex of $s$*, and any subset of $s$ is called a *face of $s$*. We say $\cal K$ is a *finite complex* if $\cal K$ itself it finite, and *locally finite complex* if every vertex belongs to only finitely many abstract simplices. The *dimension of an abstract simplex* $s\in \cal K$ is one less than the number of elements of $s$. If the dimensions of the abstract simplices of $\cal K$ are bounded above, them we say $\cal K$ is *finite dimensional*, and its *dimension* is the smallest upper bound of the dimensions of its simplices.

Now suppose that $\cal K$ and $\cal L$ are abstract complexes. Define their *vertex sets* by $${\cal K}_0 := \bigcup_{s\in \cal K}, \quad {\cal L}_0 := \bigcup_{s\in \cal L} s.$$
A map $f: \cal K \to L$ is called an *abstract simplicial map* if it is of the form $f[\{v_0,\dots, v_k\}] = \{f_0(v_0),\dots, f_0(v_k)\}$ for some map $f_0: \cal K_0 \to L_0$, called the *vertex map of $f$*, that satisfies $f[s] \in \cal L$ for every $s\in\cal K$. An abstract simplicial map $f$ is called an *isomorphism* if both $f_0$ and $f$ are bijections. In this case $f^{-1}$ is also a simplicial map.

Given a Euclidean simplicial complex $K$, let $\cal K$ denote the collection of those finite sets $\{v_0, \dots, v_k\}$ that consist of the vertices of some simplex $K$. It is immediate that $\cal K$ is an abstract simplicial complex called the *vertex schema of $K$*. 

**Obs:** Two Euclidean complexes are simplicially isomorphic iff their vertex schema are isomorphic. 

**Def:** If $K$ is a Euclidean simplicial complex vertex schema is isomorphic to $\cal K$, we say that $K$ is the *geometric realisation of $\cal K$*.  

**Prop:** Every finite abstract simplicial complex has a geometric realisation. 

**Th:** An abstract simplicial complex is the vertex schema of a Euclidean simplicial complex iff it is finite-dimensional, locally finite, and countable.

**Def:** Two simplicial complexes are said to be *combinatorially equivalent* if they have a common subdivision. 

It was conjectured that if two simplicial complexes have homeomorphic polyhedra, they are combinatorially equivalent; this conjecture became known as the *Hauptvermutung* of combinatorial topology. We know that it is true for all complexes of dimension $2$ and for triangulated compact manifolds of dimension $3$, buy false in all higher dimensions, even for compact manifolds. 

We can define certain how get subcomplexes. Let $\cal K$ be a simplicial complex.
- Let $\cal K'\subseteq K$, its *closure* is $\text{cl}({\cal K'}) := \{\tau \in {\cal K} \mid \tau \subseteq \sigma \in {\cal K'}\}$.
- The *star* of a simplex $\tau\in \cal K$ is $\text{st}(\tau) := {\sigma\in {\cal K}\mid \tau \subseteq \sigma}\}$.
- The *link* of a simplex $\tau \in \cal K$ is $$\text{lk}(\tau) := \{\sigma \in \text{cl}(\text{st}(\tau)) \mid \tau \cap \sigma = \varnothing\}.$$