---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Isometries in Vector Spaces]], [[Normal and Hermitian Operators]], [[Eigenspaces and Diagonal Matrices]], [[Orthogonal Bases]]
********Def:******** Suppose $U$ is a finite dimensional subspace of $V$. The ********orthogonal projection******** of $V$ onto $U$ is the operator $P_U \in \mathcal L(U)$ defined as follows: for $v \in V$, write $v = u +w$, where $u \in U$ and ${w \in U^\bot}$. Then $P_Uv = u$.

- Properties
    Suppose $U$ is a finite dimensional subspace of $V$ and ${v\in V}$. Then
    $P_U \in \mathcal L(U)$
    $P_U u =u$ for every $u \in U$
    $P_U w = 0$ for every $w \in U^\bot$
    $R(P_U) = U$
    $N(P_U) = U^\bot$
    $v - P_U v \in U^\bot$
    $(P_U )^2 = P_U$
    $\|P_U v\| \le \|v\|$
    for every orthonormal basis $e_1, \dots, e_m$ of $U$
    $$ P_U v = \sum_{k = 1}^m \langle v, e_k\rangle e_k $$
If $U$ is a finite dimensional subspace of $V$, $v \in V$ and $u \in U$. Then
$$ \|v-P_Uv\| \le \|v-u\| $$
Furthermore, the inequality above is an equality iff $u = P_U v$.

Def:************ Let $V$be an inner product space, and $T:V\to V$ be a projection. We say that $T$ is an orthogonal projection if ${R(T)^\bot = N(T)}$ and ${N(T)^\bot = R(T)}$.

In the case that $V$ is finite dimensional then we it’s only necessary one of the conditions.

********Th:******** Let $V$be an inner product space and ${T \in \mathcal L(V)}$. Then $T$ is an orthogonal projection iff $T$ has an adjoint and $T^2 =T = T^*$.

********Th:******** Let $V$ a finite dimensional inner product space, $W$ be a subspace of $V$, and $T$ be an orthogonal projection of $V$ on $W$. We can choose an orthonormal basis $\beta$ for $V$, where $\{v_i\}_{i = 1}^k \subseteq\beta$ is a basis for $W$. Then $[T]_\beta$ is a diagonal matrix with ones as the first $k$ diagonal entries and zero elsewhere.

$$ [T]_\beta = \begin{pmatrix} I_k & O_1 \\ O_2 & O_3 \end{pmatrix} $$

## The Spectral Theorem
Let $V$ be a finite dimensional inner product space over $\mathbb F$, and $T \in \mathcal L(V)$. Assume $T$ is normal if $\mathbb{F=C}$ and that $T$ is self-adjoint if $\mathbb{F=R}$. For each consider the set of eigenvalues of $T$ be the form $\{\lambda_i\}_{i = 1}^k$ , then for each ${1 \le i \le k}$, let $W_i = E(\lambda_i, T)$ and $T_i$ be the orthogonal projection of $V$ on $W_i$. Then

- $V = \bigoplus _{i = 1}^k W_i = \bigoplus _{i = 1}^k E(\lambda_i, T)$
- Let $W_j '$ be   $$ W_j' := \bigoplus^k_{\begin{subarray}{} i = 1 \\ i \ne j \end{subarray} } W_i $$
    then $W_j' = W_j ^\bot$    
- $T_iT_j = \delta_{ij} T_i$
- $I = \sum _{i = 1}^k T_i$
- $T = \sum_{i = 1}^k \lambda_i T_i$
    
**Def:** The set $\{\lambda_i \}_{i = 1}^k$ of the eigenvalues of $T$ is called the _********spectrum********_ of $T$, and sum $I = \sum_{i = 1}^k T_i$ is called the **resolution of the identity operator** induced by $T$, and the sum $T = \sum _{i = 1}^k \lambda_i T_i$ is called the **spectral decomposition** of $T$. The spectral decomposition of $T$ is unique up to the order of eigenvalues.

There’s a basis $\beta$ be the union of orthonormal bases of $W_i$, and ${m_i = \dim W_i}$. Then

$$ [T]_\beta = \begin{pmatrix} \lambda_1 I_{m_1} & O & \cdots & O \\ O & \lambda_2 I_{m_2} & \cdots & O \\ \vdots & \vdots & &\vdots \\ O & O& \cdots & \lambda_k I_{m_k} \end{pmatrix} $$

**Th:** Let $\sum_{i = 1}^k \lambda_i T_i$ be the spectral decomposition of $T$, then if ${g \in \mathcal P(\mathbb F)}$. Then $g(T) = \sum_{i = 1}^k g(\lambda_i) T$.

**Cor:** If $\mathbb{F =C}$, then $T$ is normal iff $T^* = g(T)$ for some polynomial $g$.

**Cor:** If $\mathbb{F =C}$, then $T$ is unitary iff $T$ is normal ${|\lambda|=1}$ for every eigenvalue of $T$.

**Cor:** If $\mathbb{F=C}$, then $T$ is self-adjoint iff $T$ is normal and every eigenvalue of $T$ is real.

**Cor:** Let $T$ be as in the spectral theorem with spectral decomposition ${T= \sum _{i = 1}^k \lambda_i T_i}$. Then each $T_j$ is a polynomial in $T$.

### Least Squares Approximation
********Th:******** Let $A \in \mathcal M_{m \times n} (\mathbb F)$ and $y \in \mathbb F^m$. Then there exists $x_0 \in \mathbb F^n$ such that $(A^* A)x_0 = A^* y$ and $\|A x_0 - y \| \le \|Ax -y\|$ for all $x \in \mathbb F^n$. Furthermore, if $\operatorname{rank}(A) = n$, then $x_0 =(A^* A)^{-1} A^* y$.

This matrix combination is the [[The Penrose Pseudoinverse]]

From this we can get the 

### Minimal Solutions to Systems of Linear Equations

**Def:** a solution $s$ to $Ax = b$ is called a **minimal solution** if $\|s\| \le \|u\|$ for all other solutions $u$.

********Th:******** Let $A \in \mathcal M_{m \times n} (\mathbb F)$ and $b \in \mathbb F^m$. Suppose that $Ax =b$ is consistent. Then the following statements are true.

- There exists exactly one minimal solution $s$ of $Ax =b$, and ${s \in R(L_{A^*})}$.
- The vector $s$ is the only solution to $Ax = b$ that lies in $R(L_{A^*})$; in fact, if $u$ satisfies $(AA^*)u = b$, then $s = A^* u$