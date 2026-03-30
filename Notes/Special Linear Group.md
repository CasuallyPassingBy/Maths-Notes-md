---
tags:
  - GroupTheory
  - DifferentialGeometry
---
Subjects: [[Group Theory]], [[Differential Geometry]]
Links: [[General Linear Group]], [[Lie Groups]], [[Commutative Ring]], [[Normal Subgroups and Quotient Groups]], [[Lie Subgroups]]

**Def:** We call the special linear group $\text{SL}(n, R)$ of degree $n$ over the commutative ring $R$ is the set of $n\times n$ matrices with determinant $1$, with the group operations of ordinary matrix multiplication and matrix inversion. This is the normal subgroup of the [[General Linear Group]] given by the kernel of the determinant. 

# Special Linear Group over $\Bbb R$

**Prop:** $\text{SL}(n, \Bbb R)$ is an embedded Lie subgroup of $\text{GL}(n, \Bbb R)$ of dimension $n^2-1$.

**Prop:** $Z(\text{SL}(2n, \Bbb R)) = \{\pm I\}$ and $Z(\text{SL}(2n+1, \Bbb R)) = \{I\}$. 

**Prop:** $\text{SL}(n, \Bbb C)$ is an embedded $(2n^2-2)$-dimensional Lie subgroup of $\text{GL}(n, \Bbb C)$. 

We can calculate the Lie algebra of $\text{SL}(n,\Bbb R)$ and it is $$\mathfrak {sl}(n, \Bbb R) = \{A \in {\frak gl}(n,\Bbb R) \mid \text{tr}(A) = 0\}. $$
**Prop:** We can get $\text{SL}(n, \Bbb R)$ is diffeomorphic to $\text{SO}(n) \times \Bbb R^{(n(n+1)/2)-1}$. 

**Prop:** Suppose $A\in \text{SL}(n, \Bbb R)$ is of the form $e^B$ for some $\mathfrak{sl}(n, \Bbb R)$. Then $A$ has a square root in $\text{SL}(n ,\Bbb R)$, meaning there is a matrix $C\in \text{SL}(n, \Bbb R)$ such that $C^2 =A$. 

# Special Linear Group over $\Bbb C$

**Prop:** The complex special linear group $\text{SL}(n,\Bbb C)$ is an embedded $(2n^2-2)$-dimensional Lie subgroup of $\text{GL}(n, \Bbb C)$. 

**Prop:** We can get $\text{SL}(n, \Bbb C)$ is diffeomorphic to $\text{SU}(n) \times \Bbb R^{n^2}$. 