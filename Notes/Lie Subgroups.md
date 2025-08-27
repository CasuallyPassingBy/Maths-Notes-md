---
tags:
  - GroupTheory
  - LinearAlgebra
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Lie Groups]], [[Subgroups]], [[Submersions, Immersions and Embeddings of Manifolds]], [[Smooth Submanifolds]]

**Def:** A *Lie subgroup* of Lie group $G$ is:
- an abstract subgroup $H$
- $H$ is an *immersed manifold* via the inclusion map
- the group operations on $H$ are smooth

**Prop:** If $H$ is an abstract subgroup and a embedded submanifold of a Lie group $G$, then it is a closed Lie subgroup of $G$.

**Def:** A subgroup $H$ that is a regular submanifold is called an *embedded Lie subgroup*, because the inclusion $i: H \to G$ of a regular submanifold is an embedding. 

$(*)$ **Th: (Closed subgroup theorem):** A closed subgroup of a Lie group is an embedded Lie group

# Lie Algebra of a Lie Subgroup

If $G$ is a Lie group and $H \le G$ is a Lie subgroup, we would like that the Lie algebra of $H$ a would be a Lie subalgebra of that of $G$. Strictly, speaking that is not possible since elements in $\text{Lie}(H)$ are vector fields in $H$, not $G$, and so are not even elements of $\text{Lie}(G)$. 

**Prop:** Suppose $H \le G$ is a Lie subgroup. The subset $\tilde{\mathfrak h} \subseteq \text{Lie}(G)$ define by $$\tilde{\frak h} := \{X \in \text{Lie}(G) \mid X_e \in T_e H\}$$is a Lie subalgebra of $\text{Lie}(G)$ canonically isomorphic to $\text{Lie}(H)$. 

