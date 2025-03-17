---
tags:
  - FourierAnalysis
  - GroupTheory
---
Subjects: [[Fourier Analysis]], [[Group Theory]]
Links: [[Main definitions for Fourier Analysis]], [[Cyclic Groups]], [[Integers modulo n]]

Let $n \in \Bbb N$. 

We first need to define the space $$L^2(\Bbb Z_n) := \Bbb C^{\Bbb Z_n}.$$It is a finite dimensiona vector space with an inner product: $$\langle f, g\rangle := \sum_{x \in \Bbb Z_n} f(x) \overline{g(x)}, \qquad \text{for }f, g \in L^2(\Bbb Z_n).$$This inner product makes $L^2(\Bbb Z_n)$ a finite dimensional inner product space. We can get a norm $$\|f\| := \langle f, f\rangle^{1/2}.$$Additionally, there's a natural base where $\delta_a(x) := \delta_{a, x}$, where $\delta_{a,x}$ is Kronecker's delta. This base is actually, orthonormal. Meaning, that $\langle \delta_a, \delta_b\rangle = \delta_{a, b}$. The way we can write $f\in L^2(\Bbb Z_n)$ as $$f(x) = \sum_{a = 1}^n f(a) \delta_a(x), \qquad f(a) = \langle f, \delta_a\rangle.$$Lastly, we can define a vector space isomorphism $T: L^2(\Bbb Z_n)  \to \Bbb C^n$ defined by $$T(f) := (f(0), \dots f(n-1)).$$
**Def:** Suppose $f, g: \Bbb Z_n \to \Bbb C$. We define the *convolution* $f * g$ by $$(f*g)(x) = \sum_{y \in \Bbb Z_n} f(y) g(x-y), \qquad x \in \Bbb Z_n.$$
**Prop:** Let,$f, g, h : \Bbb Z_n \to \Bbb C$:
- $f*g = g*f$
- $f*(g*h) = (f*g)*h$
- $\delta_a* \delta_b = \delta_{a+b}$
- $(f*\delta_a)(x) = f(x-a)$

Looking for an analogue of $e^{ix} = \cos x+ i\sin x$, for a discrete setting. 

**Def:** Suppose $a, x \in \Bbb Z_n$. Define: $$e_a(x) := \exp\left(\frac{2\pi i ax}{n}\right).$$Note that $e_a(x)$ is independent of the congruence class representation chosen for $x$ and $a$. If$\Bbb S^1$ denotes the multiplicative group of complex numbers of modulus $1$, then $e_a: \Bbb Z_n \to \Bbb S^1$ is group homomorphism. Such a homomorphism is often called a *character* of ($1$-dimensional representation) of $\Bbb Z_n$. 

**Def:** The *discrete Fourier transform* or *DFT* of $f\in L^2(\Bbb Z_n)$ is $$\mathcal F_n f(x) = \mathcal F f(x) = \hat f(x) = \sum_{y\in \Bbb Z_n} f(y) e_x(-y) = \langle f, e_x\rangle.$$Clearly $\mathcal F: L^2(\Bbb Z_n) \to L^2(\Bbb Z_n)$ is a a linear map. 

**Prop:** Using the basis of $L^2(\Bbb Z_n)$ given by the delta function defined, then $$[\mathcal F_n]_\beta = [\omega^{jk}]_{0 \le j, k < n},$$where $\omega = \exp(2\pi i/n)$. 

**Lemma:** For $a, b\in \Bbb Z_n$. Then $$\langle e_a, e_0\rangle n \delta_0(a).$$Similarly we have $$\langle e_x, e_y \rangle = n\delta_x(y).$$