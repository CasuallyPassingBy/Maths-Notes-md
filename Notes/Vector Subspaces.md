---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Vector Spaces]]

A subspace $U$ of $V$ is a vector space that $U \subseteq V$, using the same definition of addition and scalar multiplication. Denoted as $U \leq V$ (in class).

**Theorem:** $U$ is a subspace of $V$ if and only if:
- $0 \in U$
- $\forall x, y \in U (x+y \in U)$
- $\forall x \in U \forall a \in\mathbb{F} (ax \in U)$

**Theorem:** Any intersection of subspaces of $V$ is itself a subspace.

## Minkowski Sum

Suppose that $S_1, S_2$ are sets: the Minkowski sum of $S_1$ and $S_2$ is defined as :
$$ S_1+S_2 = \{x + y : x\in S_1, y \in S_2\} $$

**Theorem:** Suppose that $U, W$ be subspaces of $V$, then $U + W$ is a subspace of $V.$

**Theorem:** Suppose that $U, W$ be subspaces of $V$, then $U, W \subseteq U+W$
Given a set $\{ U_i\}_{i\in I}$be a set of subspaces of $V$and it’s sum it’s denoted as:
$$ \sum_{i\in I}U_i $$

**Definition:** Suppose that $U, W$ be subspaces of $V$, and $U \cap W =\{0\}$, then the Minkowski Sum is denoted as: $U \oplus W$,and it’s called the direct sum of $U$ and $W$.Given a set $\{ U_i\}_{i\in I}$be a set of subspaces of $V$and it’s sum it’s denoted as, their direct sum is denoted as:
$$ \bigoplus_{i \in I} U_i $$

**Theorem:** Let $U$ and $W$ be subspaces, then $U \oplus W = V$ if and only if for any $v \in V$ there’s a unique $u \in U$ and $w \in W$ such that $v = u+w$.

**Def:** Let $P \in \mathcal L(V)$, such that $P^2 = P$, then we say that $P$ is a *projection*.

Consider a vector space $V$ defined as the direct sum $V = \bigoplus_{k = 1}^n  W_k$, in other words, that $v = \sum_{k = 1}^n v_k \in V$, where $v_k \in W_k$ for all $1\le k \le n$. Let $P_k$ be a linear function defined by $$P_j(v_i) = \delta_{ji} v_i.$$It follows that $$P_j(v) = v_j.$$Thus, the operator $P_j$ is a projection. 

**Prop:** If $V = \bigoplus_{i = 1}^k W_i$, there exists $k$ operators $P_1, \dots, P_k$ in $V$ such that
- $P_j$ is a projection.
- $P_i P_j = 0$ for $i \neq j$.
- $\sum_{i = 1}^k P_i = \text{id}_V$
- $\text{Im}(P_j) = W_j$
Conversely, every family $\{P_1, \dots, P_k\}$ such that $P_i^2 = P_i$ for $i \in \{1, \dots, k\}$ and $P_i P_j = 0$ if $i \neq j$, determines a decomposition $V = \bigoplus_{i = 1}^k W_i$. 