---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Space of Linear Transformations]], [[Matrix Representation of Linear Transformations]], [[Vector Spaces]], [[Group Homomorphisms and Isomorphisms]]
## Invertibility
_**Def:**_ Let $T\in\mathcal{L}(V,W)$, $T$ is said to be invertible if there’s a $S\in\mathcal{L}(W,V)$, such that $ST = I_V$ and $TS = I_W.$ $S$ is called the _inverse of $T$_, and is denoted as $T^{-1}$.

_**Theorem:**_ Let $V, W$ be finite dimensional vector space, given $T\in\mathcal{L}(V,W)$, and $\dim V =\dim W$ then this are equivalent:

1. $T$ is invertible
2. $T$ is injective
3. $T$ is surjective

_**Corollary:**_ If there’s $T\in\mathcal{L}(V,W),$ and $T$ is invertible. If $V$ is finite dimensional, iff $W$ is finite dimensional, and $\dim V=\dim W$.

Let $A\in\mathcal{M}_{n\times n}(\mathbb{F})$. Then A is _invertible_ iff there’s a unique $B\in\mathcal{M}_{n\times m}(\mathbb{F})$ such that $AB = BA = I_n$. This matrix is called $A^{-1}$.

_**Theorem:**_ Let $V, W$ be finite dimensional vector spaces with ordered bases $\beta$ and $\gamma$, respectively. Let $T\in\mathcal{L}(V,W)$, then $T$ is invertible iff $[T]_\beta^\gamma$ is invertible. Furthermore, $([T]_\beta^\gamma)^{-1} = [T^{-1}]_\beta^\gamma.$

_**Corollary:**_ Let $V$ be a finite dimensional vector space with a base $\beta$. Let $T\in\mathcal{L}(V)$, $T$ is invertible iff $[T]_\beta$ is invertible. Furthermore, $([T]_\beta)^{-1} = [T^{-1}]_\beta$.

_**Corollary:**_ Let $A\in\mathcal{M}_{n\times n}(\mathbb{F})$. Then $A$ is invertible iff $L_A$ is invertible. Furthermore $(L_A)^{-1} = L_{A^{-1}}$

## Isomorphic Vector Spaces
_**Definition:**_ Let $V, W$ be vector spaces over the field $\mathbb{F}$, are said to be _isomorphic_ if there’s a $T\in\mathcal{L}(V,W)$, such that $T$ is invertible. Denoted as $(V, +,\cdot)\cong(W, +,\cdot)$ or simply $V\cong W$.

_**Theorem:**_ Let $V, W$ finite dimensional vector space over the field $\mathbb{F}$. $V\cong W$ iff $\dim V=\dim W$.

_**Corollary:**_ Let $V$ is a finite dimensional vector space over the field $\mathbb{F}$. Let $\dim V = n$, then $V\cong\mathbb{F}^n$.

_**Theorem:**_ Let $V$ and $W$ be finite dimensional vector space over the field $\mathbb{F}$, with ordered bases $\beta$ and $\gamma$ respectively. Then the function $\Phi_\beta^\gamma:\mathcal{L}(V,W)\to\mathcal{M}_{\dim W\times\dim V}(\mathbb{F})$, defined by $\Phi_\beta^\gamma(T) = [T]_\beta^\gamma$, is an _isomorphism._

_**Corollary:**_ Let $V$ and $W$ be finite dimensional vector space. Then, $\dim(\mathcal{L}(V,W)) =(\dim V)(\dim W)$

_**Definition:**_ Let $V$ be a finite dimensional vector space over the field $\mathbb{F}$, and with the ordered basis $\beta$. The _standard representation of $V$ with respect to $\beta$_ is the function as $\phi_\beta :V\to\mathbb{F}^n$ defined by $\phi_\beta(v) =[v]_\beta$.

_**Theorem:**_ For any finite-dimensional vector space $V$ over the field $\mathbb{F}$, with an ordered basis $\beta$, $\phi_\beta$ is an isomorphism.