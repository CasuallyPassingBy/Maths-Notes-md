---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Measure Spaces and Measurable Spaces]], [[Scalar Integral on Measure Spaces]], [[Measurable Functions]], [[Finite Product of Measures]]

**Def:** Let $(X, {\scr A})$ and $(Y, {\scr B})$ be measurable spaces. A function $K: X\times {\scr B}\to [0,\infty]$ is called a *kernel* from $(X, {\scr A})$  to $(Y, {\scr B})$ if
- for each $x\in X$, the function $B\mapsto K(x, B)$ is a measure on $(Y, {\scr B})$, and
- for each $B\in\scr B$, the function $x\mapsto K(x, B)$ is $\scr A$-measurable.

**Prop:** Suppose that $K$ is a kernel form $(X, {\scr A})$  to $(Y, {\scr B})$, that $\mu$ is a measure on $(X, {\scr A})$, and that $f: Y \to [0,\infty]$ is $\scr B$-measurable. Then the following statements are true
- $\nu(B) = \int K(x, B)\, \mu(dx)$ is a measure on $(Y, {\scr B})$. 
- $x\mapsto \int f(y)K(x, dy)$ is an $\scr A$-measurable function on $X$.
Moreover, we know that  $$\int f(y)\,\nu(dy) = \int\left(\int f(y)K(x, dy)\right)\,\mu(dx).$$
**Prop:** Suppose that $K$ is a kernel form $(X, {\scr A})$  to $(Y, {\scr B})$, that $\mu$ is a finte measure on $(X, {\scr A})$, that $\sup\{K(x, Y) \mid x\in X\}$ is finte, and that $f: Y \to \overline{\Bbb R}$ is bounded and $\scr B$-measurable. We define the measure $\nu: {\scr B}\to [0,\infty]$ to be $\nu(B) := \int K(x, B)\,\mu(dx)$. Then
- $x\mapsto \int  f(y)K(x, dy)$ is a bounded $\scr A$-measurable function on $X$, and
$$\int f(y)\,\nu(dy) = \int\left(\int f(y)K(x, dy)\right)\,\mu(dx).$$

**Prop:** Let $(X, {\scr A})$ and $(Y, {\scr B})$ be measurable spaces, and let $K$ be a kernel from $(X, {\scr A})$ to $(Y, {\scr B})$ such that $K(x, Y)$ is finite for each $x\in X$. 
- The formula $(x, E) \mapsto K(x, E_x)$ defines a kernel from $(X, {\scr A})$ to $(X\times Y, {\scr A\otimes B})$.
- If $\mu$ is a measure on $(X, {\scr A})$, then  $$\nu(E):= \int K(x, E_x)\, \mu(dx) $$defines a measure on $\scr A\otimes B$.
- If, in addition, $f:X\times Y\to [0,\infty]$ is $\scr A\otimes B$-measurable then, $x\mapsto \int f(x, y)\, K(x, dy)$ is $\scr A$-measurable, and $$\int f\, d\nu = \int_X\left(\int_Y f(x, y)\, K(x, dy)\right)\, \mu(dx).$$