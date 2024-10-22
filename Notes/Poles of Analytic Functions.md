---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Zeros of Analytic Functions]], [[Analytic Functions]]

**Def:** Let $z_0 \in \Bbb C$ be an isolated singularity of the function $f$. We say that $z_0$ is a pole of $f$ if
$$ \lim_{z \to z_0}f(z) = \infty $$

**Def:** Let $z _0 \in \Bbb C$. We say that $z_0$ is a pole of order $k\in\Bbb N$ of the function $f$ if $z_0$ is a zero of order $k$ of the function $g=1/f$

**Def:** Let $f:\Omega \to \Bbb C$ be analytic in $\Omega$ except for isolated points, that are poles, then $f$ is called meromorphic.

**Prop:** Let $z_0 \in \Omega$ and $f:\Omega \setminus \{z_0\}\to \Bbb C$ analytic. it follows that: $z_0$ is a pole of order $k\in \Bbb N$ of $f$ iff there’s $f_k : \Omega \to \Bbb C$ analytic such that
$$ f(z) = (z-z_0)^{-k} f_k(z) = \frac{f_k(z)}{(z-z_0)^k} $$
for all $z \in \Omega\setminus \{ z_0\}$ and $f_k(z_0) \ne 0$

**Prop:** Let $z_0 \in \Omega \subseteq\Bbb C$ and $f:\Omega \setminus \{z_0\} \to \Bbb C$ analytic. It follows that: $z_0$ is a pole of order $k \in \Bbb N$ of $f$ iff there’s $B_1, \dots B_k \in \Bbb C$, $B_k \ne 0$, and a function $\varphi:\Omega\to \Bbb C$ analytic such that

$$ f(z) = \sum_{n = 0}^k \frac{B_n}{(z-z_0)^n} + \varphi(z) $$

for all $z \in \Omega\setminus\{z_0\}$, additionally the numbers $B_1, \dots B_k$ and the function $\varphi$ are unique

The sum

$$ \sum_{n = 0}^k \frac{B_n}{(z-z_0)^n} $$

is called the singular part of the function $f$ at the pole $z = z_0$

**Prop:** Let $z_0 \in \Omega \subseteq\Bbb C$ and $f:\Omega \setminus \{z_0\} \to \Bbb C$ analytic and $r>0$ such that $\overline {B_r(z_0)}\subseteq \Omega$. If $z_0$ is a pole of order $k$ of $f$, then there’s $B_1, \dots B_k \in \Bbb C$, $B_k \ne 0$, and a sequence $(A_k)$ of complex numbers such that

$$ f(z) = \sum_{n = 0}^k \frac{B_n}{(z-z_0)^n} + \sum_{n = 0}^\infty A_n(z-z_0)^n $$

for all $z \in B_r(z_0) \setminus\{z_0\}$

#### L'Hôpital's Rules:
Let $f, g:\Omega \to \Bbb C$ be non constant analytic functions and $z_0 \in \Omega$. If $n$ is the order of $z_0$ as pole of $f$, and $m$ is the order of $z_0$ as pole of $g$,

- $n<m$, then   $$ \lim_{z\to z_0}\frac{f(z)}{g(z)} =0 $$
- $n = m$, then  $$ \lim_{z\to z_0}\frac{f(z)}{g(z)} = \frac{(1/g)^{(k)}(z_0)}{(1/f)^{(k)}(z_0)} $$
    
- $n> m$, then $$ \lim_{z\to z_0}\frac{f(z)}{g(z)} = \infty $$
This another analogue of [[L'Hôpital's Rules]]

## Space of Meromorphic Functions

**Def**: Let $f: U \subseteq \Bbb C\to \widehat{\Bbb C}$, and $P(f) = \{z \in U \mid f(z) = \infty\}$. We say that $f$ us meromorphic at $U$ if
- $P(f)' \cap U = \varnothing$ 
- $f \in \mathcal H(U\setminus P(f))$

We denote $\mathcal M(U) := \{f: U \to \widehat{\Bbb C} \mid f \text{ is meromorphic on }U\}$ 

**Prop**: If $\{f_n\} \subseteq \mathcal C(U, \Bbb C)$ be a sequence such that $f_n \stackrel{\rho}{\longrightarrow} f$, then $$\frac{1}{f_n} \stackrel{\rho}{\longrightarrow} \frac{1}{f}$$**Th:** $\{f_n\}\subseteq \mathcal M(U)$ is such that $f_n \stackrel{\rho}{\longrightarrow} f$ on $\mathcal C(U, \Bbb C)$, then $f \in \mathcal M(U)$ or $f\equiv \infty$. 