---
tags:
  - Topology
  - GroupTheory
---
Subjects: [[Topology]], [[Group Theory]]
Links: [[Group Actions]], [[Topological Spaces]], [[Topological Manifolds]]

**Def:** Let $X$ be a non-empty set and $G$ be a group. Then $X$ is called a $G$-space if it is equipped with an action of $G$ on $X$. A homogeneous space is a $G$-space on which $G$ acts transitively. The elements of $G$ are called the *symmetries* of $X$.

If  is an object of the category $\mathsf{C}$, then the structure of $G$-space is a group homomorphism $\rho: G \to \text{Aut}_\mathsf{C}(X)$ into the group of automorphism of the object $X$ in the category $\mathsf{C}$. The pair $(X, \rho)$ defines a homogeneous space provided $\rho(G)$ is a transitive group of symmetries of the underlying object $X$. 

**Examples:**
* If $X$ is a topological space, then group elements are assumed to act as homeomorphism on $X$. The structure of a $G$-space is a group homomorphism $\rho: G \to \text{Homeo}(X)$ into the homeomorphism group of $X$.
* If $X$ is a smooth manifold, then the group elements are diffeomorphisms. The structure of a $G$-space is a group of homomorphism $\rho: G \to \text{Diffeo}(X)$ into the diffeomorphism group of $X$.

**Def:** A *principal homogeneous space*, or *torsor* for a group $G$ is a homogeneous space $X$ for $G$ in which the stabiliser group of every point is trivial. Equivalently, a principal homogeneous group $G$ is a non-empty set $X$ on which $G$ acts freely and transitively. 