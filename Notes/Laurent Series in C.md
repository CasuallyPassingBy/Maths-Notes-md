---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[Taylor's Theorem]], [[Isolated Singularities]], [[Removable Singularities]], [[Poles of Analytic Functions]], [[Essential Singularities]]

Let $z_0\in \Bbb C$ and $0\le r_1< r_2\le \infty$. We say that the open anulus centered at $z_0$ with an inner radius $r_1$, and exterior radius $r_2$, denoted as $A_{r_1, r_2}(z_0)$, as

$$ A_{r_1, r_2}(z_0) = \{z \in \Bbb C \mid r_1 < |z-z_0| <r_2\} $$

Let $z_0\in \Bbb C$ and $0\le r_1< r_2$. If $f$ is analytic on the anulus $A_{r_1, r_2}(z_0)$, then there exists ${f_1: \Bbb C\setminus \overline B_{r_1}(z_0) \to \Bbb C}$ and $f_2: B_{r_2}(z_0) \to \Bbb C$ analytic functions such that $f= f_1+f_2$ on $A_{r_1, r_2}(z_0)$

### Laurent Theorem

Let $z_0\in \Bbb C$ and $0\le r_1< r_2$. If $f$ is analytic on the anulus $A_{r_1, r_2}(z_0)$, then there exist two sequence of numbers $(B_n)$ and $(A_n)$ such that the series

$$ \sum_{n = 1}^\infty B_n(z-z_0)^{-n} \quad \text{ and } \quad \sum_{n = 0}^\infty A_n (z-z_0)^n $$

converge and satisfy that

$$ \sum_{n= 1}^\infty \frac{B_n}{(z-z_0)^n} + \sum_{n = 0}^\infty A_n(z-z_0)^n = f(z) $$

for all $z \in A_{r_1, r_2}(z_0)$. Furthermore if $r_1 < r<r_2$ and $\gamma_r(t) = re^{it} +z_0$, with $t\in[0, 2\pi]$, then

$$ A_n = \frac{1}{2\pi i}\oint_{\gamma_r}\frac{f(\zeta)}{(\zeta-z_0)^{n+1}}\, d\zeta $$

for all $n \in \Bbb N$, and

$$ B_n = \frac{1}{2\pi i}\oint_{\gamma_r} f(\zeta)(\zeta-z_0)^{n-1}\, d\zeta $$

for all $n \in \Bbb N^+$. The numbers $A_n$ and $B_n$ are the only ones that satisfy this notion of extender Talylor series. The series

$$ \sum_{n= 1}^\infty \frac{B_n}{(z-z_0)^n} $$

it is known as the singular part of $f$ in the anulus $A_{r_1, r_2}(z_0)$.

I think I can be somewhat lazy and just call $A_{-n} = B_n$ for $n \in \Bbb N^+$, then we can just use this notation

$$ f(z) = \sum_{n = -\infty}^\infty A_n(z-z_0)^n = \sum_{n \in \Bbb Z} A_n(z-z_0)^n $$

with this series as

$$ \sum_{n = -\infty}^1 A_n(z-z_0)^n $$
using this notation we get that 

$$ A_n = \frac{1}{2\pi i}\oint_{\gamma_r}\frac{f(\zeta)}{(\zeta-z_0)^{n+1}}\, d\zeta $$
for $n \in \Bbb Z$. 


being the singular part of $f$ in the anulus $A_{r_1, r_2}(z_0)$

Let $z_0 \in \Bbb C$ be a isolated singularity of $f$ and $R>0$ such that $f$ is analytic in $B_R(z_0)$. If $A_{-1}, A_{-2}, \dots, A_{-n}, \dots$ are the coefficients of the singular part of $f$ of the anulus ${A_{0, R}(z_0) = B_R(z_0) \setminus \{ z_0\}}$, then

- $z_0$ is a removable singularity of $f$ iff $A_{-n} = 0$ for all $n \in \Bbb N^+$
- $z_0$ is a pole of order $k \in \Bbb N^+$ iff $A_{-k }\ne 0$ and $A_{-n} =0$ for all $n > k$
- $z_0$ is an essential singularity of $f$ iff $A_{-n} \ne 0$ for infinitely many $n \in \Bbb N^+$