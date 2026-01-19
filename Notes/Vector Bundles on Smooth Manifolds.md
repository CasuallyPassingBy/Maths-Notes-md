---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Topological Vector Bundles]], [[Embedded Smooth Submanifolds]] [[The Tangent Bundle]], [[Smooth Partitions of Unity for Manifolds]], [[The Cotangent Bundle]], [[Dual Vector Spaces]]

**Def:** Let $M$ be a topological space. A *real vector bundle of rank $k$ over $M$* is a topological space $E$ together with a surjective continuous map $\pi:E \to M$ satisfying the following conditions:
- For each $p\in M$, the fiber $E_p := \pi^{-1}\{p\}$ over $p$ is endowed with the structure of a $k$-dimensional real vector space.
- For each $p\in M$, there exists a neighbourhood of $U$ of $p\in M$ and homeomorphism $\Phi: \pi^{-1}[U] \to U\times\Bbb R^k$, called a *local trivialisation of $E$ over $U$*, satisfying the following conditions:
	- $\pi_U \circ \Phi = \pi$, where $\pi_U: U \times \Bbb R^k \to U$ is the projections;
	- for each $q\in U$, the restriction $\Phi$ to $E_q$ is a vector space isomorphism from $E_q$ to $\{q\}\times \Bbb R^k \cong \Bbb R^k$.
If $M$ and $E$ are smooth manifolds with or without boundary, $\pi$ is a smooth map, and the local trivialisations can be chosen to be diffemorphisms, then $E$ is called a *smooth vector bundle*. In this case, we calle any trivialisation that is a diffeomorphism onto its image a *smooth local trivialisation*. 

A rank-$1$ vector bundle is often called a *real line bundle*. *Complex vecto bundles* are defined similarly, with 'real vector space' replaced by 'complex vector space' and $\Bbb R^k$ replaced by $\Bbb C^k$ in the definition. 

The space $E$ is called the *total space of the bundle*, $M$, is called the *base*, and $\pi$ is its *projection*. 

**Obs:** If $E$ is a smooth vector bundle over $M$, then the projection map $\pi: E \to M$ is a surjective smooth submersion. 

**Def:** If there exists a local trivialisation of $E$ over all of $M$, called a *global trivialisation of $E$*, then $E$ is called to be the *trivial bundle*. In this case, $E$ is homeomorphic to the product space $M \times \Bbb R^k$. If $E \to M$ is a smooth bundle that admits a smooth global trivialisation, then we say that $E$ is *smoothly trivial*. In this case $E$ is *diffeomorphic* fo $M \times \Bbb R^k$, not just homeomorphic. 

**Example:** the simplest example of a rank $k$ vector bundle over any space $M$ is the product space $E = M \times \Bbb R^k$ with $\pi = \pi_1: M \times \Bbb R^k \to M$ as its projection. Any such bundle is called a *product bundle*, is trivial. If $M$ is a smooth manifold with or without boundary, then $M\times\Bbb R^k$ is a smoothly trivial.

**Example:** Define an equivalence relation on $\Bbb R^2$ by declaring that $(x, y) \sim (x', y')$ iff $(x', y')= (x+n, (-1)^n y)$ for some $n \Bbb Z$. Let $E := \Bbb R^2/\sim$ denote the quotient space, and let $q: \Bbb R^2\to E$ be the quotient map. 

Let $S := [0, 1]\times \Bbb R\subseteq \Bbb R^2$. The restriction to $q$ to $S$ is surjective and closed, so it is a quotient map. The only nontrivial identifications made by $q|_S$ are on the boundary lines, seo we can think of $E$ to as the space obtained from $S$ by giving the right-hand edge a half-twist to turn it upside-down, and the pasting it to left-hand edge. For any $r> 0$, the image under the quotient map $q$ of the rectangle $[0, 1] \times  [-r, r]$ is a smooth compact manifold with boundary called a *Möbius band*. 

If we consider the following commutative diagram:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\Bbb R^2 \arrow[r, "q"]\arrow[d, "\pi_1"']& E\arrow[d, dashed, "\pi"]  \\
\Bbb R \arrow[r, "\varepsilon"']& \Bbb S^1
\end{tikzcd}
\end{document}
```
where $\pi_1$ is the projection is the projection onto the first factor and $\varepsilon: \Bbb R\to \Bbb S^1$ is the smooth covering map $\varepsilon(x) := \exp(2\pi i x)$, because $\varepsilon \circ \pi_1$ is constant on each equivalence class, it descents to a continuous map $\pi: E \to \Bbb S^1$. We know that $E$ has a unique smooth manifold structure such that $q$ is a smooth covering map and $\pi: E \to \Bbb S^1$ is a smooth real line bundle over $\Bbb S^1$, called the *Möbius bundle*. 

**Prop:** Let $E$ be a vector bundle over a topological space $M$. Then the projection map $\pi: E \to M$ is a [[homotopy equivalence]].

**[[The Tangent Bundle]] as a Vector Bundle:** Let $M$ be a smooth $n$-manifold with or without boundary, and let $TM$ be its tangent bundle. With its standard projections map, its natural vector space structure on each fibre, and the topology and smooth structure, $TM$ is a smooth vector bundle or rank $n$ over $M$. 

**Lemma:** Let $\pi: E \to M$ be a a smooth vector bundle of rank $k$ over $M$. suppose $\Phi: \pi^{-1}[U] \to U\times\Bbb R^k$  and $\Psi: \pi^{-1}[V] \to V \times \Bbb R^k$ are smooth local trivialisations of $E$ with $U \cap V \neq\varnothing$. There exists a smooth map $\tau: U\cap V \to \text{GL}(k,\Bbb R)$ such that the composition $\Phi \circ \Psi^{-1} : (U \cap V)\times \Bbb R^k \to (U\cap V) \times \Bbb R^k$ has the form $$(\Phi\circ \Psi^{-1})(p, v) = (p, \tau(p)v) $$

The smooth map $\tau: U \cap V \to \text{GL}(k, \Bbb R)$ described in the lemma above is called the *transition function* between the local trivialisations $\Phi$ and $\Psi$. 

**Vector Bundle Chart Lemma:** Let $M$ be a smooth manifold with or without boundary, and suppose that for each $p\in M$ we are given a real vector space $E_p$ of some fixed dimension $k$. Let $$E := \coprod_{p\in M} E_p,$$and let $\pi: E \to M$ be the map that takes each element of $E_p$ to the point $p$. Suppose furthermore that we are given the following data:
- an open cover $\{U_\alpha\}_{\alpha\in A}$ of $M$
- for each $\alpha\in A$, a bijective map $\Phi_\alpha: \pi^{-1}[U_\alpha] \to U_\alpha\times \Bbb R^k$ whose restriction to each $E_p$ is a vector space isomorphism from $E_p$ to $\{p\}\times \Bbb R^k \cong \Bbb R^k$
- For each $\alpha,\beta\in A$ with $U_\alpha\cap U_\beta \neq \varnothing$, a smooth map $\tau_{\alpha, \beta}: U_\alpha\cap U_\beta \to \text{GL}(k, \Bbb R)$ such that the map $\Phi_\alpha \circ \Phi_\beta$ from $(U_\alpha\cap U_\beta) \times \Bbb R^k$ to itself has the form $$(\Phi_\alpha \circ\Phi_\beta^{-1})(p, v) = (p, \tau_{\alpha, \beta}(p) v).$$
Then $E$ has a unique topology and smooth structure making it into a smooth manifold with or without boundary and a smooth rank-$k$ vector bundle over $M$, with $\pi$ as a projection and $\{(U_\alpha, \Phi_\alpha) \mid \alpha\in A\}$ as smooth local trivialisations. 

**Prop:** Let $\pi: E \to M$ be a smooth vector bundle of rank $k$ over a smooth manifold $M$ with or without boundary. Suppose $\{U_\alpha\}_{\alpha\in A}$ is an open cover of $M$, and for each $\alpha\in A$ we are given a smooth local trivialisation $\Phi_\alpha:\pi^{-1}[U_\alpha] \to U_\alpha\times\Bbb R ^k$ of $E$. For each $\alpha,\beta\in A$ such that $U_\alpha\cap U_\beta \neq \varnothing$, let $\tau_{\alpha, \beta}: U_\alpha\cap U_\beta\to\text{GL}(k,\Bbb R)$. Then, for any $\alpha, \beta, \gamma\in A$ such that $U_\alpha\cap U_\beta\cap U_\gamma \neq\varnothing$, then $$\tau_{\alpha,\beta}(p)\tau_{\beta,\gamma}(p) = \tau_{\alpha, \gamma}(p), \qquad p\in U_\alpha\cap U_\beta\cap U_\gamma. $$
**Def/Example:** Given a smooth manifold $M$ and smooth vector bundles $E' \to M$ and $E'' \to M$ of ranks $k'$ and $k''$, respectively, we will construct a new vector bundle over $M$ called the *Whitney sum of $E'$ and $E''$*. whose fiber at each $p\in M$ is the direct sum $E_p'\oplus E_p''$. The total space is defined as $$E' \oplus E'' := \coprod_{p\in M} (E_p' \oplus E_p''),$$with the obvious projection $\pi: E' \oplus E'' \to M$. For each $p\in M$, we choose a neighbourhood $U$ of $p$ small enough that there exists local trivialisations $(U, \Phi')$ of $E'$ and $(U, \Phi'')$ of $E''$. We now define $\Phi: \pi^{-1}[U] \to U \Bbb R^{k' + k''}$ by $$\Phi(v', v'')  = (\pi'(v'), ((\pi_{\Bbb R^{k'}}\circ \Phi')(v'), (\pi_{\Bbb R^{k''}}\circ \Phi'')(v'')).$$Suppose we are given such a pair of trivilisations $(V, \Psi')$ and $(V, \Psi'')$. Let $\tau': U \cap V \to \text{GL}(k', \Bbb R)$ and $\tau''': U \cap V \to \text{GL}(k''', \Bbb R)$ be the corresponding transition functions. Then the transition function for $E' \oplus E''$ has the form $\tau(p) := \tau'(p) \oplus \tau''(p)\in \text{GL}(k'+k'',\Bbb R)$ is the block diagonal matrix $$\begin{pmatrix} \tau'(p) & 0 \\ 0 & \tau''(p)\end{pmatrix}. $$We see that this defines a smooth vector bundle over $M$. 

**Def/Example:** Suppose $\pi: E \to M$ is a rank-$k$ vector bundle and $S\subseteq M$ is any subset. We define the *restriction of $E$ to $S$* to be the set $E|_S := \bigcup_{p\in E} E_p$, with the projection $E|_S \to S$ obtained by restricting $\pi$. If $\Phi: \pi^{-1}[U] \to U \times \Bbb R^k$ is a local trivialisation of $E$ over $U\subseteq M$, it restricts to a bijective map $\Phi|_S: ( \pi|_S)^{-1}[U \cap S] \to (U\cap S) \times \Bbb R^k$, and it is easy that these form trivialisations for a vector bundle structure on $E|_S$. If $E$ is a smooth vector bundle and $S\subseteq M$ is an immersed or embedded submanifold, it is immediate that $E|_S$ is a smooth vector bundle. In particular, if $S\subseteq M$ is a smooth, embedded or immersed, submanifold, then the restricted bundle $TM|_S$ is called the *ambient tangent bundle* over $M$. 

**Vector Bundle Constriction Theorem:** Let $M$ be a smooth manifold with or without boundary, let $\{U_\alpha\}_{\alpha\in A}$ be an open cover of $M$. Suppose for each $\alpha, \beta\in A$ such that $U_\alpha \cap U_\beta\neq \varnothing$, we are given a smooth map $\tau_{\alpha,\beta}:U_\alpha\cap U_\beta\to \text{GL}(k,\Bbb R)$ such that 
for any $\alpha,\beta,\gamma\in A$ that satisfy $U_\alpha\cap U_\beta\cap U_\gamma \neq \varnothing$, then $$\tau_{\alpha,\beta}(p)\tau_{\beta,\gamma}(p) = \tau_{\alpha, \gamma}(p), \qquad p\in U_\alpha\cap U_\beta\cap U_\gamma.  $$There is a smooth rank-$k$ vector bundle $E\to M$ with smooth local trivialisations $\Phi_\alpha: \pi^{-1}[U_\alpha] \to U_\alpha\times \Bbb R^k$ whose transition functions are the given maps $\tau_{\alpha,\beta}$. 

**Prop:** Let ${\sf Vec}_1$ be the category whose objects are finite-dimensional real vector spaces and whose morphisms are vector space isomorphisms. If $\cal F$ is a covariant functor from $\sf Vec_1$, for each finite-dimensional vector space $V$, we get a map ${\cal F}: \text{GL}(V)\to\text{GL}(\mathcal F(V))$ sending each isomorphism $A:  V\to V$ to the induced isomorphism $\mathcal F(A): \mathcal F(V) \to \mathcal F(V)$. We say that $\mathcal F$ is a *smooth functor* if this map is smooth for every $V$. Given a smooth vector bundle $E\to M$ and a smooth functor $\mathcal F: \sf Vec_1\to Vec_1$, there is a smooth vector bundle $\mathcal F(E) \to M$ whose fiber at each point $p\in M$ is $\mathcal F(E_p)$. 

**Prop:** Let $\pi: E \to M$ be a smooth vector bundle of rank $k$, let $(V, \phi)$ be a smooth chart on $M$, and suppose there exists a smooth local frame $(s_1, \dots, s_n)$ for $E$ over $V$. If we define the map $\tilde \varphi: \pi^{-1}[V] \to \phi[V] \times \Bbb R^k$ given by $$\tilde \varphi(v^i \sigma_i(p) ) = (x^1(p), \dots, x^n(p), v^1, \dots, v^k),$$then $(\pi^{-1}[V],\tilde\varphi)$ 


# Dual Bundles

Suppose $M$ is a smooth manifold and $E \to M$ is a smooth vector bundle over $M$. We define the *dual vector bundle to $E$* to be bundle $E^* \to M$ whose total space is the disjoint union $$E^* := \coprod_{p\in M} E_p ^*, $$where $E_p^*$ is the dual space of $E_p$, with the obvious projections. Then $E^* \to M$ is a smooth vector bundle whose transition functions are given by $\tau^*(p) := (\tau(p)^{-1})^*$ for any transition function $\tau: U \to \text{GL}(k,\Bbb R)$ of $E$, where $T^*$ represents the [[Dual Vector Spaces|dual linear transformation]]. 

The reason why it is smooth it is because if $E$ is locally trivialised over $U\subseteq M$ by $\phi:\pi^{-1}[U] \to U \times \Bbb R^k$, then $E^*$ is locally trivialised by $\phi^*: (\pi^*)^{-1}[U] \to U \times (\Bbb R^k)'$. Lastly, we only need that the transitions function behave nicely.
It is easy enough to check that if $\phi_\alpha: \pi^{-1}[U_\alpha] \to U_\alpha \times \Bbb R^k$ and $\phi_\beta: \pi^{-1}[U_\beta] \to U_\beta \times \Bbb R^k$ are local trivialisations with a transition function betweeen trivilisations $\tau_{\alpha\beta}$, then $$\phi_\alpha \circ (\phi_\beta^*)^{-1}(p, v) = (p, ((\tau_{\alpha \beta}(p)'))^{-1}(v)).$$
Let $\pi_E: E \to M$, and $\pi_F: F \to M$ be vector bundles over $M$, with bundle function $(\text{id}_M, \tilde f)$ from $F$ to $e$, then we can define the *dual bundle function* from $E^*$ to $F^*$, by $(\text{id}_M, \tilde f^*)$ where $$\tilde f^*(p, \lambda) := (p, \lambda \circ \tilde f_p).$$ We can generalise this to a slight broader class of bundle maps. Let $\pi_E:E \to M$ and $\pi_F: F \to N$ be two vector bundles, with a bundle map $(f, \tilde f)$ from $F$ to $E$. If $f$ is a diffeomorphism, then we can define the dual bundle map as $(f^{-1}, \tilde f^*)$ such that the following diagram commutes

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
F \arrow[d, two heads,"\pi_M"'] \arrow[r, "\tilde f^*"] & E \arrow[d, two heads,"\pi_N"]\\
M \arrow[r, "f^{-1}"'] & N
\end{tikzcd}
\end{document}
```

# Tensor Bundles

Let $\pi: E \to M$ be a smooth vector bundle over a smooth manifold $M$ of rank $r$. We can construct the 

Suppose that $E$ is a smooth vector bundle over a smooth manifold $M$, and $V\subseteq M$ is an open set with the property that for each $p\in M$, the intersection of $V$ with the fiber $E_p$ is convex and nonempty. By a 'section of $V$' we will mean a section of $E$ whose image lies in $V$. 
- There exists a smooth global section of $V$.
- Suppose $A\to V$ is a smooth section of $V$ defined on a closed subset $A\subseteq M$. There is a smooth global section $\widetilde \sigma$ of $V$ whose restriction to $A$ is equal to $\sigma$. If $V$ contains the image of the zero section of $E$, then $\widetilde \sigma$ can be chosen to be supported in any predetermined neighbourhood of $A$. 