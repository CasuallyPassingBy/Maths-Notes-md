---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[ellp spaces]], [[Complete Metric Spaces]], [[Bounded Function Spaces]], [[Continuous Function Spaces]], [[Continuity on Metric Spaces]]

A sequence of functions $f_k :S \to X$, with $k \in \Bbb N$, is ********uniformly Cauchy********* on $S$, if for all $\varepsilon>0$, there’s $N\in\Bbb N$ such that $n, m \ge N$,

$$ d_X(f_n(z) , f_m(z)) < \varepsilon \qquad \forall z \in S $$

### Cauchy criterion for uniform convergence

Let $X$ be a complete metric space. A sequence of functions $f_k :S \to X$, with $k \in \Bbb N$, converges uniformly on $S$ iff $(f_k)$ is uniformly Cauchy on $S$

Let $S$ be a set and $Z$ be a metric space:

- If $X$ is a complete metric space, then ${\cal B}(S, X)$ and ${\cal C}^0_b(Z, X)$ are complete
- If $V$ is a Banach space, then ${\cal B}(S, V)$ and ${\cal C}^0_b(Z, V)$ are Banach spaces

We get that ${\cal C}^0(K, X)$ is complete if $X$ is complete

We can see that in particular ${\cal C}^0[a,b]$ is complete. We can show that ${\cal C^0_p}[a, b]$ is not complete for $p \in [1,\infty)$

As a corollary we get that $\ell^\infty = {\cal B}(\Bbb N, \Bbb R)$, then $\ell ^\infty$ is a Banach space.

The corollary of this corollary is that $\ell^p$ is a Banach space for $p\in [1,\infty]$