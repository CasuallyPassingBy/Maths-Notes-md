---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Matrix Representation of Linear Transformations]]
_**Theorem:**_ Let $\beta$ and $\beta'$ be two ordered basis for a finite dimensional vector space $V$, let ${Q = [I_V]_{\beta'}^{\beta}}$. Then

- $Q$ is invertible
- for any $v\in V$, $[v]_\beta = Q[v]_{\beta'}$

$Q$ is a _change of basis matrix,_ that changes from the basis $\beta'$ to $\beta$.

_**Theorem:**_ Let $T \in \mathcal{L}(V)$, and $V$ be a finite dimensional vector space, and $\beta$ and $\beta'$ be ordered basis, and $Q$ be a change of basis from $\beta'$ to $\beta$, then:

$$ [T]_{\beta'} = Q^{-1} [T]_\beta Q $$

_**Corollary:**_ Let $A \in \mathcal M_n(\mathbb F)$, and $\gamma$ be an ordered basis of $\mathbb F^n$, then $[L_A]_\gamma = Q^{-1}AQ$, where $Q$ is the change of basis from $\gamma$ to the standard basis.

_**Def:**_ Let $A, B \in \mathcal M_n(\mathbb F)$, then $A$ and $B$ are _similar_ if there’s an invertible matrix $Q$, such that $A = Q^{-1}BQ$.

This makes an equivalence relation on $\mathcal M_n(\mathbb F)$.