---
tags:
  - GroupTheory
  - DifferentialGeometry
---
Subjects: [[Group Theory]], [[Differential Geometry]]
Links: [[General Linear Group]], [[Fields]], [[Lie Subgroups]], [[Unitary Group]], [[Topological Connectedness]]


**Def:** For any field $F$, an $n \times n$ matrix with entries in $F$ such that its inverse equals its transpose is called an *orthogonal matrix over $F$*. The $n\times n$ orthogonal matrices form a subgroup, denoted $\text{O}(n, F)$, of the [[General Linear Group]] $\text{GL}(n F)$; that is $$ \text{O}(n, F) = \{Q \in \text{GL}(n, F) \mid Q Q^\top = Q^\top Q = I\}$$
If the field is not specified, then $F = \Bbb R$. 

**Def:** The special orthogonal subgroup $\text{SO}(n, F)$ is the set of orthogonal matrices with unit determinant, $\text{SO}(n, F) = \text{O}(n ,F)\cap \text{SL}(n, F)$.

**Def:** We can define its Lie algebra of the orthogonal group as $${\frak o}(n):= \{B\in {\frak gl}(n,\Bbb R) \mid B^\top + B = 0\}$$If we additionally define ${\frak so}(n) := {\frak o}(n) \cap {\frak sl}(n,\Bbb R)$, then we see that ${\frak so}(n) = {\frak o}(n)$. 
# Real Orthogonal Group

**Prop:** $\text{O}(n)$ is a real compact Lie group of dimension $n(n-1)/2$, and it is an embedded Lie subgroup of $\text{GL}(n, \Bbb R)$. 

We see that $\text{SO}(n)$ is an open subgroup of $\text{O}(n)$, and thus $\text{SO}(n)$ is a compact embedded Lie subgroup of $\text{GL}(n, \Bbb R)$. 

**Prop:** $\text{SO}(2) \cong \Bbb S^1$

We have that $\Bbb S^1$ is a Lie subgroup of $\Bbb C^*$ because it is a subgroup and an embedded submanifold.

If we want to check that $\text{O}(n)$ is an embedded submanifold, we only need to check that there's a defining map. We will consider the space of *symmetric matrices*, as $\text{S}(n, \Bbb R)$. The map we will consider is $f: \text{GL}(n, \Bbb R) \to \text{S}(n, \Bbb R)$ defined as $f(A) = A^\top A$. We clearly, see that this function is smooth, and that $\text{O}(n) = f^{-1}\{I_n\}$. We only need to compute the pushforward of $f_*: T_A\text{GL}(n, \Bbb R) \to T_{f(A)} \text{S}(n, \Bbb R)$. We can identify the tangent spaces with the original spaces. If we calculate the pushforward we get that $$f_* B = B ^\top A + A^\top B$$We only need to check if that is surjective. Let $C\in \text{S}(n, \Bbb R)$, then $f_*(\frac12AC) = C$. By the [[Smooth Submanifolds#^c2a3b8|Submersion Level Set Theorem]], we know that $\text{O}(n)$ is a closed embedded Lie subgroup. 

Using the argument above, we get that $T_{I_n} \text{O}(n) = \ker f_*$, and by the computation of the pushforward we get that $$T_{I_n} \text{O}(n) =\{B\in {\frak gl}(n,\Bbb R) \mid B^\top + B = 0\},$$also known as the set of skew-symmetric matrices. We denote this subspace of ${\frak gl}(n,\Bbb R)$ by $\mathfrak o(n)$. This means that $\text{Lie}(O(n))$ is canonically isomorphic to $\mathfrak o(n)$. 

**Prop:** We get that $\Bbb S^{n-1} \cong \text{O}(n)/\text{O}(n-1) \cong \text{SO}(n)/\text{SO}(n-1)$. 

**Prop:** For any $n \ge 1$, the Lie group $\text{SO}(n)$ is connected. The group $\text O(n)$ has exactly two components, one of which is $\text {SO}(n)$ and the other is $\text O^-(n)$. 

**Prop:** We know that ${\frak o}(3)$ is isomorphic to $(\Bbb R^3, \times)$ as Lie algebras, and ${\frak o}(3)$ is isomorphic to ${\frak su}(2)$. 