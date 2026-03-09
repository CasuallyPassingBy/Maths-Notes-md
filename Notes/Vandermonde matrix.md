---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Determinants]], [[Asymptotic Notation]] 

A *Vandermonde matrix* is a matrix with terms of an geometric progression in each row: an $(m+1)\times (n+1)$ matrix $$V = V(x_0, \dots, x_m) = \begin{pmatrix} 1 & x_0 & x_0^2 & \cdots & x_0^n  \\ 1 & x_1 & x_1^2 & \cdots & x_1^n \\ \vdots  & \vdots & \vdots & \ddots & \vdots \\ 1 & x_m & x_m^2 & \cdots & x_m^n \end{pmatrix}$$with entries $V_{ij} := x_i ^j$, for all zero-based indices $i$ and $j$. 

One of the most important properties of the Vandermonde matrix is that it has relatively simple determinant when $n = m$: $$\det V = \prod_{1 \le i < j \le n} (x_i -x_j)$$which is non-zero iff all $x_i$ are distinct. 

This property is important enough that when we analyse polynomials of the form $p(x) = (x- x_0)\cdots (x-x_n)$ we can calculate its [[Galois Groups of Polynomials|discriminant]] as the square of the determinant. The square root of the determinant is very important and can be very telling on how low degree polynomials can generate different field extensions. 

A lesser know property of the Vandermonde Matrix is that $$V^\top V = \begin{pmatrix}p_0 & p_1 & p_2 & \cdots & p_{n-1} \\ p_1 & p_2 & p_3& \cdots & p_{n} \\ \vdots  & \vdots & \vdots & \ddots & \vdots \\ p_{n-1}  & p_n & p_{n+1} & \cdots & p_{2n-2} \end{pmatrix},$$or $[V^\top V]_{ij} = p_{i+j}$, where $i$ and $j$ are zero-indexed and where $$p_{k} := \sum_{i = 0}^n x_i^k.$$We see trivially that its determinant is $\det(V)^2$, using [[Symmetric Polynomials|Newton's identities]] gives a way to calculate using exclusively the fundamental symmetric polynomials. In turn, we have a way to calculate the discriminant of a polynomial using its coefficients, but I don't think it is particularly fast.

## Applications

The polynomial interpolation problem is to find a polynomial $p(x) = a_0 + a_1 x + \dots + a_n x^n$ which satisfies $p(x_0) = y_0, \dots p(x_m) = y_m$ for some given data points $(x_0, y_0), \dots, (x_m, y_m)$. We can reformulate this problem in terms of linear algebra by means of the Vandermonde matrix. $V$ computes the values of $p(x)$ at the points $x_0,\dots, x_m$ via matrix multiplication $Va = y$, where $a$ the vector of the coefficients, and $y$ is the vector of the desired outputs. 

If $n  = m$, and $x_0,\dots, x_m$, then $V$ is an invertible matrix. Then, given $V$ and $y$ we can find the required $p(x)$ by just $a = V^{-1}y$. 

This means that the interpolation problem has a solution. This result is called the *unisolvence theorem*, and is a special case of the [[Chinese Remainder Theorem for Rings]]. 

Let us note that the [[Discrete Fourier Transform]] is defined by a specific Vandermonde matrix, the DFT matrix, where $x_i$ are chosen to be the $n$th roots of unity. The [[Fast Fourier Transform]] computes the product of this matrix with a vector in $O(n \ln^2 n)$ time. 

The Vandermonde determinant is used in the representation theory of the symmetric group. 

The equation $Va = y$ can mean in statistic that the Vandermonde matrix is the design matrix of [[polynomial regression]]. 

