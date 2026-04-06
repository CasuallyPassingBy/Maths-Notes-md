---
tags:
  - PartialDifferentialEquations
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]], [[Partial Differential Equations]]
Links: [[Symplectic Forms on Smooth Manifolds]], [[Contact Structures on Smooth Manifolds]], [[Solution of Linear and Quasilinear First Order PDEs using Vector Flows]]

We begin with a somewhat special case. A first-order PDE that involves only the first derivatives of the unknown function but not the values of the function itself is called (in this note) a *Hamilton-Jacobi equation*. Such an equation for an unknown function $u(x^1,\dots, x^n)$ can be written in the form $$F\left(x^1,\dots, x^n, \frac{\partial u}{\partial x^1}, \dots, \frac{\partial u}{\partial x^n}\right) = 0. $$
More generally, if $M$ is a smooth manifold, a Hamilton-Jacobi equation on $M$ is given by a smooth real-valued function $F$ defined on an open subset $W\subseteq T^* M$, and a solution to the equation is a real-valued function $u$ defined on an open subset $U\subseteq M$ such that the image of $du$ lies in the zero set of $F$: $$F(x, du(x)) = 0 \qquad \text{for all }x\in U. $$
We are interested in solving a Cauchy problem for the equation above, given an embedded hypersurface $S\subseteq M$ and a smooth function $\varphi: S\to\Bbb R$, we wish to find a smooth function $u$ defined on a neighbourhood of $S$ in $M$ and satisfying the equation above together with the initial condition $$u|_S = \varphi.$$
