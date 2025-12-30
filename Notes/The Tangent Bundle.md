---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Tangent Space for Manifolds]], [[Tangent Vectors in Rn]], [[Topological Manifolds]], [[Smooth Manifolds]], [[Vector Bundles on Smooth Manifolds]]

Let $M$ be a smooth manifold. The *tangent bundle* of $M$ is the union of all the tangent spaces of $M$: $$TM = \coprod_{p \in M} T_p M$$In the definition of the tangent bundle, the union $$\coprod_{p\in M} T_p M$$is the same as the disjoint union $TM = \coprod_{p \in M} T_p M$, since for distinct points $p$ and $q$ in $M$, the tangent spaces $T_p M$ and $T_q M$ are already disjoint.

There is a natural map $\pi: TM \to M$ given by $\pi(v) = p$ if $v\in T_p M$. We can make the connection more obvious and write a tangent vector $v \in T_p M$ as a pair $(p, v), to make explicit the point $p\in M$ at which $v$ is a tangent vector. 

We would like to give the tangent bundle a topology.

If $(U, \phi) = (U, x^1, \dots, x^n)$ is a coordinate chart on $M$, let $$T U = \coprod_{p\in U} T_p U = \bigcup_{p\in U} T_p M.$$At a point $p\in U$, a basis for $T_p M$ is the set of coordinate vectors $\left\{\left.\dfrac{\partial}{\partial x^i}\right\rvert_p\right\}$, so a tangent vector $v\in T_p M$ is uniquely a linear combination $$v = \sum_{i = 1}^n c^i \left.\dfrac{\partial}{\partial x^i}\right\rvert_p.$$In this expression the coefficients $c^i = c^i(v)$ depend on $v$ and so are function on $TU$. Let $\tilde \phi: TU \to \phi[U] \times \Bbb R^n$ by $$ v \mapsto (x^1(p), \dots, x^n(p), c^1(v), \dots, c^n(v))$$Then $\tilde \phi$ has an inverse: $$(\phi(p), c^1, \dots, c^n) \mapsto \sum_{i = 1}^n c^i\left.\dfrac{\partial}{\partial x^i}\right\rvert_p. $$With this we can transfer the topology of $\phi[U] \times \Bbb R^n$ to $TU$: a set $A$ in $TU$ is open iff $\tilde \phi[A]$ is open in $\phi[U] \times \Bbb R^n$. By definition $TU \cong \phi[U] \times \Bbb R^n$ (topologically). Hence the relative topology of $TV$ as a subset of $TU$ is the same as the topology induced from the bijection $\tilde\phi|_{TV}: TV \to \phi[V] \times \Bbb R^n$.

Another way to write $\tilde\phi = (\phi \circ \pi, \phi_*)$, where $\phi_*$ is the differential of $\phi$. This is because $\phi_*: T_p U \to T_{\phi(p)} (\Bbb R^n)$, and $T_{\phi(p)} (\Bbb R^n) \cong \Bbb R^n$ (as vector spaces). 

**Lemma:** 
- Let $\mathcal B$ be the collection of all open subsets of $TU$, for $U \in \mathfrak M$, where $\mathfrak M$ is the maximal atlas of $M$: $$\mathcal B := \{ A \subseteq TM \mid \exists (U, \phi) \in \mathfrak M [A \text{ is open in } TU]\}$$For any manifold $M$, the set $TM = \bigcup \mathcal B$.   
- Let $U$ and $V$ be coordinate open sets in a manifold $M$. If $A$ is open in $TU$ and $B$ is open in $TV$, then $A\cap B$ is open in $T(U \cap V)$. 

**Lemma:** A manifold $M$ has a countable basis consisting of coordinate open sets.}

**Prop:** The tangent bundle $TM$ of a manifold $M$ is second countable

**Prop:** The tangent bundle $TM$ of a manifold $M$ is Hausdorff

**Cor:** $TM$ is a topological manifold

**Prop:** If $\{(U_\alpha, \phi_\alpha) \mid \alpha < \kappa\}$ is a $\mathcal C^\infty$ atlas for $M$, then $\{(TU_\alpha, \tilde \phi_\alpha)\mid \alpha < \kappa\}$ is a $\mathcal C^\infty$ atlas for the tangent bundle $TM$, where $\tilde \phi_\alpha$ is the map on $TU_\alpha$ by $\phi_\alpha$, $\tilde\phi_\alpha = (\phi_\alpha \circ \pi, (\phi_\alpha)_*)$. 

**Cor:** The tangent bundle $TM$ is a $\mathcal C^\infty$ with $\{(TU_\alpha, \tilde \phi_\alpha)\mid \alpha < \kappa\}$ as a $\mathcal C^\infty$ atlas.

**Lemma:** Let $M$ be a smooth $n$-manifold. The smooth manifold structure on $TM$ is the unique one with respect to which $\pi: TM \to M$ is a smooth vector bundle of rank $n$ over $M$ and all coordinate vector fields are smooth local sections. 

**Def:** A manifold whose tangent bundle is trivial is said to be *paralelisable*. 

**Prop:** If $M$ is a smooth manifold of dimension $n$, parallelisability is equivalent of the existence of a smooth frame $X_1, \dots, X_n$ on $M$, and $TM$ being diffeomorphic $M \times \Bbb R^n$.  

**Prop (Transition functions for the total space of the tangent bundle):** Let $(U, \phi) = (U, x^1, \dots, x^n)$ and $(V, \psi) = (V, y^1, \dots, y^n)$ be overlapping coordinate charts on a manifolds $M$. They induce coordinate charts $(TU, \tilde \phi)$ and $(TV, \tilde \psi)$ on the total space $TM$ of the tangent bundle, with transition function $\tilde \psi \circ \tilde \phi^{-1}$: $$(x^1, \dots, x^n, a^1, \dots, a^n) \mapsto (y^1, \dots, y^n, b^1, \dots, b^n)$$
If we want to calculate the Jacobian matrix of the transition function $\tilde \psi \circ \tilde \phi^{-1}$ at $\phi(p)$, we need to calculate 4 derivatives:
- $\dfrac{\partial y^i}{\partial x^j}$ (this is already done)
- $\dfrac{\partial y^i}{\partial a^j} = 0$
$$\dfrac{\partial b^i}{\partial x^j} = \dfrac{\partial a^k}{\partial x^j}\dfrac{\partial y^i}{\partial x^k}+ a^k \dfrac{\partial^2 y^i}{\partial x^j\partial x^k}$$
- $\dfrac{\partial b^i}{\partial a^j} = \dfrac{\partial y^i}{\partial x^j}$

I am going to make a slight abuse of notation, where 
- $\dfrac{\partial y}{\partial x} = \left[\dfrac{\partial y^i}{\partial x^j}\right]$
- $\dfrac{\partial y}{\partial a} = \left[\dfrac{\partial y^i}{\partial a^j}\right] = 0$
- $\dfrac{\partial b}{\partial x} = \left[\dfrac{\partial b^i}{\partial x^j}\right]$
- $\dfrac{\partial b}{\partial a} = \left[\dfrac{\partial b^i}{\partial a^j}\right]= \left[\dfrac{\partial y^i}{\partial x^j}\right]$

Then the Jacobian is $$J(\tilde \psi \circ \tilde \phi^{-1})(\phi(p)) =
\begin{bmatrix}
\dfrac{\partial y}{\partial x} & \dfrac{\partial y}{\partial a} \\
\dfrac{\partial b}{\partial x} & \dfrac{\partial b}{\partial a}
\end{bmatrix} = 
\begin{bmatrix}
\dfrac{\partial y}{\partial x} & 0 \\
\dfrac{\partial b}{\partial x} & \dfrac{\partial y}{\partial x}
\end{bmatrix} 
$$
The Jacobian determinant of the transition function $\tilde \psi\circ \tilde \phi^{-1}$ at $\phi(p)$ is $\left(\det\left(\dfrac{\partial y}{\partial x}\right)\right)^2$. 

By putting the differentials of $F$ at all pionts of $M$, we obtained a globally defined map between tangent bundles, called the *global differential* or *global tangent map* and denoted by $dF: TM \to TN$. This is just the map whose resctriction to each tangent space $T_p M\subseteq TM$ is $dF_p$. 

**Prop:** If $F:M \to N$ is a smooth map, then its global differential $dF: TM \to TN$ is a smooth map. 

**Cor:** Suppose $F: M \to N$ and $G: N \to P$ are smooth maps.
- $d(G\circ F) = dG \circ dF$. 
- $d(\text{id}_M) = \text{id}_{TM}$.
- If $F$ is a diffeomorphism, then $dF: TM \to TN$ is also a diffeomorphism, and smooth vector bundle isomorphism, and $(dF)^{-1} = d(F^{-1}).$