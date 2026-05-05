---
tags:
  - MeasureTheory
  - Topology
  - SetTheory
  - Analysis
---
Subjects: [[Measure Theory]], [[Metric and Normed Spaces]], [[Topology]], [[Set Theory]]
Links: [[Complete Metric Spaces]], [[Separable, First and Second Countable Spaces]], [[Metrizable Spaces]], [[Product of σ-Algebras]], [[Measures on Hausdorff Spaces]], [[Zero-Dimensional Spaces]], [[Borel Sets]]

**Def:** A *Polish space* is a separable completely metrizable space. 

**Examples:** 
- For each $n<\omega$, the space $\Bbb R^n$ is Polish,
- More generally, each separable Banach space, with the topology induced by its norm, is Polish.
- Each compact metrizable space is Polish. 
- Every second countable compact Hausdorff space is Polish.
- Every second countable locally compact Hausdorff space is Polish.

**Prop:** Each closed subspace, and each open subspace, of a Polish space is Polish. 

**Prop:** The [[Sum Topology|sum]] of countable Polish spaces is Polish. 

**Prop:** The [[Product Topology|product]] of countable Polish spaces is Polish. 

**Prop:** Let $X$ be a Polish space. Then a subspace of $X$ is Polish iff it is a $G_\delta$ in $X$.

**Prop:** Let $\{X_n\mid n<\omega\}$ be a sequence of second countable spaces. Then $$\mathcal B\left(\prod_{n<\omega} X_n\right) = \bigotimes_{n<\omega} \mathcal B(X_n).$$
**Prop:** Let $X$ and $Y$ be separable metrizable spaces, and let $f:X \to Y$ be Borel measurable. Then the graph of $f$ is a Borel subset of $X\times Y$. 

**Cor:** Let $(X, {\scr A})$ be a measurable space, and let $Y$ be a metrizable topological space. If $f, g: X\to Y$ be measurable with respect to $\scr A$ and $\mathcal B(Y)$, then $\{x\in X\mid f(x) = g(x)\}$ belongs to $\scr A$.  

**Lemma:** Let $(X, {\scr A})$ be a measurable space, and let $Y$ be a metrizable topological space. Then a function $f:X \to Y$ is measurable with respect to $\scr A$ and $\mathcal B(Y)$ iff for each continuous function $g: Y\to\Bbb R$ the function $g\circ f$ is $\scr A$-measurable. 

**Prop:** Let $(X, {\scr A})$ be a measurable space, let $Y$ be a sequential topological space, and for each positive integer $n$ let $f_n:X\to Y$ be a measurable with respect to $\scr A$ and $\mathcal B(Y)$. If $\lim f_n(x)$ exists for each $x\in X$, then the function $f:X \to Y$ given by $f(x) = \lim f_n(x)$ is measurable with respect to $\scr A$ and ${\mathcal B}(Y)$. 

**Prop:** Let $(X, {\scr A})$ be a measurable space, let $Y$ be a Polish space, and for each positive integer $n$ let $f_n: X\to Y$ be measurable with respect to $\scr A$ and $\mathcal B(Y)$. Let $C :=\{x\in X \mid \lim f_n(x) \text{ exists}\}$. Then $C\in \scr A$. Furthermore, the map $f:C\to Y$ is defined by $f(x) :=\lim f_n(x)$ is measurable with respect to $\scr A$ and $\mathcal B(Y)$. 

**Prop:** Every finite Borel measure on a Polish space is regular. 

**Examples:** 
- The product space $\omega^\omega = \Bbb N^\Bbb N$ is Polish. We will denote this space by $\scr N$. Its elements are sequences of positive integers. A typical such sequence will generally be denoted by $(n_k)_{k\in\Bbb N}$ or by $\bf n$. We call this space, the Baire space. Let us note that $\omega^\omega$ is homeomorphic to $\Bbb R \setminus \Bbb Q$. 
- The space $2^\omega$ which consists of all sequences of zeros and ones, is Polish. We see that $2^\omega$ is homeomorphic to the Cantor set, and hence it is called the Cantor space.
- Let's consider the space $\mathcal C([0, \infty))$, but we will consider the bounded metric $$d(f, g) := \sum_{n= 1}^\infty \frac1{2^n} \sup\{1 \wedge |f(t) - g(t)| \mid t\in [0,n]\}.$$We see that a sequence of functions $(f_n)_{n<\omega}$ in $\mathcal C([0, \infty))$ converges to $f$ with respect to the metric above iff it converges to $f$ uniformly on each compact subset of $[0,\infty)$. We see that $\mathcal C([0,\infty))$ is complete and separable, and hence Polish. 

**Prop:** Every separable metrizable space is homeomorphic to a subspace of the product space $[0, 1]^\omega$, and thus every Polish space is homeomorphic to a $G_\delta$ in $[0, 1]^\omega$. 

**Prop:** Let $(X, {\scr A})$ be a measurable space, let $Y$ be a Polish space, let $A$ be a subset of $X$ that might not belong to $\scr A$, and let ${\scr A}_A$ be the trace of $\scr A$ on $A$. If $f:A\to Y$ is measurable with respect to ${\scr A}_A$ and $\mathcal B(Y)$, then $f$ has an extension $F:X\to Y$ that is measurable with respect to $\scr A$ and $\mathcal B(Y)$. 

# Analytic Sets

**Def:** Let $X$ be a Polish space. A subset $A$ of $X$ is *analytic* if there is a Polish space $Z$ and a continuous function $f:Z\to X$ such that $f[Z] =A$. 

**Prop:** Let $X$ be a Polish space. Then each open subset, and each closed subsets of $X$ is analytic.

**Prop:** Let $X$ be a Polish space, and let $\{A_n\mid n<\omega\}$ be a sequence of analytic subsets of $X$. Then $\bigcup_{k<\omega} A_k$ and $\bigcap_{k<\omega} A_k$ are analytic. 

**Lemma:** Let $X$ be a Hausdorff topological space. Then $\mathcal B(X)$ is the smallest family of subsets of $X$ that 
- contains open and closed subsets of $X$,
- is closed under the formation of countable intersections, and
- is closed under the formation of countable unions. 

**Prop:** Let $X$ be a Polish space. Then each Borel subset of $X$ is analytic.

**Prop:** Let $\{X_n\mid n<\omega\}$ be a sequence of Polish spaces, and for each $A_k$ be an analytic subset of $X_k$. Then $\prod_{k<\omega} A_k$ is an analytic subset of $\prod_{k<\omega} X_k$. 

**Prop:** Let $X$ and $Y$ be Polish spaces, let $A$ be an analytic subset of $X$, and let $f:A\to Y$ be Borel measurable (that is, measurable with respect to $\mathcal B(A)$ and $\mathcal B(Y)$). If $A_1$ and $A_2$ are analytic subsets of $X$ and $Y$, respectively, then $f[A\cap A_1]$ and $f^{-1}[A_2]$ are analytic subsets of $Y$ and $X$, respectively. 

**Prop:** Each nonempty Polish space is the image of the product space $\omega^\omega$ under a continuous function.

**Cor:** Each nonempty Polish space is the image of $\omega^\omega$ under a continuous open map. 

**Cor:** Each nonempty analytic subset of a Polish space is the image of the product space $\omega^\omega$ under some continuous function. 

**Prop:** Let $X$ be a Polish space. A subset $A$ of $X$ is analytic iff there is a closed subset of $\omega^\omega \times X$ whose projection on $X$ is $A$.

**Prop:** Each Borel subset of a Polish space is the image under a continuous injective map of some zero-dimensional Polish space. 

**Lemma:** Let $X$ be a zero-dimensional separable metric space, let $U$ be an open and non-compact subset of $X$, and let $\varepsilon>0$. Then $U$ is the union of countably infinite family of disjoint sets, each of which is nonempty, open, closed and of diameter of at most $\varepsilon$. 

**Def:** Let $X$ be a topological space and let $A\subseteq X$. A point $x\in X$ is a *[[Limit Points and Closure|condensation point]]* of $A$ if every open neighbourhood of $x$ contains uncountably many points of $A$. 

**Lemma:** Let $X$ be a separable metrizable space, and let $C$ be the set of condensation points of $X$. Them $C$ is closed and $X\setminus C$ is countable. 

**Cantor-Benedixson Theorem:** Every Polish space can be partitioned into a perfect set and a countable set. 

**Prop:** Let $X$ be a Polish space, and let $B$ be an uncountable Borel subset of $X$. Then there is a continuous injective map $f: \omega^\omega \to X$ such that $f[\omega^\omega]\subseteq B$ and such that $B\setminus f[\omega^\omega]$ is countable. 

**Cor:** Each uncountable Borel subset of a Polish space includes a subset that is homeomorphic to $2^\omega$. 

**Lemma:** Let $A$ be an uncountable analytic subset of the Polish space $X$. The $A$ has a subset that is homeomorphic to $2^\omega$. 

**Cor:** Every uncountable analytic subset of a Polish space has the cardinality of the continuum. 

**Def:** Let $X$ be a set, and let $\scr F$ be a family of subsets of $X$. A subset $A$ of ${\scr N} \times X$ is *universal* for $\scr F$ if the collection of sections $\{A_{\bf n}\mid {\bf n}\in {\scr N}\}$ is equal to $\scr F$.

**Lemma:** Let $X$ be a separable metrizable space. Then there is an open subset $\omega^\omega \times X$ that is universal for the collection of open subsets of $X$ and a closed subset $\omega^\omega \times X$ that is universal for the collection of closed subsets of $X$. 

**Prop:** Let $X$ be Polish space. Then there is an analytic subset of $\omega^\omega \times X$ that is universal for the collection of analytic subsets of $X$. 

**Cor:** There is an analytic subset of $\omega^\omega$ that is not a Borel set. 

**Cor:** Let $X$ be an uncountable Polish space. The collection of analytic subsets of $X$ and the collection of Borel subsets of $X$ have the cardinality of the continuum. 

**Prop:** If $X$ is an uncountable Polish space, then there is an analytic subset of $X$ that is not a Borel set. 

**Prop:** Suppose $X$ is a Polish space then for every $\alpha$ with $\alpha \in \omega_1\setminus 1$ there exists a universal $\Sigma_\alpha^0$ set $U\subseteq 2^\omega\times X$. 

## The Separation Theorem

**Th:** Let $X$ be a Polish space, and let $A_1$ and $A_2$ be disjoint analytic subsets of $X$. Then $A_1$ and $A_2$ can be separated by Borel sets.

**Cor:** Let $X$ be a Polish space, and let $\{A_n\mid n<\omega\}$ be disjoint analytic subsets of $X$. Then there are disjoint Borel subsets $\{B_n \mid n<\omega\}$ of $X$ such that $A_n\subseteq B_n$ holds for each $n<\omega$. 

**Cor:** Let $X$ be a Polish space, and let $A$ be a subset of $X$. If both $A$ and $X\setminus A$ are analytic, then $A$ is Borel. 