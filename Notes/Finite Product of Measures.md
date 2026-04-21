---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Product of sigma-Algebras]], [[Measure Spaces and Measurable Spaces]], [[Outer Measures]], [[Fubini's Theorem in Rn]]

**Def:** Let us introduce some terminology and notation. Suppose that $X$ and $Y$ are sets and $E\subseteq X\times Y$. Then for each $x\in X$ and $y\in Y$ the *sections* $E_x$ and $E^y$ are the subsets of $Y$ and $X$ given by  $$E_x := \{y\in Y\mid (x,y)\in E\} \quad \text{and} \quad E^y := \{x\in X\mid (x, y)\in E\}. $$If $f$ is a function on $X \times Y$, then the *sections* $f_x$ and $f^y$ are functions on $Y$ and $X$ given by $$f_x(y) := f(x, y) \quad \text{and} \quad f^y(x) := f(x, y). $$
**Lemma:** Let $(X. {\scr A})$ and $(Y, {\scr B})$ be measurable spaces.
- If $E\subseteq X\times Y$ that belongs to ${\scr A} \otimes {\scr B}$, then each section $E_x$ belongs to $\scr B$ and each section $E^y$ belongs to $\scr A$.
- If $f$ is an extended real-valued, or a complex-valued, ${\scr A}\otimes \scr B$-measurable function on $X\times Y$, then each section $f_x$ is $\scr B$-measurable and each section $f^y$ is $\scr A$-measurable.

**Prop:** Let $(X, {\scr A}, \mu)$ and $(Y, {\scr B},\nu)$ be $\sigma$-finite measure spaces. If $E\in {\scr A}\otimes\scr B$, then the function $x\mapsto \nu(E_x)$ is $\scr A$-measurable and the function $y\mapsto \mu(E^y)$ is $\scr B$-measurable.

**Th:** Let $(X, {\scr A}, \mu)$ and $(Y, {\scr B},\nu)$ be $\sigma$-finite measure spaces. Then there is a unique measure $\mu \times \nu$ on the $\sigma$-algebra $\scr A\otimes B$ such that $$(\mu \times \nu)(A \times B) = \mu(A) \nu(B) $$holds for each $A\in \scr A$ and $B\in \scr B$. Furthermore, the measure under $\mu\times \nu$ of an arbitrary set $E\in \scr A\otimes B$ is given by  $$(\mu \times \nu)(E) =\int_X \nu(E_x)\, \mu(dx) = \int_Y \mu(E^y)\, \nu(dy).$$The measure $\mu\times\nu$ is called the *product* of $\mu$ and $\nu$. 

**Cor:** Let $(X, {\scr A}, \mu)$ and $(Y, {\scr B},\nu)$ be $\sigma$-finite measure spaces, and let $E\in \scr A\otimes B$. If $\mu$-almost every section $E_x$ has measure zero under $\nu$, then $\nu$-almost every $E^y$ has measure zero under $\mu$.

**Prop:** Let $(X, {\scr A})$ and $(Y, {\scr B})$ be measurable spaces, and let $K$ be a [[Kernels in Measure Theory|kernel]] from $(X, {\scr A})$ to $(Y, {\scr B})$ such that $K(x, Y)$ is finite for each $x\in X$. 
- The formula $(x, E) \mapsto K(x, E_x)$ defines a kernel from $(X, {\scr A})$ to $(X\times Y, {\scr A\otimes B})$.
- If $\mu$ is a measure on $(X, {\scr A})$, then  $$E\mapsto \int K(x, E_x)\, \mu(dx) $$defines a measure on $\scr A\otimes B$.
- We see that that if $(Y, {\scr B},\nu)$ is a finite measure space and $(X, {\scr A},\mu)$ is a measurable space, then we can define a kernel $K(x, E) := \nu(E)$. Then the measure defined above is precisely the product measure on $(X\times Y, {\scr A\otimes B})$. 

**Tonelli's Theorem:** Let $(X, {\scr A}, \mu)$ and $(Y, {\scr B}, \nu)$ be $\sigma$-finite measure spaces, and let $f:X\times Y \to [0,\infty]$ be $\scr A\otimes B$-measurable. Then
- the function $x\mapsto \int_Y f_x\, d\nu$ is $\scr A$-measurable and the function $y\mapsto \int_X f^y\, d\mu$ is $\scr B$-measurable, and
- $f$ satisfies $$\int_{X\times Y} f\, d(\mu\times \nu) = \int_X \left(\int_Y f_x\, d\nu\right)\, \mu(dx) = \int_Y\left(\int_X f^y\,d\mu \right)\, \nu(dy). $$We can rewrite the equation above as $$\begin{align*}
  \int_{X\times Y}f(x, y)\, d(\mu \times \nu)(x, y) &= \int_X \left(\int_Y f(x, y)\, \nu(dy)\right)\, \mu(dx)\\ &= \int_Y \left(\int_X f(x, y)\, \mu(dx)\right)\, \nu(dy)
  \end{align*}$$

**Fubini's Theorem:** Let $(X, {\scr A}, \mu)$ and $(Y, {\scr B}, \nu)$ be $\sigma$-finite measure spaces, and let $f:X\times Y \to\overline{\Bbb R}$ be $\scr A\otimes B$-measurable and $\mu \times \nu$-integrable. Then
- for $\mu$-almost every $x\in X$ the section $f_x$ is $\nu$-integrable and for $\nu$-almost every $y\in Y$ the sections $f^y$ is integrable, 
- the function $I_f$ and $J_f$ defined by $$I_f(x) := \begin{cases}\int_Y f_x\, d\nu, & \text{if $f_x$ is $\nu$-integrable,} \\ 0 & \text{otherwise} \end{cases} $$and $$J_f(y) := \begin{cases}\int_Y f^y\, d\mu, & \text{if $f_x$ is $\mu$-integrable,} \\ 0 & \text{otherwise} \end{cases}$$belong to ${\scr L}^1(X, {\scr A}, \mu, \Bbb C)$ and ${\scr L}^1(X, {\scr A}, \nu, \Bbb C)$, respectively, and
- the relation $$\int_{X\times Y} f\, d(\mu\times \nu) = \int_X I_f\, d\mu = \int_Y J_f\, d\nu$$holds.