---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links:  [[Eigenvectors and Upper Triangular Matrices]], [[Matrix Representation of Linear Transformations]], [[Eigenvalues]], [[Vector Subspaces]]
Def:****** a Suppose $T \in \mathcal L(V)$ and $\lambda \in \mathbb F$. The **eigenspace** of $T$ corresponding to $\lambda$, denoted $E(\lambda, T)$ is defined by:

$$ E(\lambda, T) = N(T-\lambda I) $$

In other words, $E(\lambda, T)$ is the set of all eigenvectors of $T$ corresponding to $\lambda$, along with the $0$ vector.

********Th:******** Suppose $T \in \mathcal L(V)$. Suppose also that $\lambda_1, \dots, \lambda_m$ are distinct eigenvalues of $T$. Then

$$ \sum_{k = 1}^m E(\lambda_k, T) = \bigoplus_{k =1}^m E(\lambda_k, T) $$

and furthermore if $V$ is finite dimensional,

$$ \sum_{k =1}^m \dim E(\lambda_k, T) \le \dim V $$

**Def:** An operator $T \in \mathcal L(V)$ is called *diagonalizable* is the operator has a diagonal matrix with respect to some basis of $V$.

Th:****** Suppose $V$ is finite dimensional and $T \in \mathcal L(V)$. Let $\lambda_1, \dots, \lambda_m$ denote the distinct eigenvalues of $T$. Then the following are equivalent:

- $T$ is diagonalizable
- $V$ has a basis consisting of eigenvectors of $T$
- There exist $1$-dimensional subspaces $U_1, \dots, U_n$ of $V$, each invariant under $T$, such that:
    $$ V = \bigoplus_{k =1}^n U_k $$ 
- The eigenspaces of $T$ being a direct sum of $V$    $$ V = \bigoplus _{k = 1}^m E(\lambda_k, T) $$
- The dimension of eigenspaces adding up to $\dim V$$$ \dim V= \sum_{k = 1}^m \dim E(\lambda_k, T) $$

Cor:* If $T\in \mathcal L(V)$ has $\dim V$ distinct eigenvalues, then $T$ is diagonizable.
The way it is done to diagonalize a matrix is by getting the basis for each $E(\lambda_k , T)$, then by [[Change of Basis Matrix|changing the basis]], then we can write

$$ A = P^{-1}DP $$

with the colums of $P$ being the eigenbasis of $A$.

### Spectral Radius
We can define the spectral radius of a matrix $A$, as $\rho(A)$

$$ \rho(A) = \max_{1\le i\le n} |\lambda_i| $$

where $\lambda_i$ refers to the eigenvalues of $A$