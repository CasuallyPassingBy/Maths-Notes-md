---
tags:
  - GroupTheory
  - DifferentialGeometry
---
Subjects: [[Group Theory]], [[Differential Geometry]]
Links: [[Lie Groups]], [[Matrix Representation of Linear Transformations]], [[Automorphism Group]], [[Trace of Matrix]], [[Special Linear Group]]

If $V$ is a vector space over the field $F$, the general linear group of $V$ is defined as $\text{GL}(V) := \text{Aut}(V)$

Let $F$ being an field, and $\text{M}(n, F)$ be the set of all $n \times n$ matrices over the field $F$. Then $\text{GL}(n, F) := \{ A \in \text{M}(n , F) \mid \det A \neq 0\}$. 

If $V$ has finite dimension $n$, then $\text{GL}(V)$ and $\text{GL}(n ,F)$ are isomorphic. This is because we have the matrix representation of linear transformations. 

# General Linear Group over $\Bbb R$

We have that $\text{GL}(n, \Bbb R)$ has extra properties. In particular we have that $\text{GL}(n, \Bbb R) = \det^{-1}[\Bbb R\setminus\{0\}]$, meaning is an open set of $\Bbb R^{n \times n}$. Then we have that as an open subset of $\Bbb R^{n \times n}$, it is a manifold. It is fairly easy to prove that $\mu$ (matrix multiplication) and $\iota$ (matrix inverse) are $\mathcal C^\infty$. Meaning that $\text{GL}(n, \Bbb R)$ is an Lie group. 

Let $\det: \text{GL}(n, \Bbb R) \to \Bbb R$ be the determinant map. The tangent space $T_I(\text{GL}(n, \Bbb R))$ to $\text{GL}(n, \Bbb R)$ at the identity $I$ is the vector space $\mathcal M_n(\Bbb R)$. 

**Prop:** If $V$ is a finite-dimensional real or complex vector space then there's a Lie group isomorphism $\text{GL}(V) \cong \text{GL}(n, \Bbb R)$ or $\text{GL}(n, \Bbb C)$.  

**Prop:** For any $X \in \mathcal M_n(\Bbb R)$, $d(\det)_I: \mathcal M_n(\Bbb R) \to \Bbb R$, $d(\det)_I (X) = \text{tr}(X)$. 

**Prop:** For any $X\in \mathcal M_n(\Bbb R)$, $d(\det)_A : \mathcal M_n(\Bbb R) \to \Bbb R$ ,$d(det)_A(X) = (\det A)(\text{tr}(X))$. 

**Prop:** $Z(\text{GL}(n, \Bbb R)) = \{\lambda I \mid \lambda \in \Bbb R^\times\} \cong \Bbb R^\times$. 

**Prop:** Let $\phi: \text{GL}(2n+1, \Bbb R) \to \text{SL}(2n+1, \Bbb R) \times \Bbb R^\times$, defined as $\phi(A) = ((\det A)^{-1/(2n+1)} A, \det A)$. Then $\phi$ is a Lie group isomorphism. Meaning that $\text{GL}(2n+1, \Bbb R) \cong \text{SL}(2n+1, \Bbb R) \times \Bbb R^\times$.

**Prop:** $Z(\text{GL}(2n, \Bbb R)) \not\cong  Z(\text{SL}(2n, \Bbb R)\times \Bbb R^\times)$. Meaning that $\text{GL}(2n, \Bbb R)) \not\cong  \text{SL}(2n, \Bbb R)\times \Bbb R^\times$.