---
tags:
  - GroupTheory
  - DifferentialGeometry
---
Subjects: [[Group Theory]],  [[Differential Geometry]]
Links: [[Symplectic Vector Spaces]], [[Symplectic Forms on Smooth Manifolds]]

The *real symplectic group* is a subgroup $\text{Sp}(2n,\Bbb R)\subseteq\text{GL}(2n, \Bbb R)$ consisting of $2n\times 2n$ matrices leaving the standard symplectic form $\omega = \sum\limits_{i =1}^n dx^i \wedge dy^i$ invariant, that is the set of invertible maps $A: \Bbb R^{2n}\to \Bbb R^{2n}$ such that $A^*\omega = \omega$.

**Prop:** A matrix is in $\text{Sp}(2n, \Bbb R)$ iff it takes the standard basis to a symplectic base. 

**Prop:** $A\in \text{Sp}(2n,\Bbb R)$ iff $A^\top J A = J$, where $J$ is given in block form as $$J := \begin{pmatrix} 0 & I_n \\ -I_n & 0\end{pmatrix}. $$
**Prop:** $\text{Sp}(n, \Bbb R)$ is an embedded Lie subgroup of $\text{GL}(2n,\Bbb R)$ and has dimension $2n^2+n$

**Prop:** the Lie algebra of $\text{Sp}(2n,\Bbb R)$ is isomorphic to $$\mathfrak{sp}(2n) =\{X \in \mathcal M_n(\Bbb R) \mid X^\top J +JX = 0\} $$Meaning that $\text{Lie}(\text{Sp}(2n, \Bbb R)) \cong\mathfrak{sp}(2n)$. 

**Prop:** $\text{Sp}(2n,\Bbb R)$ is never compact. 