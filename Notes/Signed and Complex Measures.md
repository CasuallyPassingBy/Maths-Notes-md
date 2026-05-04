---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Measure Spaces and Measurable Spaces]], [[Rings and Algebras of Sets]], [[Lebesgue Integral on Measure Spaces]]

**Def:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a function on $\scr A$ with values in $\overline{ \Bbb R}$. The function $\mu$ is *finitely additive* if the additive$$\mu\left(\bigcup_{i = 1}^nA_i\right) = \sum_{i = 1}^n \mu(A_i) $$holds for each finite sequence $\{A_i\mid 1\le i \le n\}$ of disjoint sets in $\scr A$ is *countably additive* if the identity $$\mu\left(\bigcup_{i = 0}^\infty A_i\right) = \sum_{i = 0}^\infty \mu(A_i)$$holds for each infinite sequence $\{A_n\}_{n<\omega}$ of disjoint sets in $\scr A$. If $\mu$ is countably additive and satisfies $\mu(\varnothing) = 0$, the it is a *signed measure*. A signed measure is *finite* if neither $-\infty$ nor $\infty$ occurs among its values.

**Obs:** Suppose $\mu$ is a signed measure on the measurable space $(X, {\scr A})$. Then for each $A\in \scr A$ the sum $\mu(A) + \mu(X\setminus A)$ must be defined and must be equal to $\mu(X)$. Hence if there is a set $A\in\scr A$ for which $\mu(A) = \pm\infty$, then $\mu(X) = \pm\infty$. Consequently, a signed measure can attain at most one of the values $\infty$ and $-\infty$. We see that if $B\in \scr A$ for which $\mu(B)$ is finite, then $\mu(A)$ is finite for each $\scr A$-measurable $A\subseteq B$.

**Lemma:** Let $(X, \scr A)$ be a measurable space, and let $\mu$ be a signed measure on $(X, {\scr A})$. If $\{A_n\}_{n<\omega}$ is an increasing sequence of sets in $\scr A$, then $$\mu\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty}\mu(A_n), $$
and if $\{A_n\}_{n<\omega}$ is a decreasing sequence of sets in $\scr A$ such that $\mu(A_n)$ is finite for some $n<\omega$, then $$\mu\left(\bigcap_{n<\omega} A_n\right) = \lim_{n\to \infty}\mu( A_n). $$
**Lemma:** Suppose that $(X, \scr A)$ is a measurable space and that $\mu$ is an extended real-valued function on $\scr A$ that is finitely additive and satisfies $\mu(\varnothing)= 0$. If $\mu\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty}\mu(A_n)$ holds for each increasing $\{A_n\}_{n<\omega}$ of sets in $\scr A$ or if $\lim\mu(A_n) = 0$ holds for each decreasing $\{A_n\}_{n<\omega}$ of sets in $\scr A$ for which $\bigcap_{n<\omega} A_n = \varnothing$, then $\mu$ is a signed measure.

**Def:** Let $\mu$ be a signed measure on the measurable space $(X, \scr A)$. A subset $A$ of $X$ is a *positive set* for $\mu$ if $A\in \scr A$ and each $\scr A$-measurable $E\subseteq A$ satisfies $\mu(E) \ge 0$. Likewise $A$ is a *negative set* for $\mu$ if $A\in \scr A$ and each $\scr A$-measurable $E\subseteq A$ satisfies $\mu(E) \le 0$.

**Prop:** Let $\mu$ be a signed measure on the measurable space $(X, {\scr A})$, and let $A\in \scr A$ such that $-\infty< \mu(A)< 0$. Then there is a negative set $B$ that is included in $A$ and satisfies $$\mu(B) \le\mu(A). $$
**Hahn Decomposition Theorem:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a signed measure on $(X, {\scr A})$. Then there are disjoint subsets $P$ and $N$ of $X$ such that $P$ is a positive set for $\mu$ and $N$ is a negative set for $\mu$, and $X = P \cup N$. 

A *Hahn decomposition* of a signed measure $\mu$ is a pair $(P, N)$ of disjoint subsets of $X$ such that $P$ is a positive set for $\mu$, $N$ is a negative set for $\mu$, and $X = P \cup N$. 

**Obs:** If $\mu$ is an arbitrary signed measure on a measurable space $(X, {\scr A})$ and if $(P_1, N_1)$ and $(P_2, N_2)$ are Hahn decomposition of $\mu$, then $P_1\cap N_2$ is both positive set and negative set for $\mu$, and so each $\scr A$-measurable subset $P_1\cap N_2$ has measure zero under $\mu$. Likewise, each $\scr A$-measurable subset of $P_2\cap N_1$ has measure zero under $\mu$. Thus the Hahn decomposition of $\mu$ is essentially unique.

**Jordan Decomposition Theorem:** For every signed measure is the difference of two positive measures, at least one of which is finite. In addition, if $(P, N)$ is a Hahn decomposition, then $\mu =\mu^+-\mu^-$ where $$\mu^+(A) := \mu(A \cap P), \qquad \text{and} \qquad \mu^-(A) := \mu(A\cap N) $$for every $A\in \scr A$.

**Obs:** Let $(P, N)$ be a Hahn decomposiition of the signed measure $\mu$, let $\mu^+$ and $\mu^-$ be the measures constructed from $(P, N)$, and suppose $A\in \scr A$. Then each $\scr A$-measurable subset $B$ of $A$ satisfies  $$\mu(B) = \mu^+(B) - \mu^-(B) \le \mu^+(B) \le\mu^+(A).$$Since in addition $\mu^+(A) := \mu(A \cap P)$, we see that $$\mu^+(A) = \sup\{\mu(B) \mid B\in {\scr A}\cap \mathcal P(A)\}. $$Likewise the measure $\mu ^-$ satisfies $$\mu^-(A) = \sup\{-\mu(B) \mid B \in {\scr A}\cap \mathcal P(A)\}. $$Thus $\mu^+$ and $\mu^-$ do not depende on the particular Hahn decomposition in their construction. The measure $\mu^+$ and $\mu^-$ are called the *positive part* and the *negative part* of $\mu$, and the representation $\mu = \mu^+-\mu^-$ is called the *Jordan decomposition* of $\mu$.

**Def:** The *variation* of the signed measure $\mu$ is the positive measure $|\mu|$ defined by $|\mu| = \mu^++\mu^-$. We see that $$|\mu(A)| \le |\mu| (A)$$holds for each $A\in \scr A$. The *total variation* $\|\mu\|$ of the signed measure $\mu$ is defined by $\|\mu\| := |\mu|(X)$. 

**Prop:** Let $\mu$ be a signed measure on $(X, {\scr A})$, and let $\nu_1$ and $\nu_2$ be positive measures on $(X, {\scr A})$ such that $\mu =\nu_1-\nu_2$. We see that $\nu_1(A) \ge \mu^+(A)$ and $\nu_2(A) \ge \mu^-(A)$ hold for each $A\in \scr A$.

**Def:** Let $\mu_1$ and $\mu_2$ be finite signed measures on the measurable space $(X, {\scr A})$. Define signed measures $\mu_1 \vee \mu_2$ and $\mu_1 \wedge\mu_2$ on $(X, {\scr A})$ by $\mu_1 \vee \mu_2 := \mu_1 + (\mu_2 -\mu_1)^+$, and $\mu_1 \wedge \mu_2 := \mu_1 - (\mu_1-\mu_2)^+$. 

**Prop:**
- Let $\mu_1$ and $\mu_2$ be finite signed measures on the measurable space $(X, {\scr A})$. We see that $\mu_1 \vee \mu_2$ is the smallest of those signed measures $\nu$ that satisfy $\nu(A) \ge \mu_1(A)$ and $\nu(A) \ge \mu_2(A)$ for all $A\in \scr A$. 
- Let $\mu_1$ and $\mu_2$ be finite signed measures on the measurable space $(X, {\scr A})$. We see that $\mu_1 \vee \mu_2$ is the largest of those signed measures $\nu$ that satisfy $\nu(A) \le \mu_1(A)$ and $\nu(A) \le \mu_2(A)$ for all $A\in \scr A$. 

**Def:** Let $(X, {\scr A})$ be a measurable space. A *complex measure* on $(X, {\scr A})$ is a function $\mu$ from $\scr A$ to $\Bbb C$ that satisfies $\mu(\varnothing) = 0$ and is *countably additive*. Note that by definition a complex measure has only complex values and so has no infinite values.

**Obs:** Each complex measure on $(X, {\scr A})$ can of course be written in the form $\mu = \mu' + i\mu'',$ where $\mu'$ and $\mu''$ are finite signed measures on $(X, {\scr A})$. Hence the Jordan decomposition theorem implies that each complex measure $\mu$ can be written in the form  $$\mu = (\mu_1-\mu_2) + i(\mu_3-\mu_4),$$where $\mu_1,\mu_2, \mu_3$ and $\mu_4$ are finite positive measures on $(X, {\scr A})$. Such a representation is called the *Jordan decomposition*o of $\mu$ if $\mu' = \mu_1-\mu_2$ and $\mu'' = \mu_3-\mu_4$ are the Jordan decomposition of the real and imaginary parts of $\mu$.

**Lemma:** Let $(X, \scr A)$ be a measurable space, and let $\mu$ be a complex measure on $(X, {\scr A})$. If $\{A_n\}_{n<\omega}$ is an increasing sequence of sets in $\scr A$, then $$\mu\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty}\mu(A_n), $$
and if $\{A_n\}_{n<\omega}$ is a decreasing sequence of sets in $\scr A$ such that $\mu(A_n)$ is finite for some $n<\omega$, then $$\mu\left(\bigcap_{n<\omega} A_n\right) = \lim_{n\to \infty}\mu(A_n). $$
**Lemma:** Suppose that $(X, \scr A)$ is a measurable space and that $\mu$ is an complex function on $\scr A$ that is finitely additive and satisfies $\mu(\varnothing)= 0$. If $\mu\left(\bigcup_{n<\omega} A_n\right) = \lim_{n\to\infty}\mu(A_n)$ holds for each increasing $\{A_n\}_{n<\omega}$ of sets in $\scr A$ or if $\mu\left(\bigcap_{n<\omega} A_n\right) = 0$ holds for each decreasing $\{A_n\}_{n<\omega}$ of sets in $\scr A$ for which $\bigcap_{n<\omega} A_n = \varnothing$, then $\mu$ is a complex measure.

**Def:** We turn to the *variation* $|\mu|$ of the complex measure $\mu$. For each $A\in \scr A$ let $$|\mu|(A) := \sup \left\{\left. \sum_{j=1}^n |\mu(A_j)|\;\right\rvert\; \{A_j\}_{j=1}^n \subseteq \mathscr{A} \text{ is a partition of } A \right\}$$
**Prop:** If $\mu$ is a finite signed measure, then $\mu$ is both a signed measure and a complex measure. Then we see that both definitions of $|\mu|$ are equivalent.

**Prop:** Let $(X, {\scr A})$ be a measurable space, and let $\mu$ be a complex measure on $(X, {\scr A})$. Then the variation $|\mu|$ of $\mu$ is a finite measure on $(X, {\scr A})$. 

**Prop:** Let $\mu$ be a signed or complex measure on $(X, {\scr A})$, and let $\nu$ be a positive measure on $(X, {\scr A})$ such that $|\mu(A)|\le\nu(A)$ for each $A\in \scr A$. Then $|\mu|(A) \le \nu(A)$ holds for each $A\in \scr A$.

**Cor:** Let $\mu$ be a signed or complex measure on $(X, {\scr A})$, and let $A\in \scr A$. If $|\mu|(A) = 0$ holds iff each $\scr A$-measurable subset $B$ of $A$ satisfies $\mu(B) = 0$.

**Def:** The total variation $\|\mu\|$ of the complex measure $\mu$ is defined by $\|\mu\|:= |\mu|(X)$.

**Def:** Suppose that $(X, {\scr A})$ is a measurable space. Let $M(X, {\scr A},\Bbb R)$ be the collection of al finite signed measures on $(X, {\scr A})$, and let $M(X, {\scr A}, \Bbb C)$ be the collection of all complex measures on $(X, {\scr A})$. We see that the total variation $\|\cdot\|$ is a norm in this spaces.

**Prop:** Let $\mu$ and $\mu_0, \mu_1, \mu_2, \dots$ be finite signed or complex measures on $(X, {\scr A})$. Then $\lim_{n\to\infty} \|\mu_n -\mu\| = 0$ holds iff $\mu_n(A)$ converges to $\mu(A)$ uniformly in $A$ as $n$ approaches to infinity.

**Th:** Let $(X,{\scr A})$ be a measurable space. Then the spaces $M(X, {\scr A},\Bbb R)$ and $M(X, {\scr A},\Bbb C)$ are [[Complete Metric Spaces|complete]] under the total variation norm, meaning that are Banach spaces over their respective field.

**Def:** Suppose $(X, {\scr A})$ is a measurable space. We will denote by $B(X, {\scr A}, \Bbb R)$ the vector space of bounded real-valued ${\scr A}$-measurable functions on $X$ and by $B(X, {\scr A}, \Bbb R)$ the vector space of bounded complex-valued $\scr A$-measurable function on $X$. If $\mu$ is a finite signed measure on $(X, {\scr A})$, if $\mu = \mu^+-\mu^-$ is the Jordan decomposition of $\mu$, and if $f$ belongs to $B(X, {\scr A},\Bbb R)$, then the integral of $f$ with respect to $\mu$ is defined by $$\int f\, d\mu := \int f\, d\mu^+ -\int f\,d\mu^-. $$
We see that $f\mapsto \int f\, d\mu$ defines a linear function on $B(X, {\scr A},\Bbb R)$.

Similarly, if $\mu$ is a complex measure on $(X, {\scr A})$, then we can use the Jordan decomposition of $\mu$ to define the integral to $\mu$ of a function in $B(X, {\scr A},\Bbb C)$. The expressions $f\mapsto \int f\,d\mu$ and $\mu \mapsto \int f\, d\mu$ define linear functionals on $B(X, {\scr A},\Bbb C)$ and on $M(X, {\scr A},\Bbb C)$, respectively.

If we define norms on $B(X, {\scr A},\Bbb R)$ and $B(X, {\scr A},\Bbb C)$ by $$\|f\|_\infty = \sup \{|f(x)|\mid x\in X\}. $$If $\mu$ is a finite signed or complex measure on $(X, {\scr A})$ and if $f\in B(X, {\scr A}, \Bbb F)$, then $$\left|\int f\, d\mu\right|\le \int |f|\, d|\mu| \le \|f\|_\infty \|\mu\|,$$where $\Bbb F$ is $\Bbb R$ or $\Bbb C$. Meaning that the functionals defined above are continuous.

**Prop:** If $\mu$ is a finite signed or complex measure on $(X, {\scr A})$ and if $f\in B(X, {\scr A}, \Bbb F)$, then the linear functionals
- $g\in B(X, {\scr A}, \Bbb F) \mapsto \int g\,d\mu$, and
- $\nu \in M(X, {\scr A}, \Bbb F)\mapsto \int f\, d\nu$,
are linear functionals

**Prop:** We see that the spaces $B(X, {\scr A},\Bbb R)$ and $B(X, {\scr A},\Bbb C)$ are complete with the norm $\|\cdot \|_\infty$.

**Cor:** Let $\mu$ be a finite signed or complex measure on $(X, {\scr A})$, and $(f_n)_{n<\omega}$ be a uniformly bounded sequence of real or complex-valued$ $\scr A$-measurable functions on $X$. If $f(x) = \lim\limits_{n\to\infty} f_n(x)$ holds at each $x\in X$, then $$\int f\, d\mu = \lim_{n\to\infty}\int f_n\, d\mu. $$