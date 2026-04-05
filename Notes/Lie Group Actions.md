---
tags:
  - DifferentialGeometry
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Group Actions]], [[Continuous Actions of Groups]], [[Lie Groups]], [[Representations of Groups]], [[General Linear Group]], [[Lie Algebras]], [[Lie Algebra of a Lie Group]], [[Continuous Actions of Groups#Proper Actions|Proper Actions]], [[Riemannian Metrics on Smooth Manifolds]], [[Orientations of Smooth Manifolds]]

**Def:** A smooth manifold $M$ endowed with an smooth action from a Lie group $G$ is called a *smooth $G$-space*. 

**Prop:** Suppose $E$ and $M$ are smooth manifolds with or without boundary, and  $\pi:N \to M$ is a smooth covering map. With the discrete topology, the [[Covering Maps#^78c0a4|covering group]] $\text{Aut}_\pi(N)$ is a zero dimensional Lie group acting smoothly, freely and properly on $N$. 

Suppose $G$ is a Lie group, and $M$ and $N$ are both smooth manifolds endowed with a left or right $G$-actions. A map $F:M \to N$ is said to be *equivariant* with respect to the given $G$-actions if for each $g\in G$,  $$\begin{align*} F(g \cdot p) &= g\cdot F(p) \quad \text{for left actions}  \\  F(p \cdot g) &= F(p)\cdot g \quad \text{for right actions}   \end{align*}$$
**Equivaraint Rank Theorem:** Let $M$ and $N$ be smooth manifolds and let $G$ be a Lie group. Suppose $F: M \to N$ is a smooth map that is equivariant with respect to a transitive smooth $G$-action on $M$ and any smooth action on $N$. Then $F$ has [[Rank and Local Normal Forms of Smooth Manifolds|constant rank]]. Thus, if $F$ is surjective, it is a smooth submersion, if it is injective it is a smooth immersion; and if it is bijective it is a diffeomorphism. 

Suppose $G$ is a Lie group, $M$ is a smooth manifold, and $\theta: G\times M \to M$ is a smooth left action. For each $p\in M$, we define a map $\theta^{(p)}: G\to M$ by $$\theta^{(p)}(g) = g\cdot p. $$This is often called the *orbit map*, because its image is the orbit $G \cdot p$. We see that $\theta^{(p)}\{p\}$ is just the stabiliser group $G_p$. 

**Properties of the Orbit Map:** Suppose $\theta$ is a smooth left action of a Lie group $G$ on A smooth manifold $M$. For each $p\in M$, the orbit map $\theta^{(p)}: G\to M$ is smooth and has constant rank, so the stabiliser group $G_p$ is a properly embedded Lie subgroup of $G$. If $G_p = \{e\}$, then $\theta^{(p)}$ is an injective smooth immersion, so that $G \cdot p$ is an immersed submanifold of $M$. 

**Def:** If $G$ is a Lie group smoothly on a smooth manifold $E$, we say that the action is an *orientation preserving action* if for each $g\in G$, the diffeomorphism $x\mapsto g\cdot x$ is orientation preserving. 

**Prop:** Every discrete normal subgroup of a connected Lie group is central, i.e., contained in the centre of the Lie group. 

## Semidirect Products

Suppose $H$ and $N$ are Lie groups and $\theta: H \times N\to N$ is a smooth left action of $H$ on $N$. If is said to be an *action by automorphism* if for each $h\in H$, the map $\theta_h:N  \to N$ is a group automorphism of $N$. Given such an action, we define a new Lie group $N \rtimes_\theta H$, called the *semidirect product of $H$ and $N$,* as follows. As a smooth manifold $N \rtimes_\theta H$ is just the Cartesian product $N \times H$ by the group operation is defined by $$(n, h)(n', h') = (n\theta_h(n'), hh').$$
Sometimes, if the action of $H$ on $N$ is understood or irrelevant, the semidirect product is denoted simply by $N \rtimes H$.

**Example:** We see that the [[Euclidean Group]] is actually just the semidirect product of $\Bbb R^n \rtimes \text O(n)$, where $\text O(n)$ is the [[Orthogonal Group]]. 

**Prop:** Suppose $N$ and $H$ are Lie groups, and $\theta$ is a smooth action of $H$ on $N$ by automorphism. Let $G = N \rtimes_\theta H$. 
- The subsets $\bar N = N \times \{e\}$ and $\bar H = \{e\}\times H$ are closed Lie subgroups of $G$ isomorphic to $N$ and $H$, respectively.
- $\bar N$ is a normal subgroup of $G$.
- $\bar N \cap \bar H = \{(e, e)\}$ and $\bar N\bar H = G$. 

**Characterisation of Semidirect Products:** Suppose $G$ is a Lie group, and $N, H \le G$ are closed Lie subgroups such that $N$ is normal $N \cap H = \{e\}$, and $NH ) G$. Then the map $(n, h) \mapsto nh$ is a Lie group isomorphism between $N \rtimes_\theta H$ and $G$, where $\theta: H \times N\to N$ is the action by conjugation: $\theta_h(n) = hnh^{-1}$. 

Under the hypothesis of the theorem above, we say that $G$ is the *internal semidirect product of $N$ and $H$*. 

We see that this is just the natural extension of the [[Semidirect Product of Groups]] applied to Lie groups.

**Prop:** Suppose $G$, $N$, and $H$ are Lie groups. Then $G$ is isomorphic to a semidirect product $N \rtimes H$ iff there are Lie group homomorphism $\varphi: G \to H$ and $\psi: H \to G$ such that $\varphi \circ\psi = \text{id}_H$ and $\ker \varphi \cong N$. 

## Representations

**Def:** If $G$ is a Lie group, a *(finite-dimensional) representation of $G$* is a Lie group homomorphism $\rho: G \to \text{GL}(V)$ for some finite dimensional real or complex vector space $V$. 

**Obs:** Any representation $\rho$ yields a smooth left action of $G$ on $V$, defined by $$g \cdot v := \rho(g) v, \qquad \text{for }g \in G, v \in  V$$
**Def:** If $G$ is a Lie group, an action $G$ on a finite dimensional vector space $V$ is said to be *linear* if for each $g \in G$, the map from $V$ to itself given by $v \mapsto g\cdot v$ is linear:

**Prop:** Let $G$ be a Lie group and let $V$ be a finite-dimensional vector space. A smooth action of $G$ on $V$ is linear iff it is of the form $g \cdot v = \rho(g) v$ for some representation $\rho$ of $G$.

**Def:** If a representation $\rho: G \to \text{GL}(V)$ is injective, it is said to be a *faithful representation*. 

**Obs:** By choosing a basis of $V$, we obtain a Lie group isomorphism $\text{GL}(V) \cong \text{GL}(n, \Bbb R)$ or $\text{GL}(n, \Bbb C)$, and the image of a representation $\rho: G \to \text{Gl}(V)$ is a Lie subgroup of $\text{GL}(V)$. Meaning, a Lie group admits a faithful representation iff it is isomorphic to a Lie subgroup of $\text{GL}(n, \Bbb R)$ or $\text{GL}(n, \Bbb C)$.

**Def:** If $G$ is a Lie subgroup of $\text{GL}(n , \Bbb R)$, the inclusion map $G \hookrightarrow \text{GL}(n, \Bbb R)$ is a faithful representation, called the *defining representation* of $G$. 

Let $G$ be a Lie group. For any $g \in G$, the conjugation map $C_g: G \to G$ given y $C_g(h) = ghg^{-1}$ is a Lie group homomorphism. We let $\text{Ad}(g) = (C_g)_*: \mathfrak g\to \mathfrak g$ denote its induced Lie algebra homomorphism. Because conjugation is an action of the Lie group onto itself, we get that $\text{Ad}(g_1 g_2) = \text{Ad}(g_1) \circ \text{Ad}(g_2)$, and $\text{Ad}(g)$ is invertible with $\text{Ad}(g^{-1})$. We can show that $\text{Ad}: G \to \text{GL}(\mathfrak g)$ is smooth, it follows that it is a representation, called the *adjoint representation of $G$.*

**Def:** If $\mathfrak g$ os a finite-dimensional Lie algebra, a *(finite-dimensional) representation* of $\frak g$ is a Lie algebra homomorphism $\phi: \mathfrak g \to \mathfrak{gl}(V)$ for some finite-dimensional vector space $V$. If $\phi$ is injective, it is said to be a faithful representation, in which case $\frak g$ is isomorphic to the Lie subalgebra $\phi(\mathfrak g) \subseteq \mathfrak{gl}(V) \cong \mathfrak{gl}(n, \Bbb R)$. 

**Obs:** If $\rho: G \to \text{GL}(V)$ is any representation of the Lie group $G$, then $\rho_*: \mathfrak g \to \mathfrak{gl}(V)$ is easily seen to be a representation of $\frak g$. 

$(*)$ **Ado's Theorem:** Every finite-dimensional Lie algebra admits a faithful finite-dimensional representation.

# Actions on Riemannian Manifolds

Let $(M, g)$ be a connected Riemannian manifold, and let $\Gamma$ be a Lie group, and let $\theta: \Gamma\times  M \to M$ be a group action. We say that $\Gamma$ *acts by isometries* if for each $g\in \Gamma$, the map $\theta_g: M \to M$ is Riemannian isometry. $\Gamma$ acts *discontinuously* if no $\Gamma$-orbit has a limit point in $M$. 

Acting by isometry can be also be understood as there being an group homomorphism $\theta: \Gamma\to \text{Iso}(M)$, The action being free and acting by isometry would imply that the group homomorphism is injective. 

**Prop:** If $\Gamma$ acts, freely, smoothly, and discontinuously on $M$ by isometries, then the quotient map $M \to M/\Gamma$ is a smooth covering map. 