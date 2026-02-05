---
tags:
  - DifferentialGeometry
  - Topology/AlgebraicTopology
---
Subjects: [[Differential Geometry]], [[Algebraic Topology]]
Links: [[The de Rham Cohomology Groups]], [[Mayer-Vietoris Theorem for Singular Homology]], [[Orientations of Smooth Manifolds]], [[Orientations and Covering Maps for Smooth Manifolds]], [[The Zigzag Lemma]]

# Mayer-Vietoris Theorem

**Def:** Suppose we are given a sequence of vector spaces and linear maps$$\cdots \longrightarrow V^{p-1}\stackrel{F_{p-1}}{\longrightarrow}  V^p \stackrel{F_{p}}{\longrightarrow}  V^{p+1} \stackrel{F_{p+1}}{\longrightarrow}  V^{p+2}\longrightarrow \cdots.$$Such a sequence is said to be *exact* if the image of each map is equal to the kernel of the next: for each $p$,  $$\text{Im }F_{p-1} = \ker F_p. $$
We are given a smooth manifold $M$ with or without boundary and two open subsets $U, V\subseteq M$ whose union is $M$. There are four inclusion maps 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}
& U\arrow[dr, "k"] & \\
U \cap V\arrow[ur, "i"]\arrow[dr, "j"] && M \\
&V\arrow[ur,"\ell"']&
\end{tikzcd}
\end{document}
```

**Mayer-Vietoris Theorem:** Let $M$  be a smooth manifold with or without boundary, and let $U, V$ be open subsets of  whose union is $M$. Then for each $p$ there is a linear map $\delta: H_\text{dR}^p(U \cap V) \to H_\text{dR}^{p+1}(M)$ such that the following sequence is exact:  $$\cdots 
\stackrel{\delta}{\longrightarrow} H^p_\text{dR}(M) \stackrel{k^* \oplus \;l^*}{\longrightarrow} H^p_\text{dR}(U) \oplus H^p_\text{dR}(V)\stackrel{i^*- j^*}{\longrightarrow}H^p_\text{dR}(U \cap V)\stackrel{\delta}{\longrightarrow} H^{p+1}(M) \stackrel{k^* \oplus \;l^*}{\longrightarrow}\cdots.$$
**Cor:** The connecting homomorphism in the Mayer-Vietoris sequence, $\delta: H^p_\text{dR}(U \cap V) \to H^{p+1}_\text{dR}(M)$, is defined as follows. For each $\omega\in \mathcal Z^p(U \cap V)$, there are $p$-forms $\eta\in \Omega^p(U)$ and $\eta'\in \Omega^p(V)$ such that $\omega = \eta|_{U \cap V} - \eta'|_{U \cap V}$; and then $\delta[\omega] = [\sigma]$, where $\sigma$ is the $(p+1)$-form on $M$ that is equal to $d\eta$ on $U$ and to $d\eta'$ on $V$. If $\{\varphi, \psi\}$ is a smooth partition of unity subordinate to $\{U, V\}$, we can take $\eta =\psi\omega$ and $\eta' = -\varphi\omega$, both extend by zero outside the supports of $\psi$ and $\varphi$. 

# Computations Using Mayer-Vietoris

**Cohomology of Spheres:** For $n \ge 1$, the de Rham cohomology groups of $\Bbb S^n$ are $$H_\text{dR}^p(\Bbb S^n) \cong \begin{dcases}
\Bbb R & p = 0 \text{ or }p = n, \\
0 & 0< p <n.
\end{dcases} $$
**Cor:** If $\eta\in \Omega^n(\Bbb S^n)$ is exact iff $$\int_{\Bbb S^n}\eta = 0.$$
**Cohomology of Punctured Euclidean Space:** Suppose $n \ge 2$ and $x\in \Bbb R^n$ , and let $M =\Bbb R^n \setminus\{x\}$. The only nontrivial de Rham groups of $M$ are $H_\text{dR}^0(M)$ and $H_\text{dR}^n(M)$, both of which are $1$-dimensional. A closed $(n-1)$-form $\eta$ on $M$ is exact iff $$\int_S\eta = 0$$for some (and hence every) $(n-1)$-dimensional sphere centred at $x$. 

We can actually give the element that generates the nontrivial homology group of $\Bbb R^n\setminus\{0\}$. $$ \omega = \|x\|^{-n}\sum_{i =1 }^n(-1)^{i-1} x^i\; dx^1\wedge\dots\wedge\widehat{dx^i}\wedge\dots \wedge dx^n. $$Then we see that $\iota^*_{\Bbb S^{n-1}}\omega$ is the Riemannian volume form of $\Bbb S^{n-1}$ with respect to the round metric and standard orientation. 

**Cor:** Suppose $n \ge 2$ and $\overline B\subseteq \Bbb R^n$ is a closed ball, and let $M =\Bbb R^n \setminus\overline B$. The only nontrivial de Rham groups of $M$ are $H_\text{dR}^0(M)$ and $H_\text{dR}^n(M)$, both of which are $1$-dimensional. A closed $(n-1)$-form $\eta$ on $M$ is exact iff $$\int_S\eta = 0$$for some (and hence every) $(n-1)$-dimensional sphere centred at $x$. 

**Cor:** Suppose $n \ge 2$, $U \subseteq\Bbb R^n$ is any open subset, and $x\in U$. Then $H_\text{dR}^{n-1}(U\setminus \{x\})\ne 0$. 

**[[Topological Manifolds#^ca2c82|Topological Invariance of Dimension]]:** A nonempty $n$-dimensional  topological manifold cannot be homeomorphic to an $m$-dimensional manifold unless $m = n$. 

**[[Topological Manifolds#^cd5f36|Invariance of the Topological Boundary]]:** Suppose $M$ is an $n$-manifold with boundary. A point of $M$ cannot be a boundary point and an interior point. 

An analogous proofs exists using [[Singular Homology of Spheres|singular homology, and degree theory for spheres]].

## Degree Theory

**Degree of a Smooth Map:** Suppose $M$ and $N$ are compact, connected, oriented, smooth manifolds of dimension $n$, and $F: M \to N$ is a smooth map. There exists a unique integer $k$, called the *degree of $F$*, that satisfies both of the following conditions.
- Every smooth $n$-form $\omega$ on $N$, $$\int_M F^*\omega = k\int_N\omega.$$
- If $q\in N$ is a regular value of $F$, then $$k = \sum_{x\in F^{-1}\{q\}} \text{sgn}(x),  $$where $\text{sgn}(x) = +1$ if $dF_x$ is orientation-preserving. and $-1$ if its orientation-reversing. 
This type of degree is called the *Brouwer degree.*

**Properties of the Degree:** Suppose $M$, $N$, and $P$ are compact, connected, smooth $n$-manifolds.
- If $F: M \to N$ and $G: N \to P$ are both smooth maps, then $\deg(G\circ F)= (\deg G)(\deg F)$.
- If $F: M\to N$ is a diffeomorphism, then $\deg F = +1$ if $F$ is orientation-preserving and $-1$ if its orientation-reversing.
- If two maps $F_0, F_1: M \to N$ are homotopic, then they have the same degree.

**Def:** The proposition above allows us to define the *degree of a continuous map* $F:M \to N$ between compact, connected, oriented, smooth $n$-manifolds, by letting $\deg F$ be the degree of any smooth map that is homotopic to $F$. 

**Prop:** Suppose $M$ and $N$ are compact, connected, oriented, smooth $n$-manifolds and $F: M \to N$ is a smooth map. If $\int_M F^*\eta \ne 0$ for some $\eta\in\Omega^n(N)$, then $F$ is surjective. The converse is true, it is possible for $F$ to be surjective and $\int_M F^*\eta = 0$ for every $\eta\in \Omega^n(N)$. 

**Th:** Suppose $N$ is a compact, connected, oriented smooth $n$-manifold and $X$ is a compact, oriented, smooth $(n+1)$-manifold with connected boundary. If $f: \partial X \to N$ is a continuous map that has a continuous extension to $X$, then $\deg f = 0$. 

**Brouwer Fixed-Point Theorem:** Every continuous map from $\bar{\Bbb B}^n$ to itself has a fixed point.

There's also a proof available using [[Singular Homology of Spheres#^374dde|singular homology of spheres]]. 

**Th:** Suppose $M$ and $N$ are noncompact, connected, oriented smooth $n$-manifolds. Suppose $F: M \to N$ is a proper smooth map. There is a unique integer $k$ called the *degree of $F$* such that each smooth compactly supported $n$-form on $N$, $$\int_M F^*\omega = k\int_N \omega,  $$and for each regular value of $q$ of $F$, $$k = \sum_{x\in F^{-1}\{q\}} \text{sgn}(x),  $$where $\text{sgn}(x) = +1$ if $dF_x$ is orientation-preserving. and $-1$ if its orientation-reversing. 