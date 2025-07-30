---
tags:
  - LinearAlgebra
  - CliffordAlgebra
---
Subjects: [[Clifford Algebra]], [[Linear Algebra]]
Links: [[Vector Spaces]], [[Dual Vector Spaces]]

We are going to revisit of [[Dual Vector Spaces]], but through the a lens closer to tensors.

We are using the *Einstein summation convention*.

Let $V$ be a $K$-vector space. If $V$ is finite dimensional then there's a basis $\mathfrak B = \{e_1, \dots, e_n\}$ of $V$, then $$v = \sum_{i = 1}^n v^i e_i = v^i e_i.$$
Remember that $V' := \mathcal L(V, K)$. Since $V$ is finite-dimensional, then $V'$ is also finite dimensional and $V \cong V'$. In this context, refer to dual vectors as *covectors*. Let $\alpha$ be a covector and $v$ a be a vector, then $$\alpha (v) = \alpha(v^ie_i) = v^i \alpha(e_i) = v^i \alpha_i,$$where $\alpha_i = \alpha(e_i)$. We know that a linear function is uniquely determined by their effect on the basis $\mathfrak B$ of the vector space $V$. In consequence, let us consider the set of covectors $\mathfrak B':= \{e^1, \dots. e^n\}$ defined by $$e^i(e_j) = \delta^i_j.$$The set $\frak B'$ is a basis for $V'$. The base $\frak B'$ is said to be the *dual basis* associated with the basis $\frak B$. 

# Covariant and Contravariant Transformations

Let us consider the change of basis $\mathfrak B \mapsto \mathfrak C$ as described by $e'_j := B^i_j e_i$. A vector $v\in V$ has components $v^i$ with respect to the basis $\frak B$, and components $v'^j$ with respect to the basis $\frak C$, namely $v = v^i e_i = v'^i e'_i$. The vector components are related by $v^i = B^i_j v'^j.$

Now, let $\frak B'$, and $\frak C'$, be the dual basis respectively associated with $\frak B$ and $\frak C$. By definition, we have $e^i (e_j) = e'^i (e_j') = \delta^i_j$. The components of a $\alpha \in V'$ in the bases $\frak B'$ and $\frak C'$ are given by the evaluation of $\alpha on the bases $\frak B$ and $\frak C$, respectively. Hence, $\alpha = \alpha_i e^i = \alpha_i' e'^i$, where $\alpha_i = \alpha (e_i)$, and $\alpha'_i = \alpha(e'_i)$. Since $e'_j = B^i_j e_i$, then components of $\alpha$ transform as $\alpha'_j = B^i_j \alpha_i$, and consequently the dual bases are related by $e^i = B^i_j e^j$. 

To summarise, with a change of basis, the components of a covector transform as the basis vectors $$e'_j = B^i_j e_i, \qquad \alpha'_j = B^i_j \alpha_i,$$whereas the componentes of a vector transform as the basis covectors $$e^j = B^j_i e'^i, \qquad v^j = B^j_i v'^i.$$
The in
