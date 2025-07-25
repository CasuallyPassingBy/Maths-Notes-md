---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Bilinear Forms]]

**Def:** Let $V$ be a vector space over a field $K$ not of characteristic $2$. A function $K: V \to K$ is called a *quadratic form on $V$* if there exists a symmetric bilinear form $H\in \mathcal B(V)$ such that
$$ Q(x)= H(x,x) $$

********Th:******** Let $V$ be a vector space over a field $K$ not of characteristic $2$, and let $H$ be a symmetric bilinear from on $V$. If $K(x) = H(x,x)$ is the quadratic form associated with $H$, then for all $x, y \in V$, $$ H(x,y) = \frac{1}{2}[Q(x+y) -Q(x)-q(y) ]. $$
We can give an alternative definition to a quadratic form. A *quadratic form* over a field $K$ is a map $Q: V\to K$ from a finite dimensional $K$-vector space to $K$ such that $Q(av) = a^2 Q(v)$ for all $a\in K$, $v\in V$ and the function $B(u, v) := Q(u+v) - Q(u) - Q(v)$ is a bilinear form. More concretely, an $n$-ary *quadratic form* ove a field $K$ is a homogeneous polynomial of degree $2$ in $n$ variables with coefficients in $K$: $$Q(x_1, \dots, x_n) = \sum_{i, j = 1}^n a_{ij} x_ix_j\qquad a_{ij}\in K$$This formula can be written using matrices: let $x$ be a column vector with components $x_1, \dots, x_n$ and $A = [a_{ij}]$ be the $n\times n$ matrix over $K$. Then $$Q(x) = x^\top A x.$$
**Def:** Two $n$-ary quadratic forms $\phi$ and $\psi$ over $K$ are *equivalent* if there's a nonsingular linear transformation $C \in \text{GL}(V)$ such that $\psi(x) = \phi(Cx)$. 

**Def:** The pair $(V, Q)$ consisting of a finite dimensional $K$-vector space $V$ and a quadratic form $Q$ is called a *quadratic space*, and $H$ is the associated symmetric bilinear form.

The notion of a quadratic space is a coordinate-free version of the notion of a quadratic form. 

**Def:** Two $n$-dimensional quadratic spaces $(V, Q)$ and $(W, P)$ are *isometric* if there's an invertible linear transformation $T: V \to W$ such that $Q(v) = P(Tv)$ for all $v\in V$. The linear functions that satisfy this condition are called *isometries*.

The isometry classes of $n$-dimensional quadratic spaces over $K$ correspond to equivalence classes of $n$-ary quadratic forms over $K$.

**Th:** Let $(V, Q)$ be a quadratic space over the field $K$. If $K$ has characteristic not equal to $2,$ is equivalent to a diagonal form $$Q(x) = \sum_{i = 1}^n a_i x_i^2.$$Such a diagonal form is often denoted by $\langle a_1, \dots, a_n\rangle$. Classification of all quadratic forms, and thus quadratic spaces, up to equivalence can thus be reduced to the case of diagonal forms. ^c01a68

********Th:******** Let $V$ be a finite dimensional real inner product space, and let $H$ be a symmetric bilinear form on $V$. Then there exists an orthonormal basis $\beta$ for $V$ such that $\psi_\beta(H)$ is a diagonal matrix.

**Cor:** Let $K$ be a quadratic form on a finite dimensional real inner product space $V$. There exists an orthonormal basis $\beta = \{v_i\}_{i = 1}^n$ for $V$ and scalars $\lambda_1, \lambda_2, \dots \lambda_n$ such that $x \in V$ and $$ x = \sum_{k =1}^n s_k v_k $$Then$$K(x) = \sum_{k =1}^n\lambda_k s_k ^2$$
### Principal Axes Theorem

Let $A \in \mathcal M_n(\Bbb R)$ be a symmetric matrix, then there exists an orthogonal matrix $P$ such that $y = P^\top x$ and changes the quadratic form $x^\top Ax$ into the quadratic form $y^\top Dy$, where $D$ is diagonal, that has non cross-terms.

**Def:** Let $K$ be a quadratic form on $\Bbb R^n$
- $K$ is **positive definite** if $K(x)>0$ for all $x \in \Bbb R^n$, and $K$ is **positive semidefinite** if $K(x) \ge 0$ for all $x \in \Bbb R^n$.
- $K$ is **negative definite** if $K(x)<0$ for all $x \in \Bbb R^n$, and $K$ is **negative semidefinite** if $K(x) \le 0$ for all $x \in \Bbb R^n$.
- $K$ is **indefinite** if $K(x)$ is positive for some $x \in \Bbb R$ and negative for others.

********Th:******** Let $A$ be an $n \times n$ symmetric matrix, and suppose that ${K(x) = x^\top Ax}$. Then
- $K$ is positive definite exactly when $A$ has only positive eigenvalues
- $K$ is negative definite exactly when $A$ has only negative eigenvalues
- $K$ is indefinite exactly when $A$ has positive and negative eigenvalues

********Th:******** Let $K$ be a quadratic form on $\Bbb R^n$ $$ K(x) = \sum_{k =1}^n a_k x^2_k $$that has no cross-product terms. Let $a_i$ and $a_j$ be the maximum and minimum respectively of the coefficients $a_1, a_2, \dots, a_n$. Then subject to the constraint $\|x\|=1$,
- The maximum value of $K(x)$ is $a_i$, attained at $x = e_i$
- The minimum value of $K(x)$ is $a_j$, attained at $x = e_j$

**Cor:** Let $K(x) =x^\top Ax$ where $A$ is a symmetric $n\times n$ matrix. Suppose that $A$ has eigenvalues $\lambda_1 \le \lambda_2\le \cdots \le \lambda_n$, and let ${u_1, \dots, u_n}$ be the associated eigenvectors. The subject to the constraint $\|x\| = 1$, we have
- The maximum value of $K(x)$ is $\lambda_n$, attained at $x = u_n$
- The minimum value of $K(x)$ is $\lambda_1$, attained at $x = u_1$

**Cor:** Let $K(x) =x^\top Ax$ where $A$ is a symmetric $n\times n$ matrix. Suppose that $A$ has eigenvalues $\lambda_1 \le \lambda_2\le \cdots \le \lambda_n$, and let ${u_1, \dots, u_n}$ be the associated eigenvectors. The subject to the constraint $\|x\| = 1$ and $x \cdot u_n =0$, we have
- The maximum value of $K(x)$ is $\lambda_{n-1}$, attained at $x = u_{n-1}$
- The minimum value of $K(x)$ is $\lambda_1$, attained at $x = u_1$

**Th:** Let $A$ be a positive definite matrix, then $$p(x) = x^\top A x-2x^\top f + c$$reaches its minimum at $x_0 = A^{-1}f$ and additionally its minimum value is $$p(x_0) = c - x_0^\top A x_0$$