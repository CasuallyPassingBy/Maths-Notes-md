---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Series in R]], [[Series of Functions in Rn]], [[Uniform Convergence In Metric Spaces]], [[Power Series in R]], [[Normed Vector Spaces]], [[Normed Algebras]]

**Def:** Let $V =(V, \|\cdot \|)$ is normed vector space and $(v_k)$ is a sequence in $V$.  We say that the series
$$ \sum _{k = 1}^\infty v_k $$

_converges_ in $V$ if the sequence $(w_n)$ of partial sums $w_n := \sum\limits_{k =1}^m v_k$ converges in $V$. Its limit is denoted as $$ \sum_{k = 1}^\infty v_k := \lim_{m \to \infty} \sum_{k = 1}^m v_k $$

If the series $\sum\limits_{k =1}^\infty v_k$ converges in $V$, then $v_k \to 0$ in $V$, in particular $(v_k)$ is bounded.

**Cauchy Criterion for Series:** Let $V$ be a Banach space and $(v_k)$ a sequence $V$. The series$$ \sum_{k = 1}^\infty v_k $$
converges in $V$ iff for all $\varepsilon>0$, there’s $N \in \Bbb N$ and if $j \ge 1$, then$$ \left\|\sum_{k = N}^{N+j} v_k\right\| < \varepsilon $$**Weiestrass Criterion:** Let $V$ be a Banach space and $(v_k)$ be a sequence of $V$. If the series of real numbers$$ \sum_{k = 1}^\infty \| v_k \| $$converges, then the series$$ \sum_{k = 1}^\infty v_k $$converges on $V$, and$$ \left\| \sum_{k = 1}^\infty v_k\right\| \le \sum_{k = 1}^\infty \| v_k \| $$**Def:** We say that a **series of functions**$$ \sum_{k = 1}^\infty f_k $$*converges uniformly* on $S$ if the sequence of functions $g_n = \sum\limits_{k = 1}^n f_k$ converges uniformly on $S$ and a function $f:S \to V$ which is denoted as$$ \sum_{k = 1}^\infty f_k $$An example are power series, and all their corresponding theorems

**Prop:** Let $V$ be a normed algebra. If $a\in V$ and $\sum_{k = 0}^\infty b_k$ is a convergent series in $V$, then $a\sum_{k = 0}^\infty = \sum_{k = 0}^\infty ab_k$. 