---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]], [[Metric and Normed Spaces]]
Links: [[Outer Measures]], [[Topology of Metric Spaces]], [[Borel Sets]]

**Def:** An outer measure on the family of $\cal H$ of all subsets of a metric space $(X, d)$ is a *metric outer measure* if $$\mu^*(E \cup F) = \mu^*(E) + \mu^*(F)$$whenever $d(E, F)>0$. 

**Prop:** If $\mu⁺$ is a metric outer measure, $E$ is a subset of an open set $U$ in $X$, and $E_n = E\cap \{x \mid d(x, X\setminus U)\ge 1/n\}$, for $n <\omega$, then $\lim_{n \to \infty} \mu^*(E_n) = \mu(E)$. 

**Prop:** If $\mu^*$ is a metric measure, then every Borel set is $\mu^*$-measurable

**Prop:** If $\mu^*$ is an outer measure on the family $P(X)$ such that every open set is $\mu^*$-measurable, then $\mu^*$ is a metric outer measure.