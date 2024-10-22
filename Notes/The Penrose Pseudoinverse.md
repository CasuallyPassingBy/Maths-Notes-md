---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Singular Value Decomposition]], [[Isomorphism of Vector Spaces#Invertibility|Invertibility]], [[Gram Matrices]]

**Def:** Let $V$ and $W$ be a finite dimensional inner product spaces over the same field, and $T \in \mathcal L(V, W)$. Let $L \in \mathcal L(N(T)^\bot, R(T))$ defined by ${Lx =Tx}$ for all $x \in N(T)^\bot$, $L = T|_{N(T)^\bot}$. The **pseudoinverse** or Moore-Penrose generalized inverse of $T$, denoted by $T^+$, is defined by the unique linear transformation from $W$ to $V$ such that

$$ T^+ y = \begin{cases} L^{-1} y & \text{for }y \in R(T)\\ 0 & \text{for } y \in R(T)^\bot

\end{cases} $$

For $x \in N(T)^\bot$ , $T^+ Tx = x$.

********Th:******** Suppose that $V$ and $W$ are finite dimensional vector spaces and ${T \in \mathcal L(V,W)}$ is a linear transformation of rank $r$. Let $\{v_i\}_{i = 1}^n$ and $\{u_i\}_{i=1}^m$ be orthonormal bases for $V$ and $W$, respectively, and let ${\sigma_1 \ge \sigma_2 \cdots \ge \sigma_r}$ be nonzero singular values of $T$ satisfying The singular value decomposition for linear transformations. Then ${\{v_i\}_{i=1}^r}$ is a basis for $N(T)^\bot$, $\{v_i\}_{i = r+1}^n$ is a basis for $N(T)$, $\{u_i\}_{i= 1}^r$ is a basis for $R(T)$, and $\{u_i\}_{i =r+1}^m$ is a basis for $R(T)^\bot$. Let $L = T|_{N(T)^\bot}$, as the definition of pseudoinverse. Then ${L^{-1}u_i = \frac{1}{\sigma_i} v_i}$, for $1 \le i \le r$. Therefore

$$ T^+ u_i = \begin{cases} \frac{1}{\sigma_i} v_i & \text{if } 1 \le i \le r \\ 0 & \text{if } r <i \le m \end{cases} $$

### Penrose Conditions for Linear Transformations

Let $V$ and $W$ be finite dimensional inner product spaces, and ${T \in \mathcal L(V, W)}$ and $U \in \mathcal L(W, V)$ such that $TUT =T$, ${UTU = U}$ and both $UT$ and $TU$ are self-adjoint, then $U = T^+$

**Def:** Let $V$ and $W$ be a finite dimensional inner product spaces, and let $T \in \mathcal L(V, W)$. Then

- If $T$ is injective, then $T^* T$ is invertible and $T^+ = (T^*T)^{-1}T^*$, in this particular case $T^+$ is a left inverse of $T$.
- If $T$ is surjective, then $TT^*$ is invertible and ${T^+ = T^* (TT^*)^{-1}}$, in this particular case $T^+$ is a right inverse of $T$.

**Def:** Let $A$ be $m \times n$ matrix. Then there exists a unique $n \times m$ matrix $B$ such that $(L_A)^+ \in\mathcal L(\mathbb{F^m,F^n})$ is equal to the left-multiplication transformation $L_B$. We call $B$ the **pseudoinverse** of $A$ and denote it $B = A^+$. Thus

$$ (L_A)^+ = L_{A^+} $$

********Th:******** Let $V$ and $W$ be a finite dimensional inner product spaces with orthonormal bases $\beta$ and $\gamma$, respectively, and $T \in \mathcal L(V, W)$. Then ${([T]_\beta^\gamma)^+ = [T^+]_\beta^\gamma}$.

********Th:******** Let $A$ be an $m \times n$ matrix of a rank $r$ with a singular value decomposition of $A = U\Sigma V^*$ and nonzero singular values ${\sigma_1 \ge \sigma_2 \cdots \ge \sigma_r}$. Let $\Sigma^+$ be the $n \times m$ matrix defined by

$$ \Sigma^+ _{ij} = \begin{cases} \frac{1}{\sigma_i} & \text{if } i = j \le r \\ 0 & \text{otherwise} \end{cases} $$

Then $A^+ = V \Sigma^+ U^*$, and this is a singular value decomposition of $A^+$.

Let $A$ be an $m \times n$ matrix, then

- $(A^\top)^+ = (A^+)^\top$
- $(\overline A)^+ = \overline{A^+}$
- $(A^*)^+ = (A^+)^*$

Let $A$ be a $m \times n$ matrix, then

- If the columns of $A$ are linearly independent then $A^* A$, and $A^+$ can be calculated as $A^+ = (A^*A)^{-1}A^*$. In this case $A ^+$ is a left inverse of $A$
- If the rows of $A$ are linearly independent then $AA^*$is invertible and $A^+$ can be calculated as $A^+ = A(AA^*)^{-1}$. In this case $A ^+$ is a right inverse of $A$

### Penrose Conditions for Matrices
Let $A$ be an $n \times m$ matrix, and $B$ be an $m \times n$ matrix such that ${ABA = A}$, $BAB=B$, and both $AB$ and $BA$ are self-adjoint. Then $B = A^+$.

********Th:******** Let $V$ and $W$ be finite dimensional inner product spaces, and let ${T \in \mathcal L(V, W)}$. Then

- $T^+ T$ is the orthogonal projection of $V$on $N(T)^\bot$
- $TT^+$ is the orthogonal projection of $W$ on $R(T)$

********Th:******** Consider the system of linear equations $Ax = b$, where $A$ is an $m \times n$ matrix $b \in \mathbb F^m$. If $z = A^+ b$, then $z$ has the following properties

- If $Ax = b$ is consistent, then $z$ is the unique solution to the system to the system having minimum norm. That is, $z$ is a solution to the system, and if $y$ is any solution to the system, then ${\|z\| \le \|y\|}$ with equality iff $z = y$

- If $Ax = b$ is inconsistent, then $z$ is the unique best solution to a solution having minimum norm. That is ${\|Az -b \| \le \|Ay-b\|}$ for any $y \in \mathbb F^n$, with equality iff $Az = Ay$. Furthermore, if $Az=Ay$, then $\|z\| \le \|y\|$ with equality iff $z =y$.