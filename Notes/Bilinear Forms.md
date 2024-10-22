---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Dual Spaces]], [[Tensor Product]]

**Def:** Let $V$ be a vector space over a field $\mathbb F$. A function ${H:V\times V\to \mathbb F}$ is called a **bilinear form** on $V$ if $H$ is linear in each variable when the other variable is held fixed. That is

- $H(ax_1+x_2, y) = aH(x_1, y)+H(x_2, y)$ for all $x_1, x_2, y \in V$ and $a \in \mathbb F$.
- $H(x, ay_1+y_2) = aH(x, y_1)+H(x, y_2)$ for all $x, y_1, y_2 \in V$ and $a \in \mathbb F$.

The set of all bilinear forms on $V$ is denoted by $\mathcal B(V)$ or $\mathcal T^2(V)$, not to confuse with ${T^2 V= V^{\otimes 2}}$.

- Properties for any bilinear form $H \in \mathcal B(V)$
    
    For any $x \in V$, the functions $L_x, R_x: V \to \mathbb F$ are defined by
    
    $$ L_x(y) = H(x,y) \quad \text{ and }\quad R_x(y)= H(y,x) $$
    
    Then $L_x, R_x \in V'$
    
    $H(0, x) = H(x, 0) = 0$ for all $x \in V$
    
    If $J :V\times V \to \mathbb F$, such that $J(x,y) = H(y,x)$ then $J$ is a bilinear form, in particular we say that $J(x, y) = {^\top H(x,y)}$ and it’s said to be $H$’s transpose.
    

**********Def:********** Let $V$a vector space, let $H_1$ and $H_2$ be bilinear forms on $V$, and let $\lambda$ be a scalar. We define the ***_sum $H_1 + H_2$_ and the **************_scalar product $\lambda H_1$_ by the equations

$$ (H_1+H_2)(x,y) = H_1 (x,y)+H_2(x,y) $$

and

$$ (\lambda H_1)(x, y) = \lambda( H_1(x, y)) $$

**Def:** For any vector space $V$, the sum of two bilinear forms and the product of a scalar and a bilinear form on $V$ are again bilinear forms on $V$. Furthermore, $\mathcal B(V)$ is a vector space with respect to this operations.

**Def:** Let $\beta = \{v_i\}_{i = 1}^n$ be an ordered basis for an $n-$dimensional vector space $V$, and let $H \in \mathcal B(V)$. We can associate with $H$ an $n\times n$ matrix $A$ whose entry in row $i$ and column $j$ is defined by

$$ A_{ij} = H(v_i, v_j) $$

This matrix $A$ is called the ****matrix representation**** of $H$ with respect to the ordered basis $\beta$ and is denoted as $\psi_\beta(H)$.

********Th:******** For any $n-$dimensional vector space $V$over $\mathbb F$ and any ordered basis $\beta$ for $V$, $\psi_\beta:\mathcal B(V) \to \mathcal M_n(\mathbb F)$ is an isomorphism.

**Cor:** For any $n-$dimensional vector space $V$, $\mathcal B(V)$ has dimension $n^2$.

**Cor:** Let $V$ be an $n-$dimensional vectors over $\mathbb F$ with ordered basis $\beta$. If $H \in \mathcal B(V)$ and $A \in \mathcal M_n(\mathbb F)$, then $\psi_\beta(H) = A$ iff ${H(x, y) = [\phi_\beta(x)]^\top A[\phi_\beta(y)]}$, where $\phi_\beta$ is the isomorphism of $V$ onto $\mathbb F^n$ with respect to to the ordered basis $\beta$.

**Cor:** Let $\mathbb F$ be a field, $n \in \Bbb N^+$, and $\beta$ be the standard basis for $\mathbb F^n$. Then for any $H \in \mathcal B(\mathbb F^n)$, there exists a unique matrix $A\in \mathcal M_n(\mathbb F)$, namely, $A = \psi_\beta(H)$, such that

$$ H(x,y) = x^\top Ay $$

**Def:** Let $A, B \in \mathcal M_n(\mathbb F)$. Then $B$ is said to be **congruent to $A$ is there exists an invertible matrix $Q \in \mathcal M_n(\mathbb F)$ such that $B = Q^\top AQ$.

This is an equivalence relation on $\mathcal M_n(\mathbb F)$.

**Th:** Let $V$ be a finite dimensional vector space with ordered bases ${\beta = \{v_i\}_{i = 1}^n}$ and ${\gamma = \{w_i\}_{i= 1}^n}$, and let $Q$ be the change of coordinate matrix changing $\gamma-$coordinates and $\beta-$coordinates. Then for any ${H \in \mathcal B(V)}$, we have $\psi_\gamma(H) = Q^\top\psi_\beta(H) Q$. Thus $\psi_\gamma(H)$ and $\psi_\beta(H)$ are congruent.

**Cor:** Let $V$ be an $n-$dimensional vector space with ordered basis $\beta$, and let $H \in \mathcal B(V)$. For any $n \times n$ matrix $B$, if $B$ is congruent to $\psi_\beta(H)$, then there exists an ordered basis $\gamma$ for $V$ such that ${\psi_\gamma (H)=B}$. In this case, if $Q$ is a matrix such that ${B = Q^\top \psi_\beta(H)Q}$, then $Q$ changes $\gamma-$coordinates into $\beta-$coordinates.

We can think of elements from $\mathcal B(V)$ as linear functions form ${V\otimes V}$ to $\mathbb F$. Thus $\mathcal B(V)$ is isomorphic to $(V \otimes V)'$. In the case that $V$ is finite dimensional, then there’s a canonical isomorphism between $(V\otimes V)'$ and $V' \otimes V'$.

## Symmetric Bilinear Forms

**Def:** A bilinear form $H$ on a vector space $V$ is **symmetric** if ${H(x,y) = H(y,x)}$ for all $x, y \in V$.

********Th:******** Let $H$ be a bilinear form on a finite dimensional vector space $V$, and let $\beta$ be an ordered basis for $V$. Then $H$ is symmetric iff $\psi_\beta(H)$ is symmetric.

**Def:** A bilinear form $H$ on a finite dimensional vector space $V$ is called **diagonalizable** if there is an ordered basis $\beta$ for $V$ such that $\psi_\beta(H)$ is a diagonal matrix.

**Cor:** Let $H$ be a diagonalizable bilinear form on a finite dimensional vector space $V$. Then $H$ is symmetric.

**************Lemma:************** Let $H$ be a nonzero symmetric bilinear form on a vector space $V$ over a field $\mathbb F$ not of characteristic $2$. Then there is a vector $x \in V$ such that $H(x,x) \ne 0$.

********Th:******** Let $V$ be a finite dimensional vector space over a field $\mathbb F$ not of characteristic $2$. Then every symmetric bilinear form on $V$ is diagonalizable.

**Cor:** Let $\mathbb F$ be a field that is not of characteristic $2$. If $A \in \mathcal M_n(\mathbb F)$ is a symmetric matrix, then $A$ is congruent to a diagonal matrix.

**Def:** A bilinear form $H$ such that for all $x, y \in V$, ${H(x,y) = -H(y,x)}$, then is called **skew-symmetric** or **antisymmetric**.

********Th:******** If $V$ is vector space over the field $\mathbb F$ not with characteristic $2$. Then one can decompose a bilinear form into a symmetric and skew-symmetric parts

$$ B^+ = \frac{1}{2}(B + {^\top B}) \qquad B^- = \frac{1}{2}(B-{^\top B}) $$

### Diagonalizing Symmtric Matrices

Let $A$ be an $n \times n$ matrix with entries from a field $\Bbb F$ not of characeristic $2$. There are matrices $Q, D \in \cal M_{n}(\Bbb F)$ such that $Q$ is invertible, and $D$ diagonal such that ${Q^\top A Q=D}$.

If $E$ is an elementary matrix, $AE$ can be obtained by performing an elementary column operation on $A$. $E^\top A$ can be obtained by performing the same operation on the rows of $A$ rather than the column. Thus $E^\top A E$ can be obtained by first applying the operations into the columns and then to the rows of $AE$. Suppose that $Q$ is an invertible matrix and $D$ a diangonal matrix such that $Q^\top A Q$, then $Q$ is a product of invertible matrices say ${Q= E_1 E_2\cdots E_p}$, we get that

$$ D =Q^\top AQ = E_p ^\top \cdots E_2^\top E_1^\top AE_1 E_2\cdots E_p $$

Getting a diagonalization of $A$ using only elementary operations.
### Sylvester’s Law of Inertia

Let $H$ be a symmetric bilinear form on a finite dimensional real vector space $V$. Then the number of positive diagonal entries and the number of negative diagonal entries in any diagonal matrix representation of $H$ are each independent of the diagonal representation.

**Def:** The number of positive diagonal entries in a diagonal representation of a symmetric bilinear form on a real vector space is called the **index** of the form. The difference between the number of positive and the number of negative diagonal entries in a diagonal representation of a symmetric bilinear form is called the **signature** of the form. The three terms **rank, index** and **signature** are called the **invariants** of the bilinear form because they are invariant with respect to matrix representations. These same terms apply to the associated quadratic form. Notice that the values of any two of these invariants determine the value of the third.

### Sylvester’s Law of Inertia for Matrices

Let $A$ be real symmetric matrix. Then the number of positive diagonal entries and the number of negative entries and the number of diagonal entries in any diagonal congruent to $A$ is independent of choice of the diagonal matrix.

**Def:** Let $A$ be real symmetric matrix, and let $D$ be a diagonal matrix that is congruent to $A$. The number of positive diagonal entries of $D$ is called the **index** of $A$. The difference between the number of positive diagonal entries and the number of negative diagonal entries of $D$ is called the **signature** of $A$. As before, the **rank, index,** and **signature** of a matrix are called the **invariants** of the matrix, and the values of any two of these invariants determine the value of the third.

**Cor:** Two real symmetric $n\times n$ matrices are congruent iff they have the same invariants.

**Cor:** A real symmetric $n\times n$ matrix $A$ has index $p$ and rank a $r$ iff $A$ is congruent to $J_{pr}$, where $J_{pr}$ is defined as

$$ J_{pr} := \begin{pmatrix} I_p & O & O \\ O & -I_{r-p} & O \\ O& O& O \end{pmatrix} $$