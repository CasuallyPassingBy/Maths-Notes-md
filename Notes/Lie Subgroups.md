---
tags:
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Lie Groups]], [[Subgroups]], [[Submersions, Immersions and Local Diffeomorphism of Smooth Manifolds]], [[Immersed Smooth Submanifolds]], [[Embedded Smooth Submanifolds]], 

**Def:** A *Lie subgroup* of Lie group $G$ is:
- an abstract subgroup $H$
- $H$ is an *immersed manifold* via the inclusion map
- the group operations on $H$ are smooth

**Def:** Suppose $G$ is an arbitrary Lie group and $H \le G$ is an *open subgroup*, a subgroup that is also an open subset. Similarly, we say that $H \le G$ is a *closed subgroup* if $H$ is a closed subset of $G$ and a subgroup. 

**Prop:** Let $G$ be a Lie group, and suppose $H\le G$ is a subgroup that is also an embedded submanifold. Then $H$ is a Lie subgroup. 

**Lemma:** Suppose $G$ is a Lie group and $H\le G$ is an open subgroup. Then $H$ is an embedded Lie subgroup. In addition, $H$ is closed so it is a union of connected components of $G$. 

**Prop:** Suppose $G$ is a Lie group, and $W\subseteq G$ is any neighbourhood of the identity. 
- $W$ generates an open subgroup of $G$.
- if $W$ is connected, it generates a connected open subgroup of $G$.
- If $G$ is connected, then $W$ generates $G$. 

**Def:** If $G$ is a Lie group, the connected component of $G$ containing the identity is called the *identity component of $G$.

**Prop:** Let $G$ be a Lie group and let $G_0$ be its identity component. Then $G_0$ is a normal subgroup of $G$, and it is the only connected open subgroup. Every connected component of $G$ is diffeomorphic to $G_0$. 

**Prop:** Let $F: G\to H$ be a Lie group homomorphism. The kernel of $F$ is a properly embedded Lie subgroup of $G$, whose codimension is equal to the rank of $F$. 

**Prop:** If $F: G \to H$ is an injective Lie group homomorphism, then image of $F$ has a unique manifold structure such that $F[G]$ is a Lie subgroup of $H$ and $F:G \to F[G]$ is a Lie group isomorphism,

**Th:** Suppose $G$ is a Lie group and $H \le G$ be a Lie subgroup. Then $H$ is closed in $G$ iff it is embedded. 

**[[The Exponential Map on Lie Groups#The Closed Subgroup Theorem|Closed Subgroup Theorem]]:** Suppose $G$ is a Lie group and $H\subseteq G$ is a subgroup that is also a closed subset of $G$. Then $H$ is an embedded Lie subgroup. 

# Lie Algebra of a Lie Subgroup

If $G$ is a Lie group and $H \le G$ is a Lie subgroup, we would like that the Lie algebra of $H$ a would be a Lie subalgebra of that of $G$. Strictly, speaking that is not possible since elements in $\text{Lie}(H)$ are vector fields in $H$, not $G$, and so are not even elements of $\text{Lie}(G)$. 

**Prop:** Suppose $H \le G$ is a Lie subgroup. The subset $\tilde{\mathfrak h} \subseteq \text{Lie}(G)$ define by $$\tilde{\frak h} := \{X \in \text{Lie}(G) \mid X_e \in T_e H\}$$is a Lie subalgebra of $\text{Lie}(G)$ canonically isomorphic to $\text{Lie}(H)$. 

# Lie Subalgebras

**Def:** A [[Tangent Distributions and Involutivity on Smooth Manifolds|distribution]] $D$ on a Lie group $G$ is said to be *left-invariant* if it is invariant under every left translation. Meaning that $dL_g[D] = D$ for each $g\in G$.

**Lemma:** Let $G$ be a Lie group, if $\frak h$ is a Lie subalgebra of $\text{Lie}(G)$, then the subset $D = \bigcup_{g\in G}D_g \subseteq TG$, where  $$D_g := \{X_g\mid X \in \mathfrak h\}\subseteq T_g G, $$is a left invariant involutive distribution on $G$.

**Lie Subgroups Are Weakly Embedded:** Every Lie subgroup is an integral manifold of an involutive distribution, and therefore is a weakly embedded submanifold.

**The Lie Subgroup Associated with a Lie Subalgebra:** Suppose $G$ is a Lie group and $\frak g$ is its Lie algebra. If $\frak h$ is any Lie subalgebra of $\frak g$, then there is a unique connected Lie subgroup of $G$ whose Lie algebra is $\frak h$.

The proof uses [[Foliations on Smooth Manifolds|foliations]]. 