---
tags:
  - LinearAlgebra/AffineGeometry
  - GroupTheory
---
Subjects: [[Affine Geometry]], [[Group Theory]]
Links: [[Affine Maps]], [[Representations of Groups]]

# Representation

As we have seen above, an affine map is the composition of two functions: a translation and a linear map. Ordinary vector algebra uses matrix multiplication to represent linear maps, and vector addition to represent translations. Formally, in the finite-dimensional case, if the linear map is represented as a multiplication by an invertible matrix $A$ and translation of a vector $b$, an affine map $f$ acting on a vector $x$ can be represented as $$f(x) = Ax +b .$$
### Augmented Matrix

Using an *augmented matrix* and an augmented vector, it is possible to represent the translation and linear map using a single matrix multiplication. The technique requieres that all vector be augmented with a $1$ at the end. If $A$ is a matrix, $$\begin{pmatrix} y \\ 1\end{pmatrix} = \begin{pmatrix} A & b \\ 0 & 1\end{pmatrix}
\begin{pmatrix} x \\ 1\end{pmatrix}$$is equivalent to the following $y = Ax +b$. 

The above-mentioned augmented matrix is called an *affine transformation matrix*.
This means we can identify the affine subspace $\{(x^1, \dots, x^{n+1}) \in F^{n+1} \mid x^{n+1} = 1\}$ of $F^{n+1}$, as the one being acted by this augmented matrix. 

If we want to compute the inverse of the matrix $\begin{pmatrix} A & b \\ 0 & 1\end{pmatrix}$, we get that is of the form $$\begin{pmatrix} A^{-1} & -A^{-1}b \\ 0 & 1\end{pmatrix}$$

With this in mind we can describe the affine group of $X$ concretely as the [[Semidirect Product of Groups|semidirect product]] of $V$ by $\text{GL}(V)$, the [[general linear group]] of $V$, where $V$ is the underlying vector space of $X$: $$\text{Aff}(X)  = V \rtimes \operatorname{GL}(V).$$The action of $\text{GL}(V)$ on $V$ is the natural one, so this defined a semidirect product.

**Def:** The similarity transformations form a subgroup where $A$ is a nonzero scalar times an [[Orthogonal Group|orthogonal matrix]]. Additionally, If the affine transformation has a matrix $A$ with determinant $\pm 1$, then we call it an *equireal mapping*. Such transformations form a subsgroup called the *equi-affine group*. Lastly, a transformation that is both equi-affine and a similarity is an isometry. The subgroup of all isometries is called the [[Euclidean group]], and it is denoted as $\text E(n)$. 

Naturally, each of these subgroups has a subgroup of *orientation preserving* or *positive* affine transformations: those where the determinant is positive. We get that $$\text{Aff}^+(X)  = V \rtimes \operatorname{GL}^+(V), \quad \text{E}(n) = \Bbb R^n \rtimes \text O(n), \quad \text{SE}(n) = \Bbb R^n \rtimes \text{SO}(n).$$