---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Paracompacteness]], [[Countable compactness]], [[Collectionwise Normal Spaces]], [[Metacompactness]]

**Def:** A topological space $X$ is *countably paracompact* if every countable open cover of $X$ has a locally finite open refinement.

**Obs:** Every paracompact space is countably paracompact. Every countable compact space is coumtably paracompact. 

**Th:** The following properties are equivalent for a topological space $X$.
- $X$ is countably paracompact.
- Every countable open cover of $\{U_n \mid n <\omega\}$ has a refinement $\{V_n \mid n <\omega\}$ with $V_n \subseteq U_n$ for each $n <\omega$. 
- For every increasing sequence of open subsets $\{U_n \mid  n<  \omega\}$ of $X$ satisfying $X = \bigcup_{n<\omega} U_n$ there exists a sequence of $\{F_n \mid n <\omega\}$ of closed subsets of $X$ such that $F_n \subseteq W_n$ for each $n <\omega$ and $\bigcup_{n <\omega} \text{int}(F_n) = X$.
- For every decreasing sequence $\{F_n \mid n <\omega\}$ of closed subsets such that $\bigcap_{n<\omega} F_n = \varnothing$, there is a sequence $\{U_n \mid n <\omega\}$ of open sets such that $U_n \supseteq F_n$, and $\bigcap_{n <\omega} \text{cl}(U_n) = \varnothing$.

**Th:** The following properties of an normal space are equivalent.
- $X$ is normal countably paracompact.
- Every countable open cover of $\{U_n \mid n <\omega\}$ has a refinement $\{V_n \mid n <\omega\}$ with $\text{cl}(V_n) \subseteq U_n$ for each $n <\omega$. 
- For every increasing sequence of open subsets $\{U_n \mid  n<  \omega\}$ of $X$ satisfying $X = \bigcup_{n<\omega} U_n$ there exists a sequence of $\{F_n \mid n <\omega\}$ of closed subsets of $X$ such that $F_n \subseteq W_n$ for each $n <\omega$ and covers $X$. 

**Prop:** Every countable cover $\{U_n \mid n <\omega\}$ of a topological space $X$, where each $U_n$ is a cozero set, has a countable star-finite refinement consisting of cozero sets.

**Cor:** Every perfectly normal space is countably paracompact.

**Th:** For a normal space $X$ the following conditions are equivalent.
- $X$ is countably paracompact.
- $X$ is countably metacompact.
- $X$ is countably strongly paracompact (every countable cover of the space $X$ has a star-finite open refinement).

**Lemma:** The Cartesian product $X\times Y$ of a countably paracompact normal space $X$ and a compact second-countable space $Y$ is normal.

**Th:** A topological space $X$ is countably paracompact normal space iff the Cartesian product $X \times [0, 1]$ is normal.

**Prop (Katetov):** The following are equivalent for a normal space $X$.
- $X$ is collectionwise normal and countably paracompact.
- Every locally finite closed collection $\{F_\alpha \mid \alpha < \kappa\}$ in $X$, there is a locally finite open collection $\{U_\alpha \mid \alpha < \kappa\}$ such that $F_\alpha \subseteq U_\alpha$ for all $\alpha < \kappa$. 

We can generalise further the idea of contable paracompactness.

**Def:** Let $\kappa$ be an infinite cardinal and $X$ be a topological space. If every open cover $\cal U$ of $X$ with $|\mathcal U| \le \kappa$ has a locally finite open refinement, then $X$ is called a $\kappa$-paracompact.

**Obs:** We say that $X$ is paracompact iff it is $\kappa$-paracompact for each $\kappa$.

