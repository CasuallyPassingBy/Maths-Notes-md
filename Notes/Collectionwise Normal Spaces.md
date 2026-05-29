---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Paracompacteness]], [[Metacompactness]], [[Subparacompactness and Submetacompactness]], [[Normal Hausdorff Spaces]], [[Countable Paracompactness]]

**Def:** A space $X$ is *collectionwise normal* if for every discrete family $\{F_\alpha \mid \alpha < \kappa\}$ of closed subsets of $X$ there is a family $\{U_\alpha \mid \alpha < \kappa\}$ of open subsets of $X$ such that $F_\alpha \subseteq U_\alpha$ for every $\alpha < \kappa$. Additionally, we say that $X$ is *collectionwise $T_4$* if it is collectionwise normal and $T_1$. 

**Obs:** Every collectionwise normal space is normal.

**Th:** The following statements are equivalent for a topological space $X$.
- $X$ is collectionwise normal.
- Every discrete family $\{F_\alpha \mid \alpha < \kappa\}$ of closed subsets of $X$ there is a pairwise disjoint family $\{U_\alpha \mid \alpha < \kappa\}$ of open subsets of $X$ such that $F_\alpha \subseteq U_\alpha$.

**Prop:** Every fully normal space is collectionwise normal.

**Th:** Every $T_2$ paracompact space is collectionwise normal.

**Cor:** Every $T_2$ compact space is collectionwise normal. 

**Th:** The following statements are equivalent for a topological space $X$.
- $X$ is collectionwise normal.
- For every closed set $F$ of $X$ and every locally finite open covering $\{\mathcal U_\alpha \mid \alpha < \kappa\}$ of $F$, there is a locally finite open cover $\{V_\alpha \mid \alpha < \kappa\}$ of $X$ such that $F \cap \text{cl}(V_\alpha) \subseteq U_\alpha$ for every $\alpha < \kappa$.

Let us note that there are spaces that are collectionwise normal but not hereditarily normal. Similarly, there are examples of hereditarily normal spaces that are not collectionwise normal. 

**Th:** Let $X$ be a topological space. If $\{X_n \mid n <\omega\}$ is an increasing family of closed collectionwise normal subspaces of $X$ such that $X = \bigcup_{n < \omega} X_n$, then  $X$ is collectionwise normal. 

This result can be put in the languages of categories as:

If $(i_n: X_n \to X_{n+1})_{n < \omega}$ is a sequence of closed embeddings between collectionwise normal spaces, then the colimit $X = \text{colimit}_n X_n$ is also collectionwise normal.

**Prop:** If $X$ is a collectionwise normal space, then every point finite cover of $X$ has an open $\sigma$-discrete refinement.

**Michael-Nagami Theorem:** The topological space $X$ is a Hausdorff paracompact space iff it is collectionwise $T_4$ and metacompact.

**Prop:** Collectionwise normality is an additive property.

**Prop:** If $X$ is a collectionwise normal space, and $f:X \to Y$ is a closed, continuous and surjective function, then $Y$ is collectionwise normal.

**Prop:** If $X$ is a $T_0$, collectionwise normal developable space, then $X$ is paracompact.

**Cor:** The following statements are equivalent:
- $X$ is $T_2$, paracompact and developable.
- $X$ is $T_0$, collectionwise normal and developable.

**Th:** If $X$ is a collectionwise $T_4$ and submetacompact space, then $X$ is paracompact.

This result is an even stronger version of Michael-Nagami.