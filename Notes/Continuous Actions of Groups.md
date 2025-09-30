---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]], [[Topology]]
Links: [[Topological Groups]], [[Group Actions]], [[Quotient Topology]], [[Proper Maps]]

**Def:** Suppose $X$ is a topological space and $G$ is a group action on $X$. The action is called an *action by homeomorphism* if for each $g\in G$, the map $x\mapsto g\cdot x$ is a homeomorphism of $X$.

**Def:** Suppose an action of a topological group $G$ on a topological space $X$,  $\alpha: G \times X \to X$ is said be a continuous action if $\alpha$ is continuous with the product topology. We call $X$ a $G$-*space*. 

**Prop:** Suppose $G$ is a topological group acting a a topological space $X$.
- If the action is continuous, then it is an action by homeomorphism.
- If $G$ has a discrete topology, then the action is continuous iff it is an action by homeomorphism.

We say two points $x, y \in X$ are equivalent if they are in the same orbit, i.e., there is an element $g\in G$, such that $y = \alpha(g, x)$. Let $X/G$ be the quotient space of this equivalence relation, called the *orbit space* of the action $\alpha$. 

**Prop:** The map $\pi: X \to X/G$ is an open map. Meaning that the equivalence relation is open. 

**Hausdorff Criterion for Orbit Spaces:** Suppose $E$ is a topological space and $\Gamma$ is a group acting on $E$ by homeomorphisms. The following statements are equivalent:
-  Then $E/\Gamma$ is Hausdorff.
- If $e, e'\in E$ lie in different orbits, there exists neighbourhoods $U$ of $e$ and $V$ of $e'$ such that $U \cap (g\cdot V) = \varnothing$ for all $g\in \Gamma$. 