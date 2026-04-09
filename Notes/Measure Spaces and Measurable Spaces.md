---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Rings and Algebras of Sets]], [[Lebesgue Measure]], [[Borel Sets]], [[Rings and Algebras of Sets]], [[Measures]]

**Def:** A *measurable space* is a set and a $\sigma$-ring $\cal S$ of subsets of $X$ with the property that $\bigcup \cal S$. We shall write $(X, \mathcal S)$ for a measurable space when the $\sigma$-ring $\cal S$ is not clear. It is customary to call a $E\subseteq X$ *measurable* iff $E \in \cal S$. 

**Def:** A *measure space* is a measurable space $(X, \mathcal S)$ and a measure $\mu$ on $\cal S$; just as for measurable spaces we shall ordinarily allow ourselves to confuse a measure space whose underlying set is $X$ with the set $X$. On the occasions when it is desirable to call attention to the particular $\sigma$-ring and measure under consideration, we shall write $(X, \mathcal S, \mu)$ for $X$. The measure space $X$ is called (totally) finite, $\sigma$-finite, or complete, according as the measure $\mu$ is (totally) finite, $\sigma$-finite, or complete.

We continue with the notation that $\mu^*$ for the outer measure and $\mu_*$ for the inner measure.

We have common things to do:
- If $(X, \mathcal S, \mu)$ is a measure space and $X_0$ is a measurable space, we can induce a measure space to it. The $\sigma$-ring is $X_0 \cap \cal S$, and the measure is $\mu_0(E) = \mu(E)$. 
- Conversely, if $X_0 \subseteq X$ and $(X_0, \mathcal S_0, \mu_0)$, the $X$ may be made into a measure space $(X, \mathcal S, \mu)$, where $\mathcal S := \{E \subseteq X \mid E \cap X_0 \in \mathcal S_0\}$ and for $\mu(E) = \mu_0(E \cap X_0)$.
- If $X_0$ is a measurable subset of $X$, a new measure $\mu_0$ may be defined on the family of measurable subsets $E$ of $X$ by the equation $\mu_0(E) = \mu(E \cap X_0)$. 

**Def:** A subset $X_0$ of a measure space $(X, \mathcal S, \mu)$ is *thick* if $\mu_*(E \setminus X_0)= 0$ for every measurable set $E$. 

**Obs:** If $X$ itself is measurable, then $X_0$ is thick iff $\mu_*(X\setminus X_0) = 0$; if $\mu$ is totally finite, then $X_0$ is thick iff $\mu^*(X_0) = \mu(X)$. 

**Th:** If $X_0$ is a thick subset of a measure space, if $\mathcal S_0 = \mathcal S \cap X_0$, and if for $E\in \cal S$, $\mu_0(E\cap X_0) := \mu(E)$, then $(X_0, \mathcal S_0, \mu_0)$ is a measure space.

**Prop:** If $(X, \mathcal S, \mu)$ is measure space and if $X_0 \subseteq X$ such that for every two measurable sets $E_1$ and $E_2$, the condition $E_1 \cap X_0 = E_2 \cap X_0$ implies $\mu(E_1) = \mu(E_2)$, then $X_0$ is thick. 

**Prop:** If $(X,\mathcal S, \mu)$ is a finite measure space, then there exists a thick measurable set $X_0$. 

This result enables us, in most applications, to assume that a finite measure space is totally finite, since we can replace $X$ by $X_0$ without significan loss in generality. 

**Obs:** If $(X, \mathcal S, \mu)$ is a complete, $\sigma$-finite measure space, then every $\mu^*$-measurable space is measurable.

**Prop:** Let $(X, {\cal A}, \mu)$ be a measure space, ans let $A, B \in \cal A$ such that $A\subseteq B$. Then $\mu(A) \le \mu(B)$. If in addition $A$ satisfies $\mu(A) <\infty$, then $\mu(B\setminus A) = \mu(B) -\mu(A)$.

**Prop:** Let $(X, {\cal A},\mu)$ be a measure space. If $\{A_n\}_{n <\omega}$ be an arbitrary sequence of sets that belong to $\cal A$, then $$ \mu\left(\bigcup_{n <\omega} A_n\right) \le \sum_{n <\omega} \mu(A_n).$$
**Def:** Suppose that $(X, {\cal A})$ is a measurable space such that for each $x\in X$ the set $\{x\}$ belongs to $\cal A$. A finite or $\sigma$-finite measure $\mu$ on $(X, {\cal A})$ is *continuous* if $\mu(\{x\}) =0$ holds for each $x\in X$, and discrete if there is a countable subset $D$ of $X$ such that $\mu(X\setminus D) = 0.$

**Prop:** Let $(X, {\cal A})$ be a measurable space.
- If $\{\mu_n\}_{n <\omega}$ is an increasing sequence of measures on $(X, {\cal A})$, then the function $\mu: {\cal A} \to [0,\infty]$ defined $\mu(A) := \lim_{n \to \infty} \mu_n(A)$ is a measure on $(X, {\cal A})$.
- If $\{\mu_n\}_{n<\omega}$ is a sequence of measures on $(X, {\cal A})$, then the function $\mu: {\cal A} \to[0, \infty]$ defined by $\mu(A) := \sum_{n<\omega}\mu_n(A)$ defines a measure on $(X,{\cal A})$. 

**Prop:** Let $\mu$ be a measure on $(X, {\cal A})$ and let $\{A_n\}_{n <\omega}$ be a sequence of $\cal A$-measureable sets such that $\sum_{n<\omega} \mu(A_n) <\infty$. Then the set of points that belong to $A_n$ for infinitely many values of $n$ has measure zero under $\mu$.

# Properties that Hold Almost Everywhere

**Def:** Let $(X, {\cal A},\mu)$ be a measure space. A property of points of $X$ is said to hold *$\mu$-almost everywhere* if the set of points in $X$ at which it fails to gold is $\mu$-negligible or $\mu$-null. In other words a property holds $\mu$-almost everywhere if there is a set $N$ that belongs to $\cal A$, satisfies $\mu(N) = 0$, and contains every point at which the property fails to hold. More generally, if $E\subseteq X$, then a property is said to hold *$\mu$-almost everywhere on $E$* if the set of points in $E$ at which it fails to gold is $\mu$-negligible. The expression $\mu$-almost everywhere is often abbreviated to $\mu$-a.e. or to a.e.$[\mu]$. In cases where the measure $\mu$ is clear from context, the expression almost everywhere and a.e. are also used.

**Prop:** Let $(X, {\cal A},\mu)$ be a measure space, and let $f, g: X \to \overline{\Bbb R}$ that are equal almost everywhere. If $\mu$ is complete and if $f$ is $\cal A$-measurable, then $g$ is $\cal A$-measurable.

**Cor:** Let $(X, {\cal A},\mu)$ be a measure space, let $\{f_n\}$ be a sequence measurable functions on $X,$ and let $f: X\to \overline{\Bbb R}$ such that $\{f_n\}$ converges to $f$ almost everywhere. If $\mu$ is complete if each $f_n$ is $\cal A$-measurable, then $f$ is $\cal A$-measurable.

**Cor:** Let $f, g: \Bbb R \to \Bbb R$ continuous functions. If $f = g$ $\lambda$-almost everywhere, then $f =g$. 

**Cor:** Let $(X, {\cal A},\mu)$ be a measure space. and let $f, f_n: X \to \overline{\Bbb R}$ be $\cal A$-measurable function for each $n <\omega$. If $\{f_n\}$ converges to $f$ almost everywhere, then there are $\cal A$-measurable functions $g_1,g_2,\dots,$ that are equal to $f_1, f_2, \dots,$ almost everywhere and satisfy $f = \lim g_n$.

**Prop:** Let $(X, {\cal A},\mu)$ be a measure space and let $\cal A_\mu$ be the completion of $\cal A$ under $\mu$. Then a function $f: X \to \overline{\Bbb R}$ is $\cal A_\mu$-measurable iff there are $\cal A$-measurable functions $f_0, f_1: X \to \overline{\Bbb R}$ such that $f_0 \le f \le f_1$ holds everywhere on $X$ and $f_0 = f_1$ holds $\mu$-almost everywhere on $X$.

