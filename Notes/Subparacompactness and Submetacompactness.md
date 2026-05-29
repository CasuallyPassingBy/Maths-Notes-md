---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Paracompacteness]], [[Metacompactness]], [[Collectionwise Normal Spaces]]

**Def:** A topological space $X$ is called *subparacompact* if every open cover $\cal U$ of $X$ has a $\sigma$-discrete closed refinement. 

**Prop:** Let $X$ be a topological space. If $X$ is $T_1$ and countable, then $X$ must be subparacompact.

**Def:** $X$ is called *$\theta$-refinable* or *submetacompact* if for every open cover $\cal U$ of $X$ there is a sequence $\{\mathcal V_n \mid n <\omega\}$ of open covers such that $\cal V_n$ is a refinement of $\cal U$ for each $n <\omega$ and such that for each $x\in X$ there's an $n<\omega$ with $\text{ord}_x(\mathcal V_n) <\omega$. 

**Obs:** Every regular paracompact space is subparacompact. Thus every $T_2$ paracompact space is subparacompact.

**Prop:** Every metacompact and every subparacompact space is submetacompact.

**Th:** The following conditions are equivalent for a topological space $X$. 
- $X$ is subparacompact.
- Every open cover of $X$ has a $\sigma$-locally finite closed refinement.
- Every open cover of $X$ has a $\sigma$-closure-preserving closed refinement.
- For every open cover $\cal U$ of $X$ there is a sequence $\{\mathcal V_n \mid n <\omega\}$ of open covers such that fora each $x\in X$ there is an $n<\omega$ satisfying $\text{St}(x, \mathcal V_n ) \subseteq U$ for some $U \in \cal U$. 

**Th:** A regular space $X$ is paracompact iff it is collectionwise normal and submetacompact. 

**Cor:** Every collectionwise $T_4$ submetacompact space is paracompact.

**Prop:** Every countable compact submetacompact space is compact.