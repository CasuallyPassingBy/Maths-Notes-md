---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Double Series]], [[Tests for Series with Nonnegative terms]]

_**Theorem:**_ A double series of nonnegative terms $\sum_{n,m= 1}^\infty z_{n,m}$ converges iff the set of partial sums $\{s_{n,m} : n,m\in\mathbb{N}\}$ is bounded.

_**Corollary:**_ A double series of nonnegative terms $\sum_{n,m= 1}^\infty z_{n,m}$ either converges to a finite number or diverges towards $\infty$. ******

_**Comparison Test:**_ Supposes that:

$$ \forall n,m\in\mathbb{N}(0 \le u_{n,m} \le v_{n,m}) $$

1. If $\sum_{n,m = 1}^\infty v_{n,m}$ converges, then $\sum_{n,m = 1}^\infty u_{n,m}$ also converges.
2. If $\sum_{n,m = 1}^\infty u_{n,m}$ diverges, then $\sum_{n,m = 1}^\infty v_{n,m}$ also diverges.

_**Theorem: $\forall n,m\in\mathbb{N}[a_{n,m}\in [0, \infty)]$,**_ let $\phi:\mathbb{N}\to\mathbb{N}^2$ be bijective. Then:

$$ \sum_{n=1}^\infty\left(\sum_{m=1}^\infty a_{n,m}\right) = \sum_{k=1}^\infty a_{\phi(k)} $$

$$ \sum_{n=1}^\infty\left(\sum_{m=1}^\infty a_{n,m}\right) = \sum_{m=1}^\infty\left(\sum_{n=1}^\infty a_{n,m}\right) $$