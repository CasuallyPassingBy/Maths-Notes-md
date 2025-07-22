---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Topological Covers]]

**Def:** A topological space $X$ is *compact* if every open cover has a finite subcover.

**Obs:** A topological space $X$ is compact if every open cover has finite refinement. 

**Def:** We say that a family $\mathcal F \subseteq \mathcal P(X)$ has the *finite intersection property* if $\mathcal F \neq \varnothing$ and for every $\mathcal G \in [\mathcal F]^{<\omega}$ satisfies $\bigcap \mathcal G \neq \varnothing$.

**Th:** Let $X$ be a topological space. $X$ is compact iff every family $\cal F$ of closed subsets of $X$ that has the finite intersection property has nonempty intersection.

**Prop:** Every closed subspace of a compact space is compact.

**Prop:** If a subspace $A$ of a topological space $X$ is compact, then every family ${\cal U}\subseteq \tau_X$ such that $A \subseteq \bigcup \cal U$, then there exists $\mathcal V \in [{\cal U}]^{<\omega}$ such that $A \subseteq \bigcup \cal V$.

**Cor:** Let $X$ be a topological space, $n \in\omega\setminus 1$ and $\{F_m \mid n <\omega\}$ be a family of closed subsets of $X$. The subspace $F = \bigcup_{m  <n } F_m$ of $X$ is compact iff $F_m$ is compact for every $m <n$. 

**Cor:** Let $U$ be an open set of a topological space $X$. If a family $\mathcal F$ of closed subsets of $X$ contains at least one compact set (in particular, if $X$ is compact) and $\bigcap \mathcal F \subseteq U$, then there's $\mathcal G \in [\mathcal F]^{<\omega}$ such that $\bigcap \mathcal G \subseteq U$.

**Th:** If $A$ is a compact subspace of a regular space $X$, then for every closed set $B$ disjoint from $A$ there exist $U, V\in \tau_X$ such that $A \subseteq U$, $B \subseteq V$ and $U \cap V =\varnothing$. If, moreover, $B$ is a compact subspace of $X$, then we only need that $X$ is a $T_2$ space.

**Th:** Let $X$ be a completely regular space. If $A$ is a compact subspace of $X$, and $B$ is a closed subset of $X$ with $A \cap B = \varnothing$, then there's a continuous function $f:X \to I$ such that $f(x) = 0$ for all $x\in A$ and $f(x) = 1$ for all $x\in B$.

**Prop:** Every compact subspace of a $T_2$ space is closed.

**Cor:** Every $T_2$ compact space is normal.

**Prop:** If $f:X \to Y$ is a continuous and surjective function, and $X$ is a compact space, then $Y$ is compact, meaning that compactness is preserved by continuous surjective functions.

**Cor:** If $f: X \to Y$ is a continuous function, and $X$ is compact, then 

**Cor:** If $f: X \to Y$ us a continuous function, $X$ and $Y$ are Hausdorff spaces, then any $A\in \mathcal P(X)$ satisfies that $\text{cl}_Y(f[A]) = f[\text{cl}_X (A)]$. 

**Cor:** Every continuous function from a $T_2$ compact space to a $T_2$ space is closed. 

**Cor:** Every continuous bijective function from a $T_2$ compact space to a $T_2$ space is a homeomorphism.

**Cor:** Let $\tau_1$ and $\tau_2$ be topologies defined on a set $X$, and let $\tau_1$ be finer than $\tau_2$. If the space $(X, \tau_1)$ is compact and $T_2$ and $(X, \tau_2)$ is a $T_2$ space, then $\tau_1 = \tau_2$. In other words, among all Hausdorff topologies, compact topologies are minimal.

**Lemma:** If $A$ is a $T_2$ compact subspace of a space $X$ and $y \in Y$, then for every open set $W\subseteq X \times Y$ containing $A \times \{y\}$  there exist open sets $U \in \tau_X$ and $V \in\tau_Y$ such that $A \times \{y\} \subseteq U \times V \subseteq W$.

**Kuratowski's Theorem:** The following are equivalent for a topological space $X$.
- $X$ is a compact space.
- For every topological space $Y$, the projection $\pi_Y :X\times Y\to Y$ is closed.
- For every $T_4$ space $Y$, the projection $\pi_Y :X\times Y\to Y$ is closed.