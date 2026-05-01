---
tags:
  - MeasureTheory
  - FunctionalAnalysis
---
Subjects: [[Measure Theory]], [[Functional Analysis]]
Links: [[Scalar Integral on Measure Spaces]], [[Modes of Convergence using Measure]], [[Measure Spaces and Measurable Spaces]], [[Normed Vector Spaces]], [[ellp spaces]], [[Complete Metric Spaces]], [[Inner Products and Norms]], [[Useful Inequalities]], [[Topological Dual Vector Space]], [[Space of Continuous Compactly Supported Functions]]

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
**Minkowski's Inequalities:** Let $(X, {\scr A},\mu)$ be a measure space, and let $p$ satisfies $1\le p \le\infty$. If $f$ and $g$ belongs to ${\scr L}^p(X, {\scr A}, \mu)$ or ${\scr L}^\infty_b(X, {\scr A}, \mu, \Bbb F)$, then $f+g$ belongs to $f+g\in {\scr L}^p(X, {\scr A}, \mu)$ and $$\|f+g\|_p \le \|f\|_p + \|g\|_p,$$or $$\|f+g\|_{\infty, b}\le \|f\|_{\infty, b}+ \|g\|_{\infty, b}.$$
**Cor:** Let $(X, {\scr A},\mu)$ be a measure space, and let $p$ satisfy $1\le p\le \infty$. Then $f\in {\scr L}^p(X, {\scr A}, \mu)$ is a vector space, and $\|\cdot \|_p$ is a seminorm on $f\in {\scr L}^p(X, {\scr A}, \mu)$. 

**Cor:** Let $(X, {\scr A},\mu)$ be a measure space. Then $f\in {\scr L}^\infty_b(X, {\scr A}, \mu)$ is a vector space, and $\|\cdot \|_{\infty, b}$ is a seminorm on $f\in {\scr L}^\infty_b(X, {\scr A}, \mu)$. 

**Def:** Let $(X, {\scr A},\mu)$ be a measure space, and let ${\scr N}^p(X, {\scr A},\mu)$ be the subset of ${\scr L}^p(X, {\scr A},\mu)$ that consists of those functions $f\in {\scr L}^p(X, {\scr A},\mu)$ and satisfy $\|f\|_p = 0$. Thus if $1\le p<\infty$, then ${\scr N}^p(X, {\scr A},\mu)$ consists of the $\scr A$-measurable functions on $X$ that satisfy $$\int |f|^p \, d\mu = 0,$$and if $p =\infty$, then ${\scr N}^p(X, {\scr A},\mu)$ consists of the essentially bounded $\scr A$-measurable functions on $X$ that vanish almost everywhere. In the case where we consider the case $p =\infty$ and bounded, then ${\scr N}^\infty_b(X, {\scr A},\mu)$ is the set of bounded $\scr A$-measurable functions on $X$ that vanish almost everywhere. We see that ${\scr N}^\infty_b(X, {\scr A},\mu)$ for $p\in [1,\infty]$, ${\scr N}^p(X, {\scr A},\mu)$ are linear subspaces. 

The space $L^p(X, {\scr A},\mu )$ is defined to be the quotient of ${\scr L}^\infty_b(X, {\scr A},\mu)/{\scr N}^\infty_b(X, {\scr A},\mu)$. Similarly, the space $L^\infty_b(X, {\scr A},\mu)$ is defined to be the quotient of ${\scr L}^\infty_b(X, {\scr A},\mu)/{\scr N}^\infty_b(X, {\scr A},\mu)$. 

**Obs:** Let $(X, {\scr A},\mu)$ be a measure space, let $p$ satisfy $1\le p <\infty$, and let $f$ and $f_0, f_1, f_2,\dots$ belong to ${\scr L}^p(X, {\scr A},\mu)$. Then $(f_n)_{n<\omega}$ converges to $f$ in *$p$th mean*, or in *$L^p$-norm*, if $$\lim_{n\to\infty} \int|f_n-f|^p\, d\mu =0,$$or equivalently, if $\lim \|f_n-f\|_p = 0$ .

**Obs:** If we consider the measure space $(\Bbb N, \mathcal P(\Bbb N), \mu)$, with $\mu$ being the counting measure, then we get that $L^p(\Bbb N, \mathcal P(\Bbb N), \mu, \Bbb R) = {\scr L}^p(\Bbb N, \mathcal P(\Bbb N), \mu, \Bbb R) = \ell^p$.

**Prop:** Let $(X, {\scr A}, ¸\mu)$ be a measure space. Then $$\langle f, g\rangle := \int fg\, d\mu$$defines an inner product on $L^2(X, {\scr A}, \mu, \Bbb R)$. Similarly, $$\langle f, g\rangle := \int f\, \overline g\, d\mu$$defines an inner product on $L^2(X, {\scr A}, \mu, \Bbb C)$. 

**Prop:** Let $(X, {\scr A}, \mu)$ be a finite measure space, and let $f$ be an ${\scr A}$-measurable function on $X$. Then the $f\in {\scr L}^\infty(X, {\scr A}, \mu)$ iff
- $f$ belongs to ${\scr L}^p(X, {\scr A}, \mu)$ for each $1\le p<\infty$, and
- $\sup\{\|f|\|_p \mid 1\le p<\infty\}$ is finite.
Additionally, we know that $\lim\limits_{p\to\infty} \|f\|_p = \|f\|_\infty$. 

**Jensen's Inequality:** Let $(X, {\scr A}, \mu)$ be a probability space. Suppose $\varphi:\Bbb R\to\Bbb R$ is a convex. If $f\in{\scr L}^1(X. {\scr A},\mu,\Bbb R)$, then $$\varphi\left(\int f\, d\mu\right ) \le \int \varphi \circ f\, d\mu.$$
**Prop:** Let $(X, {\scr A},\mu)$ be a finite measurable space.
- If $1 \le s< r <\infty$, and  $f\in {\scr L}^r(X, {\scr A}, \mu)$, then $f\in {\scr L}^s(X, {\scr A}, \mu)$, and $\|f\|_s \le \mu(X)^{\frac{r-s}{sr}}\|f\|_r$. 
- If $1 \le r <\infty$, and $f\in {\scr L}^\infty(X, {\scr A}, \mu)$, then $f\in {\scr L}^\infty(X, {\scr A},\mu)$, and  $\|f\|_s \le \mu(X)^{\frac{1}{r}}\|f\|_\infty$

**Cor:** Let $(X, {\scr A},\mu)$ be a finite measurable space. If $1 \le s< r\le \infty$, and there there is a sequence $(f_n)_{n<\omega}$ in ${\scr L}^{r}(X, {\scr A}, \mu)$ that converges to $f$ in $r$th mean, then $(f_n)_{n<\omega}$ converges to $f$ is $s$th mean.

**Th:** Let $(X, {\scr A},\mu)$ be a measure space, and let $p\in [1,\infty]$. Then $L^p(X, {\scr A},\mu)$ is [[Complete Metric Spaces|complete]] under the norm $\|\cdot\|_p$. Additionally, $L^\infty_b(X, {\scr A}, \mu)$ is complete under the norm $\|\cdot \|_{\infty, b}$. 

**Cor:** Let $(X, {\scr A},\mu)$ be a measure space. Then $L^2(X, {\scr A},\mu)$ is a Hilbert space, with the inner product defined above.

**Def:** Let $(X, {\scr A},\mu)$ be a measure space. We will say that a function $f\in {\scr L}^p(X, {\scr A},\mu)$ *determines* the equivalence class $[f]$ in $L^p(X, {\scr A},\mu)$, or $L^\infty_b(X, {\scr A},\mu),$ to which it belongs. Likewise, if $S$ is a subset of ${\scr L}^p(X, {\scr A},\mu)$ and if $T$ is a subset of $L^p(X, {\scr A},\mu)$, then we will say that $S$ *determines* $T$ if $T$ consists of the equivalence classes of $L^p(X, {\scr A},\mu)$ determines by the elements of $S$. The definitions are identical when considering ${\scr L}^\infty_b(X, {\scr A},\mu)$ and $L^\infty_b(X, {\scr A},\mu)$.

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, and let $p\in [1,\infty]$. Then the simple functions in ${\scr L}^p(X, {\scr A},\mu)$ form a dense subspace of ${\scr L}^p(X, {\scr A},\mu)$ and so determine a dense subspace of $L^p(X, {\scr A},\mu)$. Additionally, Then the simple functions in ${\scr L}^\infty_b(X, {\scr A},\mu)$ form a dense subspace of ${\scr L}^\infty_b(X, {\scr A},\mu)$ and so determine a dense subspace of $L^\infty_b(X, {\scr A},\mu)$.

**Def:** We will use ${\scr L}^p([a,b])$ and $L^p([a,b])$ as abbreviations for ${\scr L}^p([a,b], \mathcal B([a,b]), \lambda)$ and $L^p([a,b], \mathcal B([a,b]), \lambda)$, where $\mathcal B([a,b])$ is the Borel $\sigma$-algebra of $[a,b]$ and $\lambda$ is the restriction of Lebesgue measure to $\mathcal B([a,b])$. Analogous, for ${\scr L}^\infty_b([a,b])$ ad $L^\infty_b([a,b])$.

**Def:** Let $[a,b]$ be a closed bounded interval. A function $f$ on $[a,b]$ is a *step function* if there are real numbers $a_0,\dots, a_n$ such that 
- $a = a_0 < a_1 <\dots< a_n = b$, and
- $f$ is constant on each interval $(a_{i-1}, a_i)$.

**Prop:** Suppose $[a,b]$ is a closed bounded interval and that $p$ satisfies $1\le p<\infty$. Then the subspace of $L^p([a,b])$ determined by the step functions on $[a,b]$ is dense in $L^p([a,b])$. 

**Prop:** Suppose $[a,b]$ is a closed bounded interval and that $p$ satisfies $1\le p<\infty$. Then the subspace of $L^p([a,b])$ determined by the [[Space of Continuous Functions|continuous functions]] on $[a,b]$ is dense in $L^p([a,b])$. 

**Def:** Let us call a function on $\Bbb R$ a *step function* if for each interval $[a,b]$ its restriction  to $[a,b]$ is a step function.

**Prop:** Suppose that $p$ satisfies $1\le p<\infty$. Then the subspace of $L^p(\Bbb R, {\cal B}(\Bbb R), \lambda)$ determined by the step functions on $\Bbb R$ with bounded support is dense in $L^p(\Bbb R, {\cal B}(\Bbb R), \lambda)$. 

**Prop:** Suppose that $p$ satisfies $1\le p<\infty$. Then the subspace of $L^p(\Bbb R, {\cal B}(\Bbb R), \lambda)$ determined by the continuos functions on $\Bbb R$ with bounded support is dense in $L^p(\Bbb R, {\cal B}(\Bbb R), \lambda)$. 

**Lemma:** Let $(X, {\scr A},\mu)$ be a finite measure space, and let ${\scr A}_0$ be an algebra of sets of $X$ such that ${\scr A} = \sigma({\scr A}_0)$. Then ${\scr A}_0$ is dense in $\scr A$, in the sense that for each $A \in \scr A$ and each positive number $\varepsilon$ there is a set $A_0 \in {\scr A}_0$ and satisfies $\mu(A \, \triangle\, A_0) <\varepsilon$.

**Lemma:** Let $(X, {\scr A},\mu)$ be a measure space. Suppose that ${\scr A}_0$ is an algebra of subsets of $X$ such that
- $\sigma({\scr A}_0) =\scr A$, and
- $X$ is the union of a sequence of sets that belong to ${\scr A}_0$ and have finite measure under $\mu.$
Then for each positive $\varepsilon$ and each set $A$ that belong to $\scr A$ and satisfies $\mu(A)<\infty$, there is a set $A_0$ that belongs to ${\scr A}_0$ and satisfies $\mu(A\,\triangle\, A_0)<\varepsilon$. 

**Prop:** Let $(X, {\scr A},\mu)$ be a measure space, and let $p$ satisfy $1\le p <\infty$. If $\mu$ is $\sigma$-finite and $\scr A$ is countably generated, the $L^p(X, {\scr A}, \mu)$ is separable.

**Cor:** If $1\le p<\infty$, then $L^p([a,b])$, $L^p(\Bbb R, {\cal B}(\Bbb R), \lambda)$ and $\ell^p$ are separable.

We see that $L^{\infty}([a,b])$ is not separable. 

When considering the dual spaces of $L^p(X, {\scr A}, \mu)$ for some measure space $(X, {\scr A}, \mu)$, we consider the topological dual rather than the algebraic dual, meaning that it is the space of all continuous functionals from $L^p(X, {\scr A}, \mu)$ to the base field.

**Prop:** Let $(X, {\scr A}, \mu)$ be a measure space, let $p$ satisfy $1 < p <\infty$, and $q$ be its harmonic conjugate. Then the map $T: {\scr L}^q(X, {\scr A}, \mu)\to (L^p(X, {\scr A}, \mu))^*$ defined as $$T_g(f) := \int fg\, d\mu.$$induces an isometry of $L^q(X, {\scr A}, \mu)$ into $(L^p(X, {\scr A}, \mu))^*$. In the special case for $p =1$ and $q =\infty$, then the map $T: {\scr L}^\infty_b(X, {\scr A}, \mu)\to (L^1(X, {\scr A}, \mu))^*$ and it is defined similarly.

**Th:** Let $(X, {\scr A}, \mu)$ be a measure space, let $p$ satisfy $1 < p <\infty$, and $q$ be its harmonic conjugate. Then the map $T: {\scr L}^q(X, {\scr A}, \mu)\to (L^p(X, {\scr A}, \mu))^*$ defined as $$T_g(f) := \int fg\, d\mu.$$induces an isometric isomorphism of $L^q(X, {\scr A}, \mu)$ into $(L^p(X, {\scr A}, \mu))^*$.

**Th:** Let $(X, {\scr A}, \mu)$ be a $\sigma$-finite measure space, then the induced map $T: L^\infty_b(X, {\scr A}, \mu)\to (L^1(X, {\scr A}, \mu))^*$ is an isometric isomorphism.

**Cor:** Let $(X, {\scr A}, \mu)$ be a measure space, let $p$ satisfy $1 < p <\infty$, and $q$ be its harmonic conjugate. Then $L^p(X, {\scr A},\mu)$ is a reflexive space with dual isometrically isomorphic to $L^q(X, {\scr A}, \mu)$.

**Obs:** Let $(X, {\scr A}, \mu)$ be a measure space. Then the formula $$T_{\langle g\rangle}(\langle f\rangle) := \int fg\, d\mu$$ defines an isometry $T$ of $L^1(X, {\scr A}, \mu)$ into $(L^\infty_b(X,{\scr A}, \mu))^*$. 

**Prop:** Let $(X, {\scr A}, \mu)$ be a finite measure space. The following conditions are equivalent.
- the map $T: L^1(X, {\scr A}, \mu)\to (L^\infty_b(X,{\scr A}, \mu))^*$ is surjective.
- $L^1(X, {\scr A}, \mu)$ is finite dimensional.
- $(L^\infty_b(X,{\scr A}, \mu))^*$ is finite dimensional.
- There is finite $\sigma$-algebra ${\scr A}_0$ on $X$ such that ${\scr A}_0\subseteq \scr A$ and such that each set in $\scr A$ differs from a set in ${\scr A}_0$ by a $\mu$-null set.

**Prop:** Let $X$ be a locally compact Hausdorff space, let $\scr A$ be a $\sigma$-algebra on $X$ that includes $\mathcal B(X)$, and let $\mu$ be a regular measure on $(X, {\scr A})$. Suppose that $1\le p <\infty$. Then $\mathcal C_c(X)$ is  dense subspace of $\mathscr L^p(X, {\scr A}, \mu, \Bbb F)$ and so determines a dense subspace of $L^p(X, {\scr A}, \mu, \Bbb F)$. 

**Th:** let $X$ be a locally compact Hausdorff space, $I$ be a positive linear functional on $\mathcal C_c(X)$. We defined an outer measure $\mu^*$ by $$\mu^*(U) := \sup\{I(f) \mid f\in \mathcal C_c(X) \land f \prec U\}, $$whenever $U$ is an open subset of $X$ and if $A\subseteq X$ $$\mu^*(A) := \inf\{\mu^*(U) \mid U\in \tau \land A\subseteq U\}.$$Let ${\scr M}_{\mu^*}$ be the $\sigma$-algebra of $\mu^*$-measurable sets. We know that $\mathcal B(X) \subseteq {\scr M}_{\mu^*}$, and that the restriction  $\mu_1$ of $\mu^*$ to ${\scr M}_{\mu^*}$ is a regular measure. The map $T$ given by $$T_{\langle g\rangle}(\langle f\rangle) := \int fg\, d\mu$$is an isometric isomorphism of $L^\infty(X, {\scr M}_{\mu^*}, \mu_1)$ onto $(L^1(X, {\scr M}_{\mu^*}, \mu_1))^*$. 

**Th:** $L^p(X, \mathscr M_{\mu^*}, \mu_1)$ and $L^p(X, \mathcal B(X),\mu)$ are isometrically isomorphic to one another, where $\mu, \mu_1,$ and $\mathscr M_{\mu^*}$ are as above. 
