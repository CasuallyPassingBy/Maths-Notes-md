---
tags:
  - NumberTheory
---
Subjects: [[Elementary Number Theory]]
Links: [[Integers modulo n]], [[Legendre Symbols]], [[Quadratic Congruences]], [[Polynomials in Several Variables over a Field]], [[Quadratic Forms]], [[Matrix Representation of Linear Transformations]]

**Def:** A polynomial in several variables is called a *form*, it is said to be *homogeneuous* if all its monomial terms have the same degree. A form of degree $2$ is called a *quadratic* form. Thus the general quadratic form is a sum of the form  $$\sum_{i, j= 1} a_{ij} x_ix_j .$$A form in two variables is called *binary*. We are gonna study forms  $$f(x, y) = ax^2+bxy+cy^2 $$with integral coefficients. 

The *discriminant* of a binary quadratic form is the quantity $d = b^2-4ac$. 

**Prop:** If $d$ is a perfect square, then $f(x, y)$ can be expressed as a product of two linear forms with integral coefficients. Conversely, if $d$ is not a perfect square, then $f(x, y)$ cannot be written as a product of two linear forms with integral coefficients, nor even with rational coefficients. 

**Th:** Let $f(x, y) = ax^2+ bxy + cy^2$ be a binary quadratic form with integral coefficients and discriminant $d$. if $d\neq  0$ and $d$ is not a perfect square, then $a\neq 0$, $c\neq 0$, and the only solution of the equation $f(x,y ) = 0$ in integers is given by $x =  y =0$. 

**Def:** A form $f(x, y)$ is called indefinite if it takes on both positive and negative values. The form positive semidefinite (or negative semidefinite) if $f(x, y) \ge 0$ (or $f(x, y) \le 0$) for all integers $x, y$. A semidefinite form is called a definite if in additions the only integers $x, y$ for which $f(x, y) = 0$ are $x =y = 0$. 

**Th:** Let $f(x, y) = ax^2 +bxy + cy^2$ be a binary quadratic form with integral coefficients and discriminant $d$. If $d >0$ then $f(x, y)$ is indefinite. If $d = 0$, then $f(x,y)$ is semidefinite but not definite. If $d <0$ then $a$ and $c$ have the same sign and $f(x, y)$ is either positive or negative definite according as $a>0$ or $a<0$. 

**Th:** Let $d$ be a given integer. There exists at least one binary quadratic form with integral coefficients and discriminant $d$, iff $d \equiv 0, 1\pmod 4$. 

**Def:** We say that a quadratic form $f(x, y)$ represents an integer $n$ if there exists integers $x$ and $y$ such that $f(x,y) = n$, Such a representation is proper if $(x, y) = 1$; otherwise it is *improper*. 

**Obs:** If $f(x, y) = n$ and $(x, y) = g$, then $g^2 \mid n$. Thus the representation of $n$ by $f$ may be found by determining the proper representation of $n/g^2$ for those integers $g$ such that $g^2\mid n$.

**Th:** Let $n$ and $d$ be given integers with $n \ne 0$. There exists a binary quadratic form of discriminant $d$ that represents $n$ properly iff only the congruence $x^2 \equiv d \pmod{4|n|}$ has a solution. 

**Cor:** Suppose that $d\equiv 0\pmod 4$. If $p$ is an odd prime, then there is a binary quadratic form of discriminant $d$ that represents $p$ iff $p \mid d$ or $\left(\dfrac dp\right) = 1$. 

**Th:** Let $M$ be a $2\times 2$ matrix with real entries. Then the following two assertions are equivalent:
- Th induced linear transformation of $M$ defines a permutation of lattice points, $\Bbb Z^2$ (lattice points are mapped to themselves in a one-to-one and onto manner);
- the matrix $M$ has integral coefficients and $\det M = \pm 1$. 

**Def:** The group of $2\times 2$ matrices with integral elements and determinant $1$ is denoted by $\Gamma$, and is called the *modular group*. 

**Def:** the quadratic forms $f(x, y) = ax^2+bxy+cy^2$ and $g(x, y) = Ax^2+ Bxy+Cy^2$ are equivalent, and write $f\sim g$ if there is an $M \in \Gamma$ such that $g(x) = f(Mx)$. In this case we say that $M$ takes $f$ to $g$.

We can write the quadratic form $f(x, y) = ax^2+bxy +c^2$ as $$\begin{pmatrix}x & y\end{pmatrix}\begin{pmatrix}a & b/2 \\ b/2 & c\end{pmatrix}\begin{pmatrix}x \\ y\end{pmatrix}$$Thus the equivalence of quadratic forms can be made clearer by phrasing it like this. Let $f$ and $g$ be quadratic forms with matrices $A$ and $B$ be symmetric matrices that induce them. Then $f$ is equivalent to $g$ iff there is a matrix $M$ of the modular group $\Gamma$ such that $M^\top A M = B$. 

**Th:** The notion of equivalence of quadratic forms is an equivalence relation.

**Th:** Let $f$ and $g$ be equivalent binary quadratic forms. For any integer $n$, the representations of $n$ by $f$ are in one-to-one correspondence with the representation of $n$ by $g$. Also, the proper representation of $n$ by $f$ are in one-to-one correspondence with a proper representation of $n$ by $g$. Moreover, the discriminant of $f$ and $g$ are equal. 

**Def:** Let $f$ be a binary quadratic form whose discriminant $d$ is not a perfect square. We call $f$ *reduced* if $$-|a| < b \le |a| < |c| \quad \text{or}\quad 0\le b \le |a| = |c|. $$
**Th:** Let $d$ be a given integer, which is not perfect square. Each equivalence class of binary quadratic forms of discriminant $d$ at least one reduced form.