---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Series in R]], [[Series of Functions in Rn]], [[Uniform Convergence In Metric Spaces]], [[Power Series in R]], [[Normed Vector Spaces]], [[Normed Algebras]], [[Absolute Convergence Test and Properties]]

**Def:** Let $V =(V, \|\cdot \|)$ is normed vector space and $(v_k)$ is a sequence in $V$.  We say that the series
$$ \sum _{k = 1}^\infty v_k $$

_converges_ in $V$ if the sequence $(w_n)$ of partial sums $w_n := \sum\limits_{k =1}^m v_k$ converges in $V$. Its limit is denoted as $$ \sum_{k = 1}^\infty v_k := \lim_{m \to \infty} \sum_{k = 1}^m v_k $$

**Prop:** Let $X$ and $Y$ be normed spaces.
- if $\sum x_n$ converges in $X$, then $x_n \to 0$.
- If $\sum x_n$ and $\sum y_n$ both converge in $X$, then so does $\sum (x_n + y_n)$, and $\sum (x_n + y_n) = \sum x_n + \sum y_n$.
- If $\sum x_n$ converges in $X$ and $\alpha$ is a scalar, then $\sum \alpha x_n$ converges, and $\sum \alpha x_n = \alpha \sum x_n$. 
- If $\sum x_n$ converges in $X$- If $\sum x_n$ converges in $X$ is a continuous linear operator from $X$ into $Y$, then $\sum Tx_n$ converges in $Y$, and $T\left(\sum x_n\right) = \sum Tx_n$.
- If $\sum x_n$ is finite or infinite sum in $X$, then $\| \sum x_n \| \le \sum \|x_n\|$.

**Cauchy Criterion for Series:** Let $V$ be a Banach space and $(v_k)$ a sequence $V$. The series$$ \sum_{k = 1}^\infty v_k $$converges in $V$ iff for all $\varepsilon>0$, there’s $N \in \Bbb N$ and if $j \ge 1$, then$$ \left\|\sum_{k = N}^{N+j} v_k\right\| < \varepsilon $$
**Def:** Let $\sum x_n$ be a formal series in a normed space.
- The series $\sum x_n$ is *absolutely convergent* if $\sum \|x_n\|$ converges.
- The series $\sum x_n$ is *unconditionally convergent* if $\sum x_{\sigma(n)}$ converges for each permutation $\sigma$ of $\Bbb N$.
- The series $\sum x_n$ is *conditionally convergent* if it is convergent but not unconditionally convergent.

**Weiestrass Criterion:** Let $V$ be a Banach space and $(v_k)$ be a sequence of $V$. If the series of real numbers$$ \sum_{k = 1}^\infty \| v_k \| $$converges, then the series$$ \sum_{k = 1}^\infty v_k $$converges absolutely on $V$, and$$ \left\| \sum_{k = 1}^\infty v_k\right\| \le \sum_{k = 1}^\infty \| v_k \| $$
**Prop:** A normed space $X$ is a Banach space iff each absolutely convergent series in $X$ converges.

**Def:** We say that a **series of functions**$$ \sum_{k = 1}^\infty f_k $$*converges uniformly* on $S$ if the sequence of functions $g_n = \sum\limits_{k = 1}^n f_k$ converges uniformly on $S$ and a function $f:S \to V$ which is denoted as$$ \sum_{k = 1}^\infty f_k $$An example are power series, and all their corresponding theorems

**Prop:** Let $V$ be a normed algebra. If $a\in V$ and $\sum_{k = 0}^\infty b_k$ is a convergent series in $V$, then $a\sum_{k = 0}^\infty = \sum_{k = 0}^\infty ab_k$. 

**Prop:** If $\sum x_n$ is absolutely convergent in a Banach space $X$, then $\sum x_n$ is unconditionally convergent.