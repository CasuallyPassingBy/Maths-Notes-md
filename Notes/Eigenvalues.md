---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Space of Linear Transformations]], [[Vector Subspaces]]
Def:************ Let $T \in \mathcal{L}(V)$. A subspace $U$ is called _**********invariant**********_ under $T$ if $u\in U$ implies $Tu \in U$.
Def:************ Let $T\in \mathcal{L}(V)$. A number $\lambda\in \mathbb F$ is called an _****eigenvalue****_ of $T$ is there exists $v \in V$ such that $v\ne 0$ and ${Tv = \lambda v}$.

********Th:******** Suppose that $V$ is finite dimensional $T \in \mathcal L(V)$, and $\lambda \in \mathbb F$. then the following are equivalent:

- $\lambda$ is an eigenvalue of $T$
- $T -\lambda I$ is not injective
- $T - \lambda I$ is not surjective
- $T-\lambda I$ is not invertible

********Cor:******** Let $A \in \mathcal M_n(\mathbb F)$. Then the scalar $\lambda$ is an eigenvalue of $A$ iff ${\det (A-\lambda I)= 0}$.

Def: Let $T\in \mathcal{L}(V)$ and $\lambda \in \mathbb F$ is an eigenvalue of $T$. A vector $v\in V$ is called an eigenvector of $T$ corresponding to $\lambda$ if $v\ne0$ and ${Tv = \lambda v}$.

Th: Let $T\in \mathcal{L}(V)$. Suppose that ${\lambda_1,\dots, \lambda_m}$ are distinct eigenvalue of $T$ and ${v_1, \dots, v_m}$ are corresponding eigenvectors. Then ${v_1, \dots , v_m}$ is linearly independent.

Cor: Suppose that $V$ finite dimensional. Then each operator of $V$ has at most ${\dim V}$ distinct eigenvalues.

********Def:******** Suppose $T\in \mathcal{L}(V)$ and $U$ is a subspace of $V$ invariant of $T$:
- The ********************_restriction operator $T|_U \in \mathcal L(U)$_ is defined by:
    
    $$ T|_U(u) = Tu $$
    
    for $u \in U$
- The ********_quotient operator $T/U \in \mathcal L(V/U)$_ is defined by:
    
    $$ (T/U) (v+U) = Tv+U $$
    
    for $v\in V$