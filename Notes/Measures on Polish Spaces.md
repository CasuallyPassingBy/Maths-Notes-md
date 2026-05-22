---
tags:
  - MeasureTheory
  - SetTheory
  - Topology
---
Subjects: [[Measure Theory]], [[Set Theory]], [[Topology]]
Links: [[Polish Spaces]], [[Measures on Hausdorff Spaces]], [[Borel Sets]], [[Extension of Measures]], [[Outer Measures]], [[Inner Measures]], [[Measure Spaces and Measurable Spaces]], [[Universally Measurable Sets]]

**Prop:** Every finite Borel measure on a Polish space is regular. 

**Reminder:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a measure on $(X, {\scr A})$. We defined the completion of $\scr A$ under $\mu$ to be the collection $\scr A_\mu$ of subsets $A$ of $X$ for which are sets $E$ and $F$ that belong to $\scr A$ and satisfy the relations $E\subseteq A\subseteq F$ and $\mu(F\setminus E) = 0$. The sets $\scr A_\mu$ are often called *$\mu$-measurable.*

We also defined the outer measure $\mu^*(A)$ and the inner measure $\mu_*(A)$ of an arbitrary subset $A$ of $X$ by $$\mu^*(A) := \inf\{\mu(B) \mid A \subseteq B \land B\in {\scr A}\} \quad \text{and}\quad \mu_*(A) := \sup\{\mu(B) \mid B\subseteq A \land B\in{\scr A}\}.$$
**Lemma:** Let $(X, {\scr A})$ be a measurable space, let $\mu$ be a finite measure on $(X, {\scr A})$, and let $\mu^*$ be defined as above. If $\{A_n\}_{n<\omega}$ is an increasing sequence of subsets of $X$, then $$\mu^*\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to \infty} \mu^*(A_n). $$
**Th:** Let $X$ be a Polish space, and let $\mu$ be a finite Borel measure on $X$. Then every analytic subset of $X$ is $\mu$-measurable. 

**Def:** Assume that $X$ is a Polish space. The *universally measurable* subsets of $X$ are those that are universally measurable with respect to $(X, \mathcal B(X))$.

**Cor:** Every analytic subset of a Polish space is universally measurable.

**Lemma:** Let $(X, {\scr A})$, be a measurable space, let $Y$ be a Polish space, and let $C$ be a subset of $X\times Y$ that belongs to the product $\sigma$-algebra ${\scr A}\otimes\mathcal B(Y)$.Then there exists a function $h:X\to Z$ and a subset $D$ of $Z\times Y$ such that
- $h$ is measurable with respect to $\scr A$ and $\mathcal B(2^\omega)$,
- $D\in \mathcal B(2^\omega\times Y)$, and
- $C = H^{-1}[D]$, where $H:X\times Y \to 2^\omega\times Y$ is the map that takes $(x, y)$ to $(h(x), y)$. 

**Lemma:** Let $(X, {\scr A})$ and $(Y, {\scr B})$ be measurable spaces, and let $f:X\to Y$ be $({\scr A}, {\scr B})$-measurable. Then $f$ is measurable with respect to the $\sigma$-algebras $\scr A_*$ and $\scr B_*$ of universally measurable sets. 

**Prop:** Let $(X, {\scr A})$, be a measurable space, let $Y$ be a Polish space, and let $C$ be a subset of $X\times Y$ that belongs to the product $\sigma$-algebra ${\scr A}\otimes\mathcal B(Y)$. Then the projection of $C$ on $X$ is universally measurable with respect to $(X, {\scr A})$. 