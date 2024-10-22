---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Eigenvalues]], [[Matrix Representation of Linear Transformations]], [[Polynomial Ring]]

Def: Let $T\in \mathcal L(V)$ and $m \in \Bbb N^+$, then

- $T^m$ is defined inductively as $T^0 = I$ and $T^{m+1}=T\circ T^m$
- Similarly $T^{-(m+1)}= T^{-1} \circ T^{-m}$

Def:************ Let $T\in \mathcal L(V)$ and $p \in \mathcal P(\mathbb F)$ is a polynomial given by:

$$ p(z) = \sum_{k=0}^m a_k z^k $$

for $z\in \mathbb F$. Then $p(T)$ is the operator defined by:

$$ p(T) = \sum_{k =0}^m a_k T^k $$

Def: If $p,q\in\mathcal P(\mathbb F)$ , then $pq \in \cal P(\mathbb F)$ is the polynomial defined by
$$ (pq)(z) = p(z)q(z) $$
********Th:******** Suppose $p,q\in \cal P(\mathbb F)$ and $T\in \mathcal L(V)$. Then
- $(pq)(T) = p(T) q(T)$
- $p(T) q(T) = q(T) p(T)$

**Th:** Every operator on a finite dimensional, nonzero, complex vector space has an eigenvalue.

********Th:******** Suppose $V$a finite dimensional complex vector space and $T\in \mathcal L(V)$. Then $T$ has an upper-triangular matrix with respect to some basis of $V$.

**Th:*** Suppose $T \in \mathcal L(V)$ has an upper-triangular matrix with respect to some basis of $V$. Then $T$ is invertible iff all the entries on the diagonal of that upper-triangular matrix are nonzero.

********Th:******** Suppose $T \in \mathcal L(V)$ and $v$ is an eigenvector of $T$ with eigenvalue $\lambda$. If ${p\in \mathcal P(\mathbb F)}$, then $p(T)v = p(\lambda)v$.

********Th:******** Suppose $S, T \in \mathcal L(V)$ and $S$ is invertible. If ${p\in \mathcal P(\mathbb F)}$, then ${p(STS^{-1}) = Sp(T)S^{-1}}$.