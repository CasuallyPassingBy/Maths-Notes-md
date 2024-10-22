---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Fourier Transform in R]]

Given a function $f\in \mathcal S(\Bbb R)$ on the line we can construct a new function on the circle by the recipe $$F_(x) = \sum_{n = -\infty}^\infty f(x+n)$$Since $f$ is rapidly decreasing, the series converges absolutely and uniformly on every compact subset of $\Bbb R$, so $F_1$ is continuous. We see that $F_1(x+1) = F(x)$, hence $F_1$ is periodic with period $1$. The function $F_1$ is called the *periodization* of $f$.

There is another way to arrive at a "periodic version" of $f$, this time by Fourier analysis. $$f(x) = \int_{-\infty}^\infty \hat f(\omega) e^{2\pi i x \omega}\, d\omega$$and consider the discrete analogue, where the integral is replaced by a sum $$F_2(x) = \sum_{n = -\infty}^\infty \hat f(n) e^{2\pi inx}$$Once again, the sum converges absolutely and uniformly since $\hat f$ belongs to the Schwarz space, hence $F_2$ is continuous, and periodic of period $1$. 

**Th:** If $f\in \mathcal S(\Bbb R)$, then $$\sum_{n = -\infty}^\infty f(x+n) = \sum_{n = -\infty}^\infty \hat f(n) e^{2\pi in x}$$in particular, when setting $x = 0$ we have that $$\sum_{n = -\infty}^\infty f(n) =\sum_{n = -\infty}^\infty \hat f(n)$$
We observe that the theorem extends to the case when we merely assume that both $f$ and $\hat f$ are of moderate decrease; the proof is in fact unchanged.

Using the same procedure of the proof i got that:

If $f\in \mathcal S(\Bbb R)$, then $$\sum_{n = -\infty}^\infty \hat f(\omega+n) = \sum_{n = -\infty}^\infty \hat f(n) e^{-2\pi in \omega}$$in particular, when setting $\omega = 0$ we have that $$\sum_{n = -\infty}^\infty f(n) =\sum_{n = -\infty}^\infty \hat f(n)$$
The following results are relevant in [[Information Theory|information theory]] when one tries to recover a signal from its samples:

Suppose $f$ is a of moderate decrease and that its Fourier transform $\hat f$ is supported in $I = [-1/2, 1/2]$. Then $f$ is entirely determined by its restriction to $\Bbb Z$. This means that if $g$ is another function of moderate decrease whose Fourier transform is supported in $I$ and $f(n) = g(n)$ for all $n\in \Bbb Z$, then $f = g$

We have the following reconstruction formula: $$f(x) = \sum_{n = -\infty}^\infty f(n) K(x-n)$$where $$K(y) = \frac{\sin \pi y}{\pi y}$$Not that $K(y) = O(1/|y|)$ as $|y|\to \infty$

If $\lambda > 1$, then $$f(x) = \sum_{n = -\infty}^\infty \frac1{\lambda}f\left(\frac{n}{\lambda}\right) K_\lambda\left(x - \frac{n}{\lambda}\right)$$where $$K_\lambda(y) = \frac{\cos\pi y- \cos\pi \lambda y}{\pi^2(\lambda-1)y^2}$$Thus, if one samples $f$ "more often", the series in the reconstruction formula converges faster since $K_\lambda(y) = O(1/|y|^2)$ as $y\to \infty$. Note that $K_\lambda \to K$ as $\lambda \to 1^+$. 

Also we have that $$\int_{-\infty}^\infty |f(x)|^2\ dx = \sum_{n =-\infty}^\infty |f(n)|^2$$
