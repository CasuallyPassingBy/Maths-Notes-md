---
tags:
  - Analysis
  - VectorAnalysis
---

Subjects: [[Metric and Normed Spaces]], [[Vector Analysis]] 
Links: [[Sequence of Functions in Rn]]
Let’s consider a subset of $A\subseteq \Bbb{R}^m$, then the space of continuous functions from $A$ into $\Bbb{R}^n$ is denoted as $\mathcal C(A, \Bbb{R}^n)$. $\mathcal C(A, \Bbb{R}^n)$ is a vector space. A subspace of interest in $\mathcal C(A, \Bbb{R}^n)$ is the space of continuous and bounded functions, denoted as $\mathcal C_b(A, \Bbb{R}^n)$.

If $A$ is compact then $\mathcal C(A, \Bbb{R}^n) = \mathcal C_b(A, \Bbb{R}^n)$ . Usually can be shortned into $\mathcal C$ and $\mathcal C_b$ respectively.

For $f\in \mathcal C_b$, then we can define $\|f\|_\infty = \sup_{x \in A}\|f(x)\|$, which exists since $f$ is bounded. This is a type of norm in $\mathcal C_b$. For the rest of this section $\|\cdot\|_\infty$ will be shortend into $\|\cdot\|$

********Th:******** The operation $\|\cdot\|$ on $\mathcal C_b(A, \Bbb{R}^n)$ satisfies the properties of a norm:

- $\|f\|\ge 0$ and $\|f\|=0$ iff $f= 0$
- $\|\alpha f\| = |\alpha|\|f\|$ , for $\alpha \in \Bbb{R}$, $f\in \mathcal C_b$
- $\|f+g\|\le \|f\| +\|g\|$

********Th: $(f_k\rightrightarrows f$** on $A)$ is the same as $(f_k \to f$ on $\mathcal C_b(A,\Bbb{R}^n))$

By the Cauchy Criterion of uniform convergence, we know that $\mathcal C_b$ is a Banach space.

********Th:******** $\mathcal C_b$ is a [[Complete Metric Spaces|Banach space]].