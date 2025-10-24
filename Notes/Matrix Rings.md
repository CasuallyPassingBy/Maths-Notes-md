---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Rings and Fields]]

Let $R$ be a ring and $n$ be a positive integer. Let $\mathcal M_n (R)$ be the set of all $n \times n$ *matrices with entries from $R$*. The element $(a_{ij})$ of ${\cal M}_n(R)$ is an $n \times n$ square array of elements of $R$ whose whose entry in row $i$ and column $j$ is $a_{ij}\in R$. 

We define addition componentwise: the $i, j$ entry if the matrix $(a_{ij}) + (b_{ij})$ is $a_{ij} + b_{ij}$. The $i, j$ entry of the matrix product $(a_{ij}) \times (b_{ij})$ is $$ \sum_{k = 1}^n a_{ik} b_{kj}.$$
**Obs:** Note that if $R$ is any nontrivial ring and $n \ge 2$ then ${\cal M}_n(R)$ is *not commutative*. We can also show that ${\cal M}_n(R)$ has zero divisors for all nonzero rings $R$ whenever $n \ge 2$.

**Def:** An element $(a_{ij}) \in {\cal M}_n(R)$ is called a *scalar matrix* if for some $a\in R$, $a_{ij} = a \delta_{ij}$  for all $i,j\in \{1,\dots, n\}$, where $\delta_{i, j}$ is the Kronecker delta. }

The set of scalar matrices is a subring of ${\cal M}_n(R)$. This means that $R \hookrightarrow {\cal M}_n(R)$. 

**Prop:** Let $R$ be unital ring. Let $n \in \Bbb N^+$ and let $A\in {\cal M}_n(R)$ whose $i, j$ entry is $a_{ij}$. Let $E_{ij}$ be element of ${\cal M}_n(R)$ whose $i,j$ entry is $1$ and whose other entries are $0$.
- $E_{ij} A$ is the matrix whose $i$th row equals the $j$th row of $A$ and all other rows are zero. 
- $AE_{ij}$ is the matrix whose $j$th column equals the $i$th column of $A$ and all other rows are zero. 
- $E_{pq}AE_{rs}$ is the matrix whose $p,s$ entry is $a_{qr}$ and all other entries are zero. 

**Prop:** If $R$ is commutative, then the scalar matrices are the centre of ${\cal M}_n(R)$.

**Prop:** If $R$ is unital, then the the scalar matrix with $1$'s down the diagonal, the identity matrix, is the $1$ of ${\cal M}_n(R)$. 

In the case where $R$ is unital, the units in ${\cal M}_n(R)$ are the invertible $n\times n$ matrices and the group units is denoted $\text{GL}_n(R) = \text{GL}(n, R)$ the *[[general linear group]] of degree $n$ over $R$.*

**Obs:** If $S$ is a subring of $R$, then ${\cal M}_n(S)$ is also a subring of ${\cal M}_n(R)$. 

**Prop:** Every two-sided [[Ring Ideals and Quotient Rings|ideal]] of ${\cal M}_n(R)$ is equal to ${\cal M}_n(J)$ for some two-sided ideal $J$ of $R.$ 

**Cor:** If $F$ is a field, then ${\cal M}_n(F)$ is [[Simple Rings|simple]]. 

**Prop:** Let $R$ be a ring with identity $1\neq 0$. If $L_j$ is the left ideal of ${\cal M}_n(R)$ consisting of arbitrary entries in the $j$th column and zero in all other entries, then $L_j = {\cal M}_n(R) E_{ij}$ for any $i$. 