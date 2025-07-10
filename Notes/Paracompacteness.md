---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Locally Finite Collections]], [[Hausdorff Spaces]], [[Normal Hausdorff Spaces]], [[Partitions of Unity]], [[Collectionwise Normal Spaces]]

**Def:** A topological space is called a *paracompact space* if every open cover of $X$ has a locally finite open [[Topological Cover|refinement]].

**Obs:** Every [[Compactness|compact]] space is paracompact.

We get the following corollary from [[Metrizable Spaces|Stone's theorem]]

**Cor:** Every metrizable space is paracompact.

**Lemma:** Let $X$ be a paracompact space and $A, B$ be a pair of closed subsets of $X$. If for every $x\in B$ there exist $U_x, V_x\in \tau$ such that $A \subseteq U_x$, x\in V_x$ and $U_x \cap V_x = \varnothing$, then there also exists $U, V\in \tau$ such that $A\subseteq U$, $B\subseteq V$ and $U \cap V = \varnothing$.

**Lemma:** Every $T_2$ paracompact space is $T_3$.

**Th:** Every $T_2$ paracompact space is $T_4$. 

**Lemma:** If every open cover of a topological space $X$ has a locally finite closed refinement, then $X$ is a paracompact. 

**Lemma:** If every open cover of a regular space $X$ has a locally finite refinement (consisting of arbitrary sets), then for every open cover $\{U_\alpha\mid \alpha< \kappa\}$ of the space $X$ there exists a closed locally finite cover $\{F_\alpha\mid \alpha < \kappa\}$ such that $F_\alpha \subseteq U_\alpha$ for every $\alpha <\kappa$.

**Cor:** If $X$ is a regular paracompact space, then for every open locally finite cover $\{U_\alpha \mid \alpha <\kappa\}$ has a open locally finite refinement $\{V_\alpha : \alpha < \kappa\}$ such that $\text{cl}_X(V_\alpha) \subseteq U_\alpha$. for every $\alpha < \kappa$.

**Lemma:** Every open $\sigma$-locally finite cover $\cal V$ of a topological space $X$ has a locally finite refinement.

**Th:** For every regular space $X$ the following conditions are equivalent:
- The space $X$ is paracompact.
- Every open cover of the space $X$ has a open $\sigma$-locally finite refinement. 
- Every open cover of the space $X$ has a finite refinement. 
- Every open cover of the space $X$ has a closed locally finite refinement. 

**Th:** 

**Th:** Every $T_2$ paracompact space is collectionwise normal.