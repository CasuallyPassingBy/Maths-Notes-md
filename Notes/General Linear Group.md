---
tags:
  - GroupTheory
  - DifferentialGeometry
---
Subjects: [[Group Theory]], [[Differential Geometry]]
Links: [[Lie Groups]], [[Matrix Representation of Linear Transformations]], [[Automorphism Group]], [[Trace of Matrix]], [[Special Linear Group]], [[Topological Connectedness]]

If $V$ is a vector space over the field $F$, the general linear group of $V$ is defined as $\text{GL}(V) := \text{Aut}(V)$. . This related to the [[automorphism group]] in any category

Let $F$ being an field, and $\text{M}(n, F)$ be the set of all $n \times n$ matrices over the field $F$. Then $\text{GL}(n, F) := \{ A \in \text{M}(n , F) \mid \det A \neq 0\}$. 

If $V$ has finite dimension $n$, then $\text{GL}(V)$ and $\text{GL}(n ,F)$ are isomorphic. This is because we have the matrix representation of linear transformations. 

# General Linear Group over $\Bbb R$

We have that $\text{GL}(n, \Bbb R)$ has extra properties. In particular we have that $\text{GL}(n, \Bbb R) = \det^{-1}[\Bbb R\setminus\{0\}]$, meaning is an open set of $\Bbb R^{n \times n}$. Then we have that as an open subset of $\Bbb R^{n \times n}$, it is a manifold. It is fairly easy to prove that $\mu$ (matrix multiplication) and $\iota$ (matrix inverse) are $\mathcal C^\infty$. Meaning that $\text{GL}(n, \Bbb R)$ is an Lie group. 

Let $\det: \text{GL}(n, \Bbb R) \to \Bbb R$ be the determinant map. The tangent space $T_I(\text{GL}(n, \Bbb R))$ to $\text{GL}(n, \Bbb R)$ at the identity $I$ is the vector space $\mathcal M_n(\Bbb R)$. 

**Prop:** If $V$ is a finite-dimensional real or complex vector space then there's a Lie group isomorphism $\text{GL}(V) \cong \text{GL}(n, \Bbb R)$ or $\text{GL}(n, \Bbb C)$.  

**Prop:** For any $X \in \mathcal M_n(\Bbb R)$, $d(\det)_I: \mathcal M_n(\Bbb R) \to \Bbb R$, $d(\det)_I (X) = \text{tr}(X)$. 

**Prop:** For any $X\in \mathcal M_n(\Bbb R)$, $d(\det)_A : \mathcal M_n(\Bbb R) \to \Bbb R$ ,$d(\det)_A(X) = (\det A)(\text{tr}(X))$. 

**Prop:** $Z(\text{GL}(n, \Bbb R)) = \{\lambda I \mid \lambda \in \Bbb R^\times\} \cong \Bbb R^\times$. 

**Prop:** Let $\phi: \text{GL}(2n+1, \Bbb R) \to \text{SL}(2n+1, \Bbb R) \times \Bbb R^\times$, defined as $\phi(A) = ((\det A)^{-1/(2n+1)} A, \det A)$. Then $\phi$ is a Lie group isomorphism. Meaning that $\text{GL}(2n+1, \Bbb R) \cong \text{SL}(2n+1, \Bbb R) \times \Bbb R^\times$.

**Prop:** $Z(\text{GL}(2n, \Bbb R)) \not\cong  Z(\text{SL}(2n, \Bbb R)\times \Bbb R^\times)$. Meaning that $\text{GL}(2n, \Bbb R)) \not\cong  \text{SL}(2n, \Bbb R)\times \Bbb R^\times$.

The subset $\text{GL}^+(n, \Bbb R)\subseteq \text{GL}(n, \Bbb R)$ consisting of real $n\times n$ matrices with positive determinants is a subgroup. It is an open subset of $\text{GL}(n, \Bbb R)$ by continuity of the determinant, thus it is an embedded Lie subgroup of dimension $n^2$.

We would like to consider the Lie algebra of $\text{GL}(n, \Bbb R)$. Since $T_{I_n} \text{GL}(n, \Bbb R)$ can be identifies with $\text{GL}(n, \Bbb R)$, then the Lie algebra of $\text{GL}(n, \Bbb R)$ is itself. To make the distinction that is equipped with the bracket commutator of matrices we denote it as ${\frak gl}(n,\Bbb R)$. 

Define a map $\beta: \text{GL}(n, \Bbb C) \to \text{GL}(2n, \Bbb R)$ by replacing each complex matrix entry $a+bi$ with the $2\times 2$ block $\begin{pmatrix} a & -b \\ b & a\end{pmatrix}$:  $$\beta \begin{pmatrix}
a_1^1+ ib_1^1 & \dots &a_1^n +ib^n_1 \\
\vdots &&\vdots \\
a_n^1+ ib_n^1 & \dots &a_n^n +ib^n_n
\end{pmatrix} =  \begin{pmatrix}
a_1^1 & -b_1^1 & \dots &a_1^n & -b^n_1 \\
b_1^1& a_1^1 & \dots & b_1^n & a^n_1 \\
\vdots &\vdots&&\vdots&\vdots \\
a_n^1 & -b_n^1 & \dots &a_n^n & -b^n_n \\
b_n^1& a_n^1 & \dots & b_n^n & a^n_n \\
\end{pmatrix}$$We can see that $\beta$ is an injective Lie group homomorphism whose image is a closed Lie subgroup of $\text{GL}(2n, \Bbb R)$. Thus $\text{GL}(n, \Bbb C)$ is isomorphic to this Lie subgroup of $\text{GL}(2n, \Bbb R)$. 

**Prop:** Let us consider the evaluation map $\varepsilon: \text{Lie}(\text{GL}(n, \Bbb C)) \to T_{I_n} \text{GL}(n, \Bbb C)$, and the usual identification between tangent spaces to an open subset of a vector space and the vector space itself $\varphi: T_{I_n} \text{GL}(n, \Bbb C) \to {\frak gl}(n, \Bbb C)$. The composition of these maps yield a Lie algebra isomorphism between $\text{Lie}(\text{GL}(n, \Bbb C))$ and the matrix algebra ${\frak gl}(n, \Bbb C)$, i.e., $\varphi \circ \varepsilon: \text{Lie}(\text{GL}(n, \Bbb C)) \to {\frak gl}(n, \Bbb C)$ is a Lie algebra isomorphism. 

**Prop:** The connected components of $\text{GL}(n,\Bbb R)$ are $\text{GL}^+(n, \Bbb R)$ and $\text{GL}^-(n, \Bbb R)$.