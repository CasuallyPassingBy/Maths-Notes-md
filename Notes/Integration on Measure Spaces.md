---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measure Spaces and Measurable Spaces]], [[Measurable Functions]]

**Def:** Let $(X, {\scr A})$ be a measurable space. We will denote by $\cal S$ the collection of all simple real-valued $\scr A$-measurable functions on $X$ and by $\cal S_+$ the collection of nonnegative functions in $\cal S$.

**Def:** Let $\mu$ be a measure on $(X, {\scr A})$. If $f$ belongs to $\cal S_+$ and is given by $f = \sum_{i = 1}^m a_i \chi_{A_i}$where $a_1,\dots, a_m$ are nonnegative real numbers and $A_1,\dots, A_m$ are disjoint subsets of $X$ that belong to $\scr A$, then $\int f\, d\mu$. the *integral* of $f$ with respect to $\mu$ is defined as $$\int f\, d\mu := \sum_{i = 1}^n a_i\mu(A_i).$$

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f, g\in \cal S_ +$, and let $\alpha \ge 0$. Then
- $\int af\, d\mu = a \int f\, d\mu,$
- $\int (f+g)\, d\mu = \int f\,d \mu + \int g\, d\mu$,
- if $f(x) \le g(x)$ holds for each $x\in X$, then $\int f\, d\mu \le \int g\, d\mu$. 

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f\in \cal S_+$ and let $(f_n)$ be a non decreasing sequence of functions in $\cal S_+$ such that $f(x) = \lim f_n(x)$ holds for each $x\in X$. Then $$\int f\, d\mu = \lim_{n \to \infty} \int f_n \, d\mu.$$
**Def:** We define the integral of an arbitrary $f: X \to [0, \infty]$ $\scr A$-measurable function on $X$. For such a function $f$, let$$\int f\, d\mu := \sup\left\{\left.\int g \, d\mu \; \right\rvert\; g\in {\cal S}_+ \land g \le f\right\}. $$

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f: X \to [0, \infty]$ be a $\scr A$-measurable function on $X$, and let $\{f_n\}$ be a non-decreasing sequence of functions in $\cal S_+$ such that $f(x) = \lim f_n(x)$ holds for each $x\in X$. Then $$\int f\, d\mu = \lim_{n\to \infty}\int f_n\, d\mu.$$
**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $f, g: X \to [0,\infty]$ be $\scr A$-measurable functions on $X$, and let $\alpha \ge 0$. Then
- $\int \alpha f\, d\mu = \alpha \int f\, d\mu$,
- $\int (f+g)\, d\mu = \int f\, d\mu+ \int g\, d\mu$, and
- if $f(x) \le g(x)$ holds at each $x\in X$, then $\int f\, d\mu \le \int g\,d\mu$.

**Def:** Suppose $(X, {\scr A},\mu)$ be a measure space. Let $f: X\to \overline{\Bbb R}$ be a $\scr A$-measurable function. If $\int f^+\, d\mu$ and $\int f^-\, d\mu$ are both finite, then $f$ is *integrable*, or $\mu$*-integrable* or *summable*, and its *integral* $\int f\, d\mu$ is defined by $$\int f\, d\mu := \int f^+\, d\mu - \int f^-\, d\mu. $$The integral of $f$ is said to *exist* it at least one of $\int f^+\, d\mu$ and $\int f^-\, d\mu$ is finte, and again in this case, $\int f\, d\mu$ is defined to be $\int f^+\, d\mu - \int f^-\, d\mu$. In either case one sometimes writes $\int f(x)\, d\mu(x)$ of $\int f\, \mu(dx)$ in place of $\int f\, d\mu$.

Suppose that $f: X\to \overline{\Bbb R}$ is a $\scr A$-measurable and that $A\in \scr A$. Then $f$ is *integrable over $A$* if the function $f\chi_A$ is integrable, and in this case $$\int_A f\, d\mu := \int f\chi_A\, d\mu.$$Likewise, if $A\in \scr A$ and $f$ is a measurable function whose domain is $A$, then the integral of $f$ over $A$ is defined to be integral of the function on $X$ that agrees with $f$ on $A$ and vanishes on $X\setminus A$. 

In the case $X = \Bbb R^d$ and $\mu = \lambda$, one often refers to *Lebesgue integrability* and the *Lebesgue integral*.

**Def:** We define $\mathscr L^1(X, {\scr A}, \mu, \Bbb R)$, or sometimes simple ${\scr L}^1$, to be the set of all $\overline{\Bbb R}$-valued integrable functions on $X$. We see that $\mathscr L^1(X, {\scr A}, \mu, \Bbb R)$ is a vector space and the integral is a linear functional on $\mathscr L^1(X, {\scr A}, \mu, \Bbb R)$. 

**Prop:** Let $(X, {\scr A},  \mu)$ be a measure space, and let $f, g\in \mathscr L^1(X, {\scr A}, \mu. \Bbb R)$. Then $f\lor g$ and $f\land g$ belongs to $\mathscr L^1(X, \mathscr A, \mu, \Bbb R)$. 

**Lemma:** Let $(X, {\scr A},\mu)$ be a measure space, and let $f_1, f_2, g_1$ and $g_2$ be nonnegative real-valued integrable functions on $X$ such that $f_1 - f_2 = g_1-g_2$. then $$\int f_1\, d\mu -\int f_2\, d\mu = \int g_1\, d\mu -\int g_2\, d\mu. $$
**Prop:** Let $(X, {\scr A},\mu)$ be a measure space, and let $f$ and $g$ be real-valued integrable functions on $X$, and let $\alpha\in\Bbb R$. Then
- $\alpha f$ and $f+g$ are integrable,
- $\int \alpha f\, d\mu = \alpha \int f\, d\mu$,
- $\int (f+g)\, d\mu = \int f\, d\mu + \int g\, d\mu$, and
- if $f(x) \le g(x)$ holds at each $x\in X$, then $\int f\, d\mu \le\int g\, d\mu$.

**Examples:**
- If $\mu$ is a finite measure, then every bounded measurable function on $(X, {\scr A}, \mu)$ is integrable.
- Every bounded Borel function on $[a, b]$ is Lebesgue integrable.
- Suppose that $\scr A$ is a the $\sigma$-algebra on $\Bbb N$ containing all subsets of $\Bbb N$ and $\mu$ is the counting measure on $\scr A$. A nonnegative function $f: \Bbb N \to\Bbb R$ is $\mu$-integrable iff the infinite series $\sum_{n <\omega} f(n)$ is convergent, and in that case $\int f\, d\mu = \sum_{n<\omega} f(n)$. If we consider that $f$ to also take negative values, then we know that $f$ is integrable iff $f^+$ and $f^-$ are integrable, meaning that $f$ is integrable iff $\sum_{n<\omega} f(n)$ is absolutely convergent. Meaning that $\mathscr L^1(\Bbb N, {\scr A}, \mu, \Bbb R) = \ell^1$. 
- A measurable function that vanishes almost everywhere is integrable with integral $0$.

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space. and let $f:X \to \overline{\Bbb R}$ be $\scr A$-measurable. Then $f$ is integrable iff $|f|$ is integrable. If these functions are integrable, then $$\left|\int f\, d\mu\right| \le \int|f|\, d\mu.$$
**Prop:** Let $(X, {\scr A},  \mu)$ be a measure space, and let $f, g: X \to \overline{\Bbb R}$ be $\scr A$-measurable and agree almost everywhere. If either $\int f\,d\mu$ or $\int g\, d\mu$ exists, then both exists and $$\int f\, d\mu = \int g\, d\mu.$$
**Prop:** Let $(X, {\scr A},  \mu)$ be a measure space, and let $f: X \to [0, \infty]$ be a $\scr A$-measurable function. If $t >0$ and if $A_t := f^{-1}[t, \infty]$, then $$\mu(A_t) \le \frac1t\int_{A_t} f\, d\mu \le \frac 1t\int f\, d\mu. $$
**Cor:** Let $(X, {\scr A},  \mu)$ be a measure space, and let $f: X \to \overline{\Bbb R}$ be an integrable function on $X.$ Then $\{x\in X\mid f(x) \neq 0\}$ is a $\sigma$-finite under $\mu$.

**Cor:** Let $(X, {\scr A},  \mu)$ be a measure space and let $f: X \to \overline{\Bbb R}$ be a $\scr A$-measurable function on $X$ that satisfies $$\int |f|\, d\mu = 0.$$ Then $f$ vanishes $\mu$-almost everywhere. 

**Cor:** Let $(X, {\scr A},  \mu)$ be a measure space and let $f:X \to \overline{\Bbb R}$ be a integrable function on $X$ such that $\int_A f\, d\mu\ge 0$ holds for all $A$ in $\scr A$, or even just for all $A$ in the smallest $\sigma$-algebra on $X$ that makes $f$ measurable. Then $f\ge 0$ holds $\mu$-almost everywhere.

**Cor:** Let $(X, {\scr A},  \mu)$ be a measure space, and let $f:X \to\overline{\Bbb R}$ be an integrable function on $X.$ Then $|f(x)| < \infty$ holds at $\mu$-almost every $x\in X$.

**Cor:** Let $(X, {\scr A},  \mu)$ be a measure space, and let $f:X\to \overline{\Bbb R}$ be a $\scr A$-measurable function on $X$. Then $f$ is integrable iff there is a function in $\mathscr L^1(X, {\scr A}, \mu, \Bbb R)$ that is equal to $f$ almost everywhere.

## Limit Theorems

**The Monotone Convergence Theorem:** Let $(X, {\scr A},  \mu)$ be a measure space and let be a sequence $(f_n: X\to [0, \infty])_{n<\omega}$ of $\scr A$-measurable functions and $f:X \to [0,\infty]$ also a measurable function. Suppose that $$f_1(x) \le f_2(x) \le \cdots, \qquad \text{and} \qquad f (x) = \lim f_n(x)$$ holds at $\mu$-almost every $x\in X$. Then $$\int f\, d\mu = \lim_{n\to \infty}\int f_n\, d\mu. $$
**Cor (Beppo Levi's Theorem):** Let $(X, {\scr A},  \mu)$ be a measure space. and $\sum_{k = 0}^\infty f_k$ be an infinite series whose terms is a sequence of nonnegative $\scr A$-measurable functions on $X$. Then $$\int\sum_{k = 0}^\infty f_k\, d\mu = \sum_{k = 0}^\infty \int f_k\, d\mu. $$
**Cor (Monotone Convergence Theorem Revised Version):** Let $(X, {\scr A},  \mu)$ be a measure space and let be a sequence $(f_n: X\to \overline{\Bbb R})_{n<\omega}$ of $\scr A$-measurable functions and $f:X \to [0,\infty]$ also a measurable function. Suppose that $f_1$ is integrable, $$f_1(x) \le f_2(x) \le \cdots, \qquad \text{and} \qquad f (x) = \lim f_n(x)$$ holds at $\mu$-almost every $x\in X$. Then $$\int f\, d\mu = \lim_{n\to \infty}\int f_n\, d\mu. $$
**Cor (Monotone Convergence Theorem Decreasing Version):** Let $(X, {\scr A},  \mu)$ be a measure space and let be a sequence $(f_n: X\to \overline{\Bbb R})_{n<\omega}$ of $\scr A$-measurable functions and $f:X \to [0,\infty]$ also a measurable function. Suppose that $f_1$ is integrable, $$f_1(x) \ge f_2(x) \ge \cdots, \qquad \text{and} \qquad f (x) = \lim f_n(x)$$ holds at $\mu$-almost every $x\in X$. Then $$\int f\, d\mu = \lim_{n\to \infty}\int f_n\, d\mu. $$

**Example:** Let $(X, {\scr A},  \mu)$ be a measure space and $f: X \to [0, \infty]$ be a $\scr A$-measurable. We define a function $\nu: {\scr A}\to [0, \infty]$ by $\nu(A) := \int_A f\, d\mu$. Then $\nu(\varnothing) = 0$, and let $\{A_n\}_{n<\omega}\subseteq\scr A$ of pairwise disjoint sets, then $\nu(\bigcup_{n <\omega} A_n)  = \sum_{n <\omega} \nu(A_n)$. Thus $\nu$ is a measure on $(X, {\scr A})$. Moreover $\nu$ is a finite measure iff $f$ is $\mu$-integrable.

**Fatou's Lemma:** Let $(X, {\scr A},  \mu)$ be a measure space. and let $\{f_n\}$ be a sequence of non negative $\scr A$-measurable functions on $X$. Then $$\int \liminf_{n \to \infty} f_n\, d\mu \le \liminf_{n\to \infty}\int f_n\, d\mu. $$
**Lebesgue's Dominated Convergence Theorem:** Let $(X, {\scr A},  \mu)$ be a measure space. let $g:X \to [0,\infty]$ be an integrable function on $X$, and let $f$ and $f_n: X \to \overline{\Bbb R}$ be a sequence of $\scr A$-measurable functions on $X$ such that $$f(x) = \lim_{n\to\infty}f_n(x),\quad \text{and} \quad |f_n(x)| \le g(x) $$holds at $\mu$-almost every $x$ in $X$. Then for each $n< \omega$, $f_n$ is integrable, $f$ is also integrable, and $$\int f\, d\mu = \lim_{n\to \infty}\int f_n\, d\mu. $$
**Lebesgue's Dominated Convergence Theorem V.2.:** Let $(X, {\scr A},  \mu)$ be a measure space. let $g:X \to [0,\infty]$ be an integrable function on $X$, and let $f$ and $f_t: X \to \overline{\Bbb R}$ be a family of functions with $t\in[0,\infty)$ of $\scr A$-measurable functions on $X$ such that $$f(x) = \lim_{t\to\infty}f_t(x),\quad \text{and} \quad |f_t(x)| \le g(x) $$for $t\in [0, \infty)$ hold at $\mu$-almost every $x$ in $X$. Then for each $n< \omega$, $f_n$ is integrable, $f$ is also integrable, and $$\int f\, d\mu = \lim_{t\to \infty}\int f_t\, d\mu. $$
**Cor (Differentiation under the Integral Sign):** Let $(X, {\scr A}, \mu)$ be a measure space, let $g:X \to [0,\infty]$ be an integrable function, let $I$ be an open interval of $\Bbb R$, and let $f: X \times I \to \Bbb R$ such that:
- for each $t\in I$ the function $x\mapsto f(x, t)$ is integrable,
- for each $x\in X$ the function $t\mapsto f(x, t)$ is differentiable on $I$, and
- the inequality $$\left|\frac{f(x, t)- f(x, t_0)}{t-t_0}\right|\le g(x)$$holds for all $t, t_0\in I$ and all $x\in X$ such that $t\neq t_0$. 
Then the function $F: I \to \Bbb R$ defined by $F(t) = \int f(x, t)\, \mu(dx)$ is differentiable and $$F'(t) = \int \frac{\partial f}{\partial t}\, \mu(dx) $$
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