---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Vector Spaces]]
Let $V$ and $W$ be vector space over the same $\mathbb{F}$. We call a function $T: V \to W$ a _**linear transformation from $V$ to $W$,**_ if for all $x, y \in V$ and $a \in\mathbb{F}$:

1. $T(x+_Vy) = T(x) +_W T(y)$
2. $T(ax) = aT(x)$
3. $T(x) = Tx$
The set of all linear transformations from $V$ to $W$ is denoted $\mathcal{L}(V,W)$. When $V = W$, then $\mathcal{L}(V,V)$ is written as $\mathcal{L}(V)$, and if $T\in\mathcal{L}(V)$ is a linear operators.

### Properties

1. If $T$ is a linear transformation then $T(0) = 0$
2. $T$ is a linear transformation iff $\forall x, y \in V \forall c \in\mathbb{F}[T(cx+y) = cT(x) + T(y)]$
3. If $T$ is a linear transformation then $\forall x,y\in V[T(x-y) = T(x) - T(y) ]$
4. T is a linear transformation iff $x_1 \dots x_n \in V$ and $a_1 \dots a_n \in \mathbb{F}$:

$$ T\left(\sum_{i=1}^na_ix_i\right)=\sum_{i=1}^na_iT(x_i) $$

_**Definition:**_ The operations are defined over $\mathcal{L}(V,W)$ of addition and scalar multiplication. Given $S, T \in \mathcal{L}(V,W)$, and $\lambda\in\mathbb{F}$, $S+T$ and $\lambda T$ defined by:

$$ (S+T)(v) =Sv+Tv \text{ and, } (\lambda T)(v) = \lambda (Tv) $$

_**Theorem:**_ $\mathcal{L}(V,W)$ is a vector space with the vector addition and scalar multiplication defined above.

_**Definition The product of Linear Maps:**_ Let $T\in\mathcal{L}(U, V)$ and $S\in\mathcal{L}(V, W)$, then the product $ST \in\mathcal{L}(U,W)$:

$$ (ST)(u)=S(Tu) $$

### Properties:

_**Associativity:**_ given the linear transformation and the correct domain, and range, then: $(T_1T_2)T_3=T_1(T_2T_3)$.

_**Identity:**_ $TI = IT = T$, given the correct domain and range.

_**Distributivity:**_ $(S_1 + S_2)T=S_1T+S_2T$, given the correct domain and range.