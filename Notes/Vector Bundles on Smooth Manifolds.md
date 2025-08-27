---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Topological Vector Bundles]], [[Smooth Submanifolds]] [[The Tangent Bundle]], [[Smooth Partitions of Unity for Manifolds]], [[The Cotangent Bundle]], [[Dual Vector Spaces]]

**Def:** For any two maps $\pi: E \to M$ and $\pi': E'\to M$ with the same target space $M$, a map $\phi: E \to E'$ is said to be *fibre-preserving* if $\phi[\pi^{-1}\{p\}] \subseteq \pi'^{-1}\{p\}$ for all $p\in M$.

**Prop:** Given two maps $\pi: E \to M$ and $\pi': E'\to M$ a map $\phi: E \to E'$ is fibre-preserving iff $\pi = \pi' \circ \phi$, or if the following diagram commutes: 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
E \arrow{rr}{\phi} \arrow{dr}{\pi}&& E'\arrow{dl}{\pi'} \\
& M
\end{tikzcd}
\end{document}
```

**Def:** A surjective map $\pi: E \to M$ of manifolds is said to be *locally trivial of rank $r$* if:
- each fibre $\pi^{-1}\{p\}$ has a structure of a vector space of dimension $r$. 
- for each $p\in M$, there are an open neighbourhood $U$ of $p$ and a fibre-preserving diffeomorphism $\phi: \pi^{-1}[U] \to U \times \Bbb R^r$ such that for every $q\in U$ the restriction $$\phi|_{\pi^{-1}\{q\}}: \pi^{-1}\{q\} \to \{q\} \times \Bbb R^r$$is a vector space isomorphism. Such an open set $U$ is called a *trivialising open set* for $E$, and $\phi$ is called a *trivialisation* of $E$ over $U$. Meaning that the diagram: 

```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}
\pi^{-1}[U] \arrow{rr}{\phi} \arrow{dr}{\pi}&& U \times R^k\arrow{dl}{\pi_1} \\
& M
\end{tikzcd}
\end{document}
```

where $\pi_1$ is the projection of the first coordinate.

The collection $\{(U_\alpha, \phi_\alpha) \mid \alpha < \kappa\}$, with $\{U_\alpha \mid \alpha < \kappa\}$ an open cover of $M$, is called a *local trivialisation* for $E$, and $\{U_\alpha \mid \alpha < \kappa\}$ is called the *trivialising open cover* of $M$ for $E$.

**Def:** A $\mathcal C^\infty$ *vector bundle of rank $r$* is a triple $(E, M, \pi)$ consisting of manifolds $E$ and $M$ and a surjective smooth map $\pi: E \to M$ that is locally trivial of rank $r$. The manifold $E$ is called the *total space* of the vector bundle and $M$ the *base space*. By abuse of language, we say that $E$ is a *vector bundle over $M$*. For any regular submanifold $S\subseteq M$, the triple $(\pi^{-1}[S], S, \pi|_{\pi^{-1}[S]})$ is a $\mathcal C^\infty$ vector bundle over $S$, called the *restriction* of $E$ to $S$. We will often write the restriction as $E|_S$ instead of $\pi^{-1}[S]$. Similarly, we denote the fibres as $E_p$ instead of $\pi^{-1}\{p\}$. 

**Example:** Given a manifold $M$, let $\pi: M \times \Bbb R^r \to M$ be the projection to the first factor. Then $M \times \Bbb R^r \to M$ is a vector bundle of rank $r$, called the *product bundle* of rank $r$ over $M$. 

**Def:** Let $\pi: E \to M$ be a $\mathcal C^\infty$ vector bundle. Suppose $(U, \psi) = (U, x^1, \dots, x^n)$ is a chart on $M$ and $$\phi: E|_U \stackrel{\sim}{\to} U \times \Bbb R^r,  \quad \phi(e) = (\pi(e), c^1(e), \dots, c ^r (e))$$is a trivialisation of $E$ over $U$. Then $$(\psi \times \text{id}_{\Bbb R^r}) \circ \phi = (x^1, \dots, x^n, c^1, \dots, c^r): E|_U \stackrel{\sim}{\to} U \times \Bbb R^r\stackrel{\sim}{\to} \psi[U] \times \Bbb R^r\subseteq \Bbb R^n \times \Bbb R^r $$
is a diffeomorphism of $E|_U$ onto its image and so is a chart on $E$. We call $x^1, \dots, x^n$ the *base coordinates* and $c^1, \dots, c^r$ the *fiber coordinates* of the chart $(E|_U, (\psi \times \text{id}_{\Bbb R^r}) \circ \phi)$ on $E$. We see that the fiber coordinates $c^i$ depend only on the trivialisation $\phi$ of the bundle $E|_U$ and not the trivialisation $\psi$ of the base $U$. 

**Lemma:** Let $\pi: E \to M$ be a smooth vector bundle, and suppose $\phi: \pi^{-1}[U] \to U \times \Bbb R^k$ and $\psi: \pi^{-1}[V] \to V \times \Bbb R^k$ are two smooth local trivialisations of $E$ such that $U \cap V \neq \varnothing$. There exists a smooth map $\tau: U \cap V \to \text{GL}(k , \Bbb R)$ such that the composition $\phi \circ \psi^{-1}: (U \cap V )\times \Bbb R^k \to (U \cap V )\times \Bbb R^k$ has the form $$\phi \circ \psi^{-1}(p, v) = (p, \tau(p) v) $$where $\tau(p)v$ denotes the usual action of the $k\times k$ matrix $\tau(p)$ on the vector $v \in \Bbb R^k$. 

The smooth map $\tau: U \cap V \to \text{GL}(k, \Bbb R)$ described in the lemma above is called the *transition function* between the local trivialisations $\phi$ and $\psi$. 

**Vector Bundle Construction Lemma:** Let $M$ be a smooth manifold, and suppose that we are given:
- for each $p\in M$, a real vector space $E_p$ of some fixed dimension $k$. 
Let $$E := \coprod_{p \in M} E_p,$$and let $\pi: E \to M$ be the map that takes each element of $E_p$ to the point $p$. Suppose furthermore that we are given
- an open cover $\{U_\alpha \mid \alpha < \kappa\}$ of $M$
- For each $\alpha < \kappa$, a bijective map $\phi_\alpha: \pi^{-1}[U_\alpha] \to U_\alpha \times \Bbb R^k$ whose restriction to each $E_p$ is a linear isomorphism from $E_p$ to $\{p\}\times \Bbb R^k \cong \Bbb R^k$.
- For each $\alpha, \beta < \kappa$ such that $U_\alpha \cap U_\beta \neq \varnothing$, a smooth map $\tau_{\alpha \beta}: U_\alpha \cap U_\beta \to \text{GL}(k, \Bbb R)$ such that the composite map $\phi_\alpha \circ \phi_\beta^{-1}: (U_\alpha \cap U_\beta) \times \Bbb R^k \to U_\alpha \cap U_\beta) \times \Bbb R^k$ has the form: $$\phi_\alpha \circ \phi_\beta^{-1}(p, v) = (p, \tau_{\alpha\beta}(p) v) $$
Then $E$ has a unique smooth manifold structure making it into a smooth vector bundle of rank $k$ over $M$, with $\pi$ as projection and $\phi_\alpha$ as smooth local trivialisations. 
# Vector Subbundles

**Def:** Given a smooth vector bundle $\pi: \to M$, a *smooth bundle* of $E$ is a subset $D \subseteq E$ with the following properties:
- $D$ is an embedded submanifold of $E$.
- For each $p \in M$, the fiber $D_p = D \cap \pi^{-1}\{p\}$ is a linear subspace of $E_p = \pi^{-1}\{p\}$.
- With the vector space structure on each $D_p$ inherited from $E_p$ and the projection $\pi|_D: D \to M$, $D$ is a smooth vector bundle over $M$.

**Local Frame Criterion for Subbundles:** Let $\pi: E \to M$ be smooth vector bundle, and suppose for each $p \in M$ we are given an $m$-dimensional linear subspace $D_p \subseteq E_p$. Then $D = \coprod_{p \in M} D_p \subseteq E$ is a smooth subbundle iff if the following condition is satisfied: each point $p \in M$ has a neighbourhood $U$ on which there are smooth local sections $s_1, \dots, s_m: U \to E$ such that $s_1|_q, \dots, s_m|_q$ form a basis for $D_q$ at each $q \in U$.

# Dual Bundles

Let $\pi: E \to M$ be a smooth vector bundle over a smooth manifold $M$ of rank $r$. The *dual bundle* of $E$, denoted $E^*$, is the smooth vector bundle $$\pi^*: E^* \to M,$$where $E_p^*:= (E_p)'$ for every $p \in M$, $$E^* := \coprod_{p\in M}E_p^*,$$and $\pi^*(\lambda) =p$ for $\lambda \in E_p^*$. 

The reason why it is smooth it is because if $E$ is locally trivialised over $U\subseteq M$ by $\phi:\pi^{-1}[U] \to U \times \Bbb R^k$, then $E^*$ is locally trivialised by $\phi^*: (\pi^*)^{-1}[U] \to U \times (\Bbb R^k)'$. Lastly, we only need that the transitions function behave nicely.
It is easy enough to check that if $\phi_\alpha: \pi^{-1}[U_\alpha] \to U_\alpha \times \Bbb R^k$ and $\phi_\beta: \pi^{-1}[U_\beta] \to U_\beta \times \Bbb R^k$ are local trivialisations with a transition function betweeen trivilisations $\tau_{\alpha\beta}$, then $$\phi_\alpha \circ (\phi_\beta^*)^{-1}(p, v) = (p, ((\tau_{\alpha \beta}(p)'))^{-1}(v)).$$
Let $\pi_E: E \to M$, and $\pi_F: F \to M$ be vector bundles over $M$, with bundle function $(\text{id}_M, \tilde f)$ from $F$ to $e$, then we can define the *dual bundle function* from $E^*$ to $F^*$, by $(\text{id}_M, \tilde f^*)$ where $$\tilde f^*(p, \lambda) := (p, \lambda \circ \tilde f_p).$$ We can generalise this to a slight broader class of bundle maps. Let $\pi_E:E \to M$ and $\pi_F: F \to N$ be two vector bundles, with a bundle map $(f, \tilde f)$ from $F$ to $E$. If $f$ is a diffeomorphism, then we can define the dual bundle map as $(f^{-1}, \tilde f^*)$ such that the following diagram commutes

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
F \arrow[d, two heads,"\pi_M"'] \arrow[r, "\tilde f^*"] & E \arrow[d, two heads,"\pi_N"]\\
M \arrow[r, "f^{-1}"'] & N
\end{tikzcd}
\end{document}
```
