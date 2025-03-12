---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]], [[Topology]]
Links: [[Topological Groups]], [[Group Actions]], [[Quotient Topology]], [[Proper Maps]]

**Def:** Suppose an action of a topological group $G$ on a topological space $X$,  $\alpha: G \times X \to X$ is said be a continuous action if $\alpha$ is continuous with the product topology. We call $X$ a $G$-*space*. 

We say two points $x, y \in X$ are equivalent if they are in the same orbit, i.e., there is an element $g\in G$, such that $y = \alpha(g, x)$. Let $X/G$ be the quotient space of this equivalence relation, called the *orbit space* of the action $\alpha$. 

**Prop:** The map $\pi: X \to X/G$ is an open map. Meaning that the equivalence relation is open. 

# Proper Actions

**Def:** The action is said to be *proper* if the map $G \times X \to X \times X$ given by $(g, p) \mapsto (\alpha(g, x), x)$ is a proper map. This is *not* the same as requiring that the map $G \times X \to x$ defining the action be a proper action.

**Def:** Given an action of $G$ on $X$, for any $g \in G$ and any subset $Y \subseteq X$, we will use the notation $$\alpha(g, Y) := \{ \alpha(g, x) \mid x \in K\}$$
**Prop:** Suppose $G$ is a topological group that acts continuously on a topological space $X$. The action is proper iff for every compact subset $K \subseteq X$, the set $G_K := \{g \in G \mid \alpha(g, K) \cap K \neq \varnothing\}$ is compact.

