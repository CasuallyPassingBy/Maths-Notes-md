---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Null Space and Range]]
### Null Spaces of Powers of an Operator
**Th:** Let $T : V \to V$ be a linear operator, then

$$ \{ 0\} = N(T^0) \subseteq N(T) \subseteq \dots \subseteq N(T^k) \subseteq N(T^{k+1}) \subseteq \cdots $$

If we suppose $m\in \Bbb N$ such that $N(T^m) = N(T^{m+1})$, then all $k \ge m$, will have that ${N(T^k ) = N(T^m)}$

What we can show that if $V$ is finite dimensional, then the null spaces stop growing

********Th:******** Suppose $T \in \mathcal L(V)$, and $n = \dim V$, then

$$ N(T^n) = N(T^{n+1}) $$

and that

$$ V = N(T^n ) \oplus R(T^n) $$

### Nillpotent Operators

**Def:** An operator is called **nilpotent** if some power of it equals $0$

********Th:******** Suppose $N \in \mathcal L(V)$ is nilpotent, with $V$ a finite dimensional vector space. Then ${N^{\dim V} = 0}$

**Th:** Suppose $N \in \mathcal L(V)$ is nilpotent, with $V$ a finite dimensional vector space. Then there is a basis of $V$with respect to which the matrix has the form

$$ \begin{pmatrix} 0 &&* \\ &\ddots & \\ 0 &&0 \end{pmatrix} $$

here all entries on and below the diagonal are $0$’s

### Square Roots

Suppose $N \in\mathcal L(V)$ is nilpotent. Then $I + N$ has a square root. This is by using the [[Taylor Series in R]] of $\sqrt{1+x}$, and we don't have to care about convergence since $N^k$ will eventually be $0$

**Th:** Suppose $V$ is a complex vector space and $T \in \mathcal L(V)$ invertible. Then $T$ has a square root

#### Basis corresponding to a nilpotent operator
Suppose $N \in \mathcal L(V)$ is nilpotent. Then there exist vectors $v_1, \dots, v_n \ in V$ and nonnegative integers $m_1, \dots, m_n$ such that
- $N^{m_1}v_1, \dots, Nv_1, v_1, \dots, N^{m_n}v_n, \dots, Nv_n, v_n$ is a basis of $V$
- $N^{m_1+1} v_1 = \dots = N^{m_n+1} v_n = 0$ 