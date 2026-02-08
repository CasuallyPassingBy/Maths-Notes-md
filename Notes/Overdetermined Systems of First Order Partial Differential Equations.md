---
tags:
  - DifferentialGeometry
  - PartialDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Partial Differential Equations]]
Links: [[Tangent Distributions and Involutivity on Smooth Manifolds]], [[Foliations on Smooth Manifolds]], [[First Order Partial Differential Equations]]

In some applications, it is necessary to consider systems of PDEs that are *overdetermined*, which means that are more equations that unknown functions. In general, overdetermined systems have solutions if they satisfy certain compatibility conditions. For some first-order systems, the compatibility condition can be interpreted as a statetment about involutivity of a distribution, and the Frobenius theorem can be used to prove local existence and uniqueness of solutions.

Suppose $W$ is an open subset of $\Bbb R^n$ and $m$ is a positive integer less than or equal to $n$. Consider the following system of $m$-linear partial differential equations for a single unknown function $u\in \mathcal C^\infty(W)$: $$
\begin{align*} a^1_1(x) \frac{\partial u}{\partial x^1} + \cdots+ a^n_1(x)  \frac{\partial u}{\partial x^n} &= f_1(x),\\&\vdots \\ 
a^1_m(x) \frac{\partial u}{\partial x^1} + \cdots+ a^n_m(x)  \frac{\partial u}{\partial x^n} &= f_m(x),
\end{align*}  $$where $(a^j_i)$ is an $n\times m$ matrix of smooth real-valued functions and $f_1,\dots, f_m$ are smooth real-valued functions on $W$. The cases $m =1$ is covered [[Solution of Linear and Quasilinear First Order PDEs using Vector Flows|here]], so the discussion is useful when $m > 1$. 

If we let $A_i$ denote the vector field $a^j_i \dfrac{\partial}{\partial x^j}$, the system above can be written more succinctly as $A_1 u = f_1, \dots, A_m u = f_m$. To avoid redundant or degenerate system of equations, we assume that the matrix $(a^j_i)$ has rank $m$ at each point of $W$, or equivalently that the vector fields $A_1,\dots, A_m$ are linearly independent.

The following theorem is the analogue of [[Solution of Linear and Quasilinear First Order PDEs using Vector Flows#^e5452a|this theorem]] but for the overdetermined case.  

**Th:** Let $W\subseteq \Bbb R^n$ be an open subset and let $m$ be an integer such that $1\le m \le n$. Suppose we are given an embedded codimension-$m$ submanifold $S\subseteq W$, a linearly independent $m$-tuple of smooth vector fields $(A_1,\dots, A_m)$ on $W$ whose span is complementary to $T_p S$ at each $p\in S$, and functions $f_1,\dots, f_m\in \mathcal C^\infty(W)$. Suppose also that there are smooth functions $c^k_{ij}\in \mathcal C^\infty(W)$ for $i, j, k = 1,\dots, m$ such that the following compatibility conditions are satisfied $$\begin{align*}
[A_i, A_j] &= c^k_{ij} A_k, \\
A_i f_j- A_j f_i &= c^k_{ij} f_k.
\end{align*}  $$
Remember we are using the Einstein summation convention up to $m$. Then for each $p\in S$ there is a unique neighbourhood $U$ of $p$ such that for every $\varphi\in \mathcal C^\infty(S\cap U)$, there exists a unique solution $u\in\mathcal C^\infty(U)$ to the following overdetermined Cauchy problem: $$\begin{align*} A_i u &= f_i \qquad \text{for }i = 1,\dots, m, \\ u|_{S\cap U} &= \varphi.\end{align*} $$
