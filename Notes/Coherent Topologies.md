---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Weak Topology]], [[Topological Subspaces]]

**Def:** Suppose $X$ is a topological space, and $\cal B$ is any family of subspaces of $X$ whose union is $X$. To say that the topology of $X$ is *coherent with $\cal B$* means that a subset $U\subseteq X$ is open in $X$ iff its intersection with each $B\in \cal B$ is open in $B$. The same applies for closed sets. 

We see that [[compactly generated]] spaces are coherent with the family of compact subsets. 

**Prop:** Suppose $X$ is a topological space whose topology is coherent with a family $\cal B$ of subspaces.
- If $Y$ is another topological space, then a map $f:X\to Y$ is continuous iff $f|_B$ is continuous for each $B\in \cal B$.
- The map $\coprod_{B\in \cal B} B \to X$ induced by the inclusion of each set $B \hookrightarrow X$ is a quotient map. 

**Prop:** Suppose $X$ is a topological space $\{X_\alpha \mid \alpha <\kappa\}$ is a family of subspaces whose union is $X$. $X$ is coherent with the subspaces iff it is the finest topology on $X$ for which all of the inclusion maps $X_\alpha \hookrightarrow X$ are continuous.

**Obs:** Suppose $X$ is a topological space. Then the topology of $X$ is coherent with each of the following collections of subspaces of $X$:
- Any open cover of $X$.
- Any locally finite closed cover of $X$

**Cor:** Suppose $X$ is a topological space whose topology is coherent with a collection $\{X_\alpha \mid \alpha < \kappa\}$ of subspaces of $X$, and for each $\alpha <\kappa$ we are given a continuous map $f_\alpha : X_\alpha \to Y$ such that $\{f_\alpha \mid \alpha <\kappa\}$ is a compatible family, then there's a unique continuous map $f: X \to Y$ whose restriction to each $X_\alpha$ is $f_\alpha$. 
