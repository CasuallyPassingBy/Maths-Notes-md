---
tags:
  - GroupTheory
  - DifferentialGeometry
---
Subjects: [[Group Theory]], [[Differential Geometry]]
Links: [[General Linear Group]], [[Orthogonal Group]], [[Fields]], [[Lie Subgroups]], [[Orthogonal Projections and Spectral Theorem]], [[Special Linear Group]], [[Topological Connectedness]]

**Def:** The set of all $n\times n$ Hermitian matrices is denoted as $$\text{U}(n) := \{A \in \mathcal M_n(\Bbb C)\mid A^* A = 1\}$$is called the *unitary group*. We see that $U(n)$ is a subgroup of $\text{GL}(n, \Bbb C)$. 

**Def:** The special unitary subgroup $\text{SU}(n)$ is the set of unitary matrices with unit determinant. $$\text{SU}(n) := \text{U}(n) \cap \text{SL}(n ,\Bbb C)$$
**Prop:** $\text{U}(n)$ is a Lie subgroup of $\text{GL}(n, \Bbb C)$, and has dimension $n^2$. 

**Prop:** $\text{SU}(n)$ is a Lie subgroup of $\text{GL}(n, \Bbb C)$, and has dimension $n^2-1$. 

**Prop:** We see that $Z(\text{SU}(n)) = \{\omega^k I_n \mid 0 \le k < n\}$ where $\omega =\exp(2\pi i/n)$. 

**Prop:** We get that $\Bbb S^{2n-1} \cong \text{U}(n)/\text{U}(n-1) \cong \text{SU}(n)/\text{SU}(n-1)$. 

**Prop:** For any $n \ge 1$, the Lie groups $\text{U}(n)$ and $\text{SU}(n)$ are connected. 

**Prop:** We know that $\text{SO}(2)$, $\text U(1)$ and $\Bbb S^1$ are all isomorphic as Lie groups.

**Prop:** There's a Lie group homomorphism $\rho: \text U(1) \to \text U(n)$ such that $\det \circ \rho = \text{id}_{\text U(1)}$. With this we know that $\text U(n)$ is diffeomorphic to $\text U(1) \times \text{SU}(n)$, but are not isomorphic as groups, and in particular, as Lie groups.

**Cor:** We see that $\text{SU}(2)$ is isomorphic to the group of unit [[Quaternions|quaternions]], and it is diffeomorphic to $\Bbb S^3$. 

We can calculate the Lie algebra of $\text{U}(n,\Bbb R)$ and it is $$\mathfrak {u}(n, \Bbb R) = \{A \in {\frak gl}(n,\Bbb C) \mid A^*+A = 0\}. $$
We can calculate the Lie algebra of $\text{SU}(n,\Bbb R)$ and it is $$\mathfrak {su}(n, \Bbb R) = \mathfrak u(n) \cap {\frak sl}(n,\Bbb C). $$
This is because of the canonical isomorphism of $\text{Lie}(\text{GL}(n,\Bbb C))$ with the matrix algebra ${\frak gl}(n, \Bbb C)$. Then we get that $\text{Lie}(\text{SL}(n, \Bbb C)) \cong {\frak sl}(n, \Bbb C)$, $\text{Lie}(\text{U}(n, \Bbb C)) \cong {\frak u}(n, \Bbb C)$, and $\text{Lie}(\text{SU}(n, \Bbb C)) \cong {\frak su}(n, \Bbb C)$, 

In the special case where $n=2$, we can get a nice basis for the lie algebra ${\frak su}(2)$. The basis is of the form $$u_1 := \begin{pmatrix}0 & i \\ i & 0\end{pmatrix}, \quad u_2 := \begin{pmatrix}0 & -1 \\ 1 & 0\end{pmatrix}, \quad u_1 := \begin{pmatrix}0 & i \\ i & 0\end{pmatrix}, \quad  $$