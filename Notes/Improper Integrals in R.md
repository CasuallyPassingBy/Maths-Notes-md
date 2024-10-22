---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Riemann Integral in R]]
## Type I (Unbounded Domains)

### Definitions

Let’s consider the following intervals: $[a, \infty), (-\infty, a]$ and $\mathbb{R}$.

_**Definition:**_ Let $f:[a, \infty)\to\mathbb{R}$, for any $b > a$, $f\in\mathcal{R}_{[a, b]}$, then the improper integral over $[a, \infty)$ is:

$$ \int_{[a,\infty)}f=\int_a^\infty f =\lim_{b\to\infty}\int_a^b f $$

_**Definition:**_ Let $f:(-\infty, b]\to\mathbb{R}$, for any $a < b$, $f\in\mathcal{R}_{[a, b]}$, then the improper integral over $(-\infty, b]$ is:

$$ \int_{(-\infty, b]} f= \int_{-\infty}^b f= \lim_{a\to-\infty}\int_a^b f $$

_**Definition:**_ Let $f:\mathbb{R}\to\mathbb{R}$, for any $a < b$, $f\in\mathcal{R}_{[a, b]}$, then the improper integral over $\mathbb{R}$ is:

$$ \int_{\mathbb{R}} f= \int_{-\infty}^\infty f= \lim_{a\to-\infty}\int_a^c f +\lim_{b\to\infty}\int_c^bf $$

For any $c\in\mathbb{R}$.
### Theorems

Let $f:[a,\infty)\to\mathbb{R}$, the improper integral over $[a, \infty)$ of $f$ converges iff:

$$ \forall\varepsilon>0\exists M\ge a\left(\forall d, c\ge M\left[\left|\int_c^df\right|<\varepsilon\right]\right) $$

_**Comparison Criterion:**_ Let $f,g:[a,\infty)\to\mathbb{R}$, and $0\le f\le g$, then:

1. If $\int_a^\infty g$ converges, then $\int_a^\infty f$ also converges.
2. If $\int_a^\infty f$ diverges, then $\int_a^\infty g$ also diverges.

_**Absolute Convergence:**_ If $\int_a^\infty |f|$ converges then $\int_a^\infty f$ also converges.


_**Limit Test:**_ Let $f,g$ be nonnegative continuous functions, defined on $I = [a,\infty)$, such that:

$$ \lim_{x\to\infty}\frac{f(x)}{g(x)} = L $$

- If $L\in\Bbb R^+$, then: $\int_If$ converges iff $\int_Ig$ converges.
- If $L = \infty$, then: If $\int_If$ converges then $\int_Ig$ converges.
- If $L = 0$, then: if $\int_Ig$ converges then $\int_If$ converges.

_**Dirichlet Test:**_ Let $f, g:[a,\infty)\to\Bbb R$, $f$ is continuous and $\lim_{x\to\infty}f(x) = 0$, and there’s an $M>0$, such that for any $b>a$ $\left|\int_a^b g\right|\le M$, then

$$

\int_a^\infty fg \text{ converges} $$

## Type II (Over Singularities)

### Definitions
Let $f:[a, b]\to\Bbb R$, with $\lim_{x\to b^-}f(x)=\pm\infty$, and for any $c\in[a,b) (f\in\mathcal{R}_{[a,c]})$. Then the integral over $[a,b]$ of is defined as:

$$ \int_a^b f= \lim_{c\to b^-}\int_a^cf $$

Let $f:[a, b]\to\Bbb R$, with $\lim_{x\to a^+}f(x)=\pm\infty$, and for any $c\in(a,b] (f\in\mathcal{R}_{[c, b]})$. Then the integral over $[a,b]$ of is defined as:

$$ \int_a^b f= \lim_{c\to a^+}\int_c^bf $$

### Theorems

_**Comparison Criterion:**_ Let $f,g:[a,b)\to\mathbb{R}$, and $0\le f\le g$, then:

1. If $\int_a^b g$ converges, then $\int_a^bf$ also converges.
2. If $\int_a^b f$ diverges, then $\int_a^b g$ also diverges.

_**Absolute Convergence:**_ If $\int_a^b |f|$ converges then $\int_a^b f$ also converges.

_**Limit Test:**_ Let $f,g$ be nonnegative continuous functions, defined on $I = [a,b)$, such that:

$$ \lim_{x\to b^-}\frac{f(x)}{g(x)} = L $$

- If $L\in\Bbb R^+$, then: $\int_If$ converges iff $\int_Ig$ converges.
- If $L = \infty$, then: If $\int_If$ converges then $\int_Ig$ converges.
- If $L = 0$, then: if $\int_Ig$ converges then $\int_If$ converges.