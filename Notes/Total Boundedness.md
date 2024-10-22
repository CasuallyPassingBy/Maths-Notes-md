---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Compactness in Metric Spaces]], [[Complete Metric Spaces]] 

A subset $A$ of $X$ is _totally bounded_ if for all $\varepsilon>0$, there’s a finite number of points $a_1, \dots, a_m \in A$ such that

$$ A \subseteq \bigcup_{i = 1}^m B_X(a_i, \varepsilon) $$

Let $A$ be a subset of $X$

- If $A$ is compact, then $A$ is totally bounded
- if $A$ is totally bounded, then $A$ is bounded
- If $D\subseteq A$ is totally bounded, then $D$ is totally bounded
- If $A$ is totally bounded, then the closure $\overline A$ on $X$ is also totally bounded

The finite union of totally bounded sets is totally bounded

All of these are equivalent
- $X$ is compact
- $X$ is sequentially compact
- $X$ is complete and totally bounded

A metric space $X$ is totally bounded iff every sequence in $X$ has a Cauchy subsequence

Let $\phi:X \to Y$ be uniformly continuous and $A$ be a totally bounded set in $X$, then $\phi[A]$ is totally bounded in $Y$

We have the following equivalence given a normed space $V$:
- $\dim V< \infty$
- The totally bounded sets of $V$, are precisely the bounded sets
