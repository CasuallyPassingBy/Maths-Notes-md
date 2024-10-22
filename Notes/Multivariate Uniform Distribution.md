---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Continuous Distributions]], [[Uniform Continuous Distribution]]

This is an extension to the uniform continuous distribution.

We have a a rectangle $R = \prod\limits_{i = 1}^n (a_i , b_i)$, then the multivariate uniform distribution function is 
$$
f(x) = \prod_{i = 1}^n(b_i-a_i)^{-1} \Bbb 1_R(x)
$$
Since every $X_i$ and $X_j$ are independent when $i \ne j$, then the variance matrix is a bit boring. 
- $E[X_i] = \frac{a_i+b_i}{2}$
- $\text{Var}(X_i) = \frac{(b_i-a_i)^2}{12}$
- $\text{Cov}(X_i, X_j) = 0$ when $i \ne j$
