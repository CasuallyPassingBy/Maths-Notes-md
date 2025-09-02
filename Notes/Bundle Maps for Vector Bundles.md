---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Smooth Functions on Smooth Manifolds]]

**Def:** Let $\pi_E: E \to M$, $\pi_F: F \to N$ be two vector bundles, and possibly of different ranks. A *bundle map* from $E$ to $F$ is a pair of maps $(f, \tilde f)$, $f: M \to N$ and $\tilde f: E \to F$, such that:
- the diagram is commutative, meaning $\pi_F \circ \tilde f = f \circ \pi_E$

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
E \arrow{r}{\tilde f} \arrow{d}{\pi_E}& F \arrow{d}{\pi_E} \\
M \arrow{r}{f}& N
\end{tikzcd}
\end{document}
```

- $\tilde f$ is linear on each fiber; meaning, for each $p\in M$, $\tilde f|_{E_p}: E_p \to F_{f(p)}$ is a linear map of vector spaces.
When both $\tilde f$ and $f$ are smooth we say that it is a *smooth bundle map*. We often refer to $\tilde f$ as a *bundle map*, and say that $\tilde f$ covers $f$. A bijective bundle map $\tilde f: E \to F$ whose inverse is also a bundle map is called a *bundle isomorphism*; if $F$ is also a diffeomorphism, it is called a *smooth bundle isomorphism* If there exists a (smooth bundle) isomorphism between $E$ and $F$, the two bundles are said to be *(smoothly) isomorphic*. 

In the spacial case in which $E$ and $F$ are vector bundles over the same base manifold $M$, we require a more restrictive notion. A *bundle map over $M$* is a bundle map covering the identity of $M$, in other words, a continuous map $f: E \to F$ such that $\pi_F \circ f = \pi_E$, 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
E \arrow{rr}{f} \arrow{dr}{\pi_E}&& F \arrow{dl}{\pi_F} \\
& M
\end{tikzcd}
\end{document}
```
and whose restriction to each fiber is linear. If $f: E \to F$ is a bundle map over $M$ that is also a (smooth) bundle isomorphism, then we say that $E$ and $F$ are *(smoothly) isomorphic over $M$.*

The collection of all vector bundles together with bundle maps between them forms a [[Categories and Functors|category]].

**Prop:** Let $\pi_E \to M$ and $\pi_F: F \to M$ be smooth vector bundles over a smooth manifold $M$, and let $\Gamma(M, E)$ and $\Gamma(M, F)$ denote their spaces of sections. A map $\mathcal F: \Gamma(M, E) \to \Gamma(M, F)$ is $\mathcal C^\infty(M)$ iff there is a smooth bundle map $f: E \to F$ over $M$ such that $\mathcal F(\sigma) = F\circ \sigma$ for all $\sigma \in \Gamma(M, E)$. 

A smooth map $f: N \to M$ of manifolds induces a bundle map $(f, \tilde f)$, where $\tilde f: TN \to TM$ is given by $$\tilde f(p, v) = (f(p), df_p (v)) \in TM$$for all $v\in T_p N$. 

**Prop:** There a covariant functor $T$ from the category of smooth manifolds and smooth maps to the category of vector bundles and bundle maps:
- to each manifold $M$, we associate its tangent bundle $TM$
- to each $\mathcal C^\infty$ map $f: N \to M$ of manifolds, we associate the bundle map $T(f) = (f: N \to M, \tilde f: TN \to TM)$ 

**Prop:** If $f: N \to M$ is a diffeomorphism, then we can define the dual bundle map of $(f, \tilde f)$, where $\tilde f: TN \to TM$, above, and consider 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
T^*M \arrow{r}{\tilde f^*} \arrow{d}{\pi_E}& T^*N \arrow{d}{\pi_E} \\
M \arrow{r}{f^{-1}}& N
\end{tikzcd}
\end{document}
```

Meaning that the reason we can pushforward differential forms only when $f$ is a diffeomorphism.