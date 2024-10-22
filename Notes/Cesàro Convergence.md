---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Properties of Limits of Sequences in R]], [[Abel's Summability]], [[Series in R]]

Let the sequence $(x_n)$ be convergent let’s define a new sequence $(y_n)$ as follows:

$$ y_n = \frac{1}{n}\sum_{k = 1}^{n} x_k $$

then $(y_n)$ converges to the same limit as $(x_n)$

It is possible to find an $(x_n)$ that doesn’t not converge, but the corresponding $(y_n)$ converging.

This kind of limit, is also known as Cesàro mean, Cesàro limit, or Cesàro summation. This kind of summation is used to give a possible limit to divergent series, more than to divergent sequences. 

### Cesàro 1-summable
Let

$$ S_n = \sum_{k = 1}^n a_k \quad \sigma_n = \frac{1}{n}\sum_{k = 1}^n S_k $$

Thus $\sigma_n$ is the arithmetic mean of the first $n$ partial sums of the series. Note the formula

$$ \sigma_n = \sum_{k = 1}^n \left(1- \frac{k-1}{n}\right) a_k $$

The series $\sum_{k = 1}^\infty a_k$ is called Cesàro 1-summable or $(C, 1)$ _summable_ to $A$ if ${\lim \sigma_n = A}$. In this case, write

$$ \sum_{k = 1}^\infty a_k = A \quad (C, 1) $$

Some properties of $(C, 1)$ summability follow.

- If $\sum_{k = 1}^\infty a_k = A \quad (C, 1)$, and $\sum_{k = 1}^\infty b_k = B \quad (C, 1)$, then ${\sum_{k = 1}^\infty (\alpha a_k +\beta b_k) = \alpha A + \beta B \quad (C, 1)}$
- If $\sum_{k = 1}^\infty a_k = A \quad (C, 1)$, then $\sum_{k = 1}^\infty a_{k+1} = A-a_1 \quad (C, 1)$
- If $\sum_{k = 1}^\infty a_k = A$ in the usual sense, then $\sum_{k = 1}^\infty a_k = A \quad (C, 1)$

We can define the $(C, 2)$ sum of the given series $\lim (\frac{1}{n} \sum_{k = 1}^n \sigma_k)$ if the limit exists.

We can generalise arbitrary values of $r \in \Bbb N$, by obtaining successively more powerful methods of summation.

Th: $\sum a_k = A \quad (C, 1)$ then $\sum a_k= A \quad \text{(Abel)}$

Th: $\sum a_k = A \quad (C, 1)$ and if $a_k = O(1/n)$, then $\sum a_k$ converges to $A$ in the usual sense.

We have that for series $$\text{summable} \implies \text{Cesàro summable} \implies \text{Abel summable}$$