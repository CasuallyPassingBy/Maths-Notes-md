---
tags:
  - SpecialPolynomials
---
Subjects: [[Special Polynomials]]
Links: [[Lp spaces]], [[Hilbert Spaces]]

**Def:** We define the *Chebyshev polynomials of the first kind*, denoted by $T_k(x)$ with the following recursion relation: $$T_{k+2} (x) := 2xT_{k+1}(x) - T_k(x), $$with $T_0(x) =  1$ and $T_1(x) =x$. 

**Prop:** For each $n<\omega$, $$T_k(x) = \cos(k\arccos(x)).$$
**Def:** We define the *Chebyshev measure of the first kind* to be $\mu: \mathcal B([-1, 1]) \to [0,\infty]$ and$$\mu_1(A) := \int_A \frac1{\sqrt{1-y^2}}\, \lambda(dy), $$where $\lambda$ represents the Lebesgue measure.

We see that the Chebyshev measure of the first kind is absolutely continuous with respect to the Lebesgue measure. 

**Prop:** We see that the collection of Chebyshev polynomials $\{T_n(x) \mid n<\omega\}$ are orthogonal basis of $L^2([-1, 1], \mathcal B([-1, 1]), \mu_1)$, where $\mu_1$ is the Chebyshev measure of the first kind. We see that  $$\langle T_n, T_m\rangle = \begin{dcases} 0 & \text{if }n \neq m, \\ \pi &\text{if }n = m = 0, \\ \frac{\pi}{2}& \text{if }n = m >0\end{dcases} $$
**Lemma:** For every $n\ge 1$, the leading coefficient of $T_n(x)$ is $2^{n-1}$.

**Def:** We define the *monic Chebyshev polynomial* for $n \ge 1$, denoted by $\tilde T_n$, as $\tilde T_n := T_n/2^{n-1}$. 

**Minimax property of Chebyshev polynomials:** Out of all monic polynomials of degree $n$, $\tilde T_n$ has the least $\|\cdot\|_\infty$-norm on the interval $[-1, 1]$, meaning that for every $p(x) = x^n + a_{n-1}x^{n-1} + \dots + a_0$ we see that $$\left\|\tilde T_n\right\|_\infty \le \|p\|_\infty. $$
**Cor:** Given that $\tilde T_n(x) = x^n - Q_{n-1}(x)$ has the minimum $\|\cdot\|_\infty$-norm, we deduce that $Q_{n-1}$ is the best uniform approximation of $x^n$ in the space of polynomials of degree less than $n$, with domain $[-1, 1]$. 