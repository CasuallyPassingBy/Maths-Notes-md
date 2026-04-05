---
tags:
  - DifferentialGeometry
  - Topology
---
Subjects: [[Differential Geometry]], [[Topology]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Covering Maps]]

**Def:** Let $M$ and $F$ be topological spaces. A *fiber bundle over $M$ with model fibre $F$* is a topological space $E$ together with a surjective continuous map $\pi:E \to M$ with the property that for each $x\in M$, there exists a neighbourhood $U$ of $x$ in $M$ and a homeomorphism $\Phi: \pi^{-1}[U]\to U \times F$, called a *local trivislisation of $E$ over $U$*, such that the following diagram commutes
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\pi^{-1}[U] \arrow[rr, "\Phi"]\arrow[dr, "\pi"']&& U \times F\arrow[dl, "\pi_1"]  \\
& U
\end{tikzcd}
\end{document}
```
The space $E$ is called the *total space of the bundle*, $M$ is its *base*, and $\pi$ is its *projection*. If $E$, $M$, and $F$ are smooth manifolds with or without boundary, $\pi$ is a smooth map, and the local trivialisations can be chosen to be diffeomorphisms, then it is called a *smooth fbre bundle*. 

A *trivial fibre bundle* is one that admits a local trivliasiation over the entire base, a *global trivialisation*. It is said to be *smoothly trivial* if it is a smooth bundle and the global trivialisation is a diffeomorphism. 

**Examples:**
- Every product space $M\times F$ is a fibre bundle with projection $\pi_1:M \times F \to M$, called the *product fibre bundle*. It has a global trivialisation given by the identity map $M \times F$ to itself, so every product bundle is trivial.
- Every rank-$k$ vector bundle is a fibre bundle with the model fibre $\Bbb R^k$.
- If $E \to \Bbb S^1$ is the Möbius bundle, then the image of $\Bbb R\times [-1, 1]$ under the quotient map $q: \Bbb R^2\to E$ is a fiber bundle over $\Bbb S^1$ with model fibre $[-1, 1]$. 
- Every [[Covering Maps|covering map]] $\pi: E\to M$ is fibre bundle whose model fibre is discrete. 

**Properties of Fibre Bundles:** Suppose $\pi: E \to M$ is a fibre bundle with fibre $F$.
- $\pi$ is an open quotient map.
- If the bundle is smooth, then $\pi$ is a smooth submersion.
- $\pi$ is a proper map iff $F$ is compact.
- $E$ is compact iff $M$ and $F$ are compact.