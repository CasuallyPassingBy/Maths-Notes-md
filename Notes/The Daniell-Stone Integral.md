---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Bourbaki's Version of Radon Measure]], [[Riesz Spaces]], [[Rings and Algebras of Sets]], [[Lebesgue Integral on Measure Spaces]], [[Measures]]

There is an alternate approach to integration theory, due to Daniel and Stone, in which one does not begin with a measure but rather with a positive linear functional on a vector space of functions. One extends this functional to a larger collection of functions, that proves analogues of the monotone and dominated convergence theorems for the extended functional, and finally shows that the extended functional can be viewed as integration with respect to a measure.

Let $X$ be a nonempty set. For (extended) real-valued functions $f$ and $g$ on $X$, the functions $f\vee g$ and $f\wedge g$ are defined by $$(f\vee g)(x) := \max\{f(x), g(x)\}, \quad \text{and} \quad (f\wedge g)(x) :=\min\{f(x), g(x)\}. $$
Let us note that the spaces $\Bbb R^X$ an $\overline{\Bbb R}^X$ are Riesz spaces. In this context, we will call a vector lattice on $X$ to be a Riesz subspace on $\Bbb R^X$ or $\overline{\Bbb R}^X$. A vector lattice $V$ satisfies *Stone's condition* if $$ f\land 1\in V \text{ whenever } f\in V.$$Just to clarify, $1$ in this context is the constant function $1$. Note that $1$ may or not be a member of $V$.

**Def:** A linear functional on a vector lattice $V$ is an *elementary integral* if it is positive, and satisfies that for any sequence of functions $(f_n)_{n<\omega}$ in $V$ that decreases pointwise to $0$, then $$\lim\limits_{n\to\infty}L(f_n) = 0.$$
**Lemma:** Suppose that $L$ is an elementary integral on the vector lattice $V$ and that $f$ and $f_0, f_1,\dots,$ are nonnegative functions on $V$.
- If the sequence $(f_n)_{n<\omega}$ increases to $f$, then $L(f) = \lim\limits_{n\to\infty}L(f_n)$.
- If $f = \sum_{n <\omega} f_n$, then $L(f) = \sum_{n<\omega}L(f_n)$.
- If $f \le \sum_{n<\omega}$, then $L(f) \le \sum_{n<\omega} L(f_n)$. 

**[[Sequence of Functions in Rn#^63872a|Dini's Theorem]]:** Suppose that $X$ is a compact Hausdorff space, like a closed and bounded interval of $\Bbb R$. Let $(f_n)_{n<\omega}$ be a sequence of nonnegative continuous functions on $X$ that decreases to $0$, in the sense that $(f_n(x))_{n<\omega}$ is an decreasing sequence that converges to $0$ for every $x\in X$. Then the sequence $(f_n)_{n<\omega}$ converges uniformly to $0$. 

**Examples:**
- Let $[a,b]$ be a closed bounded interval of $\Bbb R$ and let $\mathcal C([a, b])$. Then $\mathcal C([a,b])$ is a vector lattice that satisfies Stone's condition. Suppose we define a functional $L:\mathcal C([a, b]) \to \Bbb R$ by letting $L$ be the [[Riemann Integral in R|Riemann integral]]: $$L(f) := \int_a^b f.$$Dini's theorem implies that $L$ is an elementary integral.
- Let $X$ be a locally compact Hausdorff space, and let $\mathcal C_c(X)$ be the set of all continuous functions $f: X\to\Bbb R$ for which the [[Space of Continuous Compactly Supported Functions|support]] of $f$ is compact. Then $\mathcal C_c(X)$ is a vector lattice that satisfies Stone's condition. If $L$ is a positive linear functional on $\mathcal C_c(X)$, then $L$ is an elementary integral, again by Dini's Theorem.

**Def:** Let $X$ be a set, $V$ be a Riesz subspace of $\overline {\Bbb R}^X$, and $L$ and elementary integral, then $(X, V, L)$ is called a *Daniell space* or an *elementary integration space*. 

**Def:** Suppose that $V$ is a vector lattice of functions on a set $X$, that $V$ satisfies Stone's condition, and let $L$ is an elementary integral on $V$. Let $V^\bullet$ be the set of all $\overline{\Bbb R}$-valued functions on $X$ that are pointwise limits of increasing sequences of functions in $V$, and define $L^\bullet: V^\bullet \to \overline{\Bbb R}$ by $L^\bullet(f) := \lim\limits_{n\to\infty} L(f_n)$, where $(f_n)_{n<\omega}$ is an increasing sequence of functions in $V$ that converges pointwise to $f$. Likewise, let $V_\bullet$ be the set of all $\overline{\Bbb R}$-valued functions on $X$ that are pointwise limits of decreasing sequences of functions in $V$, and define $L_\bullet: V_\bullet \to \overline{\Bbb R}$ by $L_\bullet(f) := \lim\limits_{n\to\infty} L(f_n)$, where $(f_n)_{n<\omega}$ is a decreasing sequence of functions in $V$ that converges pointwise to $f$.

**Prop:** Both $L^\bullet$ and $L_\bullet$ are both well defined.

**Obs:** Let us note that $f\in V_\bullet$ iff there is a function $g\in V^\bullet$ such that $f=-g$ and that in this case $L_\bullet (f) = - L^\bullet(g)$. 

**Prop:** Suppose that $f, g\in V^\bullet$ and that $\alpha\ge 0$. Then the following statements are true. 
- $f \wedge g, f\vee g\in V^\bullet$,
- $f+g \in V^\bullet$ and $L^\bullet(f+g) = L^\bullet(f) + L^\bullet(g)$, and
- $\alpha f\in V^\bullet$ and $L(\alpha f) = \alpha L(f)$.
- If $f \le g$, then $L^\bullet(f) \le L^\bullet(g)$. 

**Prop:** If $g\in V_\bullet$ and $h\in V^\bullet$, then $h-g\in V^\bullet$ and $L^\bullet(h-g) = L^\bullet(h) - L_\bullet(g)$. If in addition, $g\le h$, then $L_\bullet(g) \le L^\bullet(h)$. 

**Prop:** If $(f_n)_{n<\omega}$ is a sequence of functions in $V^\bullet$ and if $(f_n)_{n<\omega}$ increases to $f$, then $f\in V^\bullet$ and $L^\bullet(f) = \lim\limits_{n\to\infty}L^\bullet(f_n)$.

**Def:** Suppose that $f: X\to \overline{\Bbb R}$ be an arbitrary function. Then we define $\overline L(f)$ and $\underline L(f)$ by $$\overline L(f) := \inf\{L^\bullet(h) \mid h\in V^\bullet \land f \le h\},\quad \text{and}\quad \underline L(f) := \sup\{L_\bullet(g) \mid g\in V_\bullet\land g\le f\}. $$
**Prop:** If $f:X\to\overline{\Bbb R}$ then $\underline L(f) \le\overline L(f)$. 

**Def:** A function $f:X\to\overline{\Bbb R}$ is $L$-*summable*, or simply summable, if $\underline L(f)$ and $\overline L(f)$ are finite and equal. We define $L_1$ on the collection of summable functions by letting $L_1(f)$ be the common finite value $\underline L(f)$ and $\overline L(f)$. 

**[[Riemann Integral in R#^9a7c62|Cauchy Criterion]] for $L$-summability:** Let $f: X\to \overline{\Bbb R}$ be an arbitrary function. Note 
that $f$ is $L$-summable iff $g\in V_\bullet$ and $h\in V^\bullet$ and $g\le f\le h$ and $L^\bullet(h-g)<\varepsilon$. 

**Prop:** If $f\in V$, then $f$ is summable and $L_1(f) = L(f)$. Thus $L_1$ is an extension of $L$.

**Prop:** If $f, g$ are $\Bbb R$-valued summable functions and $\alpha\in \Bbb R$, then
- $f+g$ is summable and $L_1(f+g) = L_1(f)+L_1(g)$. 
- $\alpha f$ is summable and $L_1(\alpha f) = \alpha L_1(f)$.

**Lemma:** Let $f, g: X\to[0,\infty]$ be $L$-summable functions, then $f+g$ is summable and $L_1(f+g) = L_1(f) + L_1(g)$.

**Prop:** If $f, g:X\to\overline{\Bbb R}$ are summable functions, then $f\vee g$ and $f\wedge g$ are summable. 

Let $f:X\to\overline{\Bbb R}$ we can define $f^+ := f\lor 0$, and $f^-:= -(f\wedge 0)$.

**Prop:** Let $f, g:X\to \overline{\Bbb R}$ be summable functions such that $f(x)+g(x)$ is defined for each $x\in X,$ then $f+g$ is summable and $L_1(f+g) = L_1(f)+L_1(g)$. 

**Prop:** A function $f:X\to\overline{\Bbb R}$ is summable iff $f^+$ and $f^-$ are summable and in that case $L_1(f) = L_1(f^+)-L_1(f^-)$. 

**Lemma:** If $f_1$ and $f_2$ are nonnegative summable functions such that $f_1\le f_2$, if $\varepsilon_1, \varepsilon > 0$, and if $g_1, g_2\in V^\bullet$ and satisfy $f_i \le g_i$ and $L^\bullet (g_i) < L_1(f) <\varepsilon_i$ for $i = 1, 2$, then $L^\bullet(g_1\vee g_2) < L_1(f_2)+ \varepsilon_1+\varepsilon_2$. 

**Monotone Convergence Theorem:** If $(f_n)_{n<\omega}$ is a sequence of $[0,\infty]$-valued summable functions $(f_n)_{n<\omega}$ increases pointwise to $f$, and if $\sup\{L_1(f_n) \mid n<\omega\}$ is finite, then $f$ is summable and  $$L_1(f) =\lim_{n\to\infty} L_1(f_n). $$

**Fatou's Lemma:** Let $(f_n)_{n<\omega}$ be a sequence of nonnegative $L$-summable functions on $X$. Then $$L_1\left(\liminf_{n\to\infty}f_n\right) \le \liminf_{n\to\infty} L_1(f_n) $$

**Dominated Convergence Theorem:** Suppose that $(f_n)_{n<\omega}$ is a sequence of $\Bbb R$-valued summable functions, that $f(x) = \lim f_n(x)$ holds for all $x\in X$, and that $g: X \to[0,\infty)$ summable function such that $|f_n(x)|\le g(x)$ holds for all $n<\omega$ and $x\in X$. Then $f$ is summable $$L_1(f) = \lim_{n\to\infty} L_1(f_n). $$
**Prop:** If $f:X\to\overline{\Bbb R}$ is a summable function, $f\wedge 1$ is summable.

**Prop:** If $f:X\to[0,\infty]$ is summable and $\alpha> 0$ and if $A := \{x\in X \mid f(x)>\alpha\}$, then $\chi_A$ is summable and $L_1(\alpha\chi_A) \le L_1(f)$. 

**Def:** A subset $A$ of $X$ is $L$-*negligible* or $L$-*null* if $\chi_A$ is summable and $L_1(\chi_A) = 0$. A property of points $x\in X$ is said to hold $L$-*almost everywhere* if the set of points at which it fails is $L$-negligible set.

**Cor:** A subset $A$ of $X$ is $L$-negligible iff for every $\varepsilon>0$ there is a function $f\in V^\bullet$ such that $\chi_A \le f$ and $L^\bullet(f)<\varepsilon$ 

**Cor:** Each subset of an $L$-negligible set is $L$-negligible.

**Cor:** The union of countable collection of $L$-negligible sets is $L$-negligible.

**Prop:** Suppose that $f$ and $g$ are $\overline{\Bbb R}$-valued functions that are equal $L$-almost everywhere. If one of these functions is summable, then both are summable and $L_1(f) = L_1(g)$.

**Prop:** If $f:X\to \overline{\Bbb R}$ is a summable function, then $\{x\in X \mid |f(x)| = \infty\}$ is $L$-negligible, or, $f$ is finite $L$-almost everywhere.

**Monotone Convergence Theorem:** If $(f_n)_{n<\omega}$ is a sequence of $[0,\infty]$-valued summable functions $(f_n)_{n<\omega}$ increases pointwise to $f$ $L$-almost everywhere, and if $\sup\{L_1(f_n) \mid n<\omega\}$ is finite, then $f$ is summable and  $$L_1(f) =\lim_{n\to\infty} L_1(f_n). $$
**Dominated Convergence Theorem V.2:** Suppose that $(f_n)_{n<\omega}$ is a sequence of $\Bbb R$-valued summable functions, that $f(x) = \lim f_n(x)$ holds $L$-almost everywhere, and that $g: X \to[0,\infty)$ summable function such that $|f_n(x)|\le g(x)$ holds for all $n<\omega$ and $L$-almost everywhere. Then $f$ is summable $$L_1(f) = \lim_{n\to\infty} L_1(f_n). $$
**Def:** A function $f:X\to\overline{\Bbb R}$ is called $L$*-measurable* or simply *measurable*, if $(g\vee f) \wedge h$ is summable for every choice of $g$ and $h$, where $g$ is a nonpositive summable functions and $h$ is a nonnegative summable function. A subset $A$ of $X$ is $L$-measurable if $\chi_A$ is a measurable function. Let $\scr M$ be the collection of all $L$-measurable subsets of $X$.

**Obs:** Every summable function is measurable.

**Lemma:** A function $f:X\to [0,\infty]$ is measurable iff for each nonnegative summable $h$ the function $f\wedge h$ is also summable.

**Cor:** A function $f:X\to \overline{\Bbb R}$ is measurable iff $f^+$ and $f^-$ are measurable. 

**Cor:** The constant function $1$ is measurable. 

**Prop:** Let $f, g: X\to \overline{\Bbb R}$ be functions that are $L$-almost everywhere. Then $f$ is measurable iff $g$ are measurable. 

**Prop:** If $f, g: X\to \overline{\Bbb R}$ are measurable functions, then $f\wedge g$ and $f\vee g$ are measurable.

**Prop:** If $(f_n)$ is a sequence of $\overline{\Bbb R}$-valued measurable functions and if $\overline f(x) =\limsup_{n\to\infty} f_n(x), \underline f(x) =\liminf_{n\to\infty} f_n(x)$ holds for almost every $x\in X$, then $\overline f$ and $\underline f$  are measurable. In particular, if $f(x) = \lim_{n\to\infty} f_n(x)$ holds for every $x\in X$, then $f$ is measurable.

**Prop:** If $f, g: X\to \overline{\Bbb R}$ are measurable functions and if $\alpha\in\Bbb R$, then $f+ g$ and $\alpha f$ are measurable.

## Back to Lebesgue Integration

**Prop:** the collection $\scr M$ of $L$-measurable sets is a $\sigma$-algebra.

**Prop:** Let $f:X\to\overline{\Bbb R}$ be an arbitrary function. We see then $f$ is $L$-measurable iff $f$ is $\scr M$-measurable.

**Def:** We define a function $\mu: {\scr M}\to [0,\infty]$ by $$\mu(A) := \begin{cases} L_1(\chi_A) & \chi_A \text{ is summable}\\ \infty & \chi_A \text{ is measurable but not summable.}\end{cases} $$
**Prop:** $\mu$ is a measure on $\scr M$.

Let us note that $(X, {\scr M}, \mu)$ is a complete measure space. 

**Th:** If $f:X\to\overline{\Bbb R}$ is an arbitrary function, then, $f$ is $L$-summable iff it is $\scr M$-measurable and $\mu$-integrable and that then  $$L_1(f) = \int f\, d\mu. $$
**Remark:** We see that the Daniell-Stone integral is essentially a generalisation of the [[Space of Continuous Compactly Supported Functions#Riesz Representation Theorem|Riesz-Markov-Kakutani Representation Theorem]]. While Riesz focuses on the functional on $\mathcal C_c(X)$ where $X$ is a locally compact Hausdorff space, Daniell-Stone workds on abstract sets $X$ and abstract vector lattices $V$, provided they satisfy the elementary integral condition.

**Cor:** Let $[a, b]$ be a closed bounded interval and let $L$ be the Riemann integral on $\mathcal C([a,b])$. Then the $L$-summable functions on $[a,b]$ are exactly the Lebesgue measurable functions on $[a,b]$ that are Lebesgue integrable, and that  $$L_1(f) = \int f\, d\lambda. $$
# Translating the Daniell-Stone Integral to Lebesgue Integration

Now suppose that $X$ is a set and that $V$ is  vector lattice on $X$. Let $\scr F$ be the collection of sets of the form $\{x\in X\mid f(x) > B\}$, where $f$ ranges over $V$ and $B$ ranges over the positive reals. Let $\scr R$ be the smallest $\sigma$-ring on $X$ that includes $\scr F$, and let $\scr A$ be the smallest $\sigma$-algebra on $X$ that makes each function in $V$ measurable. 

**Def:** Let $f$ and $g$ in $V$, let $[f, g)$ be the subset of $X \times \Bbb R$ given by $$[f,g) := \{(x, t) X \in \Bbb R\mid f(x)\le t<g(x)\} $$Note that if $f$ is nonnegative and in $V$, then $[0, f)$ can be interpreted as the region under the graph of $f$. Let $\scr I$ be the collection of all sets $[f, g)$ and let $\scr B$ be the smallest $\sigma$-algebra on $X\times \Bbb R$ that includes $\scr I$. We want need to construct a measure $\nu$ on $(X\times \Bbb R, \mathscr B)$ such that $\nu([f, g)) = L(f-g)$ holds whenever $f,g\in V$ and satisfy $f\le g$. 

**Lemma:** Suppose that $V$ is a vector lattice of functions, that $L$ is a positive linear functional on $V$, and that $\scr I$ is he collection of all sets $[f, g)$, for $f, g\in V$.
- If $I \in \scr I$, then there exists functions $f$ and $g$ in $V$ such that $f\le g$ and $I = [f, g)$.
- If the member $I\in \scr I$ can be written in the form $[f_1, g_2)$ and in the form $[f_2, g_2)$, where $f_1\le g_1$ and $f_2\le g_2$, then $g_1-f_1 = g_2-f_2$, and so $L(g_1-f_1) = L(g_2-f_2)$.
- If $I_1, I_2\in \scr I$, then $I_1\cap I_2\in \scr I$.
- If $I_1, I_2\in \scr I$, then there are disjoint $I'$ and $I''$ in $\scr I$ such that $I_1\setminus I_2 = I'\cup I''$ and hence such that $I_1 = (I_1\cap I_2) \cup I'\cup I''$. 

We can define $L_{\scr I}: {\scr I}\to \Bbb R$ by $$L_{\scr I} (I) = L(g-f) $$where $f, g\in V$ such that $f\le g$ and $I = [f, g)$.

**Lemma:** Suppose that $I\in \scr I$ and $\{I_n\}_{n<\omega}\subseteq\scr I$.
- If the sets $\{I_n\}_{n<\omega}$ is a disjoint collection, and if $I = \bigcup_{n<\omega} I_n$ then $$L_{\scr I}(I) = \sum_{n<\omega} L_{\scr I}(I_n).$$
- If $I \subseteq \bigcup_{n<\omega} I_n$, then $$L_{\scr I}(I) \le \sum_{n<\omega} L_{\scr I}(I_n).$$
We define a function $\nu^*$ on the subsets of $X\times \Bbb R$ by letting $\nu^*(A)$ be the infimum of the set of the sums of the form $\sum_{n<\omega} L_{\scr I}(I_n)$, where $\{I_n\}_{n<\omega}$ is a sequence in $\scr I$ such that $A\subseteq \bigcup_{n<\omega} I_n.$ Of course, $\nu^*(A) = \infty$ if there is no sequence $\{I_n\}_{n<\omega}$ such that $A\subseteq \bigcup_{n<\omega}I_n$. 

**Lemma:** Let $\nu^*$ be as defined above. Then
- $\nu^*$ is an [[Outer Measures|outer measure]] on $X\times \Bbb R$,
- every set in $\scr I$ is $\nu^*$-measurable, and
- if $I\in \scr I$, then $\nu^* (I) = L_{\scr I}(I)$. 

We define $\mu(A) := \nu(A \times [0, 1))$ when $A\in \scr R$ and $\mu(A) =\infty$ when $A\in \scr A\setminus R$. 

**Th:** Let $X$ be a set, let $V$ be a vector lattice on $X$ that satisfies Stone's condition, let $L$ be an elementary integral on $V$, and let $\scr R$ and $\scr A$ be as defined above. Then there is a measure $\mu$ on $(X, {\scr A})$ such that $L(f) = \int f\, d\mu$ holds for each $f\in V$. The restriction of this measure to $\scr R$ is unique, in the sense that if $\mu_1$ and $\mu_2$ are measures on $(X, {\scr A})$ such that $$\int f\,d\mu_1 = L(f) = \int f\, d\mu_2$$ holds for all $f\in V$, then $\mu_1(A) = \mu_2(A)$ holds for all $A\in \scr R$. 