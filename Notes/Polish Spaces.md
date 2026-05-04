---
tags:
  - MeasureTheory
  - Topology
---
Subjects: [[Measure Theory]], [[Metric and Normed Spaces]], [[Topology]]
Links: [[Complete Metric Spaces]], [[Separable, First and Second Countable Spaces]], [[Metrizable Spaces]], [[Product of σ-Algebras]], [[Measures on Hausdorff Spaces]]

**Def:** A *Polish space* is a separable completely metrizable space. 
**Examples:** 
- For each $n<\omega$, the space $\Bbb R^n$ is Polish,
- More generally, each separable Banach space, with the topology induced by its norm, is Polish.
- Each compact metrizable space is Polish. 
- Every second countable compact Hausdorff space is Polish.
- Every second countable locally compact Hausdorff space is Polish.

**Prop:** Each closed subspace, and each open subspace, of a Polish space is Polish. 

**Prop:** The [[Sum Topology|disjoint union]] of countable Polish spaces is Polish. 

**Prop:** The [[Product Topology|product]] of countable Polish spaces is Polish. 

**Prop:** Let $X$ be a Polish space. Then a subspace of $X$ is Polish iff it is a $G_\delta$ in $X$.

**Examples:** 
- The space $\omega^\omega = \Bbb N^\Bbb N$ is Polish. We will denote this space by $\scr N$. Its elements are sequences of positive integers. A typical such sequence will generally be denoted by $(n_k)_{k\in\Bbb N}$ or by $\bf n$. 
- The space $\{0, 1\}^\omega$ which consists of all sequences 

**Prop:** Let $\{X_n\mid n<\omega\}$ be a sequence of second countable spaces. Then $$\mathcal B\left(\prod_{n<\omega} X_n\right) = \bigotimes_{n<\omega} \mathcal B(X_n).$$
**Prop:** Let $X$ and $Y$ be separable metrizable spaces, and let $f:X \to Y$ be Borel measurable. Then the graph of $f$ is a Borel subset of $X\times Y$. 

**Cor:** Let $(X, {\scr A})$ be a measurable space, and let $Y$ be a metrizable topological space. If $f, g: X\to Y$ be measurable with respect to $\scr A$ and $\mathcal B(Y)$, then $\{x\in X\mid f(x) = g(x)\}$ belongs to $\scr A$.  

**Lemma:** Let $(X, {\scr A})$ be a measurable space, and let $Y$ be a metrizable topological space. Then a function $f:X \to Y$ is measurable with respect to $\scr A$ and $\mathcal B(Y)$ iff for each continuous function $g: Y\to\Bbb R$ the function $g\circ f$ is $\scr A$-measurable. 

**Prop:** Let $(X, {\scr A})$ be a measurable space, let $Y$ be a sequential topological space, and for each positive integer $n$ let $f_n:X\to Y$ be a measurable with respect to $\scr A$ and $\mathcal B(Y)$. If $\lim f_n(x)$ exists for each $x\in x$, then the function $f:X \to Y$ given by $f(x) = \lim f_n(x)$ is measurable with respect to $\scr A$ and ${\mathcal B}(Y)$. 

**Prop:** Let $(X, {\scr A})$ be a measurable space, let $Y$ be a Polish space, and for each positive integer $n$ let $f_n: X\to Y$ be measurable with respect to $\scr A$ and $\mathcal B(Y)$. Let $C :=\{x\in X \mid \lim f_n(x) \text{ exists}\}$. Then $C\in \scr A$. Furthermore, the map $f:C\to Y$ is defined by $f(x) :=\lim f_n(x)$ is measurable with respect to $\scr A$ and $\mathcal B(Y)$. 

**Prop:** Every finite Borel measure on a Polish space is regular. 

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

