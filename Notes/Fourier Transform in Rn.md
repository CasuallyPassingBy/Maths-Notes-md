---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Improper Integrals in Rn]], [[Fourier Transform in R]]

We care about the analysis in $\Bbb R^n$, and in particular the theory of the Fourier transform, is shaped by three important groups of symmetries of the underlying space:
- Translations
- Dilations
- Rotations

We see that translations $x \mapsto x + h$, with $h \in \Bbb R^n$ fixed. Meaning that the translations is isomorphic to $\Bbb R^n$. The dilations $x \mapsto \delta x$, with $\delta>0$. In $R^n$ we have more rotations, and the understanding of the interaction between the Fourier transform and rotations leads to interesting insights regarding spherical symmetries.

A *rotation* in $\Bbb R^n$ is a linear transformation $R\in \mathcal L(\Bbb R^n)$, which preserves the inner product. This is common enough that we have a name for the set of all rotations $O(n, \Bbb R)$, being the [[orthogonal group]]. In the case, where we are working on $\Bbb R$, we can just say $O(n)$.

# Elementary Theory of the Fourier transform

The *Schwartz space* $\mathcal S(\Bbb R^d)$ (sometimes abbreviated as $\cal S$) consists of all infinitely differentiable functions $f$ on $\Bbb R^n$ such that $$\sup_{x \in \Bbb R^n} \left| x^\alpha \partial^\beta f\right| < \infty$$
for every [[Multi-index notation|multi-index]] $\alpha$ and $\beta$. In other words, $f$ and all its derivatives are required to be rapidly decreasing

The *Fourier transform* of a Schwartz function $f$ is defined by $$\hat f(\omega) = \int_{\Bbb R^n} f(x) e^{-2\pi i x \cdot \omega}\, dx \qquad \omega \in \Bbb R^n$$
We now list some simple properties of the Fourier transform. For this proposition when $F(x) \longrightarrow G(\omega)$ means that $G(\omega) = \hat F(\omega)$

**Prop:** Let $f\in \mathcal S(\Bbb R^n)$
- $f(x+h) \longrightarrow \hat f(\omega) e^{2\pi i \omega\cdot h}$, whenever $h\in \Bbb R^n$
- $f(x) e^{-2\pi i x\cdot h}\longrightarrow \hat f(\omega +h)$, , whenever $h\in \Bbb R^n$
- $f(\delta x) = \delta^{-d}f(\delta^{-1}\omega)$, whenever $\delta >0$
- $\dfrac{\partial^\alpha}{\partial x^\alpha} f(x) \longrightarrow (2\pi i \omega) \hat f(\omega)$
- $-2\pi i x)^\alpha f(x) \longrightarrow \dfrac{\partial^\alpha}{\partial x^\alpha} \hat f(\omega)$
- $f(Rx) \longrightarrow \hat f(R\omega)$ whenever $R \in O(n)$

**Cor:** The Fourier transform maps $\mathcal S(\Bbb R^n)$ to itself

We say that a function $f$ is *radial* if it depends only on $\|x\|$; in other words, $f$ is radial if there's a function $f_0(u)$, defined for $u\ge 0$, such that $f(x) = f_0(\|x\|)$. We note that $f$ is radial iff $f(Rx) = f(x)$ for every rotation $R$. 

**Cor:** The Fourier transform of a radial function is radial

An example of a radial function in $\Bbb R^n$ is the Gaussian $e^{-\pi \|x\|^2}$. Also, we notice that the radial functions on when $n = 1$ are precisely the even functions.

**Lemma:** Let $f(x) = e^{-\pi \|x\|^2}$ has a Fourier transform of $$\hat f(\omega) = e^{-\pi \|\omega\|^2}$$and as a consequence, we have that $\delta> 0$, and $f(x) =\exp(-\pi \delta\|x\|^2)$, then $$\hat f(\omega) = \delta^{-n/2} \exp(\pi\|x\|^2/\delta)$$
**Prop:** The family $K_\delta(x) = \delta^{-n/2} e^{-\pi \|x\|^2/\delta}$ is a family of good kernels in $\Bbb R^n$:
$$\int_{\Bbb R^n} K_\delta(x)\, dx = 1$$
$$\int_{\Bbb R^n} |K_\delta(x)|\, dx \le M$$
for every $\eta >0$, $$\lim_{\delta\to 0^+}\int_{\|x\|\ge \eta}K_\delta(x) \, dx = 0$$
As a result: $$\lim_{\delta\to 0^+}\int_{\Bbb R^n} K_\delta(x) F(x)\, dx = F(0)$$when $F$ is a Schwartz function, or more generally when $F$ is bounded and continuous at the origin

**Cor:** If $f\in \mathcal S(\Bbb R^n)$, the  $$(f*K_\delta)(x) \to f(x) \qquad \text{uniformly in }x \text{ as } \delta \to 0$$
**Th:** Let $f$ and $g$ be in $\mathcal S(\Bbb R^n)$, then $$\int_{\Bbb R^n} f(x) \hat g(x) \, dx = \int_{\Bbb R^n}  \hat f(y)  g(y) \, dy $$

### Fourier Inversion
We can see that the Fourier transform $\mathcal F$ is a bijective map of $\mathcal S(\Bbb R^n)$ to itself whose inverse is $$\mathcal F^* (g)(x) = \int_{\Bbb R^n} g(\omega) e^{2\pi i x\cdot \omega}\, d\omega$$
meaning that $$f(x) = \int_{\Bbb R^n} \hat f(\omega) e^{2\pi i x\cdot \omega}\, d\omega$$
Now we get the [[Convolution]], we defined $$(f*g)(x) = \int_{\Bbb R^n} f(y)g(x-y)\, dy$$with $f,g \in \mathcal S(\Bbb R^n)$, and get that $$\widehat{(f*g)}(\omega) = \hat f(\omega) \hat g(\omega)$$
### Plancherel Formula
Moreover , for $f\in \mathcal S(\Bbb R^n)$ $$\int_{\Bbb R^n}|\hat f(\omega)|^2\, d\omega = \int_{\Bbb R^n}| f(x)|^2\, dx$$
