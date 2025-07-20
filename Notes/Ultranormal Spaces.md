---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Normal Hausdorff Spaces]], [[Zero Dimensional Spaces]], [[Ultraparacompactness]]

**Def:** A topological space $X$ is called *ultranormal* if for every disjoint closed sets $A$ and $B$, there's a a clopen set $U$ such that $A\subseteq U$ and $B\subseteq X\setminus U$. If $X$ is an ultranormal $T_1$, then I am gonna call it ultra-$T_4$. 

**Obs:** We see that every ultranormal space is zero-dimensional. Also, we could interpret that ultranormality is the zero-dimensional analogue of normality. 

**Obs:** Every ultrparacompact space is ultranormal. 

**Lemma:** Let $f: \omega_1\to \omega_1$ be a function such that $f(\alpha) <\alpha$ for each $\alpha < \omega_1$. Then there is some $\beta<\omega_1$ such that $f(\alpha) <\beta$ for uncountably many $\alpha < \omega_1$. 

**Prop:** The space $[0,\omega_1)$ is ultranormal, but not ultraparacompact.

**Th:** Let $C$ be closed subset of an ultranormal space $X$ and let $Y$ be a complete separable metric space. Then every continuous function $f:C \to Y$ can be extended to a continuous function $F:X \to Y$.

**Prop:** The following are equivalent for a topological space $X$.
- $X$ is ultra-$T_4$.
- Whenever $\{U_\alpha \mid \alpha <\kappa\}$ is a point finite cover of $X$, there is a clopen cover $\{V_\alpha \mid \alpha < \kappa\}$ such that $V_\alpha \subseteq U_\alpha$ for each $\alpha < \kappa$, and if $U_\alpha \neq \varnothing$, then $V_\alpha \neq \varnothing$.
- If $\{U_\alpha \mid \alpha < \kappa\}$ is a locally finite open cover of $X$, then there is a pairwise disjoint family $\{P_\alpha\mid \alpha < \kappa\}$ of clopen sets such that $P_\alpha \subseteq U_\alpha$ for $\alpha < \kappa$.
- $X$ is $T_4$ and strongly zero-dimensional.

