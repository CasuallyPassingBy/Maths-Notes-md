---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Space of Linear Transformations]]

_**Definition:**_ A linear transformation $T : V\to W$. The _**null space of** $T$,_ denoted as $N(T)$ or $\text{null }T$ it is the set of all the vectors $v$ of $V$such that $T(v) = 0$, that is $N(T)=\{v \in V: T(v) = 0\}$. $N(T)$ is a subspace of $V$.
Theorem: $T\in\mathcal{L}(V,W)$, $T$ is injective iff $N(T) =\{0\}$

_**Definition:**_ A linear transformation $T: V\to W$. The _**range**_ (or _**image**_) of $T$, denoted as $R(T)$ is a subspace of $W$. $R(T) = \{T(v) : v \in V\}$.

_**Theorem:**_ Given a basis $\beta$ of $V$, and $T: V\to W$ linear, then $R(T) = \text{span}(T(\beta))$.

_**Definition:**_ Given a linear transformation $T: V\to W$, $\text{dim}(N(T))$ is called the _**nullity**_ also denoted as $n(T)$ or $\text{nullity}(T)$, and, $\text{dim}(R(T))$ is called the _**rank**_ of $T$, denoted as $r(T)$ or $\text{rank}(T)$

## Rank-Nullity Theorem
Let $V$ and $W$ be vector spaces, and $T:V\to W$ be linear. If $V$ is finite-dimensional, then:

$$ n(T) + r(T) = \dim(V) $$

_**Corollary:**_ Let $V$ and $W$ be finite-dimensional vector spaces where $\dim(V) > \dim(W)$, then any $T\in\mathcal{L}(V,W)$ cannot be injective.

_**Corollary:**_ Let $V$ and $W$ be finite-dimensional vector spaces where $\dim(V) < \dim(W)$, then any $T\in\mathcal{L}(V,W)$ cannot be surjective.

_**Corollary:**_ Let $V$ and $W$ be finite-dimensional vector spaces where $\dim(V) = \dim(W)$, and any $T\in\mathcal{L}(V,W)$, $T$ is injective iff $T$ is surjective.

_**Theorem**_: Let $V$ and $W$ be finite-dimensional vector space over the field $\mathbb{F}$, suppose the set $\{v_1,\dots ,v_n\}$ be a basis for $V$. For $w_1, w_2 \dots w_n \in W$, there exists exactly one $T\in\mathcal{L}(V,W)$, such that $T(v_i) = w_i,$ for all $1\leq i \leq n$

Corollary: If for a basis $\{v_1,\dots ,v_n \}$ of $V$, and $T, U\in\mathcal{L}(V,W)$, and $T(v_i) = U(v_i)$ for all $1\leq i \leq n$, then $U =T$.