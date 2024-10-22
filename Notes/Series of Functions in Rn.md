---
tags:
  - RealAnalysis
  - VectorAnalysis
---
Subjects: [[Real Analysis]], [[Vector Analysis]]
Links: [[Sequence of Functions in Rn]], [[Sequence of Functions in Rn]]
Let $(f_n)$ be a sequence of functions on $A\subseteq\Bbb R$, let $(s_n)$ is another sequence of functions on $A$ defined as follows:

$$ s_n=\sum_{k=1}^\infty f_n $$

The limit of $s_n$ is the series of functions. also denoted as $\sum_{n=1}^\infty f_n = f$, we can say it converges pointwise or uniformly.
### Cauchy Criterion for UC of Series

A series $\sum f_n$ converges uniformly on $A\subseteq\Bbb R^n$ iff:

$$ \forall\varepsilon>0\exists N\in\Bbb N \left(\forall n > m\ge N\left[ \left\| \sum_{m<k\le n}f_n\right\|_\infty< \varepsilon \right]\right) $$

$$ \forall\varepsilon>0\exists N\in\Bbb N \left(\forall n > m\ge N\land\forall x\in A\left[ \left\| \sum_{m<k\le n}f_n(x)\right\|< \varepsilon \right]\right) $$
## Term-by-Term Theorems
### Continuity
Let $(f_n)$ be a sequence of continuous functions on $A\subseteq\Bbb R$, and $\sum_{n=1}^\infty f_n\rightrightarrows f$, then $f$ is continuous at $A$.
### Differentiability
Let $(f_n)$ be a sequence of functions be differentiable functions on the interval $I$, assume $\sum_{k=1}^\infty f'_n$ converges uniformly to a limit $g(x)$ on $A$. If there’s an $x_0\in[a,b]$ where $\sum_{n=1}^\infty f_n(x_0)$ converges, then the series $\sum_{n=1}^\infty f_n\rightrightarrows f$ where $f\in\mathcal{C}^1[a,b]$ satisfying $f'=g$. In other words:

$$ \sum_{n=1}^\infty f_n = f \text{, and } \sum_{n=1}^\infty f'_n=f' $$
## Weierstrass M-Test

Let $(f_n)$ be a sequence where for all $n\in\Bbb N$, there’s an $M_n >0$ such that$\|f_n(x)\| \le M_n$ for any $x\in A$. If $\sum_{n=1}^\infty M_n$ converges, then $\sum_{n=1}^\infty f_n$ converges uniformly on $A.$

## Weird Tests

### Abel’s Test
let $A \subseteq \Bbb R^n$ and $\phi_k :A\to \Bbb R$ be a sequence of functions which are decreasing; that is, ${\phi_{k+1}(x) \le \phi_k(x)}$ for each $x \in A$. Supose there is a constant $M$ such that ${|\phi_k(x)|\le M}$ for all $x \in A$ and all $n \in \Bbb N^+$. If $\sum_{k =1}^\infty f_k$ converges uniformly on $A$, then so does

$$ \sum_{k = 1}^\infty \phi_k f_k $$

### Dirichlet Test
Let $s_n = \sum_{k = 1}^n f_k$ for a sequence $f_k :A \subseteq \Bbb R^n \to \Bbb R$. Assume there is a constant $M$ such that $|s_n(x)| \le M$, for all $x \in A$ and all $n\in \Bbb N^+$. Let $g_n: A \to \Bbb R$ be such that ${g_k \rightrightarrows 0}$, $g_k \ge 0$, and $g_{k+1}(x) \le g_k(x)$. Then $\sum_{k =1}^\infty f_k g_k$ converges uniformly on $A$.

