---
tags:
  - MeasureTheory
  - FunctionalAnalysis
---
Subjects: [[Measure Theory]], [[Functional Analysis]]
Links: [[Scalar Integral on Measure Spaces]], [[Modes of Convergence using Measure]], [[Measure Spaces and Measurable Spaces]], [[Normed Vector Spaces]], [[ellp spaces]], [[Complete Metric Spaces]], [[Inner Products and Norms]]

In this note $\Bbb F$ denotes either $\Bbb R$ or $\Bbb C$. 

**Def:** Let $(X, {\scr A},\mu)$ be a measure space and let $p \in [1,\infty)$. Let ${\scr L}^p(X, {\scr A}, \mu, \Bbb R)$ the set of all $\scr A$-measurable function $f:X \to \Bbb R$ such that $|f|^p$ is integrable, and ${\scr L}^p(X, {\scr A}, \mu, \Bbb C)$ is the set of all ${\scr A}$-measurable function $f:X \to\Bbb C$ such that $|f|^p$ is integrable.

**Obs:** Note that if $a \in \Bbb F$ and $f\in {\scr L}^p(X, {\scr A}, \mu, \Bbb F)$, then $\alpha f\in {\scr L}^p(X, {\scr A}, \mu, \Bbb F)$. Furthermore, if $f$ and $g$ belong to ${\scr L}^p(X, {\scr A}, \mu, \Bbb F)$, then we can check that $f+g\in {\scr L}^p(X, {\scr A}, \mu, \Bbb F)$. This means that ${\scr L}^p(X, {\scr A}, \mu, \Bbb F)$ is a $\Bbb F$-vector space. 

**Def:** If $f$ is a measurable function on $X$, we define $$\|f\|_\infty := \inf \{a\ge 0 \mid \mu(\{x \mid |f(x)| >a\}) = 0\}, $$with the convention that $\inf \varnothing = \infty$. $\|f\|_\infty$ is called the *essential supremum* of $|f|$ and is sometimes written $$\|f\|_\infty = \operatorname{ess sup}_{x\in X} |f(x)|. $$If a function has an essential supremum it is called essentially bounded. Note that $f$ is essentially bounded iff there is a bounded measurable function $g$ such that $f = g$ a.e.

**Def:** We now define ${\scr L}^\infty(X, {\scr A}, \mu, \Bbb F)$ is the set of essentially bounded $\Bbb F$-valued $\scr A$-measurable functions. We can define another space ${\scr L}^\infty_b(X, {\scr A}, \mu, \Bbb F)$ which is the set of all  bounded $\Bbb F$-valued $\scr A$-measurable functions.

**Def:** Let us define, for each $p$, a seminorm $\|\cdot \|_p$ on ${\scr L}^p(X, {\scr A}, \mu)$. if $1\le p<\infty$, we define $\|\cdot \|_p$ by $$\|f\|_p := \left(\int |f|^p\, d\mu\right)^{1/p}. $$For the case where $p =\infty$, we use the essential supremum. 

**Def:** A subset $N$ of $X$ is *locally $\mu$-null*, or simply *locally null*, if for each set $A$ that belongs to $\scr A$ and satisfies $\mu(A) <\infty$ the set $A\cap N$ is $\mu$-null. A property of points of $X$ is said to hold *locally almost everywhere* if the set of points at which it fails to hold is locally null.

**Obs:** It is easy to check that 
- every $\mu$-null subset of $X$ is locally $\mu$-null,
- if $(X, {\scr A}, \mu)$ is $\sigma$-finite, then every locally $\mu$-null subset of $X$ is $\mu$-null, and
- the union of a sequence of locally $\mu$-null sets is locally $\mu$-null.

**Def:** We can define a seminorm on ${\scr L}^\infty_b(X, {\scr A}, \mu, \Bbb F)$, let $$\|f\|_{\infty, b} := \inf \{a\ge 0 \mid \{x \mid |f(x)| >a\} \text{ is locally null} \}.$$
**Obs:** Let $(X, {\scr A}, \mu)$ be a measure space. If $\mu$ is $\sigma$-finte, then ${\scr L}^\infty_b(X, {\scr A}, \mu, \Bbb F) = {\scr L}^\infty(X, {\scr A}, \mu, \Bbb F)$. 

**Young's Inequality:** Let $p$ satisfy $1< p< \infty$, and let $q$ such that $1/p + 1/q = 1$, and let $x, y\ge 0$. Then $$xy \le \frac{x^p}{p}+ \frac{y^q}{q}. $$
**Hölder's Inequality:** Let $(X, {\scr A},\mu)$ be a measure space, and let $p$ and $q$ satisfy $1\le p,q \le\infty$ and $1/p + 1/q = 1$. If $f\in {\scr L}^p(X, {\scr A}, \mu)$ and $g\in {\scr L}^q(X, {\scr A}, \mu)$, then $fg$ belongs to ${\scr L}^1(X, {\scr A}, \mu)$ and satisfies $$\|fg\|_1 \le \|f\|_p\|g\|_q. $$In the case that $f\in {\scr L}^1(X, {\scr A},\mu)$ and $g\in {\scr L}^\infty_b(X, {\scr A},\mu)$, then $fg\in {\scr L}^1(X, {\scr A},\mu)$ and    $$\|fg\|_1 \le \|f\|_1 \|g\|_{\infty, b}. $$
**Minkowski's Inequalities:** Let $(X, {\scr A},\mu)$ be a measure space, and let $p$ satisfies $1\le p \le\infty$. If $f$ and $g$ belongs to $f\in {\scr L}^p(X, {\scr A}, \mu)$ or ${\scr L}^\infty_b(X, {\scr A}, \mu, \Bbb F)$, then $f+g$ belongs to $f+g\in {\scr L}^p(X, {\scr A}, \mu)$ and $$\|f+g\|_p \le \|f\|_p + \|g\|_p,$$or $$\|f+g\|_{\infty, b}\le \|f\|_{\infty, b}+ \|g\|_{\infty, b}.$$
**Cor:** Let $(X, {\scr A},\mu)$ be a measure space, and let $p$ satisfy $1\le p\le \infty$. Then $f\in {\scr L}^p(X, {\scr A}, \mu)$ is a vector space, and $\|\cdot \|_p$ is a seminorm on $f\in {\scr L}^p(X, {\scr A}, \mu)$. 

**Cor:** Let $(X, {\scr A},\mu)$ be a measure space. Then $f\in {\scr L}^\infty_b(X, {\scr A}, \mu)$ is a vector space, and $\|\cdot \|_{\infty, b}$ is a seminorm on $f\in {\scr L}^\infty_b(X, {\scr A}, \mu)$. 

**Def:** Let $(X, {\scr A},\mu)$ be a measure space, and let ${\scr N}^p(X, {\scr A},\mu)$ be the subset of ${\scr L}^p(X, {\scr A},\mu)$ that consists of those functions $f\in {\scr L}^p(X, {\scr A},\mu)$ and satisfy $\|f\|_p = 0$. Thus if $1\le p<\infty$, then ${\scr N}^p(X, {\scr A},\mu)$ consists of the $\scr A$-measurable functions on $X$ that satisfy $$\int |f|^p \, d\mu = 0,$$and if $p =\infty$, then ${\scr N}^p(X, {\scr A},\mu)$ consists of the essentially bounded $\scr A$-measurable functions on $X$ that vanish almost everywhere. In the case where we consider the case $p =\infty$ and bounded, then ${\scr N}^\infty_b(X, {\scr A},\mu)$ is the set of bounded $\scr A$-measurable functions on $X$ that vanish almost everywhere. We see that ${\scr N}^\infty_b(X, {\scr A},\mu)$ for $p\in [1,\infty]$, ${\scr N}^p(X, {\scr A},\mu)$ are linear subspaces. 

The space $L^p(X, {\scr A},\mu )$ is defined to be the quotient of ${\scr L}^\infty_b(X, {\scr A},\mu)/{\scr N}^\infty_b(X, {\scr A},\mu)$. Similarly, the space $L^\infty_b(X, {\scr A},\mu)$ is defined to be the quotient of ${\scr L}^\infty_b(X, {\scr A},\mu)/{\scr N}^\infty_b(X, {\scr A},\mu)$. 

**Obs:** Let $(X, {\scr A},\mu)$ be a measure space, let $p$ satisfy $1\le p <\infty$, and let $f$ and $f_0, f_1, f_2,\dots$ belong to ${\scr L}^p(X, {\scr A},\mu)$. Then $(f_n)_{n<\omega}$ converges to $f$ in *$p$th mean*, or in *$L^p$-norm*, if $$\lim_{n\to\infty} \int|f_n-f|^p\, d\mu =0,$$or equivalently, if $\lim \|f_n-f\|_p = 0$ .

**Obs:** If we consider the measure space $(\Bbb N, \mathcal P(\Bbb N), \mu)$, with $\mu$ being the counting measure, then we get that $L^p(\Bbb, \mathcal P(\Bbb N), \mu, \Bbb R) = {\scr L}^p(\Bbb, \mathcal P(\Bbb N), \mu, \Bbb R) = \ell^p$. 

**Prop:** Let $(X, {\scr A}, ¸\mu)$ be a measure space. Then $$\langle f, g\rangle := \int fg\, d\mu$$defines an inner product on $L^2(X, {\scr A}, \mu, \Bbb R)$. Similarly, $$\langle f, g\rangle := \int f\overline g\, d\mu$$defines an inner product on $L^2(X, {\scr A}, \mu, \Bbb C)$. 

**Prop:** Let $(X, {\scr A}, \mu)$ be a finite measure space, and let $f$ be an ${\scr A}$-measurable function on $X$. Then the $f\in {\scr L}^\infty(X, {\scr A}, \mu)$ iff
- $f$ belongs to ${\scr L}^p(X, {\scr A}, \mu)$ for each $1\le p<\infty$, and
- $\sup\{\|f|\|_p \mid 1\le p<\infty\}$ is finite.
Additionally, we know that $\lim\limits_{p\to\infty} \|f\|_p = \|f\|_\infty$. 

**Jensen's Inequality:** Let $(X, {\scr A}, \mu)$ be a probability space. Suppose $\varphi:\Bbb R\to\Bbb R$ is a convex. If $f\in{\scr L}^1(X. {\scr A},\mu,\Bbb R)$, then $$\varphi\left(\int f\, d\mu\right ) \le \int \varphi \circ f\, d\mu.$$