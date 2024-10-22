---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Linear System of Ordinary Differential Equations]], [[Fundamental Matrices for Linear System of Differential Equations]], [[Homogeneous Linear System of Differential Equations with Constant Coefficients]], [[Variation of Parameters for nth Order Linear Differential Equations]]

We are going to approach a little bit the the nonhomogeneous systems $$x' =P(t) x + g(t)$$
where $P$ is an $n\times n$ matrix and $g$ vector, and are continuous for $\alpha<t<\beta$. By a similar argument as we did, get that the solution can be expressed as $$x = c_1x^{(1)} + \dots + c_n x^{(n)} + v(t)$$
where $c_1 x^{(1)}+\dots + c_n x^{(n)}$ is the general solution of the homogeneous system $x' = P(t) x$m and $v$ is the particular solution of the nonhomogeneous system. There are methods to get $v$.


### Diagonalization

We begin with the systems of the form $$x' = Ax +g(t)$$where $A$ is diagonalizable constant matrix. By diagonalizing the coefficient matrix, and finding $P$ the matrix composed of the eigenvectors of $A$, then we make a new dependent variable $y$ by $$x = Py$$Then by substituting into the system we get that $$Py' = APy + g(t)$$by multiplying by $P^{-1}$, we get that $$y' = P^{-1}AP y + P^{-1}g(t) =Dy+ h(t)$$where $h(t) = P^{-1}g(t)$, and $D$ is the diagonal matrix. 

From this last system we actually have a system of $n$ *uncoupled* equations for $y_1, \dots, y_n$ as a consequence we just solve them separately. We have that $$y'_k = \lambda_ky_k + h_k(t) \qquad \;\quad k = 1, \dots, n$$
Solving this we have that $$y_k(t) = e^{\lambda_k t} \int_{t_0}^t e^{-\lambda_ks} h_k(s)\, ds+c_k e^{\lambda_k t}$$where $c_k$ are arbitrary constants and we have a solution $y$. To get the solution $x$ we need to multiply by the transformation matrix $P$, getting that $x = Py$, and this produces a general solution to the equation, the second term in the right hand side is the general solution of the homogeneous system $x' = Ax$, while the first term yields a particular solution fo the nonhomogeneous system. 

In the case that $A$ cannot be diagonalized then, then it can be reduced to a Jordan form $J$ by a suitable transformation matrix $P$. In this case the differential equations for $y_1, \dots, y_n$ are not totally uncoupled since some rows of $J$ have two nonzero elements: an eigenvalue in the diagonal and a $1$ in the adjacent position to the right. However the equations for $y_1, \dots, y_n$ cam still be solved consecutively starting at $y_n$. Then the solution of the original system can be found by the relation $x = Py$


### Variation of parameters

Let $$x' = P(t) x+g(t)$$
where $P(t)$ and $g(t)$ are continuous on $\alpha<t <\beta$. Assume that the fundamental matrix $\Psi(t)$ for the corresponding homogeneous system $$x' =P(t)x$$has been found. 

Since the general solution to the homogeneous system is $\Psi(t)c$ it is a bit natural to proceed as we did for the other method of variation of parameters, and replace $c$ by a vector function $u(t)$. Thus we assume that $$x = \Psi(t) u(t)$$
where $u(t)$ is a vector to be found. If we differentiate $x$, then we obtain that $$\Psi'(t) u(t) + \Psi(t)u'(t) = P(t) \Psi(t) u(t) + g(t)$$
Since $\Psi(t)$ is a a fundamental matrix $\Psi'(t) = P(t) \Psi(t)$; hence we obtain $$\Psi(t) u'(t) = g(t)$$Finally since $\Psi(t)$ is nonsingular on the interval where $P$ is continuous, then $$u'(t) = \Psi(t)^{-1}g(t)$$
Thus for $u(t)$ we obtain that $$u(t) = \int \Psi(t)^{-1}g(t)\, dt +c$$
where $c$ is arbitrary, giving us as the general solution to be of the form $$x = \Psi(t)c+ \Psi(t) \int_{t_1}^t \Psi(s)^{-1} g(s)\, ds$$where $t_1$ is any point in the interval $(\alpha, \beta)$. If we add the initial condition as $$x(t_0) = x_0$$then we get that $$x = \Psi(t)c+ \Psi(t) \int_{t_0}^t \Psi(s)^{-1} g(s)\, ds$$
and when $t =t_0$, the integral is $0$, then the initial condition is also satisfied if we choose $$c = \Psi(t_0)^{-1} x_0$$Therefore $$x = \Psi(t)\Psi(t_0)^{-1}x_0+ \Psi(t) \int_{t_0}^t \Psi(s)^{-1} g(s)\, ds$$
The solution takes a slightly simpler form if we use the fundamental matrix $\Phi(t)$ satisfying that $\Phi(t_0) = I$, in this case we have that $$x = \Phi(t)x_0+ \Phi(t) \int_{t_0}^t \Phi(s)^{-1} g(s)\, ds$$
If we have the case where $P$ is constant, then and $t_0 = 0$, then this formula can be simplified as $$x = \exp(At) x_0 + \int_0^t \exp(A(t-s)) g(s)\, ds$$