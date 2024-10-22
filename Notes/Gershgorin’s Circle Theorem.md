---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]
Links: [[Eigenvalues]]
**********Def:********** Let $A \in \cal M_n (\mathbb C)$ for ${1 \le i, j \le n }$, define $\rho_i(A)$ to be the sum of the absolute values of the entries of row $i$ of $A$, and define $\nu_j(A)$ to be equal to the sum of the absolute value of the entries of column $j$ of $A$. Thus

$$ \rho_i (A) = \sum_{j = 1}^n |A_{ij}| \qquad \text{for }1\le i \le n $$

and

$$ \nu_j(A) = \sum_{i =1}^n |A_{ij}| \qquad \text{for }1\le j\le n $$

The ********row sum******** of $A$ denoted as $\rho (A)$, and the _column sum_ of $A$, denoted as $\nu (A)$ are defined as

$$ \rho(A) = \max_{1\le i \le n} \rho_i(A)\qquad \text{ and }\qquad \nu(A) = \max_{1\le j \le n} \nu_j(A) $$

**********Def:********** For a matrix $A \in \mathcal M_n(\mathbb C)$, we define the $i$th ***_Gershgorin disk $C_i$_ to be the disk in the disk in the complex plane with center $A_{ii}$ and radius ${r_i = \rho_i(A) - |A_{ii}|}$, that is

$$ C_i = \{z \in \mathbb C\mid |z - A_{ii}| \le r_i\} $$

### Gershgorin’s **************Circle Theorem**************

Let $A \in \mathcal M_n(\mathbb C)$. Then every eigenvalue of $A$ is contained in Gershgorin disk.

**********Cor:********** Let $\lambda$ be an eigenvalue of $A \in \mathcal M_n(\mathbb C)$, then

$$ |\lambda | \le \min\{\rho(A) , \nu(A)\} $$

********Cor:******** If $\lambda$ is an eigenvalue of a transition matrix then $|\lambda| \le 1$