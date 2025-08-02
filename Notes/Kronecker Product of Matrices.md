---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Tensor Product of Linear Functions]], [[Matrix Representation of Linear Transformations]]

**Prop:** Let $U$, $V$, $W$, and $Z$ be finite-dimensional $K$-vector spaces with basis $\beta$, $\gamma$, $\delta$ and $\theta$, respectively, and $T:U \to V$ and $S:W \to Z$ be linear operators. If $A =[a_{ij}]:= [T]_\beta^\gamma$ and $B := [S]_\delta^\theta$,respectively, then we can consider the basis $\beta \otimes \delta := \{u\otimes w \mid u\in \beta \ \land w\in \gamma\}$ of $U \otimes W$, and $\gamma \otimes \theta := \{v \otimes z \mid v\in \delta \ \land z\in \theta\}$  then $$[T\otimes S]_{\beta \otimes \delta}^{\gamma\otimes \theta} = \begin{pmatrix}
a_{11}B & a_{12}B &\cdots & a_{1n }B \\
a_{21}B & a_{22}B &\cdots&a_{2n}B \\
\vdots&\ddots&&\vdots\\
a_{m1}B &a_{m2}B&\cdots&a_{mn}B
\end{pmatrix}
$$
**Def:** Let $A$ be a $m \times n$ matrix, and $B$ be $k \times \ell$ matrix, both with entries over $K$, then we define the *Kronecker product* of $A$ and $B$ as $$A \otimes B := \begin{pmatrix}
a_{11}B & a_{12}B &\cdots & a_{1n }B \\
a_{21}B & a_{22}B &\cdots&a_{2n}B \\
\vdots&\vdots&&\vdots\\
a_{m1}B &a_{m2}B&\cdots&a_{mn}B
\end{pmatrix}$$
Note that $A\otimes B$ is a $mk \times n\ell$ matrix over $K$. Lastly, if we ever need to consider $A \otimes A \otimes \dots \otimes A$, $n$ times, we are gonna use the notation $A ^{\otimes n}$. 

**Prop:** Let $A$ and $B$ be matrices over $K$, then $\text{Tr}(A \otimes B) = \text{Tr}(A) \text{Tr}(B)$. 

**Cor:** Let $A$ be a matrix over $K$ and $n \in \Bbb N ^+$, then $\text{Tr}(A^{\otimes n}) = (\text{Tr}(A))^n$.

**Prop:** Let $A$ and $B$ be two diagonalizable matrices, then $A \otimes B$ is also diagonalizable, in fact, its eigenvalues are $\{\lambda_i \mu_j \mid 1 \le i \le n \ \land \ 1 \le j \le m\}$ where $\{\lambda_i \mid i \le i \le n \}$ and $\{\mu_j \mid 1 \le j \le m\}$ are the set of all eigenvalues of $A$ and $B$ respectively. Even more so, If $\{v_i \mid i \le n\}$ and $\{w_j \mid 1 \le j \le m\}$ be the eigenvalues of $A$ and $B$, respectively, then $\{v_i \otimes  w_j \mid 1 \le i \le n \ \land \ 1 \le j \le m\}$ is the set of eigenvectors of $A \otimes B$.

