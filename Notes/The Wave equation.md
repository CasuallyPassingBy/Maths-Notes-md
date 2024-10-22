---
tags:
  - PartialDifferentialEquations
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]], [[Partial Differential Equations]]
Links: [[Harmonic Functions]], [[The Heat Equation]], [[Fourier Transform in Rn]], [[Fourier Transform in R]]

The motion of a vibrating string satisfies the equation $$\frac{\partial^2 u}{\partial x^2} = \frac1{c^2}\frac{\partial^2 u}{\partial t^2}$$which is referred to as the one-dimensional wave equation.

A natural generalisation of this equation to $n$ space variables is $$\sum_{k = 1}^n \frac{\partial^2 u}{\partial x^2_k} = \frac1{c^2} \frac{\partial^2 u}{\partial t^2}$$
We know that in the case $d = 3$, this equation determines the behaviour of electromagnetic waves in a vacuum, with $c =$ speed of light. Also, this equation describes the propagation of sound waves. Thus, the equation above is called the *$n$-dimensional wave equation*. 

We can assume that $c = 1$, since we can rescale the variable $t$ if necessary. Using the Laplacian and this time scaling, we get the equation can be written as $$\Delta u  = \frac{\partial^2 u}{\partial t^2}$$
The goal of this section is to find a solution to this equation subject to the initial conditions $$u(x, 0) = f(x) \qquad \text{and}\qquad \frac{\partial u}{\partial t}(x, 0) = g(x)$$where $f, g\in \mathcal S(\Bbb R^n)$. This is called the *Cauchy problem* for the wave equation.

Suppose $u$ solves the Cauchy problem for the wave equation. The technique employed consists of taking the Fourier transform of the equation and of the initial conditions, with respect of the space variables, $x_1, \dots, x_n$. This reduces the problem to an ODE in the time variable. 

We find that the wave equation becomes $$-4\pi \|\omega\|^2 \hat u(\omega, t) = \frac{\partial^2 \hat u}{\partial t^2}(\omega, t) $$For each fixed $\omega\in \Bbb R^n$, this is an ODE in $t$ whose solution is given by $$\hat u(\omega, t) = A(\omega)\cos(2\pi \|\omega\| t) + B(\omega) \sin(2\pi \|\omega\|t)$$where for each $\omega$, $A(\omega)$ and $B(\omega)$ are unknown constants to be determined by the initial conditions. In fact, taking the Fourier transform (in $x$) of the initial conditions we get that $$\hat u(\omega, 0) = \hat f(\omega) \qquad \text{and}\qquad \frac{\partial \hat u}{\partial t}(\omega, 0) = \hat g(\omega)$$
We get that $$A(\omega) = \hat f(\omega) \qquad \text{and} \qquad B(\omega) = \frac{ \hat g(\omega)}{2\pi\|\omega\|}$$
getting that the solutions must satisfy that $$\hat u(\omega, t) = \hat f(\omega) \cos(2\pi \|\omega\| t) + \hat g(\omega) \frac{\sin(2\pi \|\omega\|t)}{2\pi \|\omega\|}$$
**Th:** A solution of the Cauchy problem for the wave equation is $$u(x, t) = \int_{\Bbb R^n} \left[\hat f(\omega) \cos(2\pi \|\omega\| t) + \hat g(\omega) \frac{\sin(2\pi \|\omega\|t)}{2\pi \|\omega\|}\right] e^{2\pi i x\cdot \omega}\, d\omega$$
Having proved the existence of a solution to the Cauchy problem for the wave equation, we raise the question of uniqueness. Are solutions to the problem $$\Delta u = \frac{\partial^2 u}{\partial t^2} \quad \text{subject to} \quad u(x, 0) = f(x) \quad \text{and}\quad \frac{\partial u}{\partial t} (x, 0)=g(x)$$other than the given by the formula in the theorem? The answer is no but we need a little bit more machinery.

We define the *energy* of a solution by $$ E(t) = \int_{\Bbb R^d} \left|\frac{\partial u}{\partial t}\right|^2 + \sum_{k = 1}^n \left|\frac{\partial u}{\partial x_k}\right|^2\, dx = \int_{\Bbb R^n} \|\nabla u\|^2\, dx $$
**Th:** If $u$ is the solution of the wave equation given by the formula of the theorem, then $E(t)$ is conserved, that is, $$E(t) = E(0) \qquad \forall t \in \Bbb R$$
The drawback with the the formula, is that it gives a solution but in a really indirect way, involving calculating the Fourier transforms of $f$ and $g$, and then an inverse Fourier transform. 

For every dimension $n$ there is a more explicit formula. 

A *Spherical wave* is a solution $u(x, t)$ of the Cauchy problem for the wave equation in $\Bbb R^n$, which is a function of $x$ is radial. $u$ is a spherical wave iff $f,g\in \mathcal S$ are both radial.


Let $B(x_0, r_0)$ denote the ball in the hyperplane $t =0$ centred at $x_0$ and of radius $r_0$. The *backward light cone* with base $B(x_0, r_0)$ is defined by $$\mathcal L_{B(x_0, r_0)}=\{(x, t)\in \Bbb R^n \times \Bbb R \mid \|x-x_0\|\le r_0-t, \; 0 \le t \le r_0\}$$

# 1D Wave Equation

The case where $n = 1$ it can be fairly simple to get the formula:

We can do some algebra, and exploit some properties of the Fourier transform and get that the solution is $$u(x, t) =\frac{f(x+t)+f(x-t)}{2} + \frac1{2} \int_{x-t}^{x+t} g(y)\, dy$$
The solution feels a lot like averaging our initial information. 

We can see the solution in different dimensions:
- [[2D Wave Equation]]
- [[3D Wave Equation]]

This different levels of difficulty to solve the cases where $n = 1, 3$ and when $n=2$ illustrates the  general principle that in $n$-dimensional Fourier analysis: a significant number of formulas that arise are simpler in the case of odd dimensions.