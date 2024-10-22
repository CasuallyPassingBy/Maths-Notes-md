---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Space of Linear Transformations]], [[Matrix Representation of Linear Transformations]], [[Multilinear Transformation]], [[Elementary Matrix Operations and Elementary Matrices]], [[Eigenvalues]]

# Determinants on $2\times 2$ matrix

Let $A \in \mathcal M_2 (\Bbb F)$, then:

$$ A=\begin{pmatrix} a & b \\ c & d \end{pmatrix} $$

then $\det(A) = ad - bc$ is called the determinant of $A$, in other cases it can be written as $|A|$.

The function $\det: \cal M_{2}(\Bbb {F)\to F}$, is not a linear functional of $\cal M_n(\Bbb F)$, but it is linear on matrix components, let $u, v, w \in \Bbb F$, as column vectors and $k \in \Bbb F$ then:

$$ \det(u +kv, w) = \det(u, w) + k \det(v, w) $$

and

$$ \det(u, w+kv) = \det(u, w) + k \det(u, v) $$

Thus, $\det: \Bbb{F^2 \times F^2 \to F}$ , is an alternating multilinear function, with the property that $\det I_2 =1$.

Let $A \in \cal{M_2}(\Bbb F)$, $A$ is invertible iff $\det A \ne 0$, then:

$$ A^{-1}=\frac{1}{\det A} \begin{pmatrix} A_{22} & -A_{12} \\ -A_{21} & A_{11} \end{pmatrix} $$
# Determinants on $\def\by#1{#1 \times #1}\by n$ matrix

Let $A \in \cal M_n(\Bbb F)$, then $\tilde A_{ij}$ is the $i, j$ _cofactor matrix $A$, $\tilde A_{ij} \in \cal M_{n-1}(\Bbb F)$,_ is a submatrix of $A$, where we ignored the row $i$ and column $j$.

The determinant is defined recursively, by doing induction on $n$, for $n =1$, then $A$ is a ${1 \times 1}$ matrix, $A = (A_{11})$, then $\det A = A_{11}$. For $n \ge 2$, it is defined as follows:

$$ \det A = \sum_{j = 1}^n (-1) ^{i+j}A_{ij} \det \tilde A_{ij} $$

The scalar $c_{ij}=(-1)^{i+j}\det \tilde A_{ij}$ is called _the cofactor of $A$ in row $i$ and column $j$._ Simplifying the formula for $\det A$ to:

$$ \det A = \sum_{j =1}^n A_{ij} c_{ij} $$

This method is called *Laplace expansion of the determinant*.
The determinant as a function from $\prod_{k \in n} \Bbb F^n$ to $\Bbb F$, is multilinear:

$$ \begin{align*}\det A &= \det ( a_1, \dots, a_{j-1}, r \cdot v + w, a_{j+1}, \dots, a_n ) \\ &= r \cdot \det ( a_1, \dots, v, \dots a_n) + \det(a_1, \dots, w, \dots, a_n ) \end{align*} $$

If $A\in \cal M_n(\Bbb F)$, and the rank of $A$ is less than $n$ , then $\det A = 0$

Let $B \in \cal M_n (\Bbb F)$, where $n \ge 2$. If row or column $i$ is equal to $e_k$ for some $0\le k \le n$, then $\det B = (-1)^{i+k} \det \tilde B_{ik}$.

Let $A\in \cal M_n(\Bbb F)$, and the effects of elementary operations on $A$, and $\det A$:

- Let $B$ be obtained by swapping two rows of $A$, then $\det B = -\det A$
- Let $B$ be obtained by multiplying a row of $A$ by $k$, then $\det B = k \det A$
- Let $B$ be obtained by adding a multiple of a row to another row of $A$, $\det B = \det A$

Using this we can use Gaussian Elimination to calculate the determinant in an which in general is much easier.

For any $A, B \in \cal M_n (\Bbb{F})$, then $\det(AB) = \det (A)\cdot\det(B)$. Then if $A$ is invertible then $\det(A^{-1}) = (\det A)^{-1}$.

For any $A \in \cal M_n(\Bbb F)$, then $\det A = \det A^\top$.

In particular, if $A \in \cal M_n(\Bbb C)$, then $\det \overline A = \overline{\det A}$, where $\overline A$ is the complex conjugate of $A$.

In particular, if $A \in \cal M_n(\Bbb C)$, then $\det A^* = \overline{\det A}$, where $A^*$ is the conjugate transpose of $A$.

The _classical adjoint or adjugate of a square matrix $A$_ is the transpose of the matrix whose $ij$ entry is the $ij$ cofactor of $A$. Let $C$ be the classical adjoint of $A \in \cal M_n(\Bbb F)$, then:

- $\det C = (\det A)^{n-1}$
- $C^\top$ is the classical adjoint of $A^\top$.

#### Cramer's Rule
Let $Ax = b$ be a [[System of Linear Equations|linear system of equations]] on matrix form, where ${x = (x_i)_{i=1}^n}$, if $\det A \ne 0$, then the system has a unique solution, for each $1 \le k \le n$,
$$ x_k = (\det M_k)(\det A)^{-1} $$
where $M_k$ is the $n \times n$ matrix obtained from $A$ by replacing the $k$ column of $A$ with $b$.

## Leibniz Formula for Determinants

Another formula for the determinant, is the _Leibniz Formula of Determinants:_

$$ \det A= \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i =1}^nA_{i, \sigma(i)} = \sum_{\sigma \in S_n} \operatorname{sgn}(\sigma) \prod_{i =1}^nA_{\sigma(i), i} $$

Where $S_n$ is the symmetric group of $n$ elements, and $\operatorname{sgn}(\sigma)$ which returns $\pm 1$ depending if it an even or odd permutation.

Using the Levi-Civita symbol, and the Einstein Summation notation it is

$$ \det A = \varepsilon_{i_1, \dots i_n} A_{1, i_1}\dots A_{n, i_n} $$
# Characterization of the determinant

A function $\delta : \cal{M_n}(\Bbb{ F) \to F}$, $\delta$ $n$_-linear function_, then

$$ \delta(a_1, \dots u +kv, \dots a_n) = \delta(a_1, \dots u, \dots a_n) + k \delta(a_1, \dots v, \dots a_n) $$

An $n$-linear function $\delta: \cal M_n\Bbb{(F) \to F}$, is called _alternating_ iff whenever two columns are identical, then $\delta (A) = 0$

Let $\delta: \cal M_n\Bbb{(F) \to F}$ be an alternating $n$-linear function. If $A, B \in \cal{M_n}(\Bbb{ F) }$ and $B$ is obtained by interchanging two columns of $A$, then ${\delta (B) = -\delta(A)}$.

Let $\delta: \cal M_n\Bbb{(F) \to F}$ be an alternating $n$-linear function. If $A, B \in \cal{M_n}(\Bbb{ F) }$ and $B$ is obtained by adding a multiple of a column of $A$ to another columns, then ${\delta (B) = \delta(A)}$.

Let $\delta: \cal M_n\Bbb{(F) \to F}$ be an alternating $n$-linear function. If $A \in\cal{M_n}(\Bbb{ F) }$, and the $\operatorname{rank} A < n$, then $\delta (A) = 0$

Let $\delta: \cal M_n\Bbb{(F) \to F}$ be an alternating $n$-linear function, and let $E_1, E_2, E_3 \in \cal M_n{\Bbb{(F)}}$ be elementary matrices of type $1$, $2$ and $3$ respectively. Suppose that $E_2$ is obtained by multiplying a column of $I$ by $k$. Then $\delta(E_1)= -\delta(I)$, $\delta(E_2)= k\delta(I)$, and ${\delta(E_3)= \delta(I)}$

Let $\delta: \cal M_n\Bbb{(F) \to F}$ be an alternating $n$-linear function, such that $\delta(I) =1$, then ${\delta = \det}$. Then all alternating $n$-linear functionals are determined uniquely by their value at ${I}$.

Since the determinant is invariant under change of basis, we can define $T \in \mathcal L(V)$ where $V$ is finite dimensional, as follows, choose any ordered basis $\beta$ for $V$.

$$ \det T = \det [T]_\beta $$
## Relationship to eigenvalues

Let $A$ be a linear operator represented by a square matrix with entries in an algebraicly closed field, if $\lambda_1, \dots, \lambda_n$ are the eigenvalues of $A$, then $$\det A = \prod_{i = 1}^n \lambda_i$$