---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure Spaces and Measurable Spaces]], [[Measurable Functions]], [[Measures]], [[Lebesgue Integral on Measure Spaces]]

**Def:**  Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. The sequence $(f_n)_{n<\omega}$ *converges to $f$ pointwise $\mu$ a.e.* if $$f(x) = \lim_{n\to\infty} f_n(x)$$ holds at $\mu$-almost every point $x\in X$. We also say that the sequence $(f_n)_{n<\omega}$ *converges to $f$ almost everywhere.*

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$, and let $g:\Bbb R\to\Bbb R$ be Borel measurable. The sequence $(f_n)_{n<\omega}$ converges to $f$ almost everywhere and if $g$ is continuous at $f(x)$ for almost every $x$, then $(g\circ f_n)_{n<\omega}$ converges to $g\circ f$ almost everywhere.

**Def:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. The sequence $(f_n)_{n<\omega}$ *converges to $f$ uniformly a.e.* if there exists a set $E$ with $\mu(X\setminus E) = 0$ such that $f_n \to f$ uniformly on $E$. 

**Def:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. The sequence $(f_n)_{n<\omega}$ *converges to $f$ in measure* if for any $\varepsilon > 0$, $$\lim_{n\to\infty} \mu(\{x\in X\mid |f_n(x) - f(x)| > \varepsilon\}) = 0$$
**Example:** Let $(X, {\scr A},\mu)$ be a measure space, and let $A\in \scr A$ and $\{A_n\}_{n<\omega}\subseteq\scr A$.
- $(\chi_{A_n})_{n<\omega}$ converges to $0$ in measure iff $\lim \mu(A_n) = 0$.
- $(\chi_{A_n})_{n<\omega}$ converges to $0$ almost everywhere iff $\mu(\limsup A_n) = 0$. 
- $(\chi_{A_n})_{n<\omega}$ converges to $\chi_A$ almost everywhere iff the three sets $A$, $\limsup A_n$, and $\liminf A_n$ differ only by $\mu$-null sets. 

**Obs:** If $(\Bbb N, \mathcal P(N), \mu)$ be a measure space with the counting measure. Then a sequence of measurable functions $(f_n)_{n<\omega}$ that converges in measure to $f$ iff it converges uniformly to $f$. 

**Prop:** Suppose that $(X, {\scr A},\mu)$ is a measure space and let

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. If $\mu$ is finite and $(f_n)_{n<\omega}$ converges to $f$ almost everywhere, then $(f_n)_{n<\omega}$ converges to $f$ in measure.

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. If $(f_n)_{n<\omega}$ converges to $f$ in measure, then there is subsequence of $(f_n)_{n<\omega}$ that converges to $f$ almost everywhere.

**Prop:** Let $(X, {\scr A}, \mu)$ be a finite measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. The sequence $(f_n)_{n<\omega}$ converges to $f$ in measure iff if each subsequence of $(f_n)_{n<\omega}$ has a subsequence that converges to $f$ almost everywhere. 

**Def:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. The sequence $(f_n)_{n<\omega}$ *converges to $f$ almost uniformly* if for each $\varepsilon >0$ there is a $B\in {\scr A}$ such that $\mu(X\setminus B) < \varepsilon$, and $f_n\to f$ uniformly (a.e.) on $B$. 

**Obs:** $$\text{Uniform a.e Conv.} \implies \text{Almost Uniform Conv.} \implies \text{Pointwise a.e. Conv.}$$

**Obs:** In a finite measure space pointwise a.e. convergence is equivalent to almost uniform convergence.

**Egoroff's Theorem:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ be extended real-valued $\scr A$-measurable functions on $X$. If $\mu$ is finite and if $(f_n)_{n<\omega}$ converges to $f$ almost everywhere, then $(f_n)_{n<\omega}$ converges almost uniformly to $f$.

**Obs:** In the proof of Egoroff's Theorem we prove a related fact that convergence in measure implies, in finite measure sets, almost uniform convergence.

**Prop:** Let $(X, {\scr A}, \mu)$ be a finite measure space, $f, f_0, f_1, f_2,\dots$ and a$g,g_0, g_1, g_2,\dots$ be real-valued $\scr A$-measurable function on $X$. If $\mu$ is finite, if $(f_n)_{n<\omega}$ converges to $f$ in measure, and if $(g_n)_{n<\omega}$ converges to $g$ in measure, then $(fg)_{n<\omega}$ converges to $fg$ in measure. 

**Def:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ belong to ${\scr L}^1(X, {\scr A},\mu, \Bbb R)$. Then $(f_n)_{n<\omega}$ *converges to $f$ in mean* if $$\lim_{n\to \infty}\int |f_n-f|\, d\mu = 0.$$
**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ belong to ${\scr L}^1(X, {\scr A}, \mu, \Bbb R)$. If $(f_n)_{n<\omega}$ converges to $f$ in mean, then $(f_n)_{n<\omega}$ converges to $f$ in measure. 

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ belong to ${\scr L}^1(X, {\scr A}, \mu, \Bbb R)$. If $(f_n)_{n<\omega}$ converges to $f$ almost everywhere or in measure, and if there is a nonnegative extended real-valued integrable function $g$ such that $$|f_n| \le g \text{ (for }n <\omega),\quad |f| \le g$$ hold almost everywhere, then $(f_n)_{n<\omega}$ converges to $f$ in mean.

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f$ and $f_0,f_1,f_2, \dots$ belong to ${\scr L}^1(X, {\scr A}, \mu, \Bbb R)$. If $(f_n)_{n<\omega}$ converges to $f$ in mean so fast that $$\sum_{n = 0}^\infty \int |f_n-f|\, d\mu <\infty, $$then $(f_n)_{n<\omega}$ converges to $f$ almost everywhere. 

**Prop:** Suppose $(X, {\scr A}, \mu)$ is a finite measure space. Let $T := [t_0,\infty)$, $\{f_t: X \to \Bbb R\mid t \in T\}$ is a collection of $\scr A$-measurable function, and $f:X \to \Bbb R$ is a $\scr A$-measurable function such that $\lim f_t(x) = f(x)$ almost everywhere. If for each $n<\omega$, defined $g_n(x) := \sup_{t\in [n,\infty)}|f_t(x)-f(x)|$ is measurable, then $(f_t)_{t\in T}$ converges to $f$ almost uniformly. 

