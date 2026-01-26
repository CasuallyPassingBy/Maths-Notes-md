---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Exterior Algebra of Multicovectors]], [[Determinants]]

**Def:** Let $V$ be an $n$-dimensional vector space. A *density on $V$* is a function $$\mu: V \times \dots\times V \to \Bbb R $$satisfying the following condition: if $T: V \to V$ is any linear map, then$$\mu(Tv_1,\dots, Tv_n) = |\det T| \mu(v_1,\dots, v_n).  $$
Observe that a density is *not* a tensor, because it is not linear over $\Bbb R$ in any of its arguments. Let $\mathcal D(V)$ denote the set of all densities on $V$.

**Properties of Densities:** Let $V$ be a vector space of dimension $n \ge 1$.
- $\mathcal D(V)$ is a vector space under the obvious operations:$$(c_1\mu_1+c_2\mu_2)(v_1,\dots, v_n) = c_1\mu_1  (v_1,\dots, v_n) + c_2\mu_2(v_1,\dots, v_n).$$
- if $\mu_1,\mu_2\in  \mathcal D(V)$, and $\mu_1(E_1,\dots, E_2) = \mu_2(E_1,\dots, E_n)$ for some basis $(E_i)$ of $V$, then $\mu_1 = \mu_2$.
- If $\omega \in {\textstyle \bigwedge}^{\!n } (V^*)$, the map $|\omega|: V \times \dots \times V \to \Bbb R$ defined by $$|\omega| (v_1,\dots, v_n) := |\omega(v_1,\dots, v_n)| $$is a density.
- $\mathcal D(V)$ is $1$-dimensional, spanned by $|\omega|$ for nonzero $\omega \in {\textstyle \bigwedge}^{\!n } (V^*)$. 

**Def:** A *positive density on $V$* is density $\mu$ satisfying $\mu(v_1,\dots, v_n) >0$ whenever $(v_1,\dots, v_n)$ is linearly independent $n$-tuple. A *negative density* is defined similarly.  

**Obs:** If $\omega \in {\textstyle \bigwedge}^{\!n } (V^*)$, then it is clear that $|\omega|$ is a positive density; more generally, a density $c|\omega|$ is positive, negative, or zero iff $c$ has the same property. Thus, each density on $V$ is either positive, negative or zero, and the set of positive densities is a convex subset of $\mathcal D(V)$. 