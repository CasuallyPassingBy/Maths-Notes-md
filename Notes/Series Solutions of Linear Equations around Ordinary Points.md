---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Power Series in R]], [[nth Order Linear Differential Equations]]
### Existence Theorem for Analytic Coefficients

Let $x_0$ be a real number, and suppose that the coefficients $a_1, \dots, a_n$ in 

$$
L[y] = y^{(n)} + \sum_{k = 1}^n a_k(x)y^{(k)} 
$$

have convergent power series expansion in powers $x- x_0$ on an interval 

$$
|x-x_0| <r_0 \qquad r_0 >0
$$

If $\alpha_1, \dots, \alpha_n$ are any $n$ constants, there exists a solution $\phi$ of the problem 

$$
L(y) \qquad \forall k \in\{1,\dots, n\}[ y^{(k-1)}(x_0) = \alpha_k]
$$

with a series expansion 

$$
\phi(x) = \sum_{k = 0}^\infty c_k (x-x_0)^k
$$

convergent for $|x-x_0|< r_0$. We have 

$$
\forall k \in\{0,\dots, n-1\}[k! c_k = \alpha_{k+1} ]
$$

and for $c_k$  for $k \ge n$ may be computed in terms of $c_0, c_1,\dots, c_{n-1}$ by substituing the series into $L[y] = 0$

This theorem works differential equations such of the form 

$$
\sum_{k = 0}^n A_k(x) y^{(k)} = 0
$$

such that when diving by $A_k /A_n$ is still analytic around $x_0$, then we can substitute $A_k /A_n = a_k$, and get 

$$
y^{(n)} + \sum_{k = 0}^{n-1} a_n(x) y^{(k)} = 0
$$

just as the theorem needed. If at $x_0$ we can do this procedure while mantining the analycity of $a_k$, then $x_0$ is called an *ordinary point*.