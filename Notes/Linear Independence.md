---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Linear Combinations]]
## Definitions
A subset $S$ of a vector space $V$ is called _**linearly independent**_ if for any finite number of distinct vectors $\{ u_i \}_{i=1}^{n}\subseteq S$, and scalars $\{a_i\}_{i=1}^n$ $\subseteq \mathbb{F}$:

$$ \sum_{i=1}^na_iu_i =0 $$

Implies that $\forall 1\leq i \leq n[a_i = 0]$. By definition we say that $\varnothing$ is linearly independent.

A subset $S$ of a vector space $V$ is called _**linearly dependent**_ if there exist a finite number of distinct vectors $\{ u_i \}_{i=1}^{n}\subseteq S$, and scalars $\{a_i\}_{i=1}^n$ $\subseteq \mathbb{F}$:

$$ \sum_{i=1}^na_iu_i =0 $$

Where there’s at least one $a_i \neq 0$.

## Theorems
_**Theorem:**_ Let $V$ be a vector space, and $S_1 \subseteq S_2 \subseteq V$, and if $S_1$ is linearly dependent, then $S_2$ is also linearly dependent.

_**Corollary:**_ Let $V$ be a vector space, and $S_1 \subseteq S_2 \subseteq V$, and it $S_2$ is linearly independent, then $S_1$ is also linearly dependent.

_**Theorem:**_ Let $S$ be linearly independent subset of $V$, and let $v\in V$. $S \cup \{v\}$ is linearly independent if and only if $v \not\in \text{span}(S)$.

### Linear Dependence Lemma

Let $S = \{ u_i \}_{i=1}^n$ a finite set of vectors. $S$ is linearly dependent if and only if $u_1 = 0$ or there’s a $1 \leq j \leq n$ such that $u_j \in \text{span}\{u_i\}_{i=1}^{j-1}$ and $\text{span}(S \setminus\{u_j\}) = \text{span}(S)$