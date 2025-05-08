---
tags:
  - Analysis
  - FunctionalAnalysis
---
Subjects: [[Metric and Normed Spaces]], [[Functional Analysis]]
Links: [[Quotient of Vector Spaces]], [[Complete Metric Spaces]], [[Normed Vector Spaces]]

**Def:** Let $X$ be a normed space over $\Bbb F$, and $W$ be a closed linear subspace of $M$. Let $X/M$  be the quotient vector space of $X$ modulo $M$. and we define the quotient norm $\|\cdot \|_{X/M}$ , with the quotient mapping $\pi: X \to X/M$ as $\pi (x) = x + M$ $$
\|\pi(x)\|_{X/M} := \inf_{z \in M}\|x-z\|
$$
**Th:** If $M$ is a closed subspace of a normed space $X$, then the quotient space of $X/M$ is a norm.

**Prop:** Let $M$ be a closed subspace of a normed space $X$.
- If $x\in X$, then $\|x + M\| \le \|x\|$.
- If $x\in X$ and $\varepsilon>0$, then there exists an $x' \in X$ such that $x' + M = x + M$ and $\|x'\| < \|x+ M\| + \varepsilon$.

**Th:** If $M$ is  closed subspace of a Banach space $X$, then $X/M$ is also a Banach space.

**Def:** Let $P$ be a property defined for normed spaces. Suppose that whenever $X$ is a normed space with a closed subspace $M$ such that two of the spaces $X$, $M$ and $X/M$ have that property, then the third must also have it. Then $P$ is a *three-spaces* property

**Th:** Completeness is a three-space property.

**Prop:** Finite-dimensitionality is a three-space property.

**Lemma:** If $M$ is a closed subspace of a normed space $X$ and $\pi$ is the quotient map from $X$ into $X/M$, then the image under $\pi$ of the open unit ball of $X$ is the unit ball of $X/M$, i.e., $\pi[B_X(0, 1)] = B_{X/M}(0, 1)$.

**Prop:** Let $M$ be a closed subspace of a normed space $X$. Then the quotient map $\pi$ from $X$ into $X/M$ is bounded linear operator that is also an open mapping and has $\ker \pi = M$. If $M \neq X$, then $\|\pi \| = 1$.s

**Th:** Suppose that $X$ and $Y$ are normed spaces and that $T$ is a linear operator from $X$ into $Y$, not assumed to be normed. Suppose further that $M$ is a closed bounded subspace of $X$ such that $M \subseteq \ker T$ and that $\pi$ is the quotient map from $X$ into $X/M$. Then there is a unique function $S$ from $X/M$ into $Y$ such that $T = S \circ \pi$, that is, such that the following diagram commutes
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
X \arrow[dr, two heads,"\pi"'] \arrow[rr, "T"]& & Y\\
 & X/M \arrow[ur, dashed, "S"']
\end{tikzcd}
\end{document}
```
This map $S$ is linear and has the same range as $T$. The operator $S$ is an open mapping iff $T$ is an open mapping, and is bounded iff $T$ is bounded. If $T$ is bounded, then $\|S \| = \|T\|$.

This is like the normed space equivalence of the [[Group Homomorphisms and Isomorphisms#^b63bfc|Factorising Homomorphism Theorem]] of groups. Likewise, we also get the following:

**The First Isomorphism Theorem for Banach Spaces:** Suppose that $X$ and $Y$ are Banach spaces and that $T\in \mathcal B(X, Y)$. Suppose further that the range of $T$ is closed in $Y$. Then $X/\ker T \cong T[X]$.

**The Second Isomorphism Theorem for Banach Spaces:** Let $X$ be a Banach space. If $M$ and $N$ be closed subspaces of $X$ such that $M+ N$ is a closed subspace of $X$, then $$(M + N)/N \cong M /(M \cap N).$$

**The Third Isomorphism Theorem for Banach Spaces:** Let $X$ be a Banach space. Let $M, N$ be closed subspaces of $X$ such that $N$ is a subspace of $M$. Then $N$ is a closed subspace of $M$, and $M/N$ is a closed subspace of $X/N$ and $$\frac{X/N}{M/N} \cong X/M.$$
**Prop:** Suppose that $T$ is a bounded linear operator from a normed space $X$ into a normed space $Y$, then $X/\ker T \cong T[X]$.

**Th:** Suppose that $T$ is a finite-rank linear operator from a normed space $X$ into a normed space $Y$. Then $T$ is bounded iff its kernel is a closed subset of $X$.

**Prop:** Let $f: X \to \Bbb F$ be an unbounded linear map on the normed space $X$. Then the $\ker f$ is dense in $X$.

**Prop:** Let $M$ and $N$ be closed subspaces of a normed space $X$. If either $M$ or $N$ is finite-dimensional, then $M+N$ is closed subspace of $X$.

**Th:** Suppose that $X$ and $Y$ are normed spaces and that $M$ is a closed subspace of $X$ such that $X/M$ is finite-dimensional. If $T\in \mathcal B(M, Y)$, then there is a $T_0 \in \mathcal B(X, Y)$ such that $T_0$ agrees with $T$ on $M$. That is, every bounded linear operator with domain $M$ has a bounded linear extension to $X$.