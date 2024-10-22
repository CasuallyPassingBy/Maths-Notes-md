---
tags:
  - SpecialFunctions
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]], [[Special Functions]]
Links: [[Poisson Summation Formula]], 

We define the *theta function* $\vartheta(s)$ for $\Re(s)>0$ by $$\vartheta(s) \sum_{n = -\infty}^\infty e^{-\pi n^2 s}$$The condition on $s$ ensures the absolute convergence of the series. A crucial fact about this special function is that it satisfies the following functional equation.

**Th:** $s^{-1/2}\vartheta(1/s) = \vartheta(s)$, whenever $\Re(s) >0$.  

The theta function is intimately connected with an important function un number theory, the [[Riemann Zeta Function]] $\zeta(s)$ defined for $\Re(s)>1$ by $$\zeta(s) = \sum_{n = 1}^\infty \frac1{n^s}$$
It turns out that $\zeta$, $\vartheta$ and $\Gamma$ are related by the following identity $$\pi^{-s/2} \Gamma(s/2) \zeta(s) =\frac1{2} \int_0^\infty t^{s/2-1}(\vartheta(t)-1)\, dt $$
There's a generalisation of the this $\vartheta$, which is considered the *Jacobi theta function* is defined as $$\vartheta(z; \tau) = \sum_{n = -\infty}^\infty e^{\pi i n^2 \tau}e^{2\pi i n z} = \sum_{n = -\infty}^\infty  \exp(\pi i n^2\tau + 2\pi i nz)$$
Whenever $\Im(\tau) >0$ and $z \in \Bbb C$. Taking $z = 0$ and $\tau = is$ we get that $\vartheta(z; \tau) = \vartheta(s)$. 

The Jacobi theta function defined above is sometimes considered along with three auxiliary theta functions, in which case it is written with a double $0$ subscript $$\vartheta_{00}(z;\tau) = \vartheta(z; \tau)$$
whenever 