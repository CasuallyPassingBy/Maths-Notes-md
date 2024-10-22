---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Hilbert Spaces]], [[Good Kernels and Convergence in Fourier Analysis]], [[Lp spaces]]


# In  $L^2([0, 2\pi])$ 
Let's consider the $L^2([0,2\pi])$, then we know that the inner product is of the form $$\langle f, g\rangle = \frac{1}{2\pi} \int_0^{2\pi} f(\theta) \overline{g(\theta)} \, d\theta$$and the norm $$\|f\|^2 = \frac{1}{2\pi} \int_0^{2\pi}|f(\theta)|^2\, d\theta$$
For each integer $n$, let $e_n(\theta) = e^{in\theta}$, and observe that that the family $\{e_n\}_{n \in \Bbb Z}$ is *orthonormal*; that is $$\langle e_n, e_m\rangle = \delta_{n,m}$$with $\delta_{n,m}$ being the Kronecker delta. 

Let $f$ be integrable function on the circle and let $a_n$ denote its Fourier coefficients. We see that the Fourier coefficients are represented by inner products of $f$ with the elements in the orthonormal set $\{e_n\}_{n \in \Bbb Z}$: $$\langle f, e_n\rangle  = \frac{1}{2\pi} \int_0^{2\pi} f(\theta) e^{-in\theta}\ d\theta = a_n$$
We see that $S_N(f) = \sum_{|n| \le N} a_n e_n$. Then the orthonormal property of the family $\{e_n\}$ and the fact that $\langle f, e_n\rangle$ imply that $f - \sum_{|n|\le N} a_n e_n$ is orthogonal to $e_n$, for all $|n| \le N$. There for we have that $$(f- S_N(f)) \perp \sum_{|n| \le N} b_n e_n$$for any complex numbers $b_n$. From this fact we get that, $f = (f-S_N(f)) + S_N(f)$, and $$\|f\|^2 = \|f-S_N(f)\|^2+\left\|\sum_{|n| \le N}a_n e_n\right\|^2$$by the orthonormality we have that $$\left\|\sum_{|n| \le N}a_n e_n\right\|^2 = \sum_{|n| \le N}|a_n|^2$$, we deduce that $$\|f\|^2 = \|f-S_N(f)\|^2+\sum_{|n| \le N}|a_n|^2$$
**Best Approximation:** If $f$ is integrable on the circle with Fourier coefficients $a_n$, then $$\|f-S_N(f)\| \le \left\|f-\sum_{|n|\le N} c_n e_n\right\|$$for any complex numbers $c_n$. Moreover, equality holds precisely when $c_n = a_n$ for all $|n|\le N$. 

**Th:** Let $f$ be an integrable function on the circle with $f \sim \sum_{n \in \Bbb Z} a_n e^{in \theta}$. Then we have that:
- Mean-square convergence of the Fourier series: $$\frac{1}{2\pi} \int_0^{2\pi} |f(\theta)- S_N(f)(\theta)|^2 \, \theta \to 0 \qquad N\to \infty$$or $S_N(f) \to f$ in $L^2([0, 2\pi])$
- **Parseval's identity** $$\sum_{n = -\infty}^\infty |a_n|^2 = \frac{1}{2\pi} \int_0^{2\pi}|f(\theta)|^2\, d\theta$$In general, we can make $f$ be $L$ periodic then get $$\sum_{n = -\infty}^\infty |a_n|^2 = \frac{1}{L} \int_0^{L}|f(\theta)|^2\, d\theta$$
**Bessel's Inequality:** Let $\{e_n\}$ is *any* orthogonal family of function on the circle, and $a_n = \langle f, e_n \rangle$, then we may deduce that $$\sum_{n = -\infty}^\infty |a_n|^2 \le  \|f\|^2$$
We have associated every element of $L^2([0, 2\pi])$ with a sequence $\{a_n\}$, and Parseval's identity guarantees that $\{a_n\} \in \ell^2(\Bbb Z)$. 

**Riemann-Lebesgue Lemma** If $f$ is integrable on the circle, then $\hat f(n) \to 0$ as $|n| \to \infty$. An equivalent reformulation, if that if $f$ is integrable in $[0, 2\pi]$, then $$\int_0^{2\pi} f(\theta) \sin(N\theta)\, d\theta \to 0 \qquad N \to \infty$$and $$\int_0^{2\pi} f(\theta) \cos(N\theta)\, d\theta \to 0 \qquad N \to \infty$$
**Cor:** Let $f$ be a periodic and of class $\mathcal C^k$, then $$\hat f(n) = o(1/|n|^k)$$

**Lemma:** suppose that $F$ and $G$ are integrable on the circle with $$F \sim \sum a_m e^{in\theta} \quad \text{and}\quad G \sim \sum b_n e^{in\theta}$$
Then $$\frac{1}{2\pi} \int_0^{2\pi} F(\theta) \overline{ G(\theta)}\, d\theta = \sum_{n = -\infty}^\infty a_n \overline{b_n}$$
and if we a make $F$ and $G$ be $L$ periodic, we get that $$\frac{1}{L} \int_0^L F(\theta) \overline{ G(\theta)}\, d\theta = \sum_{n = -\infty}^\infty a_n \overline{b_n}$$

With this we have more things to prove the absolute convergence and hence uniform convergence.

We say that $f$ satisfies a Hölder condition of order $\alpha$, namely $$|f(x)-f(y)| \le C|x-y|^\alpha $$for some $0 < \alpha \le 1$, and some $C>0$ and all $x, y$. Then $$\hat f(n) = O(1/|n|^\alpha)$$We note that for $\alpha = 1$, then $f$ is Lipschitz continuous. 

**Bernstein Theorem:** If $f$ satisfies a Hölder condition of order $\alpha > 1/2$, then the Fourier series of $f$ converges absolutely.

## Pointwise Convergence
**Th:** Let $f$ be an integrable function on the circle which is differentiable at a point $\theta_0$. Then $S_N(f)(\theta_0) \to f(\theta_0)$ as $N\to \infty$. 

We can weaken further if we only assume that $f$ satisfies a *Lipschitz condition* at $\theta_0$; that is $$|f(\theta) - f(\theta_0) \le |\theta - \theta_0|$$For some $M\ge 0$ and all $\theta$.

**Riemann Localisation Theorem:** Suppose $f$ and $g$ are two integrable functions defined on the circle, and for some $\theta_0$ there exists an open interval containing $\theta_0$ such that $$f|_I = g|_I$$then $S_N(f)(\theta_0) - S_N(g)(\theta_0) \to 0$ as $N\to \infty$. 

We also have that near a discontinuity, we have that the Fourier series tend to overshoot/undershoot, by around 9% of the jump at this is called *Gibb's phenomenon*