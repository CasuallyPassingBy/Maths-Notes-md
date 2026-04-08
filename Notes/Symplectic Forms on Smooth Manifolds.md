---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Differential Forms on Smooth Manifolds]], [[Symplectic Vector Spaces]], [[The Exterior Derivative on Smooth Manifolds]], [[Embedded Smooth Submanifolds]], [[Time-Dependent Vector Fields and Flows]], [[Contact Structures on Smooth Manifolds]], [[The de Rham Cohomology Groups]]

**Def:** A *symplectic form* on a smooth manifold $M$ is a smooth, closed, nondegenerate $2$-form. In other words, a smooth $2$-form is symplectic iff it is closed and $\omega_p$ is a symplectic tensor. A smooth manifold endowed with a specific choice a symplectic form is called a *symplectic manifold*. A choice of symplectic form is also sometimes called a *symplectic structure* on $M$. A symplectic manifold $(M, \omega)$ is exact iff the symplectic form $\omega$ is exact.

**Obs:** We see that a symplectic manifold must be even-dimensional. We see that if $\omega$ is a symplectic form on a $2n$-manifold, then $\omega^n$ is a $2n$-form. so every symplectic manifold is orientable. 

We know that a symplectic manifold must be even-dimensional. 

**Def:** If $(M, \omega)$ and $(\widetilde M, \widetilde \omega)$ are symplectic manifolds, a diffeomorphism $F: M \to \widetilde  M$ satisfying $F^*\widetilde \omega = \omega$ is called a *symplectomorphism*. 

The study of properties of symplectic manifold that are invariant under symplectomorphisms is known as *symplectic geometry*. 

**Examples:**
- If we denote the standard coordinates on $\Bbb R^{2n}$ by $(x^1,y^1\dots, x^n, y^n)$, the $2$-form$$\omega = \sum_{i = 1}^n dx^i \wedge dy^i $$is symplectic. This is called the *standard symplectic form* on $\Bbb R^{2n}$. 
- Suppose $\Sigma$ is any smooth $2$-manifold and $\Omega$ is any nonvanishing $2$-form on $\Sigma$. Then $\omega$ is closed because $d\Omega$ is a $3$-form, and every $3$-form on a $2$-manifold is zero. Moreover, every nonvanishing $2$-form is nondegenerate, so $(\Sigma, \Omega)$ is a symplectic manifold.

**Def:** Suppose $(M,\omega)$ is a symplectic manifold. An (immersed or embedded) submanifold $N\subseteq M$ is said to be symplectic, isotropic, coisotropic, or Lagrangian if $T_p N$, as a subspace of $T_p M$, has this property at each point $p\in N$. more generally, an immersion (or embedding) $F: N \to M$ is said to have one these properties if the subspace $F_*[T_p  N] \subseteq T_{F(p)} M$ has the corresponding property for every $p\in N$. Thus a manifold is symplectic, isotropic, coisotropic or Lagrangian iff its inclusion map has the same property. 

**Prop:** Suppose $(M, \omega)$ is a symplectic manifold, and $F: N \to M$ is an immersion. Then $F$ is isotropic iff $F^*\omega = 0$, and $F$ is symplectic iff $F^*\omega$ is a symplectic form. 

**Prop:** Let $(M, \omega)$ be a symplectic manifold, and suppose $F: N \to M$ is a smooth map. If $F^*\omega$ is symplectic, then $F$ is an immersion. 

**Prop:** Suppose $(M, \omega)$ is an $2n$-dimensional compact symplectic manifold.
- $\omega^n$ is not exact.
- $H^{2p}_\text{dR}(M) \neq 0$ for $p = 1, \dots, n$.
- This means that $\Bbb S^2$ is the only sphere that admits a symplectic structure.

**Prop:** Let $(M, \omega)$ and $(N,\eta)$ be symplectic manifold. We define a $2$-form $\Omega$ on $M \times N$ by$$\Omega := \pi_1^*\omega - \pi_2^*\eta, $$where $\pi_1: M \times N\to M$ and $\pi_2: M \times N \to N$ are projections. We see that $\Omega$ is symplectic. If $F: M \to N$ is a diffeomorphism, and let $\Gamma(F)\subseteq M \times N$, where $$\Gamma(F) := \{(x, F(x))\in M\times N\mid x\in M\},$$ then $F$ is a symplectomorphism iff $F$ is a Lagrangian submanifold of $(M \times N, \Omega)$. 

**Def:** Suppose $(M, \omega)$ is a symplectic manifold and $S\subseteq M$ is a coisotropic submanifold. An immersed submanifold $N\subseteq S$ is said to be *characteristic* if $T_pN = (T_pS)^\bot$ for each $p\in N.$

**Prop:** Suppose $(M, \omega)$ is a symplectic manifold and $S\subseteq M$ is a coisotropic submanifold. There is a foliation of $S$ by connected characteristic submaniolds of $S$ whose codimension is equal to the codimension of $S$ in $M$.

**Prop:** We see that $N^*S$ is a smooth subbundle of $T^*M|_S$, and an embedded [[Symplectic Forms on Smooth Manifolds|Lagrangian]] submanifold of $T^*M$. 

# The Canonical Symplectic Form on the Cotangent Bundle

The most important example of a symplectic manifold is the total space of the cotangent bundle of any smooth manifold $Q$, which carries a canonical symplectic structure. 

There is a natural $1$-form $\tau$ on $M = T^*Q$, called the *tautological $1$-form*, A point in $T^*Q$ is a covector $\varphi\in T_q^*Q$ for some $q\in Q$; we will denote such a point by the notation $(q, \varphi)$. The natural projection $\pi: T^*Q \to Q$ is then just $\pi(q, \varphi) = q$, and its pullback is a linear map $\pi^*: T_q^*Q \to T_{(q, \varphi)} (T^*Q)$. We define $\tau\in \Omega^1(T^*Q)$ by $$ \tau_{(q, \varphi)}(X) := \varphi(d\pi_{q, \varphi}(X)). $$
**Prop:** Let $M$ be a smooth manifold of dimension at least $1$. There is no $1$-form on $M$ such that the tautological form $\tau\in \Omega^1(T^*M)$ is equal to the pullback $\pi^*\sigma$. 

**Prop:** Let $Q$ be a smooth manifold. The tautological $1$-form $\tau$ is smooth, and $\omega = -d\tau$ is a symplectic form on the total space of $T^*Q$. 

The symplectic form defined in this proposition is called the *canonical symplectic form* on $T^*Q$. 

**Prop:** Let $M$ be a smooth manifold, and let $\sigma$ be a smooth $1$-form on $M$. Thought of as a map from $M \to T^*M$, $\sigma$ is a smooth embedding, and $\sigma$ is closed iff its image $\sigma[M]$ is a Lagrangian submanifold. 

This proof gives us coordinate representations of $\tau$ and $\omega$. Let $(x^i)$ be any smooth coordinates on $Q$, and let $(x^i, \xi_i)$ denote the corresponding standard coordinates on $T^*Q.$We see that $$\tau_{(x, \xi)} = \xi_i \, dx^i$$and $$\omega = -d\tau =\sum_{i } dx^i\wedge d\xi_i.$$
Let us note that in the proof we get the result that $\sigma^*\omega = - d\sigma$. And we see that $\sigma$ is a Lagrangian embedding iff $d\sigma = 0$. 

**Prop:** Suppose $Q$ and $\widetilde Q$ are smooth manifolds $F: Q \to \widetilde Q$ is a diffeomorphism. Let $dF^*: T^*\widetilde Q \to T^*Q$ be the smooth bundle homomorphism induced by $F$. Then $dF^*$ is a symplecteorphism when $T^*Q$ and $T^*\widetilde Q$ are endowed with their canonical symplectic form.

**Prop:** Let $Q$ be a smooth manifold, and let $S$ be an embedded Lagrangian submanifold of the total space of $T^*Q$.
- If $S$ is [[Transversailty Theorems for Smooth Manifolds|transverse]] to the fibre of $T^*Q$ at a point $q\in T^*Q$, then there exists a neighbourhood $V$ of $q$ in $S$ and a neighbourhood $U$ of $\pi(q)$ in $Q$ such that $V$ is the image of a smooth closed $1$-form defined on $U$.
- $S$ is the image of a globally defined closed $1$-form on $Q$ iff $S$ intersects each fibre transversly in exactly one point.

# The Darboux Theorem

**Obs:** Let $(M, \omega)$ be a symplectic manifold. Since $\omega$ is nondegenerate, there is a smooth bundle isomorphism $\widehat\omega : TM \to T^*M$ defined by $\widehat \omega(X) := X \;\lrcorner \;\omega$. 

**The Darboux Theorem:** Let $(M, \omega)$ be an $2n$-dimensional symplectic manifold. For any $p\in M$, there are smooth coordinates $(x^1,\dots, x^n, y^1,\dots, y^n)$ centred at $p$ in which $\omega$ has the coordinate representation $$\omega = \sum_{i = 1}^n dx^i\wedge dy^i. $$
Any coordinates satisfying the theorem above are called *Darboux coordinates, symplectic coordinates* or *canonical coordinates*. 

**Prop:** Let $M$ be a compact smooth manifold, and let $\omega_0$ be a symplectic for on $M$. Suppose there is a smooth time-dependent $1$-form $\alpha:[0, 1] \times M \to T^*M$ such that $\omega_t + d\alpha_t$ is symplectic for each $t\in [0, 1]$. Then there is a diffeomorphism $F: M \to M$ such that $F^*\omega_1 = \omega_0$. 