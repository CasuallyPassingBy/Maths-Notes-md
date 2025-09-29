---
tags:
  - GroupTheory
  - Topology
---
Subjects: [[Group Theory]], [[Topology]]
Links: [[Topological Groups]], [[Continuous Actions of Groups]], [[Proper Maps]]

**Def:** The action is said to be *proper* if the map $G \times X \to X \times X$ given by $(g, p) \mapsto (\alpha(g, x), x)$ is a proper map. This is *not* the same as requiring that the map $G \times X \to X$ defining the action be a proper action.

**Def:** Given an action of $G$ on $X$, for any $g \in G$ and any subset $Y \subseteq X$, we will use the notation $$\alpha(g, Y) := \{ \alpha(g, x) \mid x \in Y\}$$
**Prop:** Suppose $G$ is a topological group that acts continuously on a topological space $X$. The action is proper iff for every compact subset $K \subseteq X$, the set $G_K := \{g \in G \mid \alpha(g, K) \cap K \neq \varnothing\}$ is compact.

**Prop:** Let $M$ be a topological manifold, and let $G$ be a topological manifold and topological group acting continuously on $M$. The action is proper iff the following is satisfied: If $\{p_i \}$ is a convergent sequence in $M$ and $\{g_i\}$ is a sequence in $G$ such $\{g_i \cdot p_i \}$ converges, then a subsequence of $\{g_i\}$ converges.

**Cor:** Let $M$ and $G$ be a topological manifolds. If $G$ is compact and a topological group acting continuously on $M$, then the action is proper.

**Cor:** Any action action by a compact Lie group on a manifold is proper.

**Prop:** Suppose a discrete group $\Gamma$ acts continuously on a manifold $M$. The action is proper iff the following condition holds: Any two points $p, q\in M$ have neighbourhoods $U$, $V$ such that the set $\{\varphi \in \Gamma\mid (\varphi \cdot U) \cap V \neq \varnothing\}$ is finite.

**Cor:** Suppose a discrete group $\Gamma$ acts continuously on a manifold $M$. The action is proper iff the following conditions hold:
- Each $p\in M$ has a neighbourhood $U$ such that $(\varphi \cdot U) \cap U \neq \varnothing$ for only finitely many $\varphi \in \Gamma$.
- If $p, q\in M$ are not in the same $\Gamma$-orbit, there exists neighbourhoods $U$ of $p$ and $V$ of $q$ such that $(\varphi \cdot U) \cap V = \varnothing$ for all $\varphi \in \Gamma$.

**Def:** A continuous discrete group action satisfying conditions of the above corollary, or the proposition above has traditionally been called *properly discontinuous*. This term is self contradictory since every properly discontinuous action is continuous.