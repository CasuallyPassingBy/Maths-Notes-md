---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Bases and Dimension]], [[Dual Spaces]], [[Eigenvectors and Upper Triangular Matrices]], [[Inner Products and Norms]]
**********Def:********** A list of vectors is called _**********orthonormal**********_ if each vector in the list has norm $1$ and is orthogonal to all the other vectors in the list.

Let $V$ be an inner product space and $v_1, \dots, v_m$ be an orthogonal subset of $V$ consisting of nonzero vectors. If $y \in \operatorname{span}(v_1, \dots, v_m)$ then

$$ y = \sum_{k =1}^m \frac{\langle y, v_k\rangle}{\|v_k\|^2}v_k $$

If in addition, $v_1, \dots, v_m$ are orthonormal then

$$ y = \sum_{k = 1}^m \langle y, v_k\rangle v_k $$

In other words, a list $e_1, \dots, e_m$ of vectors in $V$ is orthonormal if ${\langle e_i, e_j\rangle = \delta_{i, j}}$.

Every orthonormal list of vectors us linearly independent.

****Parseval’s Identity****

If $e_1, \dots, e_m$ is an orthonormal list of vectors in $V$, then

$$ \left\|\sum_{k = 1}^m a_k e_k \right\|^2 = \sum_{k = 1}^m |a_k|^2 $$

let $u,v \in V$, then

$$ \langle u, v\rangle = \sum_{k = 1}^m \langle u, e_i \rangle \overline{\langle v, e_i \rangle} $$

**********************************Bessel’s Inequality**********************************

If $e_1, \dots, e_m$ is an orthonormal list of vectors in $V$, and $v \in V$then

$$ \sum_{k = 1}^m |\langle v, e_k\rangle| \le \|v\|^2 $$

********Def:******** An **orthonormal basis** of $V$ is an orthonormal list of vectors in $V$ that is also a basis of $V$.

Every orthonormal list of vectors in $V$ with length $\dim V$ is an orthonormal basis of $V$.

Suppose $e_1, \dots, e_n$ is an orthonormal basis of $V$ and $v \in V$. Then

$$ v = \sum_{k = 1}^n \langle v, e_k\rangle e_k $$

and

$$ \|v\|^2 = \sum_{k = 1}^n |\langle v, e_k\rangle|^2 $$

Let $V$ an inner product space, then we can define the projection operator as

$$ \operatorname{proj}_u (v) := \frac{\langle u, v\rangle}{\langle u, u\rangle} u $$

### Gram-Schmidt Process

Let $V$ be an inner product space and $S = \{w_1, \dots, w_m\}$ be a linearly independent subsets of $V$. Define $S' = \{v_1, \dots, v_m\}$ where: $v_1 = w_1$

$$ v_k = w_k -\sum_{j=1}^{k-1} \operatorname{proj}_{v_j}(w_k) $$

the $S'$ is an orthogonal set of nonzero vectors such that ${\operatorname{span}S' = \operatorname{span} S}$. This process is called Gram-Schmidt ****orthogonalization****. While if the we normalize the vector $v_1, \dots, v_m$, into $e_1, \dots, e_m$, then the procedure to get $e_1, \dots, e_m$ is called the Gram-Schmidt _orthonormalization_.

Denote by $\operatorname{GS}(w_1, \dots, w_k)$ the result of applying the Gram-Schmidt process to a collection of vectors $w_1, \dots, w_m$. This yields a map: ${\operatorname{GS}:V^k \to V^k}$

- It is continuous
- Is orientation preserving in the sense that ${\operatorname{or}(w_1, \dots, w_k) = \operatorname{or(GS}(w_1, \dots, w_k)}$
- It commutes with orthogonal maps: If $g\in \mathcal L (V)$ be an orthogonal map, then

$$ \operatorname{GS}(g(w_1), \dots, g(w_k)) = (g(\operatorname{GS}(w_1, \dots, w_k)_1), \dots, g(\operatorname{GS}(w_1, \dots, w_k)_k)) $$

Since the Gram-Schmidt process works through induction this also applies to a linearly independent countably infinite sequence ${\{w_i\}_{i \in \Bbb N}}$. The resulting orthogonal/orthonormal sequence ${\{v_i\}_{i\in \Bbb N}}$ such that for any $n\in \Bbb N$: the span of $w_1, \dots w_n$ is the same that of $v_1, \dots, v_n$.

There’s a variant that uses transfinite recursion applied to a infinite sequence of vectors.

**********Cor:********** Every finite-dimensional inner product space has an orthonormal basis.

******Cor:****** Then every orthonormal list of vectors in $V$ can be extended to an orthonormal basis if $V$.

**********Cor:********** Suppose $T \in \mathcal L(V)$. If $T$ has an upper triangleular matrix with respect to some basis of $V$, then $T$ has an upper triangleular matrix with respect to some orthonormal basis of $V$.

### ********************************Schur’s Theorem Basic Form********************************
Suppose $V$ is a finite dimensional complex vector space and $T \in \mathcal L(V)$. Then $T$ has an upper triangleular matrix with respect to some orthonormal basis of $V$.

### Schur’s Theorem General Form

Let $V$ be s finite dimensional inner product space over $\mathbb F$, and $T \in \mathcal L(V)$. If the characteristic polynomial of $T$, $\chi_T$, splits over $\mathbb F$. Then there exists an orthonormal basis $\gamma$ for $V$ such that the matrix $[T]_\gamma$ is upper triangleular.

### Riesz Representation Theorem
Suppose $V$ is finite dimensional and $\phi \in V'$. Then there’s a unique vector $u \in V$ such that

$$ \phi(v) = \langle v, u\rangle = \langle u| v\rangle $$

for all $v \in V$. Also $u$ is of the form

$$ u = \sum_{k = 1}^n \overline{\phi(e_k)}e_k $$

where $e_1, \dots e_n$ is an orthonormal basis of $V$.