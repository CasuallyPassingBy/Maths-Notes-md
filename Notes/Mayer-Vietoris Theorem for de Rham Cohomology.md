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

An analogous proofs exists using [[Singular Homology of Spheres|singular homology, and degree theory for spheres]]

### Compactly Supported de Rham Cohomology

**Poincaré Lemma with Compact Support:** Let $1 \le p \le n$, and suppose $\omega$ is a compactly supported closed $p$-form on $\Bbb R^n$. If $p =  n$, suppose in addition that $$\int_{\Bbb R^n}\omega = 0.$$Then there exists a compactly supported smooth $(p-1)$-form $\eta$ on $\Bbb R^n$ such that $d\eta = \omega$.

**Def:** Let $M$ be a smooth manifold with or without boundary and let $\Omega_c^p(M)$ denote the vector space of compactly supported smooth $p$-forms on $M$. The *$p$th compactly supported de Rham cohomology group of $M$* is the quotient space $$H_c^p(M) := \frac{\ker (d : \Omega^p_c(M) \to \Omega^{p+1}_c(M))}{\text{Im}(d: \Omega^{p-1}_c (M) \to \Omega^p_c(M))}.  $$Of course, when $M$ is compact, this just reduces to ordinary de Rham cohomology. 

**Compactly Supported Cohomology of $\Bbb R^n$:** For $n \ge 1$, the compactly supported de Rham cohomology groups of $\Bbb R^n$ are $$H_c^p(\Bbb R^n) \cong \begin{dcases}
0 & 0\le p < n, \\
\Bbb R  & p = n.
\end{dcases}$$
We see that a smooth map doesn't pull back compactly supported forms to compactly supported smooth ones. so it doesn't induce a map on compactly supported cohomology. A [[Proper Maps|proper map]] does pull back compactly supported forms to compactly supported ones, so for a proper smooth map $F: M \to N$ there is an induced cohomology map $F^*: H_c^p(N) \to H_c^p(M)$ for each $p$. 

**Top Cohomology, Orientable Compact Support Case:** If $M$ is a connected oriented smooth $n$-manifold, then the integration map $I: H_c^n(M) \to \Bbb R$ is an isomorphism, so $H_c^n(M)$ is $1$-dimensional.

**Top Cohomology, Orientable Compact Case:** If $M$ is a compact connected orientable smooth $n$-manifold, then $H_\text{dR}^n(M)$ is $1$-dimensional, and is spanned by the cohomology class of any smooth orientation form.

**Top Cohomology, Orientable Noncompact Case:** If $M$ is a noncompact connected orientable smooth $n$-manifold, then $H_\text{dR}^n(M)=0$. 

**Lemma:** Suppose $M$ is a connected nonorientable smooth manifold and $\widehat\pi: \widehat  M \to M$ is its orientation covering. For each $p$, the induced cohomology maps $\widehat\pi^*: H_\text{dR}^p(M) \to H_\text{dR}^p(\widehat M),$ and  $\widehat\pi^*: H_c^p(M)\to H_c^p(\widehat M)$ are injective.

**Top Cohomology, Nonorientable Case:** If $M$ is a connected nonorientable smooth $n$-manifold, then $H_c^n (M) = 0$ and $H_\text{dR}^n(M)=0$. 

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

**Th:** Suppose $N$ is a compact, connected, oriented smooth $n$-manifold and $X$ is a compact, oriented, smooth $(n+1)$-manifold with connected boundary. If $f: \partial X \to N$ is a continuous map that has a continuous extension to $X$, then $\deg f = 0$. 

**Brouwer Fixed-Point Theorem:** Every continuous map from $\bar{\Bbb B}^n$ to itself has a fixed point.

There's also a proof available using [[Singular Homology of Spheres#^374dde|singular homology of spheres]]. 