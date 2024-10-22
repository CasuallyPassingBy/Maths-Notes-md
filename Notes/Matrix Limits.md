---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Matrix Representation of Linear Transformations]], [[Eigenspaces and Diagonal Matrices]], [[Jordan Normal Form#Jordan Block Powers and Limits|Jordan Block Powers and Limits]]
**Def:** Let $(A_n)$ be a sequence of $n\times p$ matrices having complex entries. The sequence $(A_n)$ is said to _**converge**_ if there’s an $n\times p$ matrix $L$ called the _****limit****_ of the sequence that

$$ \lim_{n\to\infty} (A_n)_{ij} = L_{ij} $$

for all $1\le i\le n$ and $1\le j \le p$. To denote that $L$ is the limit of the sequence we write

$$ \lim_{n\to\infty} A_n = L $$

Let $(A_n)$ be a sequence of $n\times p$ matrices with complex entries that converge to the matrix $L$. Then $(A^\top_n)$ converges to $L^\top$. Then the transpose operation is continouos.

Let $(A_n)$ be a sequence of $n\times p$ matrices with complex entries that converge to the matrix $L$. Then for any $P \in \cal M_{r\times n}(\mathbb C)$ and $Q \in \cal M_{p\times s}(\mathbb C)$,

$$ \lim_{n\to \infty} PA_n = PL \text{ and } \lim_{n\to\infty}A_n Q=LQ $$

****Cor:**** Let $A \in \cal M_n(\mathbb C)$ be such that $\lim_{n\to \infty} A^n = L$. Then for any invertible matrix $Q \in \cal M_n(\mathbb C)$.

$$ \lim_{n\to\infty} (QAQ^{-1})^n = QLQ^{-1} $$

$(*)$ Let $A$ be a square matrix with complex entries. Then $\lim_{n\to \infty} A^n$ exists iff

- Every eigenvalue of $A$ is of the form $\lambda =1$ or $|\lambda | <1$
- If $1$ is an eigenvalue of $A$, then the dimension of the eigenspace corresponding to $1$ equals the multiplicity of $1$ as an eigenvalue of $A$.

This theorem depends on the theory of Jordan canonical forms, or in the use of Schur’s Theorem

A weaker form of the theorem:

Let $A \in \cal M_n(\mathbb C)$ such that:

- Every eigenvalue of $A$ is of the form $\lambda =1$ or $|\lambda | <1$
- $A$ is diagonalizable

Then $\lim_{n\to \infty} A^n$ exists

