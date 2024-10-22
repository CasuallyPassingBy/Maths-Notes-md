---
tags:
  - SpecialFunctions
---
Subjects: [[Special Functions]]

Links: 

The Bessel functions are canonical solutions $y(x)$ of [[Important Differential Equations#ODE|Bessel's differential equation]]: $$x^2 y'' + xy' (x^2-\alpha^2)y = 0$$
for arbitrary complex number $\alpha$, which represents the order of the Bessel function. We see that $\alpha$ and $-\alpha$ produce the same differential equation, it is conventional to define different Bessel functions for these two values.

Bessel's equation arises when finding solutions to [[Harmonic Functions|Laplace's equation]] and the [[Helmhotz equation]] in cylindrical or spherical coordinates. In solving problems in cylindrical systems, one obtains Bessel functions of integer order $(\alpha =  n)$; in spherical coordinates, one obtains half-integer orders $(\alpha = n+1/2)$

# Bessel functions of the First Kind

[[Calculating the Bessel Functions From the ODE]], we get that $$J_\alpha(x) = \sum_{m = 0}^\infty \frac{(-1)^m}{m! \Gamma(m+\alpha +1)}\left(\frac{x}{2}\right)^{2m+\alpha}$$This is called the Bessel function of the first kind of order $\alpha$. We see that the the [[Gamma Function]] makes an appearance. The Bessel function of the first kind is an [[Entire functions|entire function]] if $\alpha$ is an integers, otherwise it is a multi-valued function with a singularity at $0$.

For non-integer $\alpha$, the functions $J_\alpha$ and $J_{-\alpha}$ are linearly independent, and are two solutions of the differential equation. For integer order $n$, the following relationship is valid: $$J_{-n}(x) = (-1)^nJ_n(x)$$
Another definition of the Bessel function, for integer values, is possible using an integral representation: $$J_n(x) = \frac1{2\pi}\int_{-\pi}^\pi e^{ix\sin\theta}e^{-in\theta}\, d\theta = \frac1{\pi} \int_0^\pi \cos(n\theta - x \sin\theta)\, d\theta$$
This integral representation can be interpreted as, the $n$th [[Main definitions for Fourier Analysis|Fourier coefficient]] of the function $e^{ix\sin\theta}$. So $$e^{ix\sin \theta} = \sum_{n = -\infty}^\infty J_n(x) e^{in\theta}$$
We have a couple of properties, for $n$th order Bessel functions of the first kind, for $n \in \Bbb Z$:
- $J_n(x)$ is real for all real $x$
- $J_{-n}(x) = J_n(-x) = (-1)^nJ_n(x)$
- $2J_n'(x) = J_{n-1}(x)- J_{n+1}(x)$
- $\left(\dfrac{2n}{x}\right) J_n(x) = J_{n-1}(x) + J_{n+1}(x)$
- $(x^{-n} J_n(x))' = -x^{-n} J_{n+1}(x)$
- $(x^n J_n(x))' = x^n J_{n-1}(x)$
For all integers $n$ and all real numbers $a$ and $b$ we have that $$J_n(a+b) = \sum_{k \in \Bbb Z} J_k(a) J_{n-k}(b)$$
Another formula for $J_n(x)$ that allows one to define Bessel functions for non-integer valued of $n$, $n >-1/2$ is $$J_n(x) = \frac{(x/2)^n}{\Gamma(n+1/2)\sqrt \pi} \int_{-1}^1 e^{ixt} (1-t^2)^{n-1/2}\, dt$$
We have the special case, that $$J_{1/2}(x) = \sqrt{\frac{2}{\pi}} x^{-1/2}\sin x$$
We can calculate 