---
tags:
  - LinearAlgebra/AffineGeometry
---
Subjects: [[Affine Geometry]]
Links: [[Affine Spaces]], [[Vector Subspaces]]

If $S\subseteq\Bbb R^n$ is a linear subspace and $b\in \Bbb R^n$ the set $b+S$ is called an *affine subspace of $\Bbb R^n$ parallel to $S$*. An affine subspace $b+S$ is a vector subspace iff $b \in S$. Wee see that $b + S = c + \tilde S$ iff $S = \tilde S$ and $b-\tilde b\in S$. Thus we can unambiguously define the *dimension of $b+ S$* to be dimension of $S$. 

Suppose $v_0, \dots, v_k$ are $k+1$ distinct points in $\Bbb R^n$. As long as $n \ge k$, then we know there's a $k$-dimensional affine subspace that contains such $k$-points. We say that the set $\{v_0, \dots, v_k \}$ is *affinely independent*, or is in *general position* if it is not contained in any affine subspace of dimension strictly less than $k$.

**Prop:** For any $k+1$ distinct points $v_0, \dots, v_k \in \Bbb R^n$, the following are equivalent.
- The set $\{v_0, \dots, v_k \}$ is affinely independent.
- the set $\{v_1 - v_0, \dots, v_k - v_0\}$ is linearly independent.
- If $c_0, \dots, c_k$ are real numbers such that $$\sum_{i = 0}^k c_i v_i = 0\quad \text{and} \quad \sum_{i = 0}^k c_i = 0,$$then $c_0 = \dots = c_k = 0$. 

