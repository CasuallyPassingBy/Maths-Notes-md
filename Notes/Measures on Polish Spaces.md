---
tags:
  - MeasureTheory
  - SetTheory
  - Topology
---
Subjects: [[Measure Theory]], [[Set Theory]], [[Topology]]
Links: [[Polish Spaces]], [[Measures on Hausdorff Spaces]], [[Borel Sets]], [[Extension of Measures]], [[Outer Measures]], [[Inner Measures]]

**Prop:** Every finite Borel measure on a Polish space is regular. 

**Reminder:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a measure on $(X, {\scr A})$. We defined the completion of $\scr A$ under $\mu$ to be the collection $\scr A_\mu$ of subsets $A$ of $X$ for which are sets $E$ and $F$ that belong to $\scr A$ and satisfy the relations $E\subseteq A\subseteq F$ and $\mu(F\setminus E) = 0$. The sets $\scr A_mu$ are often called *$\mu$-measurable.*

We also defined the outer measure $\mu^*(A)$ and the inner measure $\mu_*(A)$ of an arbitrary subset $A$ of $X$ by $$\mu^*(A) := \inf\{\mu(B) \mid A \subseteq B \land B\in 
{\scr A}\} \quad \text{and}\quad \mu_*(A) := \sup\{\mu(B) \mid B\subseteq A \land B\in{\scr A}\}.$$
**Lemma:** Let $(X, {\scr A})$ be a measurable space, let $\mu$ be a finite measure on $(X, {\scr A})$, and let $\mu^*$ be defined as above. If $\{A_n\}_{n<\omega}$ is an increasing sequence of subsets of $X$, then $$\mu^*\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to \infty} \mu^*(A_n). $$
