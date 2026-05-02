---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Bourbaki's Version of Radon Measure]], [[Riesz Spaces]], [[Rings and Algebras of Sets]]

There is an alternate approach to integration theory, due to Daniel and Stone, in which one does not begin with a measure but rather with a positive linear functional on a vector space of functions. One extends this functional to a larger collection of functions, that proves analogues of the monotone and dominated convergence theorems for the extended functional, and finally shows that the extended functional can be viewed as integration with respect to a measure.

Let $X$ be a nonempty set. For (extended) real-valued functions $f$ and $g$ on $X$, the functions $f\vee g$ and $f\wedge g$ are defined by $$(f\vee g)(x) := \max\{f(x), g(x)\}, \quad \text{and} \quad (f\vee g)(x) :=\min\{f(x), g(x)\}. $$
Let us note that the spaces $\Bbb R^X$ an $\overline{\Bbb R}^X$ are Riesz spaces. In this context, we will call a vector lattice on $X$ to be a Riesz subspace on $\Bbb R^X$ or $\overline{\Bbb R}^X$. A vector lattice $V$ satisfies *Stone's condition* if $$ f\land 1\in V \text{ whenever } f\in V.$$Just to clarify, $1$ in this context is the constant function $1$. Note that $1$ may or not be a member of $V$.

**Def:** A linear functional on a vector lattice $V$ is an *elementary integral* if it is positive, and satisfies that for any sequence of functions $(f_n)_{n<\omega}$ in $V$ that decreases pointwise to $0$, then $$\lim\limits_{n\to\infty}L(f_n) = 0.$$
**Lemma:** Suppose that $L$ is an elementary integral on the vector lattice $V$ and that $f$ and $f_0, f_1,\dots,$ are nonnegative functions on $V$.
- If the sequence $(f_n)_{n<\omega}$ increases to $f$, then $L(f) = \lim\limits_{n\to\infty}L(f_n)$.
- If $f = \sum_{n <\omega} f_n$, then $L(f) = \sum_{n<\omega}L(f_n)$.
- If $f \le \sum_{n<\omega}$, then $L(f) \le \sum_{n<\omega} L(f_n)$. 

**Dini's Theorem:** Suppose that $X$ is a compact Hausdorff space, like a closed and bounded interval of $\Bbb R$. Let $(f_n)_{n<\omega}$ be a sequence of nonnegative continuous functions on $X$ that decreases to $0$, in the sense that $(f_n(x))_{n<\omega}$ is an decreasing sequence that converges to $0$ for every $x\in X$. Then the sequence $(f_n)_{n<\omega}$ converges uniformly to $0$. 

**Examples:**
- Let $[a,b]$ be a closed bounded interval of $\Bbb R$ and let $\mathcal C([a, b])$. Then $\mathcal C([a,b])$ is a vector lattice that satisfies Stone's condition. Suppose we define a functional $L:\mathcal C([a, b]) \to \Bbb R$ by letting $L$ be the Riemann integral: $$L(f) := \int_a^b f.$$Dini's theorem implies that $L$ is an elementary integral.
- Let $X$ be a locally compact Hausdorff space, and let $\mathcal C_c(X)$ be the set of all continuous functions $f: X\to\Bbb R$ for which the support of $f$ is compact. Then $\mathcal C_c(X)$ is a vector lattice that satisfies Stone's condition. If $L$ is a positive linear functional on $\mathcal C_c(X)$, then $L$ is an elementary integral, again by Dini's Theorem.

Now suppose that $X$ is a set and that $V$ is  vector lattice on $X$. Let $\scr F$ be the collection of sets of the form $\{x\in X\mid f(x) > B\}$, where $f$ ranges over $V$ and $B$ ranges over the positive reals. Let $\scr R$ be the smallest $\sigma$-ring on $X$ that includes $\scr F$, and let $\scr A$ be the smallest $\sigma$-algebra on $X$ that makes each function in $V$ measurable. 

**Lemma:** Suppose that $V$ is a vector lattice of functions, that $L$ is a positive linear functional on $V$, a

**Th:** Let $X$ be a set, let $V$ be a vector lattice on $X$ that satisfies Stone's condition, let $L$ be an elementary integral on $V$, and let $\scr R$ and $\scr A$ be as defined above. Then there is a measure $\mu$ on $(X, {\scr A})$ such that $L(f) = \int f\, d\mu$ holds for each $f\in V$. The restriction of this measure to $\scr R$ is unique, in the sense that if $\mu_1$ and $\mu_2$ are measures on $(X, {\scr A})$ such that $\int f\,d\mu_1 = L(f) = \int f\, d\mu_2$ holds for all $f\in V$, then $\mu_1(A) = \mu_2(A)$ holds for all $A\in \scr R$. 