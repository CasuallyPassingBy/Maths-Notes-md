---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Continuous Functions and Homeomorphims]], [[Topological Subspaces]]

**Def:** Let $f$ be a function from that topological space $X$ to the topological space $Y$
- $f$ is an *open function* if the image under $f$ of any open subset of $X$ is an open subset of $Y$
- $f$ is an *closed function* if the image under $f$ of any closed subset of $X$ is an closed subset of $Y$

**Prop:** Let $f: X \to Y$ be a function.
- $f$ is open iff $f[B]$ is open on  for each $B\in \cal B$, where $\cal B$ is a base for $Y$.
- Similarly, $f$ is closed iff $f[C]$ is open on  for each $C\in \cal C$, where $\cal C$ is a closed base for $Y$. 

If $Y$ is a subspace of $X$, then the inclusion $\iota:Y\to X$ is closed/open iff the set $Y$ is closed/open on $X$

**Th:** A continuous mapping $f: X \to Y$ is closed/open iff every $B \subseteq Y$ and every open/closed set $A\subseteq X$ which  $f^{-1}[B] \subseteq A$, there exists an open/closed set $C \subseteq Y$ containing $B$ such that $f^{-1}[C] \subseteq A$. 

**Th:** A continuous mapping $f: X\to Y$ is closed iff for every point $y\in Y$ and every open set $U \subset X$ which $f^{-1}\{y\} \subseteq U$, there exists $Y$ a neighbourhood $V$ such that $f^{-1}[V] \subseteq U$.

**Th:** If $f: X \to Y$ is an open mapping, then for every $x \in X$ we have $\chi(f(x), Y) \le \chi(x, X)$. If, moreover, $f$ is surjective, then $w(Y) \le w(X)$, and $\chi(Y) \le \chi(X)$. 

**Th:** The class of $T_i$ spaces for $i \in \{1, 4, 6\}$ are invariant under closed mappings.

If $f$ is a bijective function between the topological space $X$ and $Y$, then the following are equivalent
- $f^{-1}$ is continuous
- $f$ is open
- $f$ is closed
In particular, a continuous bijective function $f:X\to Y$ is a homeomorphism if it satisfies any of the above conditions.

**Closed Map Lemma:** Suppose $F$ is a continuous map from a compact space to a $T_2$ space.
- $F$ is a closed map.
- If $F$ is surjective, it is a quotient map.
- If $F$ is injective, it is a topological embedding.
- If $F$ is bijective, it is a homeomorphism.

**Th:** Suppose $X$ is a compact $T_2$ space and $q: X \to Y$ is a quotient map. Then the following are equivalent.
- $Y$ is Hausdorff.
- $q$ is closed.
- The set $\{(x_1, x_2)\in X \times X \mid q(x_1) = q(x_2)\}$ is closed in $X \times X$.