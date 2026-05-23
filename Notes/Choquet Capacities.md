---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Hausdorff Spaces]], [[Measures]], [[Polish Spaces]], [[Measures on Polish Spaces]], [[Borel Sets]], [[Compactness]]

**Def:** Let $X$ be a Hausdorff space. A *capacity* on $X$ is a function $I: \mathcal P(X) \to\overline{\Bbb R}$ such that
- if $A\subseteq B\subseteq X$, then $I(A) \le I(B)$,
- each increasing sequence $(A_n)_{n<\omega}$ of subsets of $X$ satisfies $$I\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty} I(A_n), $$and
- each decreasing sequence $(K_n)_{n<\omega}$ of compact subsets of $X$ satisfies $$I\left(\bigcap_{n<\omega} K_n\right) = \lim_{n\to\infty} I(K_n). $$
A subset $A$ of $X$ is $I$-*capacitable* if $$I(A) = \sup\{I(K) \mid K \subseteq A \land K \text{ is compact}\}. $$
**Choquet Capacitability Theorem:** If $X$ is a Polish space and if $I$ is a capacity on $X$, then every relatively compact analytic subset of $X$ is $I$-capacitable. 

**Prop:** Let $X$ be a Polish space that is not $\sigma$-compact, and define $I: \mathcal P(X) \to \overline{\Bbb R}$ by letting $I(A)$ be $0$ if $A$ is included in some $\sigma$-compact set and letting $I(A)$ be $1$ otherwise. Then $I$ is a capacity on $X$, and there is an analytic subset of $X$ that is not $I$-capacitable. 

# Abstract Choquet Capacities

**Def:** Let $\scr F$ be a collection of subsets of $X$. Then an $\scr F$-capacity is a function $I: \mathcal P(X) \to\overline{\Bbb R}$ such that
- if $A\subseteq B\subseteq X$, then $I(A) \le I(B)$,
- each increasing sequence $(A_n)_{n<\omega}$ of subsets of $X$ satisfies $$I\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty} I(A_n), $$and
- each decreasing sequence $(A_n)_{n<\omega}$ of elements in $\scr F$ of $X$ satisfies $$I\left(\bigcap_{n<\omega} A_n\right) = \lim_{n\to\infty} I(A_n). $$ 
A subset $A\subseteq X$ is $({\scr F}, I)$-capacitable if, for $$I(A) = \sup\{I(B) \mid B\subseteq A \land B\in {\scr F}_\delta\},$$where ${\scr F}_\delta$ denotes the collection of countable intersection of sets of $\scr F$. 

**Obs:** Note that in the case of Hausdorff spaces, we see that $\scr F$ is just the set of compact sets, and $\scr F_\delta$ is equal to $\scr F$. 