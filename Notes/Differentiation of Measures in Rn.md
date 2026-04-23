---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Cubes in Rn]], [[Lebesgue Measure]], [[Measures]], [[Measure Spaces and Measurable Spaces]], [[Absolute Continuity of Measures]]

**Def:** Let $\scr C$ be the family consisting of those nondegenerate closed cubes in $\Bbb R^n$ whose edges are parallel to the coordinate axes. In other words, let $\scr C$ be the collection of all sets of the form  $$\prod_{i = 1}^n [a_i, b_i],$$where $[a_1, b_1], \dots [a_n, b_n]$ are closed subintervals of $\Bbb R$ that have a common nonzero length. For each cube $C\in \scr C$ let $e(C)$ be the length of th edges of $C$. 

Suppose $A\subseteq \Bbb R^n$. A *Vitali covering* of $A$ is a subfamily $\scr V$ of $\scr C$ such that for each $x\in A$ and $\delta> 0$ there is a cube $C$ that belongs to $\scr V$, contains $x$ and satisfies $e(C) <\delta$.

**Vitali Covering Theorem:** Let $A$ be an arbitrary nonempty subset of $\Bbb R^n$, and let $\scr V$ be a Vitali covering of $A$. Then there is a finite or infinite sequence $\{C_n\}_{n<\omega}$ of disjoint sets that belong to $\scr V$ and are such that $\bigcup_{n<\omega} C_n$ contains $\lambda$-almost every point in $A$. 

**Prop:** The union of arbitrary family of closed cubes with edges parallel to the coordinate axes is Lebesgue measurable.

**Def:** Let $\mu$ be a finite Borel measure on $\Bbb R^n$. Then $(\overline D\mu)(x)$ the *upper derivative of $\mu$ at $x$,* is defined by  $$(\overline D\mu)(x) := \limsup_{\varepsilon \to 0^+}\left\{\left. \frac{\mu(C)}{\lambda(C)}\; \right\rvert\; C\in {\scr C}, x\in C, e(C) <\varepsilon\right\}, $$and $(\underline D\mu)(x)$, the *lower derivative of $\mu$ at $x$*, is defined by $$(\underline D\mu)(x) := \liminf_{\varepsilon \to 0^+}\left\{\left. \frac{\mu(C)}{\lambda(C)}\; \right\rvert\; C\in {\scr C}, x\in C, e(C) <\varepsilon\right\}. $$The *upper derivative* and *lower derivative* of $\mu$ are the $[0, \infty]$-valued functions $\overline D\mu$ and $\underline D\mu$ whose values at $x$ are given above. The measure $\mu$ is *differentiable* at $x$ if $(\overline D\mu)(x)$ and $(\underline D\mu)(x)$ are finite and equal, and at each such $x$ the *derivative* $(D\mu)(x)$ of $\mu$ at $x$ is defined by  $$(D\mu)(x) := (\overline D\mu)(x) = (\underline D\mu)(x). $$The *derivative* of $\mu$ is the function $D\mu$ that is defined above at each $x$ at which $\mu$ is differentiable and is undefined elsewhere. 

**Lemma:** Let $\mu$ be a finite Borel measure on $\Bbb R^n$. Then $\overline D\mu$, $\underline D\mu$ and $D\mu$ are Borel measurable.

**Lemma:** Let $\mu$ be a finite Borel measure on $\Bbb R^n$, let $a> 0$, and let $A$ be a Borel subset of $\Bbb R^n$ such that $(\overline D\mu)(x) \ge a$ holds at each $x\in A$. Then $\mu(A) \ge a \lambda (A)$.

**Lemma:** Let $\mu$ be a finite Borel measure on $\Bbb R^n$ that is absolutely continuous with respect to Lebesgue measure, let $a> 0$, and let $A$ be a Borel subset of $\Bbb R^d$ such that $(\underline D\mu)(x) \le a$ holds at each $x\in A$. Then $\mu(A) \le a\lambda(A)$.

**Th:** Let $\mu$ be a finite Borel measure on $\Bbb R^n$. Then $\mu$ is differentiable at $\lambda$-almost everywhere point in $\Bbb R^d$, and the function defined by  $$x\mapsto \begin{cases} (D\mu)(x) & \text{if $\mu$ is differntiable at $x$}, \\ 0 &\text{otherwise} \end{cases}$$is a [[Absolute Continuity of Measures#^22e27b|Radon-Nikodym derivative]] of the absolutely continuous part of $\mu$. 

**Prop:** Let $f$ be a nonnegative function in ${\scr L}^1(\Bbb R^n, \mathcal B(\Bbb R^n), \lambda, \Bbb R)$, and let $\mu$ be a finite Borel measure on $\Bbb R^n$ given by $\mu(A) :=\int_A f\,d\lambda$. We see that $(D\mu)(x) = f(x)$ holds at each $x$ at which $f(x)$ is continuous. 

**Def:** Let $E$ be a Lebesgue measurable subset of $\Bbb R^n$. A point $x\in \Bbb R^d$ is a *point of density* of $E$ if for each $\varepsilon >0$ there is a $\delta> 0$ such that $$\left|\frac{\lambda(E \cap C)}{\lambda(C)}-1\right| <\varepsilon $$holds whenever $C$ is a cube in $\scr C$, contains $x$ and satisfies $e(C) <\delta$. Less formally, $x$ is a point of density of $E$ if $$\lim_{e(C) \to 0} \frac{\lambda(E \cap C)}{\lambda (C)} = 1,$$where the limits is taken as $C$ approaches $x$, through the collection of cubes in $\scr C$ that contain $x$. A point $x$ is a *point of dispersion* of $E$ if it is a point of density of $\Bbb R^n \setminus E$. Equivalently, $x$ is a point of dispersion of $E$ if $$\lim_{e(C) \to 0} \frac{\lambda(E \cap C)}{\lambda (C)} = 0$$ holds as the cube $C$ approaches $x$.

**Lebesgue Density Theorem:** Let $E$ be a Lebesgue measurable subset of $\Bbb R^n$. Then $\lambda$-almost every point in $E$ is a point of density of $E$ and $\lambda$-almost every point in $\Bbb R^n \setminus E$ is a point of dispersion of $E$.

# Differentiation of Functions

**Lemma:** Let $\mu$ be a finite Borel measure on $\Bbb R$, and let $F:\Bbb R\to\Bbb R$ be defined by $F(x) = \mu((-\infty, x])$. If $\mu$ is differentiable at $x_0$, then $F$ is differentiable at $x_0$, and $F'(x_0) = (D\mu)(x_0)$.

**Lemma:** Let $F:\Bbb R \to\Bbb R$ be nondecreasing. If $\varepsilon> 0$, then each bounded interval contains only a finite number of values of $x$ such that $F(x+) - F(x-) \ge \varepsilon$. 

**Lemma:** Let $F: \Bbb R\to \Bbb R$ be nondecreasing. Then
- the one-sided limits $F(x-)$ and $F(x+)$ exist at each $x\in \Bbb R$,
- the set of points at which $F$ fails to be continuous is at most countably infinite, and
- the function $G: \Bbb R\to \Bbb R$ defined by $G(x) = F(x+)$ is nondecreasing and right-continuous, and agrees with $F$ at each point at which $F$ is continuous.

**Th (Lebesgue):** Let $F:\Bbb R \to \Bbb R$ be nondecreasing. Then $F$ is differentiable $\lambda$-almost everywhere.

**Cor:** Let $F:\Bbb R\to \Bbb R$ be of finite variation. Then $F$ is differentiable $\lambda$-almost everywhere.

**Th (Fubini):** Let $F_n: \Bbb R\to \Bbb R$, $n<\omega$, be nondecreasing functions such that the series $\sum_{n<\omega} F_n(x)$ converges at each $x\in \Bbb R$. Define $F: \Bbb R\to \Bbb R$ by $F(x) := \sum_{n<\omega} F_n(x)$. Then $F' = \sum_{n<\omega} F_n'$ holds $\lambda$-almost everywhere. 

**Th (Lebesgue):** Suppose that $f \in {\scr L}^1(\Bbb R,\mathcal L(\Bbb R) ,\lambda, \Bbb R)$ and that $F: \Bbb R\to \Bbb R$ is defined by $F(x) = \int_{-\infty}^x f(t)\, d\lambda(t)$. Then $F$ is differentiable, and its derivative is given by $F'(x) = f(x)$, at $\lambda$-almost every $x\in \Bbb R$. 

**Prop:** Let $F: [a,b]\to \Bbb R$ be a continuous function. If $D\subseteq [a,b]$ is the set of points where $F$ is differentiable, then $D$ is Borel measurable, and $F':D \to \Bbb R$ is Borel measurable.

**Lemma:** Let $F:[a,b]\to \Bbb R$ be a Lebesgue measurable function that is differentiable almost everywhere. Suppose that $g: [a,b] \to \Bbb R$ satisfies $g(x) = F'(x)$ almost everywhere. Then $g$ is Lebesgue measurable, as is $F'$, whose domain is the set where $F$ is differentiable. 

**Def:** A function $F:\Bbb R\to\Bbb R$ is *absolutely continuous* if for each $\varepsilon >0$ there is a $\delta> 0$ such that $\sum_i |F(t_i)- F(s_i)| <\varepsilon$ holds whenever $\{(s_i, t_i)\}$ is finite sequence of disjoint open intervals for which $\sum_i(t_i-s_i)<\delta$. 

**Obs:** We see that every absolutely continuous function is continuous and, in fact, uniformly continuous. There are, however, functions that are uniformly continuous and of finite variation, but are not absolutely continuous. 

**Prop:** If $F: \Bbb R\to \Bbb R$ is absolutely continuous, then $F$ is of finite variation on each bounded interval.

**Cor:** A function $F: [a,b] \to \Bbb R$ is absolutely continuous iff it is differentiable $\lambda$-almost everywhere, $F'$ is integrable, and $F$ can be reconstructed from its derivative through the formula  $$F(x) = F(a) + \int_a^xF'(t)\, dt. $$
**Cor:** Let $F$ and $G$ be absolutely continuous functions on the interval $[a,b]$. Then $$F(b)G(b)-F(a)G(a) = \int_a^b F(t)G'(t) +\int_a^bF'(t) G(t)\, dt.  $$
**Prop:** Suppose that $f \in {\scr L}^1(\Bbb R,\mathcal L(\Bbb R) ,\lambda, \Bbb R)$. Then  $$\lim_{\lambda(I) \to 0} \frac1{\lambda(I)} \int_I |f(t) - f(x) |\, d\lambda(t) = 0 $$holds at $\lambda$-almost every $x\in \Bbb R$; here $I$ is a closed interval that contains $x$, and the limit is taken as the length of $I$ approaches zero. 

**Def:** Points $x$ at which $$\lim_{\lambda(I) \to 0} \frac1{\lambda(I)} \int_I |f(t) - f(x) |\, d\lambda(t) = 0 $$holds are called *Lebesgue points* of $f$, and the set of all Lebesgue points of $f$ is called the *Lebesgue set* of $f$.

**Lemma:** Let $f: [a,b] \to \overline{\Bbb R}$ be Lebesgue integrable. Then for each $\varepsilon> 0$ there is a lower semicontinuous $g: \Bbb R\to \overline{\Bbb R}$ that is integrable on $[a,b]$ and satisfies $f(t) \le g(t)$ holds at each $t\in [a,b]$, and $$\int_a^b g(t)\, d\lambda(t) <\int_a^b f(t)\, d\lambda(t) + \varepsilon.$$
**Lemma:** Let $H:[a,b] \to \Bbb R$ be continuous and let $C$ be a countable subset of $[a,b]$. Suppose that for each $x\in [a,b)\setminus C$ there is a $\delta_x>0$ such that $H(t) > H(x)$ holds at each $t$ in the interval $(x, x+\delta_x)$. Then $H$ is strictly increasing.

**Th:** Let $F: [a, b] \to \Bbb R$ be a continuous function such that
- $F$ is differentiable at all countably many points of the points in $[a,b]$, and
- $F'$ is integrable.
Then $F$ is absolutely continuous, and so $F(x) = F(a) +\int_a^x F'(t)\, d\lambda(t)$ holds at each $x\in [a,b]$. 

**Prop:** There is a strictly increasing continuous function $F:[0, 1] \to \Bbb R$ such that $F'(x) = 0$ holds at $\lambda$-almost every $x\in [0, 1]$. 