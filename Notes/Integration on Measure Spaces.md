---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure Spaces and Measurable Spaces]], [[Measurable Functions]]

**Def:** Let $(X, {\cal A})$ be a measurable space. We will denote by $\cal S$ the collection of all simple real-valued $\cal A$-measurable functions on $X$ and by $\cal S_+$ the collection of nonnegative functions in $\cal S$.

**Def:** Let $\mu$ be a measure on $(X, {\cal A})$. If $f$ belongs to $\cal S_+$ and is given by $f = \sum_{i = 1}^m a_i \chi_{A_i}$where $a_1,\dots, a_m$ are nonnegative real numbers and $A_1,\dots, A_m$ are disjoint subsets of $X$ that belong to $\cal A$, then $\int f\, d\mu$. the *integral* of $f$ with respect to $\mu$ is defined as $$\int f\, d\mu := \sum_{i = 1}^n a_i\mu(A_i).$$

**Prop:** Let $(X, {\cal A}, \mu)$ be a measure space, and let $f, g\in \cal S_ +$, and let $\alpha \ge 0$. Then
- $\int af\, d\mu = a \int f\, d\mu,$
- $\int (f+g)\, d\mu = \int f\,d \mu + \int g\, d\mu$,
- if $f(x) \le g(x)$ holds for each $x\in X$, then $\int f\, d\mu \le \int g\, d\mu$. 

**Prop:** Let $(X, {\cal A}, \mu)$ be a measure space, and let $f\in \cal S_+$ and let $(f_n)$ be a non decreasing sequence of functions in $\cal S_+$ such that $f(x) = \lim f_n(x)$ holds for each $x\in X$. Then $$\int f\, d\mu = \lim_{n \to \infty} \int f_n \, d\mu.$$
**Def:** We define the integral of an arbitrary $f: X \to [0, \infty]$ $\cal A$-measurable function on $X$. For such a function $f$, let$$\int f\, d\mu := \sup\left\{\left.\int g \, d\mu \; \right\rvert\; g\in {\cal S}_+ \land g \le f\right\}. $$


**Prop:** Let $(X, {\cal A}, \mu)$ be a measure space, and let $f: X \to [0, \infty]$ be a $\cal A$-measurable function on $X$, and let $\{f_n\}$ be a non-decreasing sequence of functions in $\cal S_+$ such that $f(x) = \lim f_n(x)$ holds for each $x\in X$. Then $$\int f\, d\mu = \lim_{n\to \infty}\int f_n\, d\mu.$$
**Prop:** Let $(X, {\cal A}, \mu)$ be a measure space, and let $f, g: X \to [0,\infty]$ be $\cal A$-measurable functions on $X$, and let $\alpha \ge 0$. Then
- $\int \alpha f\, d\mu = \alpha \int f\, d\mu$,
- $\int (f+g)\, d\mu = \int f\, d\mu+ \int g\, d\mu$, and
- if $f(x) \le g(x)$ holds at each $x\in X$, then $\int f\, d\mu \le \int g\,d\mu$.