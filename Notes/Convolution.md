---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Main definitions for Fourier Analysis]]
# Periodic functions

**Def**: Given $2\pi$-periodic integrable function $f$ and $g$ on $\Bbb R$, we the define the *convolution* $f*g$ on $[-\pi, \pi]$, by $$(f*g)(x) = \frac{1}{2\pi}\int_{-\pi}^\pi f(y)g(x-y)\, dy $$
Loosely speaking, convolutions correspond to "weighted averages". Also the convolution plays a similar role to the pointwise product $f(x)g(x)$ of the two functions $f$ and $g$. 

We can look at the $N$th partial sum of the Fourier series, then with some algebra we get that $$S_N(f)(x) =(f*D_N)(x) $$
where $D_N$ is the $N$th Dirichlet kernel

**Prop:** Suppose that $f, g$ and $h$ are $2\pi$-periodic integrable functions. Then:
- $f*(g+h) = (f*g)+(f*h)$
- $(cf)*g = c(f*g) = f*(cg)$ for any $c \in \Bbb C$
- $f*g= g*f$
- $(f*g)*h=f*(g*h)$
- $f*g$ is continuous
- $\widehat{f*g}(n) = \hat f(n) \hat g(n)$

**Lemma:** Suppose $f$ is integrable on the circle an bounded by $B$. Then there exists a sequence $\{f_k\}_{k = 1}^\infty$ of continuous functions on the circle so that $$\sup_{x \in [-\pi, \pi]} |f_k(x)| \le B\qquad k \in \in \Bbb N^+$$
and $$\int_{-\pi}^\pi |f(x)-f_k(x)|\, dx \to 0 \quad \text{as} \quad k \to \infty$$
# Rapidly Decreasing Functions

Let $f, g$ be functions on $\Bbb R$, we define their *convolution* is defined by $$(f*g)(x) = \int_{-\infty}^\infty (fx-t)g(t)\, dt$$