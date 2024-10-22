---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Vector Spaces]]

A subspace $U$ of $V$ is a vector space that $U \subseteq V$, using the same definition of addition and scalar multiplication. Denoted as $U \leq V$ (in class).

_**Theorem: $U$**_ is a subspace of $V$ if and only if:

- $0 \in U$
- $\forall x, y \in U (x+y \in U)$
- $\forall x \in U \forall a \in\mathbb{F} (ax \in U)$

_**Theorem:**_ Any intersection of subspaces of $V$ is itself a subspace.

## Minkowski Sum
Suppose that $S_1, S_2$ are sets: the Minkowski sum of $S_1$ and $S_2$ is defined as :
$$ S_1+S_2 = \{x + y : x\in S_1, y \in S_2\} $$
_**Theorem:**_ Suppose that $U, W$ be subspaces of $V$, then $U + W$ is a subspace of $V.$_**Theorem:**_ Suppose that $U, W$ be subspaces of $V$, then $U, W \subseteq U+W$
Given a set $\{ U_i\}_{i\in I}$be a set of subspaces of $V$and it’s sum it’s denoted as:

$$ \sum_{i\in I}U_i $$
_**Definition:**_ Suppose that $U, W$ be subspaces of $V$, and $U \cap W =\{0\}$, then the Minkowski Sum is denoted as: $U \oplus W$,and it’s called the direct sum of $U$ and $W$.Given a set $\{ U_i\}_{i\in I}$be a set of subspaces of $V$and it’s sum it’s denoted as, their direct sum is denoted as:

$$ \bigoplus_{i \in I} U_i $$

_**Theorem:**_ Let $U$ and $W$ be subspaces, then $U \oplus W = V$ if and only if for any $v \in V$ there’s a unique $u \in U$ and $w \in W$ such that $v = u+w$.