---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Main definitions for Fourier Analysis]], [[Improper Integrals in R]], [[Good Kernels and Convergence in Fourier Analysis]] 

A function $f$ defined on $\Bbb R$ is said to be of *moderate decrease* if $f$ is there exist constants $A >0$ and $\alpha > 1$so that $$|f(x)| \le \frac{A}{1+x^\alpha} \qquad \forall x \in \Bbb R$$
We denote by $\mathcal M(\Bbb R)$ the set of all moderate decrease functions on $\Bbb R$, this forms a vector space over $\Bbb C$.

**Prop:** The integral of a function of moderate decrease defined as the improper integral satisfies the following properties:
- *Linearity*: if $f,g \in \mathcal M(\Bbb R)$ and $a, b\in \Bbb C$, then $$\int_{-\infty}^\infty (af(x)+bg(x))\, dx = a \int_{-\infty}^\infty f(x)\, dx +b\int_{-\infty}^\infty g(x)\, dx$$
- *Translation invariance*: for every $h\in \Bbb R$ we have that $$\int_{-\infty}^\infty f(x-h) \,dx = \int_{-\infty}^\infty f(x)\, dx$$
- *Scaling under dilation*: if $\delta>0$, then $$\delta \int_{-\infty}^\infty f(\delta x)\, dx = \int_{-\infty}^\infty f(x)\, dx$$
- *Continuity*: if $f$ is continuous and $f\in \mathcal M(\Bbb R)$, then $$\lim_{h \to 0} \int_{-\infty}^\infty|f(x-h) -f(x)| \, dx = 0$$
**Def:** If $f\in \mathcal M(\Bbb R)$, we define its *Fourier transform* for $\omega\in \Bbb R$ by $$\hat f(\omega) = \int_{-\infty}^\infty f(x) e^{-2\pi i x \omega}\, dx$$Since the integrand is of moderate decrease, the integral is well defined. 

# Schwartz space

The *Schwartz space* on $\Bbb R$ consists of the set of all infinitely differentiable function $f$ so that $f$ and all its derivatives $f', f'', \dots, f^{(n)}, \dots,$ are *rapidly decreasing*, in the sense that $$\sup_{x \in \Bbb R} |x|^k |f^{(n)}(x)| < \infty \qquad \forall k, n \ge 0$$We denote this space $\mathcal S = \mathcal S(\Bbb R)$, we can see that $\mathcal S(\Bbb R)$ is a vector space over $\Bbb C$. Moreover if $f\in \mathcal S(\Bbb R)$, then $$f'(x), xf(x) \in \mathcal S(\Bbb R)$$
Not only if the Schwartz space a vector space, it can also be equipped with an inner product: $$\langle f, g\rangle = (f,g) = \int_{-\infty}^\infty f(x)\overline{g(x)}\, dx $$

**Def:** The *Fourier Transform* of a function $f \in \mathcal S(\Bbb R)$ is defined by $$\hat f(\omega) = \int_{-\infty}^\infty f(x) e^{-2\pi i x \omega}\, dx $$
We use the notation $$f(x) \longrightarrow \hat f(\omega)$$to mean that $\hat f$ denotes the Fourier transform of $f$.

**Prop:** If $f\in \mathcal S(\Bbb R)$ then
- $f(x+h) \longrightarrow \hat f(\omega) e^{2\pi i h \omega}$ whenever $h \in \Bbb R$
- $f(x)e^{-2\pi i x h}  \longrightarrow \hat f(\omega + h)$ whenever $h \in \Bbb R$
- $f(\delta x) \longrightarrow \delta^{-1} \hat f(\delta^{-1} \omega)$, whenever $\delta > 0$
- $f'(x) \longrightarrow 2\pi i \omega \hat f(\omega)$
- $-2\pi i x f(x) \longrightarrow \dfrac{d}{d\omega}\hat f(\omega)$

**Th:** If $f\in \mathcal S(\Bbb R)$, then $\hat f\in \mathcal S(\Bbb R)$

# Gaussians as Good Kernels

We begin by considering the case $e^{-\pi x^2}$ because of normalization $$\int_{-\infty}^\infty e^{-\pi x^2} \, dx = 1$$
**Th:** If $f(x) = e^{-\pi x^2}$, then $\hat f(\omega) = f(\omega)$

**Cor:** If $\delta>0$ and $K_\delta(x) = \delta^{-1/2}e^{\pi x^2/\delta}$, then $\widehat{K_\delta}(\omega) = e^{\pi \delta \omega^2}$ 

**Th:** The collection $\{K_\delta\}_{\delta>0}$ satisfies the following conditions:
- $\int_{-\infty}^\infty K_\delta(x) \,dx = 1$
- $\int_{-\infty}^\infty |K_\delta(x)| \,dx \le M$
- For every $\eta >0$, we have that $\int_{|x| > \eta} |K_\delta|\, dx \to 0$ as $\delta \to 0$
Meaning is a family of good kernels as $\delta >0$

**Cor:** If $f\in \mathcal S(\Bbb R)$, then $$(f*K_\delta)(x) \to f(x) \qquad \text{uniformly in }x \text{ as } \delta \to 0$$
with the [[Convolution#Rapidly Decreasing Functions|Convolution For Rapidly Decreasing Functions]], just like the

# The Fourier Inversion

**Prop:** If $f, g \in \mathcal S(\Bbb R)$, then $$\int_{-\infty}^\infty f(x) \hat g(x) = \int_{-\infty}^\infty \hat f(y) g(y) \, dy$$
This is true since 

**Th (Fourier Inversion):** If $f \in \mathcal S(\Bbb R)$, then $$f(x) = \int_{-\infty}^\infty \hat f(\omega) e^{2\pi i x\omega}\, d\omega$$
We may define two mapping $\mathcal F, \mathcal F^*: \mathcal S(\Bbb R) \to \mathcal S(\Bbb R)$   by $$\mathcal F(f)(\omega) = \int_{-\infty}^\infty f(x) e^{-2\pi i x\omega}\, dx \qquad \text{and}\qquad \mathcal F^*(g)(\omega) = \int_{-\infty}^\infty g(x) e^{2\pi i x\omega}\, d\omega$$
Thus $\mathcal F$ is the Fourier transform, and the theorem above guarantees that $\mathcal F^* \circ \mathcal F = I$ on $\mathcal S(\Bbb R)$, where $I$ is the identity mapping. They only differ by a sign in the exponential, we see that $\mathcal F(f)(y) = \mathcal F^*(f)(-y)$, so we also have that $\mathcal F \circ \mathcal F^* =I$. As a consequence, we see that $\mathcal F^*$ is the inverse Fourier transform on $\mathcal S(\Bbb R)$.

**Cor:** The Fourier transform is a bijective mapping on the Schwartz space

**Cor:** Suppose $f$ is an even function such that $f$ and $\hat f$ are of moderate decrease. Then $\hat f$ is also even and the Fourier transform of $\hat f$ is $f$. 

# The Plancherel Formula

**Prop:** If $f, g \in \mathcal S(\Bbb R)$ then
- $f*g\in \mathcal S(\Bbb R)$
- $f*g=g*f$ 
- $(\widehat{f*g})(\omega) = \hat f(\omega) \hat g(\omega)$

The Schwartz space can be equipped with a Hermitian inner product: $$\langle f, g\rangle = \int_{-\infty}^\infty f(x)\overline{g(x)}\, dx $$whose associated norm is $$\|f\| = \left(\int_{-\infty}^\infty |f(x)|^2\, dx \right)^{1/2} $$
#### Plancherel Formula
If $f \in \mathcal S(\Bbb R)$ then $$\|f\| = \|\hat f\|$$

Suppose that $f$ is a function of moderate decrease on $\Bbb R$ whose Fourier transform $\hat f$ is continuous and satisfies $$\hat f(\omega) = O\left(\frac1{|\omega|^{1+\alpha}}\right) \qquad \text{as } |\omega|  \to \infty$$
for some $0<\alpha <1$. Then $f$ satisfies the Hölder condition of order $\alpha$. We see that the decay of $\hat f$ is related to the smoothness of $f$. 

If $\hat f(\omega) = 0$ for all $\omega$, then $f$ is identically $0$


# Extension to functions of moderate decrease

To extend to moderate decrease functions instead of only to the Schwarz space. The key observation, is that the convolution $f*g$ of two functions $f$ and $g$ of moderate decrease is again a function of moderate decrease; also $\widehat{f*g}= \hat f\hat g$. Moreover, the multiplication formula continuous to hold, and we deduce the Fourier inversion and Plancherle formulas when $f$ and $\hat f$ are both of moderate decrease. 

We can bring another proof of the [[Stone-Weierstrass Theorem#Weierstrass Approximation Theorem|Weierstrass Approximation Theorem]]. 

# Analogue to Fourier Series

We can have an analogue to [[Good Kernels and Convergence in Fourier Analysis#Fejér Theorem|Fejer's Theorem for Fourier series]] in the context of the Fourier transform, where the *Fejér kernel on the real line* is defined by $$\mathcal F_R(x) = \begin{dcases}R \left(\frac{\sin \pi R x}{\pi R x}\right)^2 & x \ne 0 \\
R & x = 0 \end{dcases}$$
We can see that $\{\mathcal F_R\}$ is a family of good kernels as $R\to \infty$, and we have that $$(f*\mathcal F_R)(x) =\int_{-R}^R \left(1-\frac{|\omega|}{R}\right) \hat f(\omega) e^{2\pi i x \omega}\, d\omega $$
and since it is a good kernel, we see that that expression tends uniformly to $f(x)$ as $R\to\infty$. 

We can see that the periodization of the Fejér kernel $\mathcal F_N$ on the real line is equal to the Fejér kernel for periodic functions of period $1$. In other words $$\sum_{n = -\infty}^\infty \mathcal F_N(x+n) = F_N(x)$$when $N \ge 1$ is an integer. using [[Poisson Summation Formula]]