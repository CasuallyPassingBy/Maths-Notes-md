---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Topological Manifolds]]

# $\mathcal C^\infty$-compatible Charts

**Def:** Two charts $(U, \varphi: U \to \Bbb R^n)$ and $(V, \psi: V\to \Bbb R^n)$ of a topological manifold are $\mathcal C^\infty$*-compatible* if the two maps $$\phi \circ \psi^{-1}: \psi[U \cap V] \to \phi[U \cap V], \qquad \psi \circ \phi^{-1}: \phi[U \cap V] \to \psi[U \cap V]$$are $\mathcal C^\infty$. These two maps are called the *transition functions* between the charts. If $U\cap V = \varnothing$, the the two charts are automatically $\mathcal C^\infty$-compatible. To simplify the notation, we will sometimes write $U_{\alpha \beta}$ for $U_\alpha\cap U_\beta$ and $U_{\alpha\beta\gamma}$ for $U_\alpha \cap U_\beta\cap U_\gamma$. Since we are interested in only $\mathcal C^\infty-$compatible chars, we often omit mention of "$\mathcal C^\infty$" and speak simply of compatible charts.

**Def:** A $\mathcal C^\infty$ *atlas* is on locally Euclidean space $M$ is a collection of charts $\mathfrak U =\{(U_\alpha, \varphi_\alpha) \mid \alpha<\kappa\}$ of pairwise $\mathcal C^\infty$-compatible charts that cover $M$. Lastly, we say that a chart $(U, \psi)$ is *compatible with an atlas* $\mathfrak U$ it it is $\mathcal C^\infty$-compatible with all the charts of $\mathfrak U$. If the context is clear, $\mathcal C^\infty$ *atlas* will be refereed as atlas. 

**Lemma:** Let $\mathfrak U$ be an atlas on a locally Euclidean space. If two charts $(U, \phi)$ and $(V, \psi)$ are both compatible with the atlas $\mathfrak U$, then they are compatible with each other.

# Smooth  or Differentiable Manifolds 

**Def:** A *smooth* or $\mathcal C^\infty$ manifold is a topological manifold $M$ together with a maximal atlas. The maximal atlas is also called a *differentiable structure* on $M$. 

**Prop:** Any atlas $\mathfrak U$ on a locally Euclidean space is contained in a unique maximal atas. 

**Prop:** Two smooth atlases for $M$ determine the same maximal smooth atlas iff their union is a smooth atlas.

**Prop:** Let $\mathfrak U$ be the maximal atlas on a manifold $M$. For any open set $U$ in $M$ and a point $p\in U,$ there existes a coordinate open set $U_\alpha$ such that $p \in U_\alpha \subseteq U$.

in the context of manifolds, we denote the standard coordinates in $\Bbb R^n$ by $r^1, \dots, r^n$. If $(U, \phi: U \to \Bbb R^n)$ is a char on a manifold, we let $x^i = r^i \circ \phi$ be the $i$th component and write $\phi = (x^1, \dots, x^n)$  and $(U, \phi) = (U, x^1, \dots, x^n)$. Thus, for $p \in U$, $(x^1(p), \dots, x^n(p))$ is a point in $\Bbb R^n$. The functions $x^1, \dots, x^n$ are called *coordinates* or *local coordinate* on $U$. By abuse of notation, we sometimes omit the $p$. So the notation $(x^1, \dots, x^n)$ stands alternatively for local coordinates on the open set $U$ and por a point in $\Bbb R^n$. By a *chart $(U, \phi)$ about $p$* in a manifold $M$, we will mean a chart in the differentiable structure of $M$ such that $p\in U$. 

**Example:** If $M$ and $N$ $\mathcal C^\infty$ manifold, then $M \times N$ with its product topology is Hausdorff and second countable. 

**Smooth Manifold Construction Lemma:** Let $M$ be a set, and suppose you are given a collection $\{U_\alpha \mid \alpha < \kappa\}$ of subsets of $M$, together with an injective map $\phi_\alpha: U_\alpha \to \Bbb R^n$ for each $\alpha < \kappa$, such that the following properties are satisfied:
- For each $\alpha < \kappa$, $\phi_\alpha[U_\alpha]$ is an open subset of $\Bbb R^n$. 
- For each $\alpha, \beta <\kappa$, $\phi_\alpha[U_\alpha \cap U_\beta]$ and $\phi_\beta[U_\alpha \cap U_\beta]$ are open in $\Bbb R^n$. 
- Whenever $U_\alpha \cap U_\beta \neq \varnothing$, $\phi_\alpha \circ \phi^{-1}_\beta: \phi_\beta[U_\alpha\cap U_\beta] \to \phi_\alpha[U_\alpha \cap U_\beta]$ is a diffeomorphism.
- there's a $C \in [\{U_\alpha \mid \alpha < \kappa\}]^{\le \omega}$ such that $\bigcup C = M$.
- Whenever $p, q$ are distinct points in $M$, either there exists some $U_\alpha$ containing both $p$ and $q$ or there exists disjoint sets $U_\alpha, U_\beta$ with $p\in U_\alpha$ and $q \in U_\beta$.
Then $M$ has a unique smooth manifold structure such that each $(U_\alpha, \phi_\alpha)$ for $\alpha < \kappa$ is a smooth chart. 

**Prop:**  If $\mathfrak U$ and $\mathfrak V$ are $\mathcal C^\infty$ atlases for the manifolds $M$ and $N$ of dimension $m$ and $n$, respectively, then the collection $$\{(U\times V, \phi \times \psi: U\times V \to \Bbb R^n \times \Bbb R^n) \mid (U, \phi)\in \mathfrak U, (V, \psi)\in \mathfrak V \}$$of charts is $\mathcal C^\infty$ atlas on $M \times N$. Therefore, $M \times N$ is a $\mathcal C^\infty$ manifold of dimension $m + n$.

**Def:** If $M$ is a smooth manifold, we say that an open cover $\{W_n \mid n < \omega\}$ of $M$ is *regular* it it satisfies the following properties:
- The cover $\{W_n\}_{n < \omega}$ is locally finite.
- Each $W_n$ is the domain of a smooth coordinate map $\phi_n: W_n \to \Bbb R^k$ where $\phi[W_n] \subseteq B(0, 3)$
- The collection $\{U_n \mid n < \omega\}$ still covers $M$, where $U_n = \phi_n^{-1}[B(0, 1)]$. 

**Prop:** Let $M$ be a smooth manifold. Every open cover of $M$ has a regular refinement. In particular, $M$ is paracompact.

# Manifolds with Boundary

We would like to define a smooth structure on a manifold with boundary. Recall that a smooth map from an arbitrary subset $A\subseteq \Bbb R^n$ to $\Bbb R^m$ is defined to be a map that admists a smooth extension to an open neighbourhood of each point. Thus if $U$ is an open subset of $\Bbb H^n$, a map $F: U \to \Bbb R^k$ is smooth if for each $x\in U$, there exists an open set $V\subseteq \Bbb R^n$ and a smooth map $\tilde F: V \to \Bbb R^k$ that agrees with $F$ in $V \cap \Bbb H^n$. If $F$ is such map, the restriction of $F$ to $U \cap \text{Int}(\Bbb H^n)$ is smooth in the usual sense. 

We can see that continuity makes the partial derivative of $F$ at $U \cap \partial \Bbb H^n$ are determined by their values in $U \cap \text{Int}(\Bbb H^n)$, and therefore in particular are independent of the choice of extension. 

Let $M$ be a topological manifold with boundary. Just as in the manifold case, a smooth structure for $M$ is defined to be a maximal smooth atlas. With such a structure $M$ is called a *smooth manifold with boundary*. a point $p\in M$ is called a *boundary point* if its image under some smooth chart is in $\partial \Bbb H^n$, and an interior if its image under some smooth chart is in $\text{Int}(\Bbb H^n)$. The *boundary* of $M$, the set of all boundary points, is denoted by $\partial M$; similarly, its *interior*, the set of all interior points, is denoted by $\text{Int}(M)$. 

We can see that if $M$ is a smooth manifold with boundary, then $\text{Int}(M)$ is a smooth manifold.