---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Vector Spaces]], [[Vector Subspaces]]
## Definition
Let $S$ be a non-empty subset of $V$ (a vector space over a field $\mathbb{F}$), a vector $v \in V$ is a a _**linear combination**_ of vectors of $S$ if exist a finite number of vectors $\{ u_i\}_{i=1}^n$ $\subseteq S$ and scalars $\{a_i\}_{i=1}^n\subseteq \mathbb{F}$ such that $v = \sum_{i=1}^na_iv_i$, $\{a_i\}_{i=1}^n$ are called the coefficients of the linear combination.

## Span
The span of any subset $S$ of $V$ (a vector space over the field $\mathbb{F})$ is the smallest subspace that contains $S.$ Moreover any subspace containing $S$ must contain the span of $S$ denoted as $\text{span}(S)$ or $\text{L}(S)$. $\text{span}(\varnothing) := \{ 0 \}$.
A subset $S$ is said to generate or spans $V$ if $\text{span}(S) = V$ . The vectors of $S$ generates (or span) $V$.
If a finite list $\{ u_i\}_{i=1}^n$ spans $V$, then $V$ is a _**finite dimensional vector space**_.
A vectors space that is not _**finite dimensional**_ then it is an _**infinite dimensional vector space.**_