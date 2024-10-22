---
tags:
  - LinearAlgebra
  - Analysis
---
Subjects: [[Metric and Normed Spaces]], [[Linear Algebra]]
Links: [[Normal and Hermitian Operators]], [[Adjoint Operators and Matrices]]

**Def:** Let $V$ be a dimensional inner product space over a field $\mathbb F$, and ${T \in \mathcal L(V)}$. If $\|Tv\| =\|v\|$ for all $v \in V$, then $T$ is an **isometry**. We call $T$ a **unitary operator** if $\mathbb {F=C}$ and an **orthogonal operator** if ${\mathbb {F= R}}$. In infinite dimensional vector spaces, if the operator that preserves norms, and is surjective, then it is an **isometry.**

********Th:******** Let $T$ be linear operator on a finite dimensional inner product space $V$. Then following statements are equivalent:

- $T^* T=I$
- $T T^*=I$
- $\langle Tu, Tv\rangle = \langle u, v\rangle$ for all $u, v \in V$
- If $\beta$ is an orthonormal basis for $V$, then $T[\beta]$ is an orthonormal basis for $V$.
- There exists on orthonormal basis $\beta$ for $V$ such that $T[\beta]$ is an orthonormal basis for $V$.
- $\|T v\| =\|v\|$ for all $v \in V$.
- $T^*$ is an isometry
- $T$ is invertible and $T^{-1} = T^*$

********Cor:******** Let $T$ be linear operator on a finite dimensional real inner product space $V$. Then $V$ has an orthonormal basis of eigenvectors of $T$ with corresponding eigenvalues of absolute value $1$ iff $T$ is orthogonal and self-adjoint.

********Cor:******** Let $T$ be linear operator on a finite dimensional complex inner product space $V$. Then $V$ has an orthonormal basis of eigenvectors of $T$ with corresponding eigenvalues of absolute value $1$ iff $T$ is unitary.

### Partial Isometries
**Def:** Let $V$ be a finite dimensional inner product space. A linear operator $U$ on $V$ is called a **partial isometry** if there exists a subspace $W$ of $V$ such that $\|U(w)\| =\|w\|$ for all $w \in W$, and $U(v) =0$ for $v \in W^\bot$. This doesn’t imply that $W$ is $U-$invariant.
- $\langle Ux, Uy\rangle =\langle x, y\rangle$ , for all $x, y \in W$
- If $\beta$ is an orthonormal basis for $W$, then $U[\beta]$ is also an orthonormal basis for $R(U)$.
- There exists a basis $\gamma$ for $V$ such that the first $\dim W$ columns of $[U]_\gamma$ form an orthonormal set and the remaining columns are zero.
- Let $\gamma$ be an orthonormal basis for $R(U)^\bot$, and $\beta$ be an orthonormal basis of $W$, then $R[\beta]\cup \gamma$ is an orthonormal basis for $V$.
- Suppose $\beta$ be an orthonormal basis of $W$, and $\gamma$ be an orthonormal basis for $R(U)^\bot$. Let $T \in \mathcal L(V)$, such that if ${v \in\beta}$ then $TU v=v$ and if $v \in \gamma$, then $Tv = 0$. Then $T = U^*$.
- $U^*$ is a a partial isometry.
- $U^* U$ is orthogonal projection on $W$.
- $UU^*U = U$

**Def:** A square matrix $A$ is called on **orthogonal matrix** if ${AA^\top= A^\top A = I}$ and ********unitary******** if $A A^* = A^* A=I$.

The set of all orthogonal transformations/matrices is called the [[orthogonal group]], and the set of all unitary transformations/matrices is called the [[unitary group]]

**Def:** $A$ and $B$ are **unitarily/orthogonally equivalent** iff there exists a unitary/orthogonal matrix $P$ such that $A =P^*BP$. This forms an equivalence relation on $\mathcal M_n(\mathbb C)/\mathcal M_n(\Bbb R)$

********Th:******** Let $A$ be a complex $n\times n$. Then $A$ is normal iff $A$ is unitarily equivalent to a diagonal matrix.

********Th:******** Let $A$ be a real $n\times n$. Then $A$ is symmetric iff $A$ is orthogonally equivalent to a diagonal matrix.

********Th:******** A matrix that is both unitary and upper triangular then it is diagonal.

### Schur’s Theorem Again

Let $A \in \mathcal M_n(\mathbb F)$ be a matrix whose characteristic polynomial splits over $\mathbb F$.
- If $\mathbb{F=C}$, then $A$ is unitarily equivalent to a complex upper triangular matrix
- If $\mathbb{F=R}$, then $A$ is orthogonally equivalent to a real upper triangular matrix.

**Cor:** Suppose $V$ is a complex inner product space and $T \in\mathcal L(V)$. The the following are equivalent:

- $T$ is an isometry
- There is an orthonormal basis of $V$ consisting of eigenvectors of $T$ whose corresponding eigenvalues all have absolute value $1$.
### QR Factorization
********Th:******** Let $A \in \mathcal M_{n\times m}(\mathbb C)$ with linearly independent columns. Then $A$ can be factorized as $A= QR$, where $Q \in \mathcal M_{n\times m}(\mathbb F)$ with orthogonal columns and $R \in \mathcal M_m(\mathbb F)$ upper triangleular matrix with positive diagonal entries.

We can consider the $i$th column of $A$ as $a_i$, then we can apply the Gram-Schmidt orthonormalization process to $\{a_i\}_{i=1}^m$, the following vectors $\{q_i\}_{i = 1}^m$ will form the matrix $Q$.

Similarly given the set of orthonormal vectors we can calculate the matrix $R$, as follows $R_{ij} = \langle q_i, a_j\rangle$ for $1 \le i \le j \le m$, otherwise $R_{ij} = 0$.

If $A \in \mathcal M_n(\mathbb C)$, then $Q$ will be a unitary/orthogonal matrix.

Given a linear system $Ax = b$ when is invertible. We can decompose $A = QR$, and solve the system $QRx = b$, or $Rx = Q^* b$, this an be solved easily since $R$ is upper triangleular.

### Rigid Motions
**Def:** Let $V$be a real inner product space. A function ${f:V\to V}$ is called a **rigid motion** if for all $x,y \in V$

$$ \|f(x) -f(y)\| = \|x-y\| $$

********Th:******** Let ${f:V\to V}$ be a rigid motion on a finite dimensional real inner product space $V$. The there exists a unique orthogonal operator $T$ on $V$ and a unique translation $g$ on $V$ such that ${f=g\circ T}$.

********Th:******** Let $f:V\to V$ be a rigid motion then $f$ is invertible and ${f^{-1}}$ is also a rigid motion.

********Cor: Th:******** Let ${f:V\to V}$ be a rigid motion on a finite dimensional real inner product space $V$. The there exists a unique orthogonal operator $T$ on $V$ and a unique translation $g$ on $V$ such that ${f = T\circ g}$.

### Orthogonal Operators on $\Bbb R^2$

********Th:******** Let $T$ be an orthogonal operator in $\Bbb R^2$. Then exactly one of the following conditions is satisfied:

- $T$ is a rotation, and $\det T =1$
- $T$ is a reflection about a line through the origin, and $\det T= -1$

**Cor:** Any rigid motion on $\Bbb R^2$ is either a rotation followed by a translation or a reflection about a line through the origin followed by a translation.

### Householder Operators

**Def:** Let $V$ be a finite dimensional complex/real inner product space, and let $u$ be a unit vector in $V$. Define the **Householder** operator $H_u :V\to V$ by $H_u(x) = x-2\langle x, u\rangle u$ for all $x \in V$.
- $H_u$ is linear
- $H_u(x) = x$ iff $x$ is orthogonal to $u$
- $H_u(u) = -u$
- $H_u^* = H_u$ and $H_u^2 =I$, and hence $H_u$ is a unitary/orthogonal operator. If $V$ is real inner product space, then $H_u$ is a reflection.
- $\det H_u = -1$.
- $H_u$ has eigenvalues of $\pm 1$. We know that ${E(1, H_u) = \operatorname{span}(u)^\bot}$, and ${E(-1, H_u) = \operatorname{span}(u)}$.

This type of operator can be used to calculate the $QR$ factorization of ${n\times m}$ matrix, when $n \le m$.