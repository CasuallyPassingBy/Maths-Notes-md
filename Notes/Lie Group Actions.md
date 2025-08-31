---
tags:
  - DifferentialGeometry
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Group Actions]], [[Continuous Actions of Groups]], [[Lie Groups]], [[Representations of Groups]], [[General Linear Group]], [[Lie Algebra]], [[Lie Algebra of a Lie Group]], [[Continuous Actions of Groups#Proper Actions|Proper Actions]]

**Def:** A smooth manifold $M$ endowed with an smooth action from a Lie group $G$ is called a *smooth $G$-space*. 
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

**Equivariant Rank Theorem:** Let $M$ and $N$ be smooth manifolds and let $G$ be a Lie group. Suppose $F: M \to N$ is a smooth map that is equivariant with respect to a transitive smooth $G$-action on $M$ and any smooth $G$-action on $N$. Then $F$ has constant rank. In particular, its level sets are closed embedded submanifolds of $M$. 

This is a consequence of the [[Submersions, Immersions and Embeddings of Manifolds#^815841|Constant Rank Theorem]].

**Prop:** Let $F: G \to H$ be a Lie group homomorphism. The kernel of $F$ is an embedded Lie subgroup of $G$, whose codimension is equal to the rank of $F$. 

**Prop:** Any continuous action by a compact Lie group on manifold is proper.

**Quotient Manifold Theorem:** Suppose a Lie group $G$ acts smoothly, freely, and properly on a smooth manifold $M$. Then the *orbit space* $M/G$ is a topological manifold of dimension equal to $\dim M - \dim G$, and has a unique smooth structure with the property that the quotient map $\pi: M \to M/G$ is a smooth submersion.

**Prop:** Let $\pi:N \to M$ be a smooth covering map. With the discrete topology, the [[Covering maps#^78c0a4|covering group]] $\mathcal C_\pi(N)$ is a zero dimensional Lie group acting smoothly, freely and properly on $N$. 

**Th:** Suppose $M$ is a connected smooth manifold, and $\Gamma$ is a discrete group acting smoothly, freely and properly on $M$. Then the quotient space $M/\Gamma$ is a topological manifold and has a unique smooth structure such that $\pi: M \to M/\Gamma$ is a [[Smooth Covering Maps|smooth]] [[Covering maps#^06bb5b|normal]] covering map.