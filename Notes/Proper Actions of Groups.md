---
tags:
  - GroupTheory
  - Topology
---
Subjects: [[Group Theory]], [[Topology]]
Links: [[Topological Groups]], [[Continuous Actions of Groups]], [[Proper Maps]]

**Def:** The action is said to be *proper* if the map $G \times X \to X \times X$ given by $(g, p) \mapsto (\alpha(g, x), x)$ is a proper map. This is *not* the same as requiring that the map $G \times X \to X$ defining the action be a proper action.

**Prop:** Every continuous action of a compact topological group on a Hausdorff space is proper. 

**Def:** Given an action of $G$ on $X$, for any $g \in G$ and any subset $Y \subseteq X$, we will use the notation $$\alpha(g, Y) := \{ \alpha(g, x) \mid x \in Y\}$$
**Prop:** Suppose $G$ is a topological group that acts continuously on a topological space $X$. The action is proper iff for every compact subset $K \subseteq X$, the set $G_K := \{g \in G \mid \alpha(g, K) \cap K \neq \varnothing\}$ is compact.

**Prop:** If a topological group $G$ acts continuously and properly on a locally compact $T_2$ space $E$, then the orbit space $E/G$ is Hausdorff. 

The converse is not true, if $E$ is any locally compact $T_2$ space and $G$ is any noncompact group acting trivially on $E$, then $E/G =E$ is Hausdorff but the action is not proper. 

**Prop:** Suppose we are given a [[Covering Space Actions|covering space action]] of a group $\Gamma$ on a topological space $E,$ and $E/\Gamma$ is $T_2$. Then, with the discrete topology, $\Gamma$ acts properly on $E$. 

**Th:** Suppose $E$ is a connected, locally path-connected, and locally compact Hausdorff space, and a discrete group $\Gamma$ acts continuously, freely and properly on $E$. The action is a covering space action, $E/\Gamma$ is Hausdorff, and the quotient $q:E \to E/\Gamma$ is a normal covering map. 

**Cor:** Let $M$ be a connected $n$-manifold on which a discrete group $\Gamma$ acts continuously, freely and properly. Then $M/\Gamma$ is an $n$-manifold. 

**Prop:** Let $M$ be a topological manifold, and let $G$ be a topological manifold and topological group acting continuously on $M$. The action is proper iff the following is satisfied: If $\{p_i \}$ is a convergent sequence in $M$ and $\{g_i\}$ is a sequence in $G$ such $\{g_i \cdot p_i \}$ converges, then a subsequence of $\{g_i\}$ converges.

**Cor:** Let $M$ and $G$ be a topological manifolds. If $G$ is compact and a topological group acting continuously on $M$, then the action is proper.

**Cor:** Any action action by a compact Lie group on a manifold is proper.

**Prop:** Suppose a discrete group $\Gamma$ acts continuously on a manifold $M$. The action is proper iff the following condition holds: Any two points $p, q\in M$ have neighbourhoods $U$, $V$ such that the set $\{\varphi \in \Gamma\mid (\varphi \cdot U) \cap V \neq \varnothing\}$ is finite.

**Cor:** Suppose a discrete group $\Gamma$ acts continuously on a manifold $M$. The action is proper iff the following conditions hold:
- Each $p\in M$ has a neighbourhood $U$ such that $(\varphi \cdot U) \cap U \neq \varnothing$ for only finitely many $\varphi \in \Gamma$.
- If $p, q\in M$ are not in the same $\Gamma$-orbit, there exists neighbourhoods $U$ of $p$ and $V$ of $q$ such that $(\varphi \cdot U) \cap V = \varnothing$ for all $\varphi \in \Gamma$.

**Def:** A continuous discrete group action satisfying conditions of the above corollary, or the proposition above has traditionally been called *properly discontinuous*. This term is self contradictory since every properly discontinuous action is continuous.