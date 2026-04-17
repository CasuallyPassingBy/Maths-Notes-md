---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Lp spaces]], [[Measure Spaces and Measurable Spaces]], [[Scalar Integral on Measure Spaces]], [[Absolute Continuity of Measures]], [[Modes of Convergence using Measure]]

**Def:** Let $(X, {\scr A},\mu)$ be a finite measure space, and let $\scr F$ be a subset of ${\scr L}^1(X, {\scr A},\mu)$. Then $\scr F$ is called $L^1$-*bounded* if the set $\{\|f\|_1 \mid f\in \scr F\}$ is bounded aove, is called *uniformly absolutely continuous* if for each $\varepsilon> 0$ there is a $\delta>0$ such that if $A\in \scr A$, $\mu(A) <\delta$, and $f\in \scr F$, then $\int_A |f|\,d\mu<\varepsilon$, and is called *uniformly integrable* if it is $L^1$-bounded and uniformly absolutely continuous.

**Obs:** Let $(X, {\scr A},\mu)$ be a finite measure space, and let $\scr F$

**Prop:** Let $(X, {\scr A},\mu)$ be a finite measure space, and let $\scr F$ be a subset of ${\scr L}^1(X, {\scr A},\mu)$. Then $\scr F$ is uniformly integrable iff satisfies $$\lim_{a\to\infty}\sup\left\{\left.\int_{\{|f| >a \}}|f|\,d\mu \;\right\rvert\; f\in {\scr F}\right\} =0.  $$
**Prop:** If $(X, {\scr A},\mu)$ is a finite measure space, then every finite subset of ${\scr L}^1(X, {\scr A}, \mu)$ is uniformly integrable. 

**Prop:** Let $(X, {\scr A},\mu)$ be a finite measure space, and let $g$ be a nonnegative function that belongs to ${\scr L}^1(X, {\scr A},\mu)$. If $\scr F$ is a collection of measurable functions $|f(x)|\le g(x)$ holds for each $f\in \scr F$ and each $x\in X$, then $\scr F$ is uniformly integrable.

**Prop:** Let $(X, {\scr A},\mu)$ be a finite measure space, let $\{f_n\}_{n<\omega}\subseteq {\scr L}^1(X, {\scr A}, \mu)$, and let $f$ be an $\scr A$-measurable function on $X$.
- If $\{f_n\}_{n<\omega}$ is uniformly integrable and if $(f_n)_{n<\omega}$ converges to $f$ in measure, then $f$ integrable and $$\int f\,d\mu = \lim_{n\to \infty}\int f_n\, d\mu.$$
- If $f\in {\scr L}^1(X, {\scr A}, \mu)$. Then $(f_n)_{n<\omega}$ converges to $f$ in mean iff $\{f_n\}_{n<\omega}$ is uniformly integrable and converges to $f$ in measure.