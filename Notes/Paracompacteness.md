---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Special Types of Collections in Topology]], [[Hausdorff Spaces]], [[Normal Hausdorff Spaces]], [[Partitions of Unity]], [[Collectionwise Normal Spaces]] [[Special Types of Collections in Topology]]

**Def:** A topological space is called a *paracompact space* if every open cover of $X$ has a locally finite open [[Topological Covers|refinement]].

**Obs:** Every [[Compactness|compact]] space is paracompact.

There are various topological properties related to the paracompactness:
- [[Countable paracompactness]]
- [[Metacompactness]]
- [[Subparacompactness and Submetacompactness]]
- [[Strong Paracompactness]]
- [[Fully Normal Spaces]]

We get the following corollary from [[Metrizable Spaces|Stone's theorem]]

**Cor:** Every metrizable space is paracompact.

**Lemma:** Let $X$ be a paracompact space and $A, B$ be a pair of closed subsets of $X$. If for every $x\in B$ there exist $U_x, V_x\in \tau$ such that $A \subseteq U_x$, x\in V_x$ and $U_x \cap V_x = \varnothing$, then there also exists $U, V\in \tau$ such that $A\subseteq U$, $B\subseteq V$ and $U \cap V = \varnothing$.

**Lemma:** Every $T_2$ paracompact space is $T_3$.

**Th:** Every $T_2$ paracompact space is $T_4$. 

**Lemma:** If every open cover of a topological space $X$ has a locally finite closed refinement, then $X$ is a paracompact. 

**Lemma:** If every open cover of a regular space $X$ has a locally finite refinement (consisting of arbitrary sets), then for every open cover $\{U_\alpha\mid \alpha< \kappa\}$ of the space $X$ there exists a closed locally finite cover $\{F_\alpha\mid \alpha < \kappa\}$ such that $F_\alpha \subseteq U_\alpha$ for every $\alpha <\kappa$.

**Cor:** If $X$ is a regular paracompact space, then for every open locally finite cover $\{U_\alpha \mid \alpha <\kappa\}$ has a open locally finite refinement $\{V_\alpha : \alpha < \kappa\}$ such that $\text{cl}_X(V_\alpha) \subseteq U_\alpha$. for every $\alpha < \kappa$.

**Lemma:** Every countable, open cover $\{V_n \mid n <\omega\}$ of a topological space $X$, there is a locally finite covering $\{A_n \mid n <\omega\}$ such that $A_n \subseteq V_n$ for each $n <\omega$.

**Lemma:** Every open $\sigma$-locally finite cover $\cal V$ of a topological space $X$ has a locally finite refinement.

**Th:** For every regular space $X$ the following conditions are equivalent:
- The space $X$ is paracompact.
- Every open cover of the space $X$ has a open $\sigma$-locally finite refinement. 
- Every open cover of the space $X$ has a finite refinement. 
- Every open cover of the space $X$ has a closed locally finite refinement. 

**Cor:** Every regular Lindelöf space is paracompact.

**Th:** Every $T_2$ paracompact space is collectionwise normal.

**Th:** Every $T_2$ paracompact space is fully normal.

**Stone's coincidence theorem:** A $T_2$ space $X$ is paracompact iff it is fully normal.

**Th:** Paracompactness is hereditary with respect to $F_\sigma$-sets.

**Prop:** If $X$ be a $T_1$ space and $\{F_\alpha \mid \alpha < \kappa\}$ a locally finite closed cover of $X$ whose members are paracompact $T_2$, then $X$ is paracompact $T_2$.

**Th:** The sum $\bigoplus_{\alpha < \kappa} X_\alpha$ is paracompact iff all the spaces $X_\alpha$ are paracompact.

**Remark:** The product of two paracompact spaces is not necessarily paracompact. We can strengthen this assertion that the product of a paracompact space with a separable metric space is not necessarily paracompact.

**Lemma:** If a cover $\cal U$ have a cushioned refinement, then it has a indexed cushioned refinement.

**Th:** A $T_1$-space $X$ is paracompact iff every open cover of $X$ has a cushioned (not necessarily open) refinement.

**Th:** A $T_1$ space $X$ is paracompact iff every open cover of $X$ has a $\sigma$-cushioned open refinement.

**Th:** The following statements are equivalent for a regular space $X$.
- $X$ is paracompact.
- Every open cover of $X$ has an open closure-preserving refinement.
- Every open cover of $X$ has a closure-preserving refinement.
- Every open cover of $X$ has a closed closure-preserving refinement.
- Every open cover of $X$ has an open $\sigma$-closure-preserving refinement.

**Th:** Let $X$ be a Hausdorff paracompact space. If $f: X \to Y$ is a perfect function, then $Y$ is also a $T_2$ paracompact space.

**Michael's Theorem:** Let $X$ be a Hausdorff paracompact space. If $f: X \to Y$ is a closed, continuous and surjective function, then $Y$ is also a $T_2$ paracompact space.

**Th:** If a topological space $X$ has a locally finite closed cover consisting of paracompact subspaces, then $X$ is itself paracompact.

**Th:** Let $Y$ be a paracompact space. If $f: X\to Y$ is a perfect function, then $X$ is also paracompact.

**Prop:** A space is hereditarily paracompact if every open subspace is paracompact.

**Michael-Nagami Theorem:** The topological space $X$ is a Hausdorff paracompact space iff it is collectionwise $T_4$ and metacompact.

**Th:** If $X$ is a collectionwise $T_4$ and submetacompact space, then $X$ is paracompact.

This result is an even stronger version of Michael-Nagami.

**Prop:** If $X$ is paracompact and $Y$ is compact, then $X\times Y$ is paracompact.

**Prop:** If $X$ is a $T_0$, collectionwise normal developable space, then $X$ is paracompact.

**Cor:** The following statements are equivalent:
- $X$ is $T_2$, paracompact and developable.
- $X$ is $T_0$, collectionwise normal and developable.