---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Eigenspaces and Diagonal Matrices]], [[Isometries in Vector Spaces]]
## Positive Semidefinite Linear Operators

**Def:** Let $T \in \mathcal L(V)$ is called _********positive semidefinite********_ if $T$ is self-adjoint and for all $v \in V$,

$$ \langle Tv, v\rangle \ge 0 $$

**Def:** An operator $R$ is called a **square root** of an operator $T$ if $R^2 = T$.

********Th:******** Let $T \in \mathcal L(V)$. Then the following are equivalent:
- $T$ is positive
- $T$ is self-adjoint and all the eigenvalues of $T$ are nonnegative
- $T$ has a positive square root
- $T$ has a self-adjoint square root
- there exists an operator $R \in \mathcal L(V)$ such that $T = R^* R$.

********Th:******** Let $V$ be a finite dimensional inner product space, and $T \in \mathcal L(V)$. If $T$ is a positive semidefinite operator, then has a unique positive semidefinite square root. Thus we can use the following notation to refer to the unique positive semidefinite square root of $T$

$$ \sqrt T $$

## Positive Definite Matrix

**Def:** A symmetric $n \times n$ matrix $A$ is **positive semidefinite** if the corresponding quadratic form $Q(x) = x^\top Ax$ is positive definite. Analogous definition apply for **negative definite** and *********indefinite**********.

********Th:******** If $A$ is symmetric positive definite matrix, then $A$ is nonsingular and $\det A>0$.

********Th:******** A symmetric matrix $A$ is positive definite iff the leading principal submatrices satisfy

$$ \det A_1 >0, \; \det A_2>0, \; \dots, \; \det A_n >0 $$

**Th:** Suppose that the leading leading submatrices of a symmetric matrix $A$ satisfy having a strictly positive determinant. Then $A$ can be reduced to row echelon form without using row interchanges, and the pivot elements will all be positive.

Then $A$ has an $LDU$ factorization.

********Th:******** A symmetric matrix $A$ that satisfies that the leading principal submatrices having positive determinant, can be uniquely factored as ${A = LDL^\top}$, where $L$ is lower triangular with $1$’s on the diagonal, and $D$ is a diagonal matrix with all positive diagonal entries.

## Polar Decomposition of Linear Transformations
Let $V$be a finite dimensional inner product space and $T \in \mathcal L(V)$. Then there exists an isometry $S \in \mathcal L(V)$ such that

$$ T = S\sqrt{T^*T} $$

Similarly, there exists an isometry $S \in \mathcal L(V)$, such that

$$ T = \sqrt{TT^*}S $$

## Polar Decomposition of Matrices
For any square matrix $A$, there exists a unitary matrix $W$ and a positive semidefinite matrix $P$ such that

$$ A = WP $$

If $A$ is invertible, then the representation is unique. Similarly there exist a unitary matrix $W$ and a positive semidefinite matrix $P$ such that

$$ A =PW $$

## Singular Value Theorem for Linear Transformations

Let $V$ and $W$ be finite dimensional inner product spaces, and let ${T \in \mathcal L(V, W)}$ be a linear transformation of rank $r$. Then there exist orthonormal bases $\{v_i\}_{i =1}^n$ for $V$ and $\{u_j\}_{j = 1}^m$ for $W$ and positive scalars $\sigma_1 \ge \sigma_2 \cdots \ge \sigma_r$ such that:

$$ Tv_i= \begin{cases} \sigma_i u_i & \text{if } 1\le i \le r \\ 0 & \text{if } i > r \end{cases} $$

Conversely, suppose that the preceding conditions are satisfied. Then for ${1 \le i \le n}$, $v_i$ is an eigenvector of $T^*T$ with corresponding eigenvalue $\sigma_i^2$ if $1 \le i \le r$ and $0$ if $i >r$. Therefore the scalars $\sigma_1, \sigma_2, \dots, \sigma_r$ are uniquely determined by $T$.

**********Def:********** The unique scalars $\sigma_1, \sigma_2,\dots \sigma_r$ in the theorem above are called the **********singular values********** of $T$. If $r$ is less than both $m$ and $n$, then the term singular value is extended to include $\sigma_{r+1} = \cdots = \sigma_{k} = 0$, where $k$ is the minimum of $m$ and $n$.

We can think of the singular values of $T$ as the eigenvalues of $\sqrt{T^*T}$ , with each eigenvalue $\lambda$ repeated $\dim E(\lambda, \sqrt{T^*T})$.

In the special case that $V =W$, we get that, there exists $\{v_i\}_{i = 1}^n$ and $\{u_i\}_{i = i }^n$ orthonormal bases of $V$, such that for all $v \in V$

$$ Tv = \sum_{k = 1}^n \sigma_k\langle v, v_i \rangle u_k $$

## Singular Value Theorem for Matrices

Let $A$ be an $m\times n$ matrix of rank $R$ with the positive singular values ${\sigma_1 \ge \sigma_2 \cdots \ge \sigma_r}$, and let $\Sigma$ be the $m \times n$ matrix defined by

$$ \Sigma_{ij} = \begin{cases} \sigma_{i} & \text{if } i = j \le r\\ 0 & \text{otherwise} \end{cases} $$

The there exists an $m \times m$ matrix $U$ and an $n\times n$ unitary matrix $V$ such that

$$ A = U\Sigma V^* $$

This is the ************singular value decomposition************ of $A$.