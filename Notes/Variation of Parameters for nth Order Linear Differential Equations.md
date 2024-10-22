---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Variation of Parameters for Second Order Differential Equations]], [[nth Order Linear Differential Equations]], [[Constant Coefficient nth Order Linear Differential Equation]]

The method of variation of parameters for determining a particular solution of the nonhomogeneous $n$th order linear differential equation $$L[y] = y^{(n)} + \sum_{k = 0}^{n-1}p_k(t) y^{(k)} = g(t)$$Suppose that we know a fundamental set of solutions $y_1, \dots, y_n$ of the homogeneous equation. Then the general solution of the homogeneous equation is $$y_c = \sum_{k = 1}^n c_k y_k$$
The method of variation of parameters for determining a particular solution of $L[y] = g$ rests on the possibility if determining $n$ functions $u_1, \dots, u_n$ such $Y$ is of the form $$Y = \sum_{k = 1}^n u_k y_k $$
We add the following conditions $$\sum_{k = 1}^n u_k' y_k^{(m-1)} =0 \qquad \;\qquad m = 1, 2,\dots, n-1$$So that $$Y^{(m)} = \sum_{k = 1}^n u_k y_k^{(m)} \qquad \;\qquad m = 1, 2,\dots, n-1$$The $n$th derivative of $Y$ is $$Y^{(n)} = \sum_{k = 1}^nu_k y_k^{(n)} + \sum_{k = 1}^n u_k'y_k^{(n-1)} $$
If we substitute $Y$ into $L[y]$, and we get the last condition $$\sum_{k = 1}^n u_k' y_k^{(n-1)} = g$$Then we have the system of $n$ simultaneous linear nonhomogeneous algebraic equations for $u_1', \dots, u_n'$: $$
\begin{align*}
	y_1u_1' + y_2u_2'+\dots +y_nu_n' &= 0 \\
	y_1'u_1' + y_2'u_2'+\dots +y_n'u_n' &= 0 \\
	y_1''u_1' + y_2''u_2'+\dots +y_n''u_n' &= 0 \\
	&\vdots \\
	y_1^{(n-1)}u_1' +\dots +y_n^{(n-1)}u_n' &= g
\end{align*}$$
We use [[Determinants#Cramer's Rule|Cramer's Rule]] to solve the system of equations to get the form $$u_m'(t)= \frac{g(t)W_m(t)}{W(t)},  \qquad \;\qquad m = 1, 2,\dots, n$$
Here $W(t) = W(y_1, \dots, y_n)(t)$ and $W_m$ is the determinant obtained from $W$ by replacing the $m$th column by the column $(0,0, \dots, 0,1)$. With this notation a particular solution is given by $$Y(t) = \sum_{m = 1}^n y_k(t) \int_{t_0}^t \frac{g(s)W_m(s)}{W(s)}\, ds  $$where $t_0$ is arbitrary. We can use [[Solutions to Homogeneous nth Order Linear Differential Equations#Abel’s Identity|Abel's identity]] to simplify the algebra. 