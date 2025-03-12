---
tags:
  - LinearAlgebra
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]], [[Linear Algebra]]
Links: [[Bases and Dimension]], [[Exterior Algebra of Multicovectors]], [[Exterior Algebra]], [[Local and Global Sections of Vector Bundles]]

# Vector Spaces

**Def:** Two ordered bases $u = [u_1 \cdots u_n]$ and $v = [v_1 \cdots v_n]$ of a vector space $V$ are said to be *equivalent*, written $u  \sim v$, if $u = vA$ for an $n \times n$ matrix $A$ with positive determiant. An *orientation* of $V$ is an equivalence class of ordered bases. 

Any finite-dimensional vector spaces $V$ has two orientations. if $\mu$ is an orientation of a finite-dimensional vector space $V$, we denote the other orientation $-\mu$ and call it the *opposite* orientation of $\mu$. 

**Lemma:** Let $u_1, \dots, u_n$ and $v_1, \dots, v_n$ be vectors in a vector space $V$. Suppose $$ u_j = \sum_{i = 1}^n v_i a^i_j, \quad j = 1, \dots, n,$$for a matrix $A = [a^i_j]$ of real numbers. $\beta$ is an $n$-covector in $V$, then $$\beta(u_1, \dots, u_n) = (\det A) \beta(v_1, \dots, v_n)$$

**Cor:** If $u_1, \dots, u_n$ and $v_1, \dots, v_n$ are ordered bases of a vector space $V$, then $\beta(u_1, \dots, u_n)$ and $\beta(v_1, \dots, v_n)$ have the same sign iff $u_1, \dots, u_n$ and $v_1, \dots, v_n$ are equivalent ordered bases.

**Def:** We say that the $n$-covector $\beta$ *determines* or *specifies* the orientation $(v_1, \dots, v_n)$ if $\beta(v_1, \dots, v_n)>0$ . 

**Obs:** Two $n$-covectors $\beta$ and $\beta'$ on $V$ determine the same orientation iff $\beta = a\beta'$ for some positive real number $a$. 

**Def:** We define an equivalence relation on the nonzero $n$-covectors on the $n$-dimensional vector space $V$ by setting $\beta \sim \beta'$ iff for some $a > 0$, $\beta = a \beta'$. Thus an orientation is not only an equivalence class of ordered bases, but an equivalence class on nonzero $n$-covectors on $V$.

**Obs:** Since ${\textstyle \bigwedge}^n(V^*) \cong \Bbb R$, then the set of nonzero $n$-covectors on $V$ can be identified with $\Bbb R^\times$, which has two connected components. Two nonzero $n$-covectors $\beta$ and $\beta'$ are in the same component iff $\beta \sim \beta'$ with the same equivalence relation as above. Thus, each connected component of ${\textstyle \bigwedge}^n(V^*)\setminus \{0\}$ determines an orientation of $V$.

# Smooth Manifolds

**Def:** We introduce an equivalence relation on frames on $U$: $$(X_1, \dots, X_n) \sim (Y_1, \dots, Y_n) \iff (X_{1, p}, \dots, X_{n, p}) \sim (Y_{1, p}, \dots, Y_{n, p})\;\;\;\; \text{ for all }p\in U.$$ In other words, if $Y_j = \sum_i a ^i_j X_i$ then two frames $(X_1, \dots, X_n)$ and $(Y_1, \dots, Y_n)$ are equivalent iff the change of basis matrix $A = [a^i_j]$ has positive determinant at every $p\in U$. 

**Def:** A *pointwise orientation* on a manifold $M$ assigns to each $p \in M$ an orientation $\mu_p$ of the tangent space $T_p M$. 