---
tags:
  - RealAnalysis
connections:
---
Subjects: [[Real Analysis]]
Links: [[Series in R]]
### Divergence Test

If $\sum_{n=1}^\infty a_n$ then, $a_n \to 0$. Equivalently, if $a_n \not\to 0$ then, $\sum_{n = 1}^\infty a_n$ diverges.

### Absolute Convergence Test

If $\sum_{n=1}^\infty |a_n|$ converges, then $\sum_{n=1}^\infty a_n$ converges.

### Dirichlet’s Test
Let the sequence $(a_n)$ be decreasing with and $a_n \to 0$, and the partial sums of the form $\sum_{n=1}^m y_n = s_m$ be bounded then, the series $\sum x_ny_n$ is convergent.

The Alternating Series Test is a Corollary of this Test

### Abel’s Test
**Abel’s Lemma:**
Let $b_n$ be a nonnegative decreasing sequence, and let $\sum_{n =1}^\infty a_n$ be a series for which the partial sums are bounded, in other words there exists $A>0$ such that

$$ \left|\sum_{k = 1}^n a_k\right| \le A \quad \text{for all }n \in \mathbb N $$

Then for all $n \in \mathbb N$

$$ \left|\sum_{k = 1}^n a_k b_k\right| \le Ab_1 $$

**Th:** Let $(a_n)$ be a _monotone convergent sequence_ and, the series $\sum b_n$ be _convergent_, then the series $\sum a_nb_n$ converges