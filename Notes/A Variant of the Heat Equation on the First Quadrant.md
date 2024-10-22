---
tags:
  - FourierAnalysis
  - PartialDifferentialEquations
---
Subjects: [[Fourier Analysis]], [[Partial Differential Equations]]
Links: [[The Heat Equation]], [[Fourier Transform in R]], [[The Heat Equation on the Real line]]

The equation $$x^2 \frac{\partial^2 u}{\partial x^2}+ ax\frac{\partial u}{\partial x} = \frac{\partial u}{\partial t}$$with $u(x, 0) = f(x)$, for $0<x<\infty$ and $t>0$ is a variant of the heat equation which occurs in a number of applications. We can see some similarity with a [[Cauchy-Euler Differential Equation|Cauchy-Euler differential equation]], and thus use a similar technique by making the substitution $x = e^{-y}$, so that $-\infty < y<\infty$. 

We set $U(y, t) = u(e^{-y}, t)$ and $F(y) = f(e^{-y})$. Then The problem reduces to the equation $$\frac{\partial^2 U}{\partial y^2} + (1-a) \frac{\partial U}{\partial y} = \frac{\partial U}{\partial t}$$with $U(y, 0) = F(y)$. 

With this in mind, we can apply the Fourier transform on $y$, and get that $$-4\pi^2\omega^2 \hat U + (1-a) 2\pi i \omega \hat U = \frac{\partial \hat U}{\partial t}$$Fixing $\omega$, then we have that $$\hat U (\omega, t)= A(\omega) \exp(-4\pi^2\omega^2 t)\exp(2\pi i \omega (1-a)t)$$
Given the initial condition, then $$\hat U (\omega, t)= \hat F(\omega) \exp(-4\pi^2\omega^2 t)\exp(2\pi i \omega (1-a)t)$$
We can calculate the inverse Fourier transform of $\exp(-4\pi^2\omega^2 t)\exp(2\pi i \omega (1-a)t)$, if we do that we get that $$\int_{-\infty}^\infty \exp(-4\pi^2\omega^2 t) e^{2\pi i \omega(x+(1-a)t)}\, d\omega = \mathcal H_t(x+(1-a)t)=g_t(x)$$
Then we can get that $$U(y, t) = (F* g_t)(x)$$
expanding the integrals and returning to the original variables we get that $$u(x,t) = \frac1{\sqrt{4\pi t}} \int_0^\infty f(v) \exp\left(\frac{-(\ln(v/x)+(1-a)t)^2}{4t}\right) \frac{dv}{v}$$