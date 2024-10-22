---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Vector Spaces]]

Let $\{(V_i, +, \cdot)\}_{i=0}^n$ be a collection of vector spaces over the field $\mathbb F$. Then the _product of vector spaces is:_

$$ \prod_{i=0}^nV_i=\left\{(v_i)_{i=0}^n\mid \forall 0\le i \le n [v_i\in V_i]\right\} $$

with the following operations, let $(v_i)_{i=0}^n, (w_i)_{i=0}^n \in \prod V_i$, and $\lambda \in \mathbb F$:

$$ (v_i)_{i=0}^n +(w_i)_{i=0}^n = (v_i + w_i)_{i= 0}^n \newline \newline \lambda(v_i)_{i=0}^n = (\lambda v_i)_{i=0}^n $$

Then $\prod V_i$ is a vector space over the field $\mathbb F$.

Given that every $V_i$ is finite dimensional vector spaces, then:

$$ \dim\left(\prod_{i=0}^n V_i\right) = \sum_{i=0}^n \dim(V_i) $$

Let $\{U_i\}_{i=0}^n$ be a collection of subspaces of $V$. Defining a linear map $\Gamma: \prod U_i \to \sum U_i$, such that:

$$ \Gamma(u_i)_{i=0}^n = \sum_{i=0}^n u_i $$

$\Gamma$ is injective iff $\sum U_i$ is a direct sum.