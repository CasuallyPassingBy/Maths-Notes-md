---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Metric Outer Measures]], [[Extension of Measures]]

**Def:** If $X$ is a metric space, $p> 0$ and $E \subseteq X$, then the $p$-dimensional *Hausdorff (outer) measure* of $E$ is defined to be the number $$\mu_p^*(E) := \sup_{\varepsilon>0} \inf\left\{\left.\sum_{n = 1}^\infty (\text{diam}(E_n))^p\ \right\rvert\ E = E = \bigcup_{n = 1}^\infty E_n,\ \land \ \text{diam}(E_n)< \varepsilon, n \in \Bbb N^+\right\}$$
**Prop:** The set function $\mu^*_p$ is a metric outer measure.

**Prop:** The outer measure $\mu^*_p$ is regular; in fact, for every subset $E$ of $X$, there exists a decreasing sequence $\{U_n \mid n \in \Bbb N\}$ of open sets containing $E$ such that $$\mu^*_p(E) = \mu^*\left(\bigcap_{n = 0}^\infty U_n\right).$$
