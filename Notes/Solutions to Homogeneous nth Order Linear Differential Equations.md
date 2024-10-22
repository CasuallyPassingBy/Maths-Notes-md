---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[nth Order Linear Differential Equations]], [[Solutions to Homogeneous Second Order Linear Differential Equations]], [[Null Space and Range]], [[Bases and Dimension]]

The equation

$$ L[y] =y^{(n)} + \sum_{k = 0}^{n-1}p_k y^{(k)}=0 $$

If the functions $y_1, \dots, y_n$ are solutions, then it follows that if $y \in \operatorname{span}\{y_1, \dots, y_n\}$ is also a solution of $L[y] =0$. We want to find constants $c_1, \dots, c_n$ such that we can satisfy the initial conditions namely, so that the equations

$$ \begin{align*} \sum_{k = 1}^n c_ky_k(t_0) &= y_0 \\ \sum_{k = 1}^n c_ky'_k(t_0) &= y'_0 \\ &\vdots \\ \sum_{k = 1}^n c_ky^{(n-1)}_k(t_0)&= y_0^{(n-1)} \end{align*} $$

are satisfied. This equations can be solved iff the determinant of the coefficients is nonzero, then it is always possible to choose values of $y_0, y_0', \dots, y_0^{(n-1)}$, so that it always have solution.

### Wronskian

We define the _**Wronskian**_ of $y_1, \dots, y_n$ as

$$ W(y_1, \dots, y_n) = \det \begin{pmatrix} y_1 & y_2 & \dots & y_n\\ y'_1 & y'_2 & \dots & y'_n\\ \vdots & \vdots & & \vdots\\ y^{(n-1)}_1 & y_2^{(n-1)} & \dots & y_n^{(n-1)}\\ \end{pmatrix} $$

### Test For Linear Independence

If the functions $p_0, \dots, p_{n-1}$ are continuous on the open interval $I$. The functions $y_1, \dots, y_n$ are solutions $L[y] =0$ and if $W(y_1, \dots, y_n) (t) \ne0$ for at least one point in $I$, then every solution of $L[y] =0$ can be expressed as a linear combination of the solutions $y_1, \dots, y_n$.

A set $y_1, \dots y_n$ whose Wronskian is nonzero is referred to a ****************************fundamental set of solutions****************************. This also forms a basis for $N(L)$. We know that the base exists since we can get $L[y] =0$ with the initial condition $y^{(j)} (t_0) = \delta_{i, j+1}$. The solution to the initial value problem will be $y_i$.

### Linear Dependence and Independence

The functions $f_1, \dots, f_n$ are said to be _linearly dependent_ on an interval if there exists a set of constants $k_1, \dots, k_n$ , not all zero, such that

$$ \sum_{j = 1}^nk_j f_j(t) =0 $$

for all $t \in I$. The functions $f_1, \dots, f_n$ are said to be ******************linearly independent****************** on $I$ if they are not linearly dependent.

This conscept lets us get another use of the Wronskian, let $k_1, \dots, k_n$ be constants such that

$$ \begin{align*} \sum_{i = 1}^n k_iy_i(t) &= 0 \\ \sum_{i = 1}^n k_iy'_i(t) &= 0 \\ &\vdots \\ \sum_{i = 1}^n k_iy_i^{(n-1)}(t) &= 0 \end{align*} $$

We now get a system of $n$ algebraic linear equations for $n$ unkowns. The determinant of the coefficients for this system is the Wronskian $W(y_1, \dots, y_n) (t)$ of $y_1, \dots, y_n$.

**************Th:************** If $y_1, \dots, y_n$ is a fundamental set of solutions of $L[y] = 0$ on the interval, then $y_1, \dots, y_n$ are linearly independent on $I$. Conversrly if $y_1, \dots y_n$ are linearly independent solutions on $L[y] =0$ on $I$, then they form a fundamental set of solutions on $I$.

Then we know $N(L)$ is an $n$ dimensional real vector space

### Abel’s Identity

Let the differential equation

$$ L[y] = y^{(n)} + \sum_{k = 0}^{n-1}p_k y^{(k)} = 0 $$

with $y_1, \dots, y_n$ be solutions, with $p_{n-1}$ be continuous on $I$. Then

$$ W(y_1, \dots, y_n)(t) = W(y_1, \dots, y_n) (t_0) \exp\left(-\int_{t_0}^t p_{n-1}(x)\, dx\right) = c \exp\left(-\int p_{n-1}(t) \, dt\right) $$
 
### Exploiting Linearity

Let $H, L$ be linear differential operators, then $H\circ L$ is also a linear differential operator. Then if we find a solution to $L$, then it is a solution to $H\circ L$.