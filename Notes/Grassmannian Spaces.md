---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Real Projective Space]], [[The Rank of a Matrix and Matrix Inverses]], [[Continuous Actions of Groups]], [[Multi-index notation]]

**Def:** The Grassmannian $G(k, n)$ is the set of all $k$-planes through the origin of $\Bbb R^n$. Such a $k$-plane is a linear subspace of dimension $k$ of $\Bbb R^n$ and has a basis consisting of $k$ linearly independent vectors $a_1, \dots, a_k \in \Bbb R^n$. It is therefore completely specified by an $n\times k$ matrix $A = [a_1, \dots, a_k]$ of rank $k$. 

Two bases $a_1, \dots, a_k$ and $b_1, \dots, b_k$ determine the same $k$-plane if there is a change of basis matrix $G \in \text{GL}(k, \Bbb R)$ such that: $B = AG$, where$A = [a_1, \dots, a_k]$ and $B = [b_1, \dots, b_k]$. 

**Def:** Let $F(k, n)$ be the set of all $n\times k$ matrices of rank $k$, with the topology as subspace of $\Bbb R^{n\times k}$, and $\sim$ the equivalence relation: $$A \sim B \iff \exists G\in \text{GL}(k, \Bbb R) [ B= AG]$$In the notation. From this [[The Rank of a Matrix and Matrix Inverses#^82654b|corollary]], we get that $F(k, n)$ is an open subset of $\Bbb R^{n\times k}$. There is a bijection between $G(k, n)$ and the quotient space $F(k, n)/ \text{GL}(k, \Bbb R)$. We give the Grassmannian $G(k, n)$ the quotient topology $F(k, n)/ \text{GL}(k, \Bbb R)$. 

**Obs:** Since $\text{GL}(k, \Bbb R)$ is a topological group and has a continuous action on $F(k, n)$, then the equivalence relation is open. Then $G(k, n)$ is second countable. 

**Prop:** Mimicking the the proof the real projective space, we have that $G(k, n)$ is $T_2$. 

Let $I$ be a strictly ascending multi-index $1 \le i_1 < \dots< i_k \le n$, and for $A\in F(k ,n)$, let $A_I$ be the $k\times k$ submatrix of $A$ consisting of the $i_1$th, $\dots$, $i_k$th rows of $A$. We define $$V_I := \{A \in F(k, n) \mid \det A_I \neq 0\}$$
We get that $\{V_I \mid I\text{ stricly ascending mult-index of lenght }k\}$ is an open cover of $F(k, n)$.
- If $A \in V_I$, then for any $G \in \text{GL}(k, \Bbb R)$ then $AG \in V_I$.

We define $U_I = V_I /\sim$, is an open subset of $G(k, n)$. We define the function $\tilde \phi_I: V_I \to \Bbb R^{(n-k)\times k}$ by $$\tilde \phi_I(A) = (A A_I^{-1})_{I'}$$where $(\;\;)_{I'}$ denotes $(n-k) \times k$ sub-matrix from the complement of $I'$ of the multi-index $I$. Then $\tilde \phi_I$ induces a homeomorphism $\phi_I: U_I \to \Bbb R^{(n-k)\times k}$. We see that $\{U_I \mid  I\text{ stricly ascending mult-index of lenght }k\}$ is an open cover of $G(k, n)$. Then the $\{(U_I, \phi_I) \mid  I\text{ stricly ascending mult-index of lenght }k\}$ is a $\mathcal C^\infty$ atlas for $G(k, n)$. Therefore the Grassmannian $G(k, n)$ is a $\mathcal C^\infty$ manifold of dimension $k(n-k)$. 

We see that the $\Bbb {RP}^n = G(1, n+1)$. 