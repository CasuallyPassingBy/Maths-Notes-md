---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Double Sequences Limits]], [[Series in R]]

Let $z:\mathbb{N}^2\to\mathbb{C}$ a double sequence of complex numbers, and let $s_{n,m}$ de defined by the equation:

$$ s_{n,m} =\sum_{i=0}^n\left(\sum_{j=1}^mz_{i,j}\right) $$

The pair $(z,s)$ is called the _double series_ and is denoted as $\sum_{n,m= 1}^\infty z_{n,m} = \lim_{n,m\to\infty} s_{n,m}$ or more briefly $\sum z_{n,m}$. The series $\sum_{n=1}^\infty\left(\sum_{m=1}^\infty z_{n,m}\right)$ and $\sum_{m=1}^\infty\left(\sum_{n=1}^\infty z_{n,m}\right)$ are called _iterated series._

_**Theorem:**_ If the double series $\sum_{n,m=1}^\infty z_{n,m}$ converges then:

$$ \lim_{n,m\to\infty}z_{n,m} = 0 $$

_**Cauchy Convergence Criterion for Double series:**_ A double series $\sum_{n,m= 1}^\infty z_{n,m}$ converges iff its sequence of partial sums $s_{n,m}$ is _Cauchy._

_**Theorem:**_ If $\sum_{n,m = 1}^\infty z_{n,m} = s$, and $\sum_{n,m = 1}^\infty w_{n,m} = s'$ then:

- $\sum_{n,m = 1}^\infty z_{n,m} +w_{n,m} = s+s'$
- $\sum_{n,m = 1}^\infty cz_{n,m} = cs$ for any $c\in\mathbb{C}$.

_**Theorem:**_ The series $\sum_{n,m = 1}^\infty z_{n,m} = s$. Then the _iterated series_ $\sum_{n=1}^\infty\left(\sum_{m=1}^\infty z_{n,m}\right)$ and $\sum_{m=1}^\infty\left(\sum_{n=1}^\infty z_{n,m}\right)$ are both convergent with sum $s$ iff:

1. for every $m\in\mathbb{N}$, the series $\sum_{n=1}^\infty z_{n,m}$ is convergent, and
2. for every $n\in\mathbb{N}$, the series $\sum_{m=1}^\infty z_{n,m}$ is convergent.