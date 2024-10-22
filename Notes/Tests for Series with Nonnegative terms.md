---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Series in R]]
### Boundedness

If a the sequence of partial sums $s_m = \sum_{n=k}^ma_n$ are bounded and $\forall n \in\mathbb{N}(a_n\geq0)$, then by the Monotone Convergence Theorem then $\sum a_n$ will converge

### **Cauchy’s Condensation Test**

Given the the sequence $(b_n)$ being _decreasing_ and _non-negative_, then:

$$ \sum_{n= 1}^{\infty} b_n \text{ converges } \iff \sum_{n= 1}^{\infty} 2^nb_{2^n} \text{ converges } $$

### Comparison Test

Suppose that there are two sequences that $\forall k \in \mathbb{N(}0 \leq a_k\leq b_k)$ then:

- _If the series $\sum_{n=1}^\infty b_n$ converges, then $\sum_{n=1}^\infty a_n$ also converges._
- _If the series $\sum_{n=1}^\infty a_n$ diverges, then $\sum_{n=1}^\infty b_n$ also diverges._

### Limit Comparison

Let the sequences $(a_n)$ , and $(b_n)$ be strictly positive, and that the following limit exists:

$$ r = \lim_{n\to\infty} \frac{a_n}{b_n} $$

- If $r \neq 0$, then $\sum a_n$ converges if and only if $\sum b_n$ converges.
- If $r = 0$, then if $\sum b_n$ converges, then, $\sum a_n$ converges.

### Alternating Series

Given the sequence $(a_n)$ where is monotonically decreasing and _non-negative_. If $(a_n) \to 0$, then the series $\sum_{n=1}^\infty (-1)^na_n$ converges.

### Integral Test

Let $f: \mathbb{R} \to \mathbb{R}$, this function needs to be positive and decreasing at $\{t: t\geq k \}$, for some $k$ , then:

$$ \sum_{n=1}^\infty f(n) \text{ converges } \iff \int_1^\infty f \text{ converges} $$