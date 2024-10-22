---
tags:
  - ComplexAnalysis
---

Subjects:  [[Complex Analysis]]
Links: [[Analytic Functions]], [[Taylor Series in R]], [[Power Series in R]], [[Analytic Convergence]], [[Higher Derivatives of Analytic Functions]]

********Def:******** Let $f:\Omega\subseteq \Bbb C \to \Bbb C$ analytic, $z_0 \in \Omega$ and $n\in \Bbb N$. We define $n$th degree Taylor polynomial of $f$ at $z_0$, (denoted by Paez as $p_{n , f, z_0}$) but the context good to just say

$$ T_n(z) = \sum_{k = 0}^n\frac{f^{(k)}(z_0)}{k!}(z-z_0)^k $$

******Th (Taylor):****** Let $f:\Omega\subseteq \Bbb C \to \Bbb C$ analytic, $z_0 \in \Omega$, $r>0$ such that $\overline {B_r(z_0)}\subseteq\Omega$ and ${\gamma_r(t) =re^{it}+ z_0}$ with $t\in [0 , 2\pi]$. For all $n \in \Bbb N$, there’s $f_n: \Omega\to \Bbb C$ analytic such that

$$ f(z) = T_{n-1}(z) + f_n(z) (z-z_0)^n $$

for all $z \in \Omega$, furthermore

$$ f_n(z) = \oint_{\gamma_r}\frac{f(\zeta)}{(\zeta-z_0)^n(\zeta-z)}\, d\zeta $$

for all $z \in B_r(z_0)$

********Th:******** Let $f:\Omega \subseteq\Bbb C \to \Bbb C$ analytic, $z_0 \in \Omega$ and $r>0$ such that $\overline {B_r(z_0)}\subseteq\Omega$. For each ${z \in B_r(z_0)}$ the series

$$ \sum \frac{f^{(k)}(z_0)}{k!}(z-z_0)^k $$

is convergent and furthermore

$$ \sum_{k = 0}^\infty \frac{f^{(k)}(z_0)}{k!}(z-z_0)^k = f(z) $$

********Prop:******** Let $f:\Omega \subseteq \Bbb C \to\Bbb C$ analytic and $z_0\in \Omega$ (a region, meaning open and connected) such that $f(z_0) =0$. If $f^{(n)}(z_0) =0$ for all $n \in \Bbb N$, then $f$ is the constant function $0$

## Power Series

********Cauchy-Hadamard Theorem:******** Let $\{a_n\}$ be a sequence of complex numbers

$$ R= \begin{cases} \frac{1}{\limsup \sqrt[n]{|a_n|}} &0< \limsup \sqrt[n]{|a_n|} <\infty \\ \infty & \limsup \sqrt[n]{|a_n|} = 0 \\ 0 & \limsup \sqrt[n]{|a_n|} =\infty \end{cases} $$

- If $0 < R\le \infty$, then the power series $\sum a_n(z-z_0)^n$ converges uniformly in $\overline{B_r(z_0)}$ for all $0 < r<R$
- If $0\le R< \infty$, then the power series $\sum a_n(z-z_0)^n$ doesn’t converge for any $z \in \Bbb C$ such that $|z-z_0|>R$
- If $0<r'$ is such that the power series $\sum a_n(z-z_0)^n$ converges for all $z \in \overline{B_{r'}(z_0)}$, then $r' \le R$

This number $R$ is called ************************the radius of convergence of the power series************************ $\sum a_n(z-z_0)^n$

************Prop:************ Let $f: \Omega\to \Bbb C$ analytic, $z_0\in \Omega$ and $r>0$ such that $\overline{B_r(z_0)} \subseteq \Omega$. The sequence $(\sqrt[n]{|f^{(n)}(z_0)|/n!})$ is such that

$$ \limsup \sqrt[n]{\frac{|f^{(n)}(z_0)|}{n!}} \le \frac{1}{r} $$

********Th:******** Let $(a_n)$ be a sequence of complex numbers such that

$$ \limsup_{n \to \infty} \sqrt[n]{|a_n|} = \alpha < \infty $$

If $R>0$, is the radius of convergence of the power series $\sum a_n(z-z_0)^n$, then the function ${f:B_R(z_0) \to \Bbb C}$ defined as

$$ f(z) = \sum_{n = 0}^\infty a_n(z-z_0)^n $$

is analytic in $B_R(z_0)$ and

$$ a_n= \frac{f^{(n)}(z_0)}{n!} $$

for each $n \in \Bbb N$

********Cor:******** Let $(a_n)$ and $(b_n)$ be sequences of complex numbers, $z_0 \in \Bbb C$ and $r>0$ such that the series $\sum a_n(z-z_0)^n$ and $\sum b_n(z-z_0)^n$ converge for all $z \in B_r(z_0)$. If

$$ \sum_{n = 0^\infty} a_n(z-z_0)^n= \sum_{n = 0^\infty} b_n(z-z_0)^n $$

for all $z \in B_r(z_0)$, then $a_ n = b_n$ for all $n \in\Bbb N$