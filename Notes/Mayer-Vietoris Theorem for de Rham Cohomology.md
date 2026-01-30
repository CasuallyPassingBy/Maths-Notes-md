---
tags:
  - DifferentialGeometry
  - Topology/AlgebraicTopology
---
Subjects: [[Differential Geometry]], [[Algebraic Topology]]
Links: [[The de Rham Cohomology Groups]], [[Mayer-Vietoris Theorem for Singular Homology]], [[Orientations of Smooth Manifolds]], [[Orientations and Covering Maps for Smooth Manifolds]]

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

\stackrel{\delta}{\longrightarrow} H_p(M) \stackrel{k^* \oplus \;l^*}{\longrightarrow} H_p(U) \oplus H_p(V)\stackrel{i^*- j^*}{\longrightarrow}H_p(X)\stackrel{\delta}{\longrightarrow} H_{p-1}(M) \stackrel{k^* \oplus \;l^*}{\longrightarrow}\cdots.$$
# Computations Using Mayer-Vietoris

**Cohomology of Spheres:** For $n \ge 1$, the de Rham cohomology groups of $\Bbb S^n$ are $$H_\text{dR}^p(\Bbb S^n) \cong \begin{dcases}
\Bbb R & p = 0 \text{ or }p = n, \\
0 & 0< p <n.
\end{dcases} $$
**Cor:** If $\eta\in \Omega^n(\Bbb S^n)$ is exact iff $$\int_{\Bbb S^n}\eta = 0.$$
**Cohomology of Punctured Euclidean Space:** Suppose $n \ge 2$ and $x\in \Bbb R^n$ , and let $M =\Bbb R^n \setminus\{x\}$. The only nontrivial de Rham groups of $M$ are $H_\text{dR}^0(M)$ and $H_\text{dR}^n(M)$, both of which are $1$-dimensional. A closed $(n-1)$-form $\eta$ on $M$ is exact iff $$\int_S\eta = 0$$for some (and hence every) $(n-1)$-dimensional sphere centred at $x$. 

**Cor:** Suppose $n \ge 2$ and $\overline B\subseteq \Bbb R^n$ is a closed ball, and let $M =\Bbb R^n \setminus\overline B$. The only nontrivial de Rham groups of $M$ are $H_\text{dR}^0(M)$ and $H_\text{dR}^n(M)$, both of which are $1$-dimensional. A closed $(n-1)$-form $\eta$ on $M$ is exact iff $$\int_S\eta = 0$$for some (and hence every) $(n-1)$-dimensional sphere centred at $x$. 

**Cor:** Suppose $n \ge 2$, $U \subseteq\Bbb R^n$ is any open subset, and $x\in U$. Then $H_\text{dR}^{n-1}(U\setminus \{x\})\ne 0$. 

**Topological Invariance of Dimension:** A nonempty $n$-dimensional  topological manifold cannot be homeomorphic to an $m$-dimensional manifold unless $m = n$. 

### Compactly Supported de Rham Cohomology

**Poincaré Lemma with Compact Support:** Let $n \ge p \ge 1$, and suppose $\omega$ is a compactly supported closed $p$-form on $\Bbb R^n$. If $p =  n$, suppose in addition that $$\int_{\Bbb R^n}\omega = 0.$$Then there exists a compactly supported smooth $(p-1)$-form $\eta$ on $\Bbb R^n$ such that $d\eta = \omega$.

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
- If $q\in N$ is a regular value of $F$, then $$k = \sum_{x\in F^{-1}\{q\}} \text{sgn}(x),  $$where $\text{sgn}(x) = +1$ if $dF_x$ is orientation-preserving. and $-1$ if its orientation reversing. 