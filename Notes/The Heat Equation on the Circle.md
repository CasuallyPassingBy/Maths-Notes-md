---
tags:
  - FourierAnalysis
  - PartialDifferentialEquations
---
Subjects: [[Fourier Analysis]], [[Partial Differential Equations]]
Links: [[Applications of Fourier Series in a Mathematical Context]], [[The Heat Equation]], [[Convolution#Periodic functions|Convolution for periodic functions]], [[Main definitions for Fourier Analysis]]

Suppose we are given an initial temperature distribution on $t= 0$ on a ring and that we are asked to describe the temperature at points on the ring at times $t >0$. 

The ring is modelled by the unit circle. A point on this circle is described by its angle $\theta = 2\pi x$, where the variable $x$ lies between $0$ and $1$. If $u(x, t)$ denoted the temperature at time $t$ of a point described by the angle $\theta$. Then $u$ satisfies the differential equation $$\frac{\partial u}{\partial t} = c  \frac{\partial^2 u}{\partial x^2}$$
The constant $c$ is a positive physical constant which of which the ring is made. After rescaling the time variable, we may assume that $c = 1$. If $f$ is our initial data, we impose the condition $$u(x, 0) = f(x)$$To solve the problem, we separate variables and look for special solutions of the form $$u(x, t) = A(x) B(t)$$With the added constraint that $A$ must be periodic of period $1$. Then plugging this possible solution to the heat equation $$ \frac{B'(t)}{B(t)} = \lambda = \frac{A''(t)}{A(t)}$$with $\lambda$ a constant. Then we get two equations $$\begin{align*}
A''(t) - \lambda A(t) &= 0 \\
B'(t) - \lambda B(t)  &= 0
\end{align*}$$
With the restriction of $A(t)$ being periodic, we see that $\lambda = -4\pi^2 n^n$ where $n \in \Bbb Z$. Then $A$ is a linear combination of the exponentials $e^{2\pi i nx}$ and $e^{-2\pi i n x}$, and $B(t)$ is a multiple of $e^{-4\pi^2 n^2 t}$. By superposing these solutions, we are led to $$u(x,t) = \sum_{n = -\infty}^\infty a_n e^{-4\pi^2n^2 t} e^{2\pi i nx}$$where, setting $t= 0$, we see that $\{a_n\}$ are the Fourier coefficients of $f$. 

If $f$ is Riemann integrable, the coefficients $a_n$ are bounded, and since the factor $e^{-4\pi ^2n^2 t}$ tends to zero extremely fast, the series defining $u$ converges. In fact, $u$ is twice differentiable and solves the equation. 

We can write the solution $u$, as $$u(x, t) = (f*H_t)(x)$$where $H_t$ is the *heat kernel for the circle*, given by $$H_t(x) = \sum_{n = -\infty}^\infty e^{-4\pi^2 n^2 t}{e^{2\pi i nx}}$$and where the convolution for periodic functions with period $1$ is defined by $$(f*g) (x) = \int_0^1 f(x-y)g(y)\, dy$$
We would like to have that consider in what sense does $u(x, t) \to f(x)$ as $t\to 0$. Like in a lot of the theory is in the $L^2$ sense. Meaning that $$\lim_{t \to 0} \int_0^1 |u(x, t)-f(x)|^2\, dx = 0$$
We can consider the a change of variable with $x =\theta/2\pi$ and $t = \tau/4\pi^2$, then $$u(\theta, \tau) = \sum a_n e^{-n^2 \tau} e^{in\theta} = (f*h_\tau)(\theta)$$
solves the equation $$\frac{\partial u}{\partial \tau} = \frac{\partial^2 u}{\partial \theta^2} \qquad 0 \le \theta \le 2\pi, \tau >0$$
with boundary condition $u(\theta, 0) = f(\theta) \sim \sum a_n e^{in\theta}$. Where $$h_\tau(\theta) = \sum_{n = -\infty}^\infty e^{-n^2\tau} e^{in\theta}$$
This version of the heat kernel on $[0, 2\pi]$ is the analogue to the Poisson kernel. 

Using the [[Poisson Summation Formula]], and using the [[The Heat Equation on the Real line]] we can get that

**Th:** The kernel $H_t(x)$ is a good kernel as $t \to 0$. 