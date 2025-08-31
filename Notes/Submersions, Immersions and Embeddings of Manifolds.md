---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Functions on Smooth Manifolds]], [[Differentiability of Vector valued functions of Rn]], [[Proper Maps]], [[Continuous Functions and Homeomorphims]], [[Topological Subspaces]]

**Def:** We consider a smooth map $F: N\to M$ of manifolds. Its *rank* at a point $p$ is $N$, denoted as $\text{rank } F(p)$, is defined as the rank of the differential $dF_p : T_p N \to T_{F(p)} M$. Relative to the coordinate neighbourhoods $(U, x^1, \dots, x^n)$ and $(V, y^1, \dots, y^m)$ at $F(p)$, the differential is represented by the Jacobian matrix $\left[\dfrac{\partial F^i}{\partial x^j}(p)\right]$, so $$\text{rank } F(p) = \text{rank } \left[\dfrac{\partial F^i}{\partial x^j}(p)\right]$$
If $F$ has the same rank $k$ at every point, we say that it has *constant* rank and write $\text{rank } F = k$.

**Def:** A $\mathcal C^\infty$ $F: N \to M$ is said to be an *immersion* at $p\in N$ if its differential $dF_p: T_pN \to T_{F(p)} M$ is injective, and a *submersion* at $p$ if $dF_p$ is surjective. We call $F$ an *immersion* if it is an immersion at every $p\in N$ and a *submersion* if it is a submersion at every $p\in N$. 

**Obs:** Suppose  and $M$ are manifolds of dimension $n$ and $m$ respectively. then $\dim T_p N = n$ and $\dim T_{F(p)} M = m$. The injectivity of the differential $dF_p$  implies that $n \le m$. Similarly, the surjectivity of the differential $dF_p$ implies that $n \ge m$. Meaning, if $F: N \to M$ is a an immersion at a point or , then $n \le m$ and if  is a submersion at a point of , then $n \ge m$. Thus immersions and submersion are special maps of constant rank.

**Def:** One special kind of immersion is particularly important. A *smooth embedding* is an immersion $F: M \to N$ that is also a topological embedding, i.e., a homeomorphism onto its image $F[M]$ in the subspace topology. Thus, we have two types of embeddings topological and smooth. 

**Examples:**
- If $M_1, \dots, M_k$ are smooth manifolds, each of the projections $\pi_i: M_1 \times \dots\times M_k \to M_i$ is a submersion.
- Alternatively, with $M_1, \dots, M_k$ as above it $p_i \in M_i$ are arbitrarily choses points, each of the inclusion maps $\iota_j : M_j \to M_1 \times \dots \times M_k$ given by $$\iota_j(q) = (p_1,\dots, p_{j-1}, q, p_{j+1}, \dots, p_k)$$is a smooth embedding.
- If $\gamma: J \to M$ is a smooth curve in a smooth manifold $M$, then $\gamma$ is an immersion iff $\gamma'(t) \neq 0$ for all $t\in J$. 
- If $F: M \to N$ is a local diffeomorphism, then $F$ is both an immersion and submersion.
- If $\pi:E \to M$ is a smooth vector bundle over a smooth manifold $M$, the projection map $\pi$ is a submersion.

**Prop:** Let $F: M \to N$ and $G: N \to L$. If both $F$ and $G$ are submersions, then $G \circ F$ is a submersion. Similarly, if both $F$ and $G$ are both immersions, then $G\circ F$ is an immersion. 

Just to emphasise, but $\text{embedding} \implies \text{immersion}$, but we can find examples of immersed manifolds that are not embedded manifolds.

**Prop:** Suppose $F: M \to N$ is an injective immersion. If either of the following conditions holds, then $F$ is a smooth embedding with closed image:
- $M$ is compact.
- $F$ is a proper map. 

# Constant-Rank Maps Between Manifolds

**Inverse Function Theorem for Manifolds:** Suppose $M$ and $N$ are smooth manifolds, $p\in M$, and $F: M \to N$ is a smooth map such that $F_*: T_p M \to T_{F(p)}N$ is bijective. Then there exist connected neighbourhoods $U_0$ of $p$ and $V_0$ of $F(p)$ such that $F|_{U_0}: U_0 \to V_0$ is a diffeomorphism.

**Cor:** Suppose $M$ and $N$ are smooth manifolds of the same dimension, and $F: M \to N$ is an immersion or submersion. Then $F$ is a local diffeomorphism. If $F$ is bijective, it is a diffeomorphism.

**Rank Theorem for Manifolds:** Suppose $M$ and $N$ are smooth manifolds of dimension $m$ and $n$, respectively, and $F: M \to N$ is a smooth map with constant rank $k$. For each $p\in M$ there exists a smooth coordinates $(x^1, \dots, x^m)$ centred at $p$ and $(v^1, \dots, v^n)$ centred at $F(p)$ in which $F$ has the coordinate representation $$F(x^1, \dots, x^m) = (x^1, \dots, x^k, 0, \dots, 0).$$
**Cor:** Let $F: M \to N$ be a smooth map, and suppose $M$ is connected. Then the following are equivalent. ^815841
- For each $p\in M$ there exist smooth charts near $p$ and $F(p)$ in which the coordinate representation of $F$ is linear.
- $F$ has constant rank.

**Th:** Let $F: M \to N$ be a smooth map of constant rank.
- If $F$ is surjective, then it is a submersion.
- If $F$ is injective, then it is an immersion.
- If $F$ is bijective, then it is a diffeomorphism.

**Prop:** Suppose $M$ is a smooth manifold, $p \in M$ and $y^1, \dots, y^n$ are smooth real-valued functions defined on a neighbourhood $p$ of $M$.
- If $dy^1|_p, \dots, dy^n|_p$ form a basis for $T^*_pM$, then $(y^1, \dots, y^n)$ are smooth coordinates for $M$ in some neighbourhood.
- If $dy^1|_p, \dots, dy^n|_p$ are independent, then are real valued functions $y^{n+1}, \dots, y^m$ such that $(y^1, \dots, y^m)$ are smooth coordinates for $M$ in some neighbourhood of $p$.
- If $dy^1|_p, \dots, dy^n|_p$ span $T_p^*M$, then there are indices $i_1, \dots, i_k$ such that $(y^{i_1}, \dots, y^{i_k})$ are smooth coordinates for $M$ in some neighbourhood of $p$.
# Submersions

**Prop:** Let $\pi: M \to N$ be a submersion.
- $\pi$ is an open map.
- Every point of $M$ is in the image of a smooth local section of $\pi$. 
- If $\pi$ is surjective it is a quotient map.

**Cor:** Let $M$ be a compact smooth manifold. Then there cannot be a submersion $F: M \to \Bbb R^n$ for any $n > 0$. 

**Cor:** Suppose $\pi: M \to N$ is a smooth map such that every point of $M$ is in the image of a smooth local section of $\pi$, then $\pi$ is a submersion.

**Lemma:** Suppose $V\subseteq \text{Int}(\Bbb H^n)$ is open and $f: V \to f[V] \subseteq \Bbb H^n$ is a diffeomorphism onto its image. Then $f[V] \cap \partial \Bbb H^n = \varnothing$.

**Cor:** Let $M$ be smooth manifold with boundary, then the set of interior points and boundary points are disjoint, i.e., $\text{Int}(\Bbb H^n) \cap \partial \Bbb H^n = \varnothing$. 

**Prop:** Suppose $M, N$ and $P$ are smooth manifolds, $\pi: M \to N$ is a surjective submersion, and $F: N \to P$ is any map. Then $F$ is smooth iff $F\circ \pi$ is smooth. 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}     
M \arrow[d,two heads, "\pi"'] \arrow[dr, "F\circ \pi"] \\ N \arrow[r, "F"'] & P.
\end{tikzcd}
\end{document}
```

**Passing Smoothly to the Quotient:** Suppose $\pi: M \to N$ is a surjective immersion. If $F: M \to P$ is a smooth map that is constant on the fibres of $\pi$, then there is a unique smooth map $\tilde F: N \to P$ such that $\tilde F \circ \pi = F$ . 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}     
M \arrow[d,two heads, "\pi"'] \arrow[dr, "F"] \\ N \arrow[r, "\widetilde F"] & P.
\end{tikzcd}
\end{document}
```

**Uniqueness of Smooth Quotients:** Suppose $\pi_1: M \to N_1$ and $\pi_2: M \to N$ are surjective submersions that are constant on each other's fibres. Then there exists a unique diffeomorphism $F: N_1 \to N_2$ such that $F \circ \pi_1 = \pi_2$. 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}     
& M \arrow[dl,two heads, "\pi_1"'] \arrow[dr,two heads, "\pi_2"] \\ 
N \arrow[rr, "F"] & & P.
\end{tikzcd}
\end{document}
```

**Prop:** If $\pi: M \to N$ is a submersion and $X$ is a smooth vector field on $N$, then there is a smooth vector field on $M$, called a *lift of $X$*, that is $\pi$[[Vector Fields on Smooth Manifolds#Related Vector Fields|-related]] to $X$.

**Cor:** Suppose $\pi: M \to N$ is a surjective submersion. If $X$ is a vector field on $M$ such that $\pi_* X_p = \pi_* X_q$ whenever $\pi(p) = \pi(q)$, then there exists a unique smooth vector field on $N$ that is $\pi$-related to $X$.

**Def:** Let $M_1$ and $M_2$ be connected smooth manifolds of dimension $n$. For $i = 1, 2$, let $(W_i, \varphi_i)$ be a smooth coordinate domain centred at some point $p_i \in M_i$ such that $\varphi_i[W_i] \subseteq B(0, 2) \subseteq \Bbb R^n$. We define $U_i = \varphi_i^{-1}[B(0, 1)]\subseteq W_i$ and $M'_i := M_i \setminus U_i$. The *connected sum* of $M_1$ and $M_2$, denoted by $M_1 \# M_2$, is the quotient space of $M_1' \sqcup M_2'$ obtained by identifying each $q\in \partial U_1$ with $\varphi_2^{-1}\circ \varphi_1(q)\in \partial U_2$. 

$M_1 \# M_2$ is a connected topological $n$-manifold and has a unique structure such that the restriction of the quotient map to each $M_i'$ is a smooth embedding, where $M_i'$ is considered a smooth manifold with boundary. There are open subsets $U,V \subseteq M_1 \# M_2$ that are diffeomorphic to $M_1 \setminus \{p_1\}$ and $M_2\setminus \{p_2\}$, respectively, and such that $U \cap V$ is diffeomorphic to $B_2(0) \setminus \{0\}$.
