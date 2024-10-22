---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Discrete Distributions]], [[Binomial Distribution]], [[Discrete Distributions]]

This actually comes from [[Multinomial Theorem|multinomial theorem]]

We have an experiment that can have $k$ different outcomes, and it is repeated $n$ times, where each outcome has a probability $p_i$ for $i =1, \dots, k$. Then the probability mass function is of the form
$$
f(x_1, \dots, x_k; n, p_1, \dots, p_k) = 
\begin{dcases}
{n \choose x_1\cdots x_k}\prod_{i = 1}^k p_i ^{x_i}& \text{when } \sum_
{i = 1}^k x_i = n\\
0 &\text{otherwise}
\end{dcases}
$$
We use the multinomial coefficient, and maybe we can simplify the notation a bit to
$$
f(x; n,k, p) = 
\begin{dcases}
{n \choose x}p^x& \text{when } |x| = n\\
0 &\text{otherwise}
\end{dcases}
$$
We are using actually the [[Multi-index notation]] for $x$ and $p$ is a probability vector.

- $E[X_i] = np_i$
- $\text{Var}[X_i] = np_i(1-p_i)$
- $\text{Cov}(X_i, X_j) = -n p_i p_j$