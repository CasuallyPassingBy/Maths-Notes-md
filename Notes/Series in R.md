---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Properties of Limits of Sequences in R]]

Let the sequence $(b_n)$, and the partial sums $(s_m)$ as:

$$ s_m = \sum_{n = 1}^m b_n $$

The series $\sum_{n= 1}^{\infty} b_n = \lim_{m\to\infty} s_m = B$ and the series converges if the limit of the partial sums exist.

### Original Definition

$$ \forall\varepsilon>0\exists N \in \mathbb{N} \left[ \forall n \geq N \left(\Bigg|\sum_{k = 1}^n b_k - B \Bigg|\right) \right] $$

### Cauchy Criterion

$$ \forall\varepsilon>0\exists N \in \mathbb{N} \left[ \forall n,m \geq N \left(\Bigg|\sum_{k = n+1}^m b_k \Bigg|\right) \right] $$
## Algebraic Properties

Given the series $\sum_{n=1}^\infty a_n = A$ and $\sum_{n=1}^\infty b_n = B$ then behave as follows:

1. For any $c \in\mathbb{R}$, $\sum_{n=1}^\infty ca_n = cA$
2. $\sum_{n=1}^\infty(a_n +b_n) = A+B$