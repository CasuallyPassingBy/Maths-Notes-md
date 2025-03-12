---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]]

**Def:** A family $\{A_\alpha \mid \alpha < \kappa\}$ of subsets of a topological space $X$ is *locally finte* if for every point $x\in X$ there exists a neighbourhood such that the set $\{\alpha < \kappa \mid U \cap A_\alpha\}$ is finite. If every point $x \in X$ has a neighbourhood that intersects at most one set of a given family, then we say that the family is *discrete*. 

**Obs:** A discrete family, as well as any finite family, is locally finite. 

**Th:** For every locally finite family $\mathcal A =\{A_\alpha \mid \alpha < \kappa\}$ we have the equality $$\bigcup\text{cl}(\mathcal A) = \text{cl}\left(\bigcup\mathcal A\right).$$
**Th:** Let $\mathcal F$ be a locally finite family and $F = \bigcup \cal F$. If all members of $\cal F$ are closed, then $F$ is closed set and if all members of $\cal F$ are clopen, then $F$ is a clopen set. 

**Th:** If $\cal A$ is a locally finite (discrete) family, then the family $\text{cl}(\mathcal A)$ is also locally finite (discrete). 

**Def:** A family $\{A_\alpha \mid \alpha < \kappa\}$ of subsets of a set $X$ is called *point-finite/point-countable* if dor every $x\in X$ the set $\{\alpha <\kappa\mid x\in A_\alpha\}$ is finite/countable. 

We see that every locally finite cover is point-finite. 