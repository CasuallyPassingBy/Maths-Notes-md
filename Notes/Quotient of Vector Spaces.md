---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Vector Subspaces]], [[Vector Spaces]], [[Null Space and Range]], [[Normal Subgroups and Quotient Groups]]

Let $V$ be a vector space over the field $\mathbb F$, and $v \in V$, let $U$ be a subspace of $V$, then $v +U$ is a subset of $V$ with the following characteristics:
$$ v + U = \{v+u \mid u \in U\} $$

An _affine subset_ of $V$ is a subset of $V$ of the form $v +U$, for some $v \in V$ and some subspace $U$ of $V$.

For $v\in V$ , and $U$ be subspace of $V$, the affine subspace $v+U$ is _parallel to $U$._

Suppose $U$ is a subspace of $V$. Then the _quotient space $V/U$_ is the set of all affine subsets $V$ parallel to $U$. In other words:

$$ V/U =\{ v+ U\mid v \in V\} $$

Suppose that $U$ is a subspace of $V$, and $v, w \in V$, then all of the following is equivalent:
- $u - w \in U$
- $u + U = w+U$
- $(u+U) \cap (w+U) \neq\varnothing$

Similarly it can be thought of, an equivalence relation of $u \sim_{U} w$ iff $u -w \in U$, and $V/U$ is simply the quotient of set of $V/\sim_U$.

Suppose that $U$ is a subspace of $V$, then the addition and scalar multiplication will be defined as follows. Let $v,u \in V$ and $\lambda \in\mathbb F$:
$$ (u+U)+(v+U)=(u+v) +U \newline \lambda(v+U)= (\lambda v)+U $$

Thus $(V/U, +, \cdot)$ is a vector space.

Suppose that $U$ is a subspace of $V$. The _quotient map $\pi$_ is a linear map ${\pi: V\to V/U}$, defined by:
$$ \pi(v) = v+ U $$

Let $U$ subspace of $V$, and $V$ be a vectors space. Let $W$ be a subspace such that $U \oplus W =V$, then $W \cong V/U$

Let $V$ be a finite dimensional vector space, and $U$ a subspace of $V$, then:
$$ \dim (V/U) = \dim V -\dim U $$

Suppose $T \in \mathcal{L}(V,W)$, then defining the following function $\tilde{T}:V/N(T) \to W$, defined by:
$$ \tilde T(v + N(T)) = Tv $$

then $\tilde T$ has the following properties:
- $\tilde T \in \mathcal L(V/N(T), W)$
- $\tilde T$ is injective
- $R(\tilde T) = R(T)$
- $V/N(T) \cong R(T)$

This last point could be considered a reformulation of the [[Null Space and Range#Rank-Nullity Theorem|Rank-Nullity Theorem]] even for infinite dimensional spaces. This generalisation is actually a result from the [[Group Homomorphisms and Isomorphisms|First Isomorphism Theorem for Groups]]

In general $\tilde T$ can be used to rephrase the idea of the rank-nullity theorem for infinite dimensional vector spaces
