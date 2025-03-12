---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Rings and Algebras of Sets]], [[Lebesgue Measure]], [[Borel Sets]], [[Rings and Algebras of Sets]]

**Def:** A *measurable space* is a set and a $\sigma$-ring $\cal S$ of subsets of $X$ with the property that $\bigcup \cal S$. We shall write $(X, \mathcal S)$ for a measurable space when the $\sigma$-ring $\cal S$ is not clear. It is customary to call a $E\subseteq X$ *measurable* iff $E \in \cal S$. 

**Def:** A *measure space* is a measurable space $(X, \mathcal S)$ and a measure $\mu$ on $\cal S$; just as for measurable spaces we shall ordinarily allow ourselves to confuse a measure space whose underlying set is $X$ with the set $X$. On the occasions when it is desirable to call attention to the particular $\sigma$-ring and measure under consideration, we shall write $(X, \mathcal S, \mu)$ for $X$. The measure space $X$ is called (totally) finite, $\sigma$-finite, or complete, according as the measure $\mu$ is (totally) finite, $\sigma$-finite, or complete.

We continue with the notation that $\mu^*$ for the outer measure and $\mu_*$ for the inner measure.

We have common things to do:
- If $(X, \mathcal S, \mu)$ is a measure space and $X_0$ is a measurable space, we can induce a measure space to it. The $\sigma$-ring is $X_0 \cap \cal S$, and the measure is $\mu_0(E) = \mu(E)$. 
- Conversely, if $X_0 \subseteq X$ and $(X_0, \mathcal S_0, \mu_0)$, the $X$ may be made into a measure space $(X, \mathcal S, \mu)$, where $\mathcal S := \{E \subseteq X \mid E \cap X_0 \in \mathcal S_0\}$ and for $\mu(E) = \mu_0(E \cap X_0)$.
- If $X_0$ is a measurable subset of $X$, a new measure $\mu_0$ may be defined on the family of measurable subsets $E$ of $X$ by the equation $\mu_0(E) = \mu(E \cap X_0)$. 

**Def:** A subset $X_0$ of a measure space $(X, \mathcal S, \mu)$ is *thick* if $\mu_*(E \setminus X)= 0$ for every measurable set $E$. 

**Obs:** If $X$ itself is measurable, then $X_0$ is thick iff $\mu_*(X\setminus X_0) = 0$; if $\mu$ is totally finite, then $X_0$ is thick iff $\mu^*(X_0) = \mu(X)$. 

**Th:** If $X_0$ is a thick subset of a measure space, if $\mathcal S_0 = \mathcal S \cap X_0$, and if for $E\in \cal S$, $\mu_0(E\cap X_0) := \mu(E)$, then $(X_0, \mathcal S_0, \mu_0)$ is a measure space.

**Prop:** If $(X, \mathcal S, \mu)$ is measure space and if $X_0 \subseteq X$ such that for every two measurable sets $E_1$ and $E_2$, the condition $E_1 \cap X_0 = E_2 \cap X_0$ implies $\mu(E_1) = \mu(E_2)$, then $X_0$ is thick. 

**Prop:** If $(X,\mathcal S, \mu)$ is a finite measure space, then there exists a thick measurable set $X_0$. 

This result enables us, in most applications, to assume that a finite measure space is totally finite, since we can replace $X$ by $X_0$ without significan loss in generality. 

**Obs:** If $(X, \mathcal S, \mu)$ is a complete, $\sigma$-finite measure space, then every $\mu^*$-measurable space is measurable.