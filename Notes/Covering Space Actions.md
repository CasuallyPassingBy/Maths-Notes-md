---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Group Actions]], [[Covering Maps]], [[Covering Group]]

**Def:** Suppose we are given an action by a group $\Gamma$ on a topological space $E$. It is called a *covering space action* if $\Gamma$ acts by homeomorphism and every point $e\in E$ has a neighbourhood $U$ satisfying the following condition: $$U \cap (g \cdot U) \neq \varnothing \iff g = 1.$$
We get an even stronger property, that *all* of its images under elements of $\Gamma$ are pairwise disjoint: if $g, h\in \Gamma$ are distinct elements, then $(g\cdot U) \cap (h\cdot U) = g \cdot(U \cap gh^{-1}\cdot U) = \varnothing$.

Let us note that if $\Gamma$ acts on a topological space $E$ by homeomorphism, then there exists a group homomorphism $\varphi: \Gamma \to \text{Homeo}(E)$. 

**Obs:** For any covering $q: E \to X$, the action $\text{Aut}_q(E)$ on $E$ is a covering space action. 

**Obs:** Given a covering space action of a group $\Gamma$ on a topological space $E$, then the restriction of the action to any subgroup of $\Gamma$ is a covering space action.

Covering space actions are often called *properly discontinuous actions*. 

**Def:** Given an action of a group $\Gamma$ on a space $E$ by homeomorphism, each $g\in \Gamma$ determines a homeomorphism from $E$ to itself by $e \mapsto g\cdot e$. We say that the action is *effective* if the identity of $\Gamma$ is the only element for which this homeomorphism is the identity. 

We see that every free action is effective. If $\Gamma$ acts effectively, it is frequently useful to identify $\Gamma$ with the corresponding group of homeomorphisms of $E$. 

Using the group homomorphism because $\Gamma$ acts on $E$ by homeomorphism, then the action of $\Gamma$ is effective iff $\Phi: \Gamma \to \text{Homeo}(E)$ is injective. 