---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Measure Spaces and Measurable Spaces]], [[Rings and Algebras of Sets]]

**Def:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a function on $\scr A$ with values in $\overline{ \Bbb R}$. The function $\mu$ is *finitely additive* if the additive$$\mu\left(\bigcup_{i = 1}^nA_i\right) = \sum_{i = 1}^n \mu(A_i) $$holds for each finite sequence $\{A_i\mid 1\le i \le n\}$ of disjoint sets in $\scr A$ is *countably additive* if the identity $$\mu\left(\bigcup_{i = 0}^\infty A_i\right) = \sum_{i = 0}^\infty \mu(A_i)$$holds for each infinite sequence $\{A_n\}_{n<\omega}$ of disjoint sets in $\scr A$. If $\mu$ is countably additive and satisfies $\mu(\varnothing) = 0$, the it is a *signed measure*. A signed measure is *finite* if neither $-\infty$ nor $\infty$ occurs among its values.

**Obs:** Suppose $\mu$ is a signed measure on the measurable space $(X, {\scr A})$. Then for each $A\in \scr A$ the sum $\mu(A) + \mu(X\setminus A)$ must be defined and must be equal to $\mu(X)$. Hence if there is a set $A\in\scr A$ for which $\mu(A) = \pm\infty$, then $\mu(X) = \pm\infty$. Consequently, a signed measure can attain at most one of the values $\infty$ and $-\infty$. We see that if $B\in \scr A$ for which $\mu(B)$ is finite, then $\mu(A)$ is finite for each $\scr A$-measurable $A\subseteq B$.

**Lemma:** Let $(X, \scr A)$ be a measurable space, and let $\mu$ be a signed measure on $(X, {\scr A})$. If $\{A_n\}_{n<\omega}$ is an increasing sequence of sets in $\scr A$, then $$\mu\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty}\mu(A_n), $$
and if $\{A_n\}_{n<\omega}$ is a decreasing sequence of sets in $\scr A$ such that $\mu(A_n)$ is finite for some $n<\omega$, then $$\mu\left(\bigcap_{n<\omega} A_n\right) = \lim_{n\to \infty} A_n. $$
**Lemma:** Suppose that $(X, \scr A)$ is a measurable space and that $\mu$ is an extender real-valued function on $\scr A$ that is finitely additive and satisfies $\mu(\varnothing)= 0$. If $\mu\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty}\mu(A_n)$ holds for each increasing $\{A_n\}_{n<\omega}$ of sets in $\scr A$ or if $\mu\left(\bigcap_{n<\omega} A_n\right) = 0$ holds for each decreasing $\{A_n\}_{n<\omega}$ of sets in $\scr A$ for which $\bigcap_{n<\omega} A_n = \varnothing$, then $\mu$ is a signed measure.

**Def:** Let $\mu$ be a signed measure on the measurable space $(X, \scr A)$. A subset $A$ of $X$ is a *positive set* for $\mu$ if $A\in \scr A$ and each $\scr A$-measurable $E\subseteq A$ satisfies $\mu(E) \ge 0$. Likewise $A$ is a *negative set* for $\mu$ if $A\in \scr A$ and each $\scr A$-measurable $E\subseteq A$ satisfies $\mu(E) \le 0$.

**Prop:** Let $\mu$ be a signed measure on the measurable space $(X, {\scr A})$, and let $A\in \scr A$ such that $-\infty< \mu(A)< 0$. Then there is a negative set $B$ that is included in $A$ and satisfies $$\mu(B) <\mu(A). $$
**Hahn Decomposition Theorem:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a signed measure on $(X, {\scr A})$. Then there are disjoint subsets $P$ and $N$ of $X$ such that $P$ is a positive set for $\mu$ and $N$ is a negative set for $\mu$, and $X = P \cup N$. 