---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Normal and Hermitian Operators]], [[Inner Products and Norms]], [[Singular Value Decomposition#Positive Definite Matrix|Positive Definite Matrix]], [[Orthogonal Projections and Spectral Theorem]]

**Def:** Let $V$ be an inner product space, and let $v_1, \dots, v_n \in V$. We can define the **************Gram Matrix********* or the *Gramian matrix* as the $G \in \cal M_n(\Bbb F)$, $G_{ij} = \langle v_i, v_j\rangle$.

**************Prop:************** A set of vectors linearly independent iff the determinant of the Gram matrix is nonzero.

### Properties
- It is Hermitian
- It is positive semidefinite
- We can decompose $M$ into $B^*B$, where $B \in \cal M_{k\times n}(\Bbb F)$, where $k = \operatorname{rank}(M)$, then the columns $b^{(1)}, \dots,b^{(n)}$ of $B$ can be seen as $n$ vectors in $\Bbb F^k$. Then    $$ M_{ij} = b^{(i)} \cdot b^{(j)} $$
    Thus a Hermitian matrix $M$ is positive semidefinite iff it is the Gram matrix of those vectors $b^{(1)}, \dots, b^{(n)}$. Such vectors are called a **realisation** of $M$. The realisation vectors are unique up to isometries
    
The determinant of the Gram matrix is
$$ |\det(G(v_1, \dots, v_n) )| = \|v_1 \wedge\cdots\wedge v_n\|^2 $$
