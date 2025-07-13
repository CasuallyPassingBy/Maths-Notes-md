---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Paracompacteness]], [[Metrizable Spaces]]

**Def:** A family $\{f_\alpha : X \to [0, 1] \mid \alpha < \kappa\}$  of continuous functions from the space $X$ is called a *partition of unity*on the space $X$ if $$ \sum_{\alpha < \kappa} f_\alpha (x) =  1$$ for every $x\in X$. 

Note that for even that a partition of unity to exists for each $x\in X$ the set $I_x := \{\alpha < \kappa \mid f_\alpha (x) \neq  0\}$ is at most countable, and the series $\sum_{\alpha \in I_x} f_\alpha (x)$ absolutely converges to $1$. If we have a partition of unity, then the family $\{f^{-1}_\alpha[(0, 1]]\mid \alpha < \kappa\}$ is point-countable. 

**Def:** We say that a partition of unity $\{f_\alpha : \alpha <\kappa\}$ on a space $X$ is *locally finite* if the cover $\{f^{-1}_\alpha(0,1] \mid \alpha < \kappa\}$ is locally finite. This means that for each $x\in X$, there exists a neighbourhood $U_x$ of the point $x$ and a finite set $I_x := \{\alpha <\kappa \mid f_\alpha(x) \neq 0\}$ is finite, and $\sum_{\alpha \in I_x} f_\alpha(x) = 1$. 

**Def:** A partition of unity $\{f_\alpha \mid \alpha < \kappa\}$ on a space $X$ is *subordinated to a cover $\cal A$* of $X$ if the cover $\{f^{-1}_\alpha(0,1] \mid \alpha < \kappa\}$ of $X$ is a refinement of $\cal A$. Conversely, a cover $\cal U$ of a space $X$ is said to be *numerable* if it has a subordinated partition of unity.

**Lemma:** If for an open cover $\cal U$ of a space $X$ there exists a partition of unity $\{f_\alpha \mid \alpha < \kappa\}$ subordinated to it, then $\cal U$ has an open locally finite refinement.

**Prop:** Every numerable cover, admits a subordinate locally finite partition of unity.

**Prop:** Every numerable cover has a shrinking.

**Def:** A cover $\mathcal U$ is called a *normal cover* if there is a sequence $\{\mathcal U_n \mid n <\omega\}$ of open covers such that $\mathcal U > \mathcal U_0$ and $\mathcal U_n^* > \mathcal U_{n+1}$ for every $n <\omega$. 

**Prop:** If $\cal U$ be a normal cover of a topological space $X$, then $\cal U$ has a $\sigma$-discrete open refinement.

**Prop:** If a cover $\cal U$ of a topological space $X$ has a $\sigma$-locally finite open refinement consisting of cozero sets, then $\cal U$ is a normal cover.