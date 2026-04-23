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
- the function $I_f$ and $J_f$ defined by $$I_f(x) := \begin{dcases}\int_Y f_x\, d\nu, & \text{if $f_x$ is $\nu$-integrable,} \\ \\ 0 & \text{otherwise} \end{dcases} $$and $$J_f(y) := \begin{dcases}\int_Y f^y\, d\mu, & \text{if $f_x$ is $\mu$-integrable,} \\ \\ 0 & \text{otherwise} \end{dcases}$$belong to ${\scr L}^1(X, {\scr A}, \mu, \Bbb C)$ and ${\scr L}^1(X, {\scr A}, \nu, \Bbb C)$, respectively, and
- the relation $$\int_{X\times Y} f\, d(\mu\times \nu) = \int_X I_f\, d\mu = \int_Y J_f\, d\nu$$holds.

**Fubini-Tonelli Theorem:** Let $(X, {\scr A}, \mu)$ and $(Y, {\scr B}, \nu)$ be $\sigma$-finite measure spaces, and let $f:X\times Y \to\overline{\Bbb R}$, then $$\int_{X\times Y} |f|\, d(\mu\times \nu) = \int_X \left(\int_Y |f_x|\, d\nu\right)\, \mu(dx) = \int_Y\left(\int_X |f^y|\,d\mu \right)\, \nu(dy). $$Furthermore, if any of these integrals is finite, then  $$\int_{X\times Y} f\, d(\mu\times \nu) = \int_X \left(\int_Y f_x\, d\nu\right)\, \mu(dx) = \int_Y\left(\int_X f^y\,d\mu \right)\, \nu(dy).  $$

**Prop:** Let $(X, {\scr A}, \mu)$ and $(Y, {\scr B}, \nu)$ be measure spaces, and let $f:X\times Y\to [0, \infty]$ be $\scr A\otimes B$-measurable. If $\mu$ and $\nu$ are sums of series of finite measures, then the function $x\mapsto \int f(x, y)\, \nu(dy)$ and $y\mapsto \int f(x, y)\, \mu(dx)$ are measurable, and  $$\int_X \left(\int_Y f(x, y)\, \nu(dy)\right)\, \mu(dx) =\int_Y \left(\int_X f(x,y) \, \mu(dx)\right)\, \nu(dy). $$
**Prop:** Let $(X, {\scr A})$ and $(Y, {\scr B})$ be a measurable spaces, let $\mu_1$ and $\mu_2$ be finite measures on $(X, {\scr A})$, and let $\nu_1$ and $\nu_2$ be finite measures on $(Y, {\scr B})$. If $\mu_2 \ll \mu_1$ and $\nu_2\ll\nu_1$, then $\mu_2\times \nu_2\ll \mu_1 \times\nu_1$, and $$\frac{d(\mu_2\times \nu_2)}{d(\mu_1\times \nu_1)}(x, y) = \frac{d\mu_2}{d\mu_1}(x) \frac{d\nu_2}{d\nu_1}(y).$$

## Applications

**Prop:** Let $(X, {\scr A}, \mu)$ be a $\sigma$-finite measure space, let $\lambda$ be Lebesgue measure on $(\Bbb R, {\cal B}(\Bbb R)),$ and let $f:X \to [0,\infty]$ be $\scr A$-measurable. We have the useful relation $$\int_X f(x)\, \mu(dx) =\int_0^\infty \mu(\{x\in X\mid f(x) >y\}) \, \lambda(dy). $$
**Cor:** Let $\mu$ be a $\sigma$-finite on $(X, {\scr A})$, and let $f,g:X \to [0, \infty]$ be $\scr A$-measurable functions such that  $$\mu(\{x\in X\mid f(x) > t\}) \le \mu(\{x\in X\mid g(x) > t\}) $$holds for each positive $t$. Then $$\int f\, d\mu \le \int g\, d\mu. $$
**Cor:** **Prop:** Let $(X, {\scr A}, \mu)$ be a $\sigma$-finite measure space, let $\lambda$ be Lebesgue measure on $(\Bbb R, {\cal B}(\Bbb R)),$ let $f:X \to [0,\infty]$ be $\scr A$-measurable, and $p\in [1, \infty)$. We have the useful relation $$\int_X f^p\, d\mu =\int_0^\infty p t^{p-1} \mu(\{x\in X\mid f(x) >t\}) \, \lambda(dt). $$

**Prop:** Let $\sum_{m, n} a_{m, n}$ be a [[double series]], and let $\mu$ be counting measure on $\Bbb N$. The series $\sum_{m, n} a_{m,n}$ is absolutely convergent iff if the function $(m,n)\mapsto a_{m, n}$ is $\mu\times\mu$-integrable. Thus we see that if $\sum_{m,n} a_{m,n}$ if absolutely convergent, then $\sum_{m = 1}^\infty \sum_{n = 1}^\infty a_{m,n} =\sum_{n = 1}^\infty \sum_{m = 1}^\infty a_{m,n}$; in other words, the order of summation can be reversed for absolutely convergent series. 

**Prop:** Let $F, G :\Bbb R\to\Bbb R$ be bounded nondecreasing right-continuous functions that vanish at $-\infty$, let $\mu_F$ and $\mu_G$ be the measures they induce on ${\mathcal B}(\Bbb R)$, and let $a, b\in\Bbb R$ such that $a<b$. Then  $$\int_{[a,b]} \frac{F(x)+F(x-)}{2} \mu_G(dx) + \int_{[a,b]} \frac{G(x)+ G(x-)}{2} = F(b)G(b)-F(a-)G(a-).$$If, in addition, the functions $F$ and $G$ have no points of discontinuity in common, then the equation above can be simplified to $$\int_{[a, b]}F(x)\, \mu_G(dx) + \int_{[a,b]} G(x)\, \mu_F(dx) =  F(b)G(b)-F(a-)G(a-). $$
**Prop:** Let $f$ and $g$ belong to ${\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$. Then 
- for almost every $x$ the function $f(x-t)g(t)$ belongs to ${\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$, and
- the function $f*g$ defined by $$(f*g)(x) := \begin{dcases}
  \int f(x-t)g(t)\, \lambda(dt) & \text{if }t \mapsto f(x-t)g(t) \text{ is Lebesgue integrable,} \\ \\0 & \text{otherwise}
  \end{dcases} $$belongs to $\mathscr L^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$ and satisfies $\|f*g\|_1 \le \|f\|_1 \|g\|_1$. 

The *convolution* of the functions $f, g\in {\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$ is the function $f*g$ defined above. Note that if $f_1, f_2, g_1, g_2\in {\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$ and if $f_1 = f_2$ and $g_1 = g_2$ hold $\lambda$-almost everywhere, then $(f_1*g_1)(x) = (f_2*g_2)(x)$ holds for each $x\in \Bbb R$. Thus, convolution, which we have defined as an operator that assigns a function ${\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$ to each pair of functions in ${\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$, can be considered as an operator that assigns an element of $L^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$ to each pair of elements of $L^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$. In addition, note that the convolution operator is bilinear. 

**Prop:** The convolution operator is associative.

**Prop:** Let $f$ and $g$ belong to ${\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$. Then $f*g = g*f$. 

**Prop:** If $f, g\in {\scr L}^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$, and $g$ is bounded, then $f*g$ is continuous.

**Obs:** We see that $L^1(\Bbb R, \mathcal B(\Bbb R), \lambda)$ is a commutative Banach algebra under the convolution.