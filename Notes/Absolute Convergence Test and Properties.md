---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Series in R]]

If $\sum |a_n|$ converges, then $\sum a_n$ it is said that it _converges absolutely._ If $\sum |a_n|$ diverges but $\sum a_n$ still converges, then $\sum a_n$ is said to it _converges conditionally._

### Rearrangements

_**Definition:**_

Let $f: \mathbb{N}\to\mathbb{N}$, where $f$ is bijective, $b_n = a_{f(n)}$ then, $\sum b_n$ is a _rearrangements_ of $\sum a_n$

_**Theorem:**_ If the series $\sum a_n$ is _absolutely convergent,_ then any rearrangements of this series will converge to the same limit.

### Riemann Rearrangement Theorem
Let $\sum_{n = 1}^\infty a_n$ an be a conditionally convergent series.
1. For every $x \in\overline{\Bbb{R}}$ there exists a rearrangement $\sigma$ such that:
    
    $$ \sum_{n=1}^\infty a_{\sigma(n)} = x $$
    
2. There’s a rearrangement $\sigma$ such that $\sum_{n=1}^\infty a_{\sigma(n)}$ doesn’t converge in $\overline{\Bbb{R}}$.

### Limit Comparison V.2

Let the sequences $(a_n)$ , and $(b_n)$ be _non-zero_, and that the following limit exists:

$$ r = \lim_{n\to\infty} \bigg|\frac{a_n}{b_n} \bigg| $$

- If $r \neq 0$, then $\sum a_n$ absolutely converges if and only if $\sum b_n$ absolutely converges.
- If $r = 0$, then if $\sum b_n$ absolutely converges, then, $\sum a_n$ absolutely converges.

### Ratio and Root Test

Let the sequence $(a_n)$, given the following limits:

$$ \lim_{n\to\infty} \Big|\frac{a_{n+1}}{a_n}\Big| = \lim_{n\to\infty} |a_n|^{1/n} = r $$

- If $r < 1$ then the series $\sum a_n$ converges absolutely.
- If $r> 1$ then the series $\sum a_n$ diverges.
- If $r =1$, then the tests are inconclusive

### Raabe’s Test

If the Ratio and Root Test are inclusive, then by checking the following limit, it can help:

$$ r' = \lim_{n\to\infty}\left(n\left( 1-\bigg|\frac{a_{n+1}}{a_n} \Bigg|\right) \right) $$

- If $r' < 1$ then the series $\sum a_n$ converges absolutely.
- If $r'> 1$ then the series $\sum a_n$ diverges.
- If $r' =1$, then the test is inconclusive.