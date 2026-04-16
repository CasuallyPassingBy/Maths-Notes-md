---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Lp spaces]], [[Measure Spaces and Measurable Spaces]], [[Scalar Integral on Measure Spaces]], [[Absolute Continuity of Measures]]

**Def:** Let $(X, {\scr A},\mu)$ be a finite measure space, and let $\scr F$ be a subset of ${\scr L}^1(X, {\scr A},\mu)$. Then $\scr F$ is called $L^1$-*bounded* if the set $\{\|f\|_1 \mid f\in \scr F\}$ is bounded aove, is called *uniformly absolutely continuous* if for each $\varepsilon> 0$ there is a $\delta>0$ such that if $A\in \scr A$, $\mu(A) <\delta$, and $f\in \scr F$, then $\int_A |f|\,d\mu<\varepsilon$, and is called *uniformly integrable* if it is $L^1$-bounded and uniformly absolutely continuous.

**Prop:** Let $(X, {\scr A},\mu)$ be a finite measure space, and let $\scr F$ be a subset of ${\scr L}^1(X, {\scr A},\mu)$. Then $\scr F$ is uniformly integrable iff satisfies $$\lim_{a\to\infty}\sup\left\{\left.\int_{\{|f| >a \}}|f|\,d\mu \;\right\rvert\; f\in {\scr F}\right\} =0.  $$