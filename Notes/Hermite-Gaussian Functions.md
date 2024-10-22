---
tags:
  - SpecialFunctions
---
Subjects: [[Special Functions]]
Links: [[Hermite Polynomials]]

The *Hermite functions or the Hermite-Gaussian functions* $h_k (x)$ are defined by the generating identity $$\sum_{k = 0}^\infty h_k(x)\frac{t^k}{k!} = \exp\left(-\left(\frac{x^2}{2} -2tx +t^2 \right)\right)$$
We have the formula $$h_k(x) = (-1)^k e^{x^2/2}\frac{d^k}{dx^k} e^{-x^2}$$
We can see from this that $h_k(x)$ has the form of $P_k(x) e^{-x^2/2}$ where $P_k$ is a polynomial of degree $k$. This polynomials are the [[Physicist's Hermite Polynomials]]. In particular, the Hermite functions belong to the Schwartz space.

We also see that the family $\{h_k\}_{k \in \Bbb N}$ is complete in the sense that if $f$ is a Schwartz function, and $$(f, h_k) = \int_{-\infty}^\infty f(x)h_k(x)\, dx  =0$$ then $f \equiv 0$

We define $h^*_k(x) = h_k((2\pi)^{1/2}x)$. Then $$\widehat{h_k^*}(\omega)= (-i)^k h_k^*(\omega)$$
Therefore, each $h_k^*$ is an eigenfunction for the [[Fourier transform in R]]

Considering an [[The Heisenberg uncertainty principle from a mathematical lens#Operators|operator form quantum mechanics]], being $$L = -\frac{d^2}{dx^2} + x^2$$Then we get that $$Lh_k(x) = (2k+1)h_k$$
Since $L$ is hermitian, and $h_k$ are its eigenfunctions, then $h_k$ are mutually orthogonal for the $L^2$ inner product on the Schwarz space

We get that $$\int_{-\infty}^\infty [h_k(x)]^2\, dx =  2^k k!\sqrt\pi$$
We can consider the function $$\psi_k(x) = (-1)^n\frac1{\sqrt{2^k k! \sqrt \pi}} e^{x^2/2} \frac{d^k}{dx^k}e^{-x^2}$$
The the normalisation of the Hermite function, meaning that we have $$\int_{-\infty}^\infty \psi_n(x) \psi_m(x)\, dx = \delta_{n, m}$$

These functions are related to the Schrödinger equation for a harmonic oscillator in quantum mechanics, so these functions are the eigenfunctions.