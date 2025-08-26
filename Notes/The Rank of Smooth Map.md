---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Submanifolds]], [[Smooth Functions on Smooth Manifolds]], [[Submersions, Immersions and Embeddings of Manifolds]]

**Constant rank theorem:** Let $N$ and $M$ be manifolds of dimension $n$ and $m$ respectively. Suppose $f: N \to M$ has constant rank $k$ in a neighbourhood of a point $p \in N$. Then there are charts $(U, \phi)$ centred at $p\in N$ and $(V, \psi)$ centred at $f(p)$ in $M$ such that for $(r^1, \dots, r^n)$ in $\phi[U]$. $$(\psi \circ f \circ \phi^{-1})(r^1, \dots, r^n) = (r^1, \dots, r^k, 0, \dots, 0)$$
**Constant-rank level set theorem**: Let $f: N\to M$ be a smooth map of manifolds and $c\in M$. If $f$ has constant rank $k$ in a neighbourhood of the level set $f^{-1}\{c\}$ in $N$, then $f^{-1}\{c\}$ is a regular submanifold of $N$ of codimension $k$. ^54458e

Let $f: N \to M$ be a smooth map between manifolds of manifolds of dimension $n$ and $m$ respectively. We have the following:
- $df_p$ is injective iff $n  \ge m$  and $\text{rank} (df_p) = n$
- $df_p$ is surjective iff $n \le m$ and $\text{rank} (df_p) = m$

We have that being an immersion or submersion at $p$ is equivalent to the maximality of $\text{rank}(df_p)$. 

Having maximal rank at a point is an *open condition* in the sense that the set $$D_\max(f) := \{p\in U \mid df_p \text{ has maximal rank at } p\}$$is an open subset of $U$. This has a similar reason as why $\text{GL}(n, \Bbb R)$ is an open subset of $\Bbb R^{n\times n}$. 

**Prop:** Let $N$ and $M$ be manifolds of dimensions $n$ and $m$ respectively. If a $\mathcal C^\infty$ map $f: N \to M$ is an immersion at a point $p\in N$, then it has a constant rank $n$ in a neighbourhood of $p$. If a $\mathcal C^\infty$ map $f: N \to M$ is a submersion at a point $p\in N$, then it has constant rank $m$ in a neighbourhood of $p$.

**Theorems:** Let $N$ and $M$ be manifolds of dimensions $n$ and $m$ respectively.
- **Immersion Theorem:** Suppose $f: N \to M$ is an immersion at $p \in N$. Then there are charts $(U, \phi)$ centred at $p$ in $N$ and $(V, \psi)$ centred at $f(p)$ in $M$ such that in the neighbourhood of $\phi(p)$, $$(\psi \circ f \circ \phi^{-1})(r^1, \dots, r^n) = (r^1, \dots, r^k, 0, \dots, 0)$$
- **Submersion Theorem**: Suppose $f: N \to M$ is an submersion at $p \in N$. Then there are charts $(U, \phi)$ centred at $p$ in $N$ and $(V, \psi)$ centred at $f(p)$ in $M$ such that in the neighbourhood of $\phi(p)$, $$(\psi \circ f \circ \phi^{-1})(r^1, \dots, r^m, r^{m+1},\dots, r^n) = (r^1, \dots, r^m)$$
**Cor:** A submersion $f: N \to M$ of manifolds is an open map

# Images of Smooth Maps

It is in general not true that, if $f:N \to M$ a smooth function between manifolds, then $f[N]$ is a manifold. We can't even consider for the manifold to be smooth. 

**Def:** A $\mathcal C^\infty$ map $f: N \to M$ is called an *smooth embedding* if
- it is an immersion
- It is a [[Topological subspaces#^22f29a|topological embedding]]
We call $f[N]$ to be an *embedded manifold*. 

**Th:** If $f: N\to M$ is an embedding, then its image $f[N]$ is a regular submanifold of $M$.

**Th:** If $N$ is a regular submanifold of $M$, then the inclusion $i: N \to M$, $i(p) = p$, is an embedding.

From these theorems, we see that an embedded manifold is the same as a regular submanifold.

**Th:** Suppose $f: N \to M$ is smooth and $f[N] \subseteq S \subseteq M$. If $S$ is a regular submanifold of $M$, then the induced map $\tilde f: N \to S$ is smooth.