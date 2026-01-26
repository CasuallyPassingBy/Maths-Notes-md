---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]], [[Vector Analysis]]
Links: [[Fubini's Theorem]], [[Riemann Integral in R]], [[Improper Integrals in R]], [[Riemann-Steiltjes Integral on R]]
### Differentiation under the integral sign
Let $f:[a,b]\times [c,d]\to \Bbb R$ continuous such that $\partial_y f$ exists and is continuous on ${[a,b]\times[c,d]}$. Let $g:[c,d] \to \Bbb R$ as:
$$ g(y) = \int_a^b f(x,y)\,dx $$

Then $g$ is differentiable on $[c,d]$ and
$$ g'(y) = \int_a^b \frac{\partial f}{\partial y}(x,y)\,dx $$

**Rudin's Version:** Suppose
- $\varphi(x, t)$ is defined for $(x, t)\in [a,b]\times[c, d]$.
- $\alpha$ is an increasing function on $[a, b]$.
- $varphi_t\in \mathcal R(\alpha)$ for every $t\in [c, d]$.
- $c<s<d$, and to every $\varepsilon >0$ corresponds a $\delta>0$ such that $$|\partial_t \varphi(x, t) - \partial_t\varphi(x, s)| <\varepsilon $$for all $x\in [a,b]$ and for all $t\in (s-\delta, s+\delta)$. 
Define $$f(t) := \int_a^b \varphi(x,t)\, d\alpha(x).  $$Then $(\partial_t\varphi)^s\in \mathcal R(\alpha),$ $f'(s)$ exists and $$f'(s) = \int_a^b \frac{\partial \varphi}{\partial t}(x, s)\, d\alpha(x). $$

***Def:*** Let $f:D=A\times [c, \infty) \to \Bbb R$ be integrable over $[c,\infty)$ for all $x \in [a,b]$. Then we can define

$$ F(x) = \int_c^\infty f(x,t)\, dt =\lim_{d\to \infty }\int_c^d f(x, t)\, dt $$
This is _pointwise convergence_ of $F$.

We can define _uniform convergence_ of $F$. If for all $x \in A$, $F(x)$ exists. We say that the improper integral converges uniformly to $F$ on $A$ if for all $\varepsilon>0$, there’s an $M > c$ such that if $d\ge M$ and any $x \in A$ then
$$ \left|F(x) - \int_c^d f(x, t)\, dt\right| <\varepsilon $$

********Cor:********* If the improper integral $\int_c^\infty f(x, t)\, dt$ converges uniformly, and we define a sequence

$$ F_n(x) = \int_c^{c+n} f(x, t)\, dt $$

Then $F_n$ converges uniformly to $F$.
**************Th:************** If $f: D= [a,b]\times [c,\infty ) \to \Bbb R$ is continuous and ${F(x) = \int_c^\infty f(x, t)\, dt }$ converges uniformly, then $F$ is uniformly continuous.

### Weiestrass M-Test for Improper Integrals V.2
If $f(x, t)$ satiesfies $|f(x,t) |\le g(t)$ for all $x \in A$, and $\int_c^\infty g(t)\, dt$ converges, then $\int_a^\infty f(x,t)\, dt$ converges uniformly.

**************Th:************** If $f: D= [a,b]\times [c,\infty ) \to \Bbb R$ is continuous and ${F(x) = \int_c^\infty f(x, t)\, dt }$ converges uniformly, then $F$ is uniformly continuous.

### Differentiation under the integral sign for improper integrals
Let $f:[a,b]\times[c,\infty)\to \Bbb R$ is continuous and ${F(x) = \int_c^\infty f(x,t)\, dt}$ for each $x \in [a,b]$. If the partial derivative of $\partial _xf(x,t)$ exists and is continuous, then

$$ F'(x) = \int_c^\infty \frac{\partial f}{\partial x}(x, t)\, dt $$
# Multivariate Version

**Differentiation Under an Integral Sign:** Let $U\subseteq \Bbb R^n$ be an open subset, and let $a, b\