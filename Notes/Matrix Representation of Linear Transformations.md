---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Space of Linear Transformations]]
## Matrix Algebra
_**Def:**_ Let $A, B\in\mathcal{M}_{n\times m}(\mathbb{F})$, $(A + B)\in\mathcal{M}_{n\times m}(\mathbb{F})$ and

$$ (A+B)_{ij}=A_{ij} +B_{ij} $$

for $1\le i\le n$, and $1\le j \le m.$
_**Definition:**_ Let $A$ be a $n\times m$ matrix, or similarly $A\in\mathcal{M}_{n\times m}(\mathbb{F})$, and $B$ be a $m\times p$ matrix, $B\in\mathcal{M}_{n\times m}(\mathbb{F})$, then $(AB)$ is an $n\times p$ matrix that:

$$ (AB)_{ij} = \sum_{k=1}^mA_{ik}B_{kj} $$

for $1\le i\le n, 1\le j\le p$.

_**Def:**_ The _Kronecker delta_ $\delta_{ij}$, is defined as:

$$ \delta_{ij} =\begin{cases} 1 &i = j\\ 0 &i\ne j \end{cases} $$

The $n\times n$ identity matrix $I_n$ is defined by $(I_n)_{ij} = \delta_{ij}$.

_**Theorem:**_ Let $A\in\mathcal{M}_{m\times n}(\mathbb{F})$; $B, C\in\mathcal{M}_{n\times p}(\mathbb{F})$; $D, E\in\mathcal{M}_{q\times n}(\mathbb{F})$, then:

1. $A(B+C) = AB +AC$ and, $(D+E)A = DA + EA$
2. $a(AB) = (aA)B = A(aB)$, for any scalar $a\in\mathbb{F}$
3. $I_mA = AI_n= A$

_**Theorem:**_ Given $A, B, C$ matrices such that $(AB)C$ is well defined then,

$$ (AB)C =A(BC) $$

## Transformation into Matrix Form
_**Definition:**_ Let $V$ be a finite dimensional vector space. An _ordered basis_ for $V$ is a basis endowed with a specific order. That is an _ordered basis_ is a finite sequence of vectors that is also a basis for $V$.

_**Definition:**_ Let $\beta =\{v_1, v_2, \dots, v_n\}$ an ordered basis of $V$. For $x\in V$, there are unique scalars $a_1, a_2, \dots, a_n$, such that:

$$ x =\sum_{i = 1}^na_iv_i $$

We define the _**coordinate vector of $x$ relative to $\beta$**_ as:

$$ [x]_{\beta} = \begin{pmatrix} a_1 \\ a_2 \\ \vdots \\ a_n \end{pmatrix} $$

_**Definition:**_ Let $T\in\mathcal{L}(V,W)$, where $V$, and $W$ are finite dimensional vector space, with the basis $\beta = \{v_1, v_2, \dots, v_n\}$ and $\gamma = \{w_1, w_2, \dots w_m\}$, then for $1 \le j\le n$, there exist unique scalars $a_{ij}\in\mathbb{F}$, with $1\le i \le m$, such that:

$$ Tv_j =\sum_{i=1}^ma_{ij}w_i $$

The _**matrix representation of $T$ in ordered bases $\beta$ and $\gamma$**_ is defined as the matrix $A$, such that $A_{ij} = a_{ij}$ given by the definition of $T$, furthermore $A = [T]_\beta^\gamma$. If $V = W$ and $\beta = \gamma$ then is denoted as $[T]_\beta$.

_**Corollary:**_ Let $T, U\in\mathcal{L}(V,W)$, where $V, W$ are finite dimensional vector spaces, with bases $\beta$ and $\gamma,$ respectively. If $[U]_\beta^\gamma = [T]_\beta^\gamma$, then $U = T$.

_**Theorem:**_ Let $V$ and $W$ finite dimensional vector spaces with the bases $\beta$ and $\gamma$ respectively. Let $T, U \in\mathcal{L}(V,W)$, then:

1. $[T + U]_\beta^\gamma = [T]_\beta^\gamma + [U]_\beta^\gamma$
2. $a\in\mathbb{F}$, then $[aT]_\beta^\gamma = a[T]_\beta^\gamma$

_**Theorem:**_ Let $V, W, Z$ be finite dimensional vector spaces with bases $\alpha,\beta, \gamma$ respectively. $T\in\mathcal{L}(V,W)$ and $U\in\mathcal{L}(W,Z)$. Then:

$$ [UT]_\alpha^\gamma = [U]_\beta^\gamma[T]^\beta_\alpha $$

_**Corollary:**_ Let $V$ is a finite dimensional vector space with a basis $\beta$. Let $T,U\in\mathcal{L}(V)$, then:

$$ [UT]_\beta =[U]_\beta[T]_\beta $$

_**Theorem:**_ Let $V, W$ be finite dimensional vector spaces having ordered bases $\beta$ and $\gamma,$ respectively, and $T\in\mathcal{L}(V,W)$. Then $u\in V$:

$$ [Tu]_\gamma = [T]_{\beta}^\gamma[u]_\beta $$

## Matrix into Linear Transformation

_**Def:**_ Let $A\in\mathcal{M}_{m\times n}(\mathbb{F})$, we denote $L_A:\mathbb{F}^n\to\mathbb{F}^m$, defined as $L_A(x) = Ax$. $L_A$ is _left-multiplication transformation._

_**Theorem:**_ Let $A, B\in\mathcal{M}_{m\times n}(\mathbb{F})$, let $\beta$ and $\gamma$ be the standard basis for $\mathbb{F}^n$ and $\mathbb{F}^m$

, respectively. We have the following properties:

1. $[L_A]_\beta^\gamma = A$
2. $L_A = L_B$ iff $A= B$
3. $L_{A+B} = L_A + L_B$, and $L_{aA} = aL_A$ for any scalar $a\in\mathbb{F}$.
4. If $T\in\mathcal{L}(\mathbb{F}^n, \mathbb{F}^m)$, then there’s a unique $C\in\mathcal{M}_{m\times n}(\mathbb{F})$, such that $T =L_C$ in fact, $[T]_\beta^\gamma = C$.
5. If $E\in\mathcal{M}_{p\times n}(\mathbb{F})$, then $L_{AE} = L_AL_E$.
6. If $m=n,$ then $L_{I_n} = I_{\mathbb{F}^n}$