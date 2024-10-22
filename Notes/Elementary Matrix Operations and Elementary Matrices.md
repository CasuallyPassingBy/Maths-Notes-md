---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Space of Linear Transformations]], [[Matrix Representation of Linear Transformations]]

**********Def:********** Let $A \in \mathcal M_{m \times n }(\Bbb F)$. Any one of the following three operations on the rows (columns) of $A$ is called an **********************elementary row (column) operation:**********************

1. interchanging any two rows (columns) of $A$
2. multiplying any row (column) of $A$ by a nonzero escalar
3. adding any scalar multiple of a row (column) of $A$ to another row (column)

Any of these three operations is called an ********************elementary operation********************. Elementary operations are of type $1$, type $2$ and type $3$ depending on weather they are obtained by $(1)$, $(2)$ and $(3)$

**********Def:********** An $n \times n$ _**********elementary matrix**********_ is a matrix obtained by performing operation on $I_n$. The elementary matrix is said to be _**type**_ $1$, $2$ or $3$ according to weather the elementary operation performed on $I_n$ is a type $1$, $2$ or $3$ operations respectively.

**********Th:********** Let $A \in \cal M_{m \times n }(\Bbb F)$, and suppose that $B$ is obtained from $A$ by performing an elementary row (column) operation. Then there exists an $m \times m$ ($n \times n$) elementary matrix $E$ such that ${B = EA}$ ( $B= AE$). In fact, $E$ is obtained from $I_m$ ($I_n$) by performing the same elementary row (column) operation as that which was performed on $A$ to obtain $B$. Conversely, if $E$ is an elementary $m \times m$ ($n \times n$ ) matrix, then $EA$ ($AE$) is the matrix obtained from $A$ by performing the same elementary row (column) operation as that which produces $E$ from $I_m$ $(I_n)$

**********Th:********** Elementary matrices are invertible, and the inverse of an elementary matrix is an elementary matrix of the same type.