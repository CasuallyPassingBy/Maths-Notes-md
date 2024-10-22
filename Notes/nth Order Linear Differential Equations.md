---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Existence and Uniqueness of Solutions to Systems of Differential Equations]]
An $n$th order linear differential equation is an equation of the form

$$ \sum_{k = 0}^n P_k(t) y^{(k)} = G(t) $$

We assume that $P_0,\dots, P_n$ and $G$ are continuous real valued functions on some open interval $(\alpha, \beta)$, and that $P_n$ is nowhere zero in this interval. Then dividing by $P_n$ we get that

$$ L[y] = y^{(n)} + \sum_{k = 0}^{n-1}p_k y^{(k)} = g(t) $$

$L$ is a linear differential operator of order $n$. The theory is analogous to the second order linear differential operator. $L$ is of the form

$$ L=D^n + \sum_{k = 0}^{n-1} p_k D^k $$

### Existence and Uniqueness

If there are functions $p_0, \dots, p_{n-1}$ and $g$ are continuous on the open interval $I$. Then there exists exctly one solution $y = \phi(t)$ of the differential equation $L[y] = g$, that satisfies the initial conditions

$$ y(t_0) = y_0, \quad y'(t_0) = y'_0, \quad \dots \quad y^{(n-1)}(t_0) = y^{(n-1)}_0 $$

where $t_0$ is a point on the interval $I$. This solution exists throughout $I$.

