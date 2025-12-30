---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Functions on Smooth Manifolds]], [[Differentiability of Vector valued functions of Rn]], [[Proper Maps]], [[Continuous Functions and Homeomorphims]], [[Topological Subspaces]]

**Def:** A $\mathcal C^\infty$ $F: N \to M$ is said to be an *immersion* at $p\in N$ if its differential $dF_p: T_pN \to T_{F(p)} M$ is injective, and a *submersion* at $p$ if $dF_p$ is surjective. We call $F$ an *immersion* if it is an immersion at every $p\in N$ and a *submersion* if it is a submersion at every $p\in N$. Note that both immersion and submersions are full rank.

**Prop:** Suppose $F: M \to N$ is a smooth map and $p\in M$. If $dF_p$ is surjective, then $p$ has a neighbourhood $U$ such that $F|_U$ is a submersion. If $dF_p$ is injective, then $p$ has a neighbourhood $U$ such that $F|_U$ is an immersion. 

**Def:** If $M$ and $N$ are smooth manifolds with or without boundary, a map $F: M \to N$ is called a *local diffeomorphism* if every point $p\in M$ has a neighbourhood $U$ such that $F[U]$ is open in $N$ and $F|_U: U \to F[U]$ is a diffeomorphism. 

**Inverse Function Theorem for Manifolds:** Suppose $M$ and $N$ are smooth manifolds, and $F:M \to N$ is a smooth map. If $p\in M$ is a point such that $dF_p$ is invertible, then there are connected neighbourhoods $U_0$ of $p$ and $V_0$ of $F(p)$ such that $F|_{U_0}: U_0 \to V_0$ is a diffeomorphism,.

**Elementary Properties of Local Diffeomorphisms:**
- Every composition of local diffeomorphisms is a local diffeomorphism.
- Every finite product of local diffeomorphisms between smooth manifolds is a local diffeomorphism.
- Every local diffeomorphism is a local homeomorphism and an open map.
- The restriction of a local diffeomorphism to an open submanifold with or without boundary is a local diffeomorphism.
- Every diffeomorphism is a local diffeomorphism.
- Every bijective local diffeomorphism is a diffeomorphism.
- A map between smooth manifolds with or without boundary is a local diffeomorphism iff in a neighbourhood of each point of its domain, it has coordinate representation that is a local diffeomorphism. 

**Prop:** Suppose $M$ and $N$ are smooth manifolds with or without boundary, and $F: M\to N$ is a map.
- $F$ is a local diffeomorphism iff it is both an immersion and a smooth submersion.
- If $\dim M = \dim N$ and $F$ is either a smooth immersion or a smooth submersion, then it is a local diffeomorphism.

**Prop:** Suppose $M, N$ and $P$ are smooth manifolds with or without boundary, and $F: M \to N$ is a local diffeomorphism.
- If $G: P \to M$ is continuous, then $G$ is smooth iff $F\circ G$ is smooth.
- If $F$ is surjective, and $G: N \to P$ is any map, then $G$ is smooth iff $G\circ F$ is smooth.

**Examples:**
- If $M_1, \dots, M_k$ are smooth manifolds, each of the projections $\pi_i: M_1 \times \dots\times M_k \to M_i$ is a submersion.
- Alternatively, with $M_1, \dots, M_k$ as above it $p_i \in M_i$ are arbitrarily choses points, each of the inclusion maps $\iota_j : M_j \to M_1 \times \dots \times M_k$ given by $$\iota_j(q) = (p_1,\dots, p_{j-1}, q, p_{j+1}, \dots, p_k)$$is a smooth embedding.
- If $\gamma: J \to M$ is a smooth curve in a smooth manifold $M$, then $\gamma$ is an immersion iff $\gamma'(t) \neq 0$ for all $t\in J$. 
- If $F: M \to N$ is a local diffeomorphism, then $F$ is both an immersion and submersion.
- If $\pi:E \to M$ is a smooth vector bundle over a smooth manifold $M$, the projection map $\pi$ is a submersion.

**Prop:** Let $F: M \to N$ and $G: N \to L$. If both $F$ and $G$ are submersions, then $G \circ F$ is a submersion. Similarly, if both $F$ and $G$ are both immersions, then $G\circ F$ is an immersion. 

**Cor:** Let $M$ and $N$ be smooth manifolds, let $F: M \to N$ be a smooth map, and suppose $M$ is connected. Then the following are equivalent: ^815841
- For each $p\in M$ there exist smooth charts near $p$ and $F(p)$ in which the coordinate representation of $F$ is linear.
- $F$ has constant rank.

**Global Rank Theorem:** Let $F: M \to N$ be a smooth map of constant rank.
- If $F$ is surjective, then it is a submersion.
- If $F$ is injective, then it is an immersion.
- If $F$ is bijective, then it is a diffeomorphism.

**Local Immersion Theorem for Manifold with Boundary:** Suppose $M$ is a smooth $m$-manifold with boundary, $N$ is a smooth $n$-manifold, and $F: M \to N$ is a smooth immersion. For any $p\in \partial M$, there exists a smooth boundary chart $(U, \varphi)$ for $M$ centred at $p$ and a smooth coordinate chart $(V,\psi)$ for $N$ centred at $F(p)$ with $F[U] \subseteq V$, in which $F$ has coordinate representation $$\widehat F(x^1,\dots, x^m) = (x^1,\dots, x^m, 0,\dots 0) $$

**Prop:** Suppose $M$ is a smooth manifold, $p \in M$ and $y^1, \dots, y^n$ are smooth real-valued functions defined on a neighbourhood $p$ of $M$.
- If $dy^1|_p, \dots, dy^n|_p$ form a basis for $T^*_pM$, then $(y^1, \dots, y^n)$ are smooth coordinates for $M$ in some neighbourhood.
- If $dy^1|_p, \dots, dy^n|_p$ are independent, then are real valued functions $y^{n+1}, \dots, y^m$ such that $(y^1, \dots, y^m)$ are smooth coordinates for $M$ in some neighbourhood of $p$.
- If $dy^1|_p, \dots, dy^n|_p$ span $T_p^*M$, then there are indices $i_1, \dots, i_k$ such that $(y^{i_1}, \dots, y^{i_k})$ are smooth coordinates for $M$ in some neighbourhood of $p$.

**Def:** If $X$ and $Y$ are topological spaces, a continuous map $F: X \to Y$ is called a *topological immersion* if every point of $X$ has a neighbourhood $U$ such that $F|_U$ is a topological embedding. Thus, every smooth immersion is a topological immersion. 

# Submersions

**Def:** If $\pi: M \to N$ is a smooth map, a *section of $\pi$* is a continuous right inverse for $\pi$, i.e., a continuous map $\sigma: N\to M$ such that $\pi \circ \sigma = \text{Id}_N$. A *local section of $\pi$* is a continuous map $\sigma: U \to M$ defined on some open subset $U\subseteq N$ and satisfying $\pi\circ \sigma = \text{Id}_U$. This is just the analogous definition for [[covering maps]] . 

**Local Section Theorem:** Suppose $M$ and $N$ are smooth manifolds and $\pi:M \to N$ is a smooth map. Then $\pi$ is a smooth submersion iff every point of $M$ is in the image of a smooth local section of $\pi$. 

This theorem motivates a generalisation for submersion.

**Def:** If $\pi: X \to Y$ is a continuous map, we say that $\pi$ is a *topological submersion*if every point of $X$ is in the image of a continuous local section of $\pi$. 

**Prop:** Let $M$ and $N$ be smooth manifolds, and suppose $\pi$ is a smooth submersion. Then $\pi$ is an open map, and it it is surjective it is a quotient map. 

**Cor:** Let $M$ be a compact smooth manifold. Then there cannot be a submersion $F: M \to \Bbb R^n$ for any $n > 0$. 

**Cor:** Suppose $\pi: M \to N$ is a smooth map such that every point of $M$ is in the image of a smooth local section of $\pi$, then $\pi$ is a submersion.

**Lemma:** Suppose $V\subseteq \text{Int}(\Bbb H^n)$ is open and $f: V \to f[V] \subseteq \Bbb H^n$ is a diffeomorphism onto its image. Then $f[V] \cap \partial \Bbb H^n = \varnothing$.

**Cor:** Let $M$ be smooth manifold with boundary, then the set of interior points and boundary points are disjoint, i.e., $\text{Int}(\Bbb H^n) \cap \partial \Bbb H^n = \varnothing$. 

**Characteristic Property of Surjective Smooth Submersions:** Suppose $M$ and $N$ are smooth  manifolds, and $\pi:  M \to N$ is a surjective smooth submersion. For any smooth manifold $P$ with or without boundary, a map $F: N \to P$ is smooth iff $F \circ \pi$ is smooth: 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]    
M \arrow[d,two heads, "\pi"'] \arrow[dr, "F\circ \pi"] \\ N \arrow[r, "F"'] & P.
\end{tikzcd}
\end{document}
```

**Passing Smoothly to the Quotient:** Suppose $M$ and $N$ are smooth manifold and $\pi: M \to N$ is a surjective smooth submersion. If $P$ is a smooth manifold with or without boundary and $F: M \to P$ is a smooth map that is constant on the fibres of $\pi$, then there exists a unique smooth map $\tilde F: N \to P$ such that $\tilde F \circ \pi = F$ . 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]     
M \arrow[d,two heads, "\pi"'] \arrow[dr, "F"] \\ N \arrow[r, "\widetilde F"] & P.
\end{tikzcd}
\end{document}
```

**Uniqueness of Smooth Quotients:** Suppose $M$, $N_1$ and $N_2$ are smooth manifolds, and $\pi_1: M \to N_1$ and $\pi_2: M \to N_2$ are surjecitve smooth submersions that are constant on each other's fibres. Then there exists a unique diffeomorphism $F: N_1 \to N_2$ such that $F \circ \pi_1 = \pi_2$.  ^a3a253
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]     
& M \arrow[dl,two heads, "\pi_1"'] \arrow[dr,two heads, "\pi_2"] \\ 
N \arrow[rr, "F"] & & P.
\end{tikzcd}
\end{document}
```


