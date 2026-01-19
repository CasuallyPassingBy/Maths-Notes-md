---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Smooth Functions on Smooth Manifolds]], 


**Def:** If $\pi: E \to M$ and $\pi': E' \to M'$ are vector bundles, a continuous map $F: E \to E'$ is called a *bundle homomorphism* if there exists a map $f: M \to M'$ satisfying $\pi' \circ F = f \circ \pi$, 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
E \arrow{r}{F} \arrow{d}{\pi}& E' \arrow{d}{\pi'} \\
M \arrow{r}{f}& M'
\end{tikzcd}
\end{document}
```
with the property that for each $p\in M$, the restricted map $F|_{E_p}: E_p \to E_{f(p)}'$ is linear. The relationship between $F$ and $f$ is expressed by saying that $F$ *covers* $f$. 

**Prop:** Suppose $\pi: E \to M$ and $\pi': E' \to M$ are vector bundles and $F: E \to E'$ is a bundle homomorphism covering $f: M \to M'$. Then $f$ is continuous and it is uniquely determined by $F$. If the bundles and $F$ are all smooth, then $f$ is smooth as well. 

**Def:** A bijective bundle homomorphism $F: E \to E'$ whose inverse is also a bundle homomorphism is called a *bundle isomorphism*; if $F$ is also a diffeomorphism, it is called a *smooth bundle isomorphism*. If there is exists a (smooth) bundle isomorphism between $E$ and $E'$, the two bundles are said to be *(smoothly) isomorphic.*

**Def:** In the special case in which both $E$ and $E'$ are vector bundles over the same base space $M$, a slightly more restrictive notion of bundle homomorphisms is usually more useful. A *bundle homomorphism over $M$* is a bundle homomorphism covering the identity map of $M$, in other words, a continuous map $F: E \to E$ such that $\pi' \circ F = \pi$, 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
E \arrow{rr}{F} \arrow{dr}{\pi}&& E' \arrow{dl}{\pi'} \\
& M
\end{tikzcd}
\end{document}
```
and whose restriction to each fiber is linear. If there exists a bundle homomorphism $F: E \to E'$ over $M$ that is also a (smooth) bundle isomorphism, then we say that $E$ and $E'$ are *(smoothly) isomorphic over $M$*.

The collection of all vector bundles together with bundle maps between them forms a [[Categories and Functors|category]].

**Prop:** Suppose $E$ and $E'$ are smooth vector bundles over a smooth manifold with or without boundary, and $F: E \to E'$ is a bijective smooth bundle homomorphism over $M$. Then $F$ is a smooth bundle isomorphism. 

**Prop:** Let $\pi_E \to M$ and $\pi_F: F \to M$ be smooth vector bundles over a smooth manifold $M$, and let $\Gamma(M, E)$ and $\Gamma(M, F)$ denote their spaces of sections. A map $\mathcal F: \Gamma(M, E) \to \Gamma(M, F)$ is linear over $\mathcal C^\infty(M)$ iff there is a smooth bundle homomorphism $F: E \to F$ over $M$ such that $\mathcal F(\sigma) = F\circ \sigma$ for all $\sigma \in \Gamma(M, E)$. 

**Prop:** Let $\sf VB$ denote the category whose objects are smooth vector bundles and whose morphisms are smooth bundle homomorphisms, and let $\sf Diff$ denote the category whose objects are smooth manifolds whose morphisms are smooth maps. The assignment $M \mapsto TM$ and $F\mapsto dF$ defines a covariant functor from $\sf Diff$ to $\sf VB$, called the *tangent functor*. 

**Prop:** Let $\pi:E \to M$ and $\widetilde\pi: \widetilde E\to M$ be two smooth rank-$k$ vector bundle over a smooth manifold $M$ with or without boundary. Suppose $\{U_\alpha\}_{\alpha\in A}$ is an open cover of $M$ such that $E$ and $\widetilde E$ admits smooth local trivilalisations over each $U_\alpha$. Let $\{\tau_{\alpha.\beta}\}$ and $\{\widetilde\tau_{\alpha, \beta}\}$ denote the transition functions determined by the given trivialisations of $E$ and $\widetilde E$, respectively. Then, $E$ and $\widetilde E$ are smoothly isomorphic over $M$ iff for each $\alpha\in A$ there exists a smooth map $\sigma_\alpha: U_\alpha\to\text{GL}(k,\Bbb R)$ such that for every $\beta\in A$ that satisfy $U_\alpha\cap U_\beta \neq \varnothing$, then$$\widetilde\tau_{\alpha,\beta}(p) = \sigma_\alpha(p) \tau_{\alpha,\beta}(p)\sigma_\beta^{-1}(p),\qquad p\in U_\alpha \cap U_\beta. $$