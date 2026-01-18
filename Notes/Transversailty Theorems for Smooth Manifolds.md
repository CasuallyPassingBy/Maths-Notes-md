---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Sets of Measure Zero in Smooth Manifolds and Sard's Theorem]], [[Tangent Spaces and Vector Fields on Submanifolds]], [[Embedded Smooth Submanifolds]], [[Immersed Smooth Submanifolds]], [[The Whitney Embedding Theorem]]

**Def:** Suppose $M$ is a smooth manifold. Two embedded submanifolds $S, S'\subseteq M$ are said to *intersect transversely* if for each $p\in S\cap S'$, the tangent spaces $T_p S$ and $T_p S'$ together span $T_p M$. We can denote this relation as $S \pitchfork S'$.

If $F:N \to M$ is a smooth map and $S\subseteq M$ is an embedded submanifold, we say that $F$ is *transverse to $S$* if for every $x\in F^{-1}[S]$, the spaces $T_{F(x)} S$ and $dF_x [T_xN]$ together san $T_{F(x)} M$. We can denote this relation as $F \pitchfork S$. If $F$ is a smooth submersion, then it is automatically transverse to every embedded submanifold of $M$. Two embedded submanifolds intersect transversely iff the inclusion of either one is transverse to the other. 

**Th:** Suppose $N$ and $M$ are smooth manifolds and $S\subseteq M$ is an embedded submanifold.
- $F: N \to M$ is a smooth map that is transverse to $S$, then $F^{-1}[S]$ is an embedded submanifold of $N$ whose codimension is equal to the codimension of $S$ in $M$.
- If $S'\subseteq M$ is an embedded submanifold that intersects $S$ transversely, then $S \cap S'$ is an embedded submanifold of $M$ whose codimension is equal to the sum of the codimensions of $S$ and $S'$.

**Cor:** Suppose $N$ and $M$ are smooth manifolds, $S\subseteq M$ is an embedded submanifold of codimension $k$, then $F: N \to M$ is a submersion. Then $F^{-1}[S]$ is an embedded codimension $k$ submanifold of $N$.

**Prop:** Suppose $F:N \to M$ is a smooth map that is transverse to an embedded submanifold $X\subseteq M$, and let $W:= F^{-1}[X]$. To each $p\in W$ we have that $T_p W = (dF_p)^{-1}[T_{F(p)} X]$. In particular, we see that two embedded submanifolds $X, X' \subseteq M$ intersect transversely, then $T_p(X \cap X') = T_p X \cap T_p X'$. 

**Prop:** Suppose $F: M \to N$ and $G:N\to P$ are smooth maps, and $G$ is transverse to an embedded submanifold $X\subseteq P$. Then $F$ is transverse to $G^{-1}[X]$ iff $G\circ F$ is transverse to $X$. 

**Global Characterisation of Graphs:** Suppose $M$ and $N$ are smooth manifolds and $S\subseteq M \times N$ is an immersed submanifold. Let $\pi_M$ and $\pi_N$ denote the projections from $M\times N$ onto $M$ and $N$, respectively. The following are equivalent.
- $S$ is the graph of a smooth map $f: M \to N$.
- $\pi_M|_S$ is a diffeomorphism from $S$ onto $M$.
- For each $p\in M$, the submanifolds $S$ and $\{p\}\times N$ intersect transversely in exactly one point.
If these conditions hold, then $S$ is the graph of the map $f: M \to N$ defined by $f := \pi_N \circ (\pi_M|_S)^{-1}$. 

**Local Characterisation of Graphs:** Suppose $M$ and $N$ are smooth manifolds, $S\subseteq M \times N$ is an immersed submanifold submanifold, and $(p, q)\in S$. If $S$ intersects the submanifold $\{p\}\times N$ transversely at $(p, q)$, then there exists a neighbourhood $U$ of $p$ in $M$ and a neighbourhood $V$ of $(p,q)$ in $S$ such that $V$ is the graph of a smooth map $f: U \to N$.  ^dadb54

**Def:** Suppose $N$, $M$ and $S$ are smooth manifolds, and for each $s\in S$ we are given a map $F_s:N \to M$. The collection $\{F_s: s\in S\}$ is called a *smooth family of maps* if the map $F: N \times S \to M$ defined by $F(x, s) = F_s(x)$ is smooth. This family is like a higher-dimensional analogue of smooth homotopy. 

**Prop:** If $\{F_s\mid s\in S\}$ is a smooth family of maps from $N$ to $M$ and $S$ is connected, then for any $s_1, s_2\in S$, the maps $F_{s_1}, F_{s_2}: N \to M$ are homotopic. 

**Def:** If $S$ is a smooth manifold and $B\subseteq S$ is a subset whose complement has measure zero in $S$, we say that $B$ contains *almost every element in $S$.*

**Parametric Transversality Theorem:** Suppose $N$ and $M$ are smooth manifolds, $X\subseteq M$ is an embedded submanifold, and $\{F_s\mid s\in S\}$ is a smooth family of maps from $N$ to $M$. If the map $F:N \times S \to M$ is transverse to $X$, then for almost every $s\in S$, the map $F_s: N \to M$ is transverse to $X$. 

**Def:** Suppose $M$ and $N$ are smooth manifolds. A class $\cal F$ of smooth maps from $N$ to $M$ is said to be *stable* if it has the following property: whenever $\{F_s\mid s\in S\}$ is a smooth family from $N$ to $M$, and $F_{s_0}\in\cal F$ for some $s_0\in S$, then there is a neighbourhood $U$ of $s_0$ in $S$ such that $F_s\in\cal F$ for all $s\in U$. 

**Prop:** If $N$ is compact then the following classes of smooth maps from $N$ to $M$ are stable:
- immersions
- submersions
- embeddings
- diffeomorphisms
- local diffeomorphisms
- maps that are transverse to a given properly embedded submanifold $X\subseteq M$. 

**Transversality Homotopy Theorem:** Suppose $M$ and $N$ are smooth manifolds and $X\subseteq M$ is an embedded submanifold. Every smooth map $f:N \to M$ is homotopic to a smooth map $g: N \to M$ that is transverse to $X$. 

**Def:** Let $M$ be a smooth manifold. If $F:N \to M$ and $G: N' \to M$ are smooth maps into $M$, we say that $F$ and $F'$ are *transverse to each other* if every $x\in N$ and $x'\in N'$ such that $F(x) = G(x')$, the spaces $dF_x[T_x N]$ and $dG_{x'}[T_{x'}N']$ together span $T_{F(x)} M$. We denote this relationship as $F\pitchfork G$ .

**Obs:** If $S$ is an embedded submanifold of $M$ a smooth map $F. N\to M$ is transverse to $S$ iff it is transverse to the inclusion map $\iota: S\hookrightarrow M$. 

**Prop:** Let $M$ be a smooth manifold. Then $F:N \to M$ and $G: N' \to M$ are smooth maps that are transverse to each other iff the map $F\times G: N \times N' \to M \times M$ is transverse to the diagonal $\Delta_M = \{(x, x)\mid x\in M\}$, meaning that $F\pitchfork G$ iff $(F\times G) \pitchfork \Delta_M$. 

**Prop:** If $F: N \to M$ and $G: N'\to M$ are smooth maps that are transverse to each other, then $F^{-1}[G[N']]$ is an embedded submanifold of $N$ of dimension equal to $\dim N+ \dim N'-\dim M$. 