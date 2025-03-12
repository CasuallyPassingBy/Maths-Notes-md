---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth or Differentiable Manifolds]], [[Immersions and Submersions of Manifolds]]

**Def:** A subset $S$ of a manifold $N$ of dimension $n$ is a *regular submanifold* of dimension $k$ if every $p \in S$ there is a coordinate neighbourhood $(U, \phi) = (U, x^1, \dots, x^n)$ of $p$ in the maximal atlas of $N$ such that $U \cap S$ is defined by vanishing of $n-k$ of the coordinate functions. By renumbering the coordinates, we may assume that these $n-k$ coordinates functions are $x^{k+1}, \dots, x^n$. 

We call a chart $(U, \phi)$ in $N$ an *adapted chart* relative to $S$. On $U \cap S$, $\phi = $(x^1, \dots, x^k, 0,\dots, 0)$. Let $$\phi_S : U \cap S \to \Bbb R^k$$be the restriction of the first $k$ componentes to $\phi$ to $U \cap S$, that is $\phi_S = (x^1, \dots, x^k)$. Note that $(U \cap S, \phi_S)$ is a chart for $S$ in the subspace topology. 

**Def:** If $S$ is a regular manifold of dimension $k$ in a manifold $N$ of dimension $N$, then $n-k$ is said to be the *codimension* of $S$ in $N$.

**Prop:** Let $S$ be a regular submanifold of $N$ and $\mathfrak U$ a collection of compatible charts that covers $S$. Then $\{U \cap S, \phi_S) \mid (U, \phi) \in \mathfrak U\}$. is an atlas for $S$. Therefore, a regular submanifold is itself a manifold. If $N$ has dimension $n$ and $K$ is locally defined by the vanishing of $n-k$ coordinates, then $\dim S = k$. 

# Levels Sets of a Function

**Def:** A *level set* of a map $F: N \to M$ is a subset $F^{-1}\{c\}$ for some $c\in M$. The value $c \in M$ is called the *level* of the level set $F^{-1}\{c\}$. If $F: N\to \Bbb R^n$, then $Z(F) := F^{-1}\{0\}$ is the *zero set* of $F$. The inverse image image $F^{-1}\{c\}$ of a regular value $c$ is called a *regular level set*. If the zero set $F^{-1}\{0\}$ is a regular set of $F:N \to \Bbb R^m$, it is called a *regular zero set*.

**Obs:** If regular level set $F^{-1}\{c\}$ is a nonempty, say $p\in F^{-1}\{c\}$, then the map $F: N\to M$ is a submersion at $p$. Then, $\dim N \ge \dim M$. 

**Lemma:** Let $g: N \to \Bbb R$ be a $\mathcal C^\infty$ function. A regular level set $g^{-1}\{c\}$ of the level $c$ of the function $g$ is the regular set $f^{-1}\{0\}$ of the function $f= g-c$. 

**Th:** Let $g: N \to \Bbb R$ be a $\mathcal C^\infty$ function on the manifold $N$. Then, a nonempty regular level set $S = g^{-1}\{c\}$ is a regular submanifold of $N$ of codimension $1$. 

# The Regular Level Set Theorem

**Th (Regular Level Set Theorem):** Let $F: N\to M$ be a smooth map of manifolds, with $\dim N = n$, and $\dim M = m$. Then a nonempty regular set $F^{-1}\{c\}$ where $c\in M$, is a regular submanifold of $N$ of dimension equal $n-m$. 

**Lemma:** Let $F: N \to \Bbb R^m$ be a $\mathcal C^\infty$ map on a manifold $N$ of dimension $n$ and let $S$ be the level set $F^{-1}\{0\}$. If relative to some coordinate chart $(U, x^1, \dots, x^n)$ about $p\in S$, the Jacobian determinant $\dfrac{\partial (F^1, \dots, F^m)}{\partial(x^{j_1}, \dots, x^{j_m})}(p)$ is nonzero, then in some neighbourhood of $p$ one may replace $x^{j_1}, \dots, x^{j_m}$ by $F^1, \dots, F^m$ to obtain an adapted chart for $N$ relative to $S$. 

# Transversality Theorem

**Def:** A $\mathcal C^\infty$ map $f: N \to M$ is said to be *transversal* to a regular submanifold $S \subseteq M$, if for every $p\in f^{-1}[S]$, $$df_p[T_p N] + T_{f(p)} S = T_{f(p)} M.$$
**Th:** A $\mathcal C^\infty$ map $f: N \to M$ is transversal to a regular submanifold $S$ of codimension $k$ in $M$, then $f^{-1}[S]$ is regular submanifold of codimension $k$ in $N$. 

When $S$ consists of a single point $c$, transversality of $f$ to $S$ simply means that $f^{-1}\{c\}$ is a regular level set. Thus the transversality theorem is a generalisation of the regular level set theorem. It is specially useful in giving conditions under which the intersection of two submanifolds is a submanifold. 