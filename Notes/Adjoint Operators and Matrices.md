---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Space of Linear Transformations]], [[Matrix Representation of Linear Transformations]], [[Inner Products and Norms]], [[Orthogonal Complements]]
**Def:** Suppose $T \in \mathcal L(V, W)$. The _adjoint_ of $T$ is the function ${T^* :W \to V}$ such that

$$ \langle Tv, w\rangle = \langle v, T^*w\rangle $$

for every $v \in V$ and every $w\in W$.

If $T \in \mathcal L(V,W)$, then $T^* \in \mathcal L(W, V)$.

- ********************Properties********************
    $( S+T)^* =S^*+T^*$, for all $S, T \in \mathcal L(V, W)$
    $(\lambda T)^* = \overline \lambda T^*$, for all $\lambda \in \mathbb F$ and $T \in\mathcal L(V,W)$
    $(T^*)^* = T$ for all $T \in \mathcal L(V,W)$
    $I^* = I$, where $I$ is the identity operator on $V$
    $(ST)^* = T^*S^*$ for all $T \in \mathcal L(V,W)$ and $S \in\mathcal L(W,U)$
    

********Th:******** For arbitrary vector spaces $V$ and $W$, and ${T \in \mathcal L(V,W)}$ then

- $N(T^*) = R(T)^\bot$
- $N(T) = R(T^*)^\bot$
- $(*)\operatorname{cl}_V(R(T^*)) = N(T)^\bot$
- $(*)\operatorname{cl}_W(R(T)) = N(T^*)^\bot$
- $R(T^* )\subseteq N(T)^\bot$
- $R(T)\subseteq N(T^*)^\bot$

Some special cases are:

- $R(T^*) = N(T)^\bot$ if $V$ is finite dimensional
- $R(T) = N(T^*)^\bot$ if $W$ is finite dimensional

********Th:******** Let $V$ be a finite dimensional inner product space, and $\beta$ be an orthonormal basis for $V$. If $T \in \mathcal L(V)$, then

$$ [T^*]_\beta = [T]^*_\beta $$
Where $[T]^*_\beta$ is the conjugate transpose of $[T]_\beta$.
**********Cor:********** Let $A \in \mathcal M_n(\mathbb C)$, then $L_{A^*}=(L_A)^*$
**************Cor:************** If $A \in \mathcal M_{m\times n}(\mathbb F)$, $x \in \mathbb F^n$, and $y \in \mathbb F^m$. Then

$$ \langle Ax, y\rangle_m = \langle x, A^* y\rangle_n $$

****Th:**** Let $A \in \mathcal M_{m\times n}(\mathbb F)$. Then $\operatorname{rank}(A^*A) = \operatorname{rank}(A)$

****Cor:**** If $A \in \mathcal M_{m\times n}(\mathbb F)$ such that $\operatorname{rank}(A) =n$, then $A^* A$ is invertible.

********Th:******** Let $V$ be finite dimensional and $T \in \mathcal L(V)$. If $T$ has eigenvector, then so does $T^*$. Additionally, if $\lambda$ is an eigenvalue of $T$, then $\overline \lambda$ is an eigenvalue of $T^*$.

****Th:**** Suppose $V$is a complex inner product space and $T \in \mathcal L(V)$. If for all $v \in V$

$$ \langle Tv, v\rangle=0 $$

Then $T=0$.