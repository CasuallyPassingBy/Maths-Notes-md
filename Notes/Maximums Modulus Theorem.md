---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Cauchy's Integral Formula]], [[Homotopy Cauchy's Theorem]], [[Homology Cauchy's Theorem]]

### Mean Value Property

Let $f$ be holomorphic inside and on a circle of radius $r$ and center $z_0$ (that is, holomorphic on a region containing the circle and its interior). Then

$$ f(z_0)= \frac{1}{2\pi } \int_0^{2\pi} f(z_0 + re^{i\theta})\, d\theta $$

This is a direct consequence of [[Cauchy's Integral Formula]]

### Maximum Modulus Principle - Local Version

Let $f$ be holomorphic on a region $A$ and suppose $|f|$ has a relative maximum at $z_0 \in A$ .(That is, ${|f(z)| \le |f(z_0)|}$ for all $z$ in some neighborhood of $z_0$.) Then $f$ is constant in some neighborhood of $z_0$.

### Maximum Modulus Principle

Let $A$ be an open, connected, and bounded set in $C$ and suppose $f:\operatorname{cl}(A) \to \Bbb C$ is holomorphic on $A$ and continuous $\operatorname{cl}(A)$. Then $|f|$ has a finite maximum modulus on $\operatorname{cl}(A)$ which is attained at some point on the boundary of $A$. If it also attained in the interior of $A$, then $f$ must be constant on $\operatorname{cl}(A)$.

### Schwarz Lemma

Let $f$ be an holomorphic on the open set $A = B_1(0)$ with $f(0) = 0$ and each $|f(z)|\le 1$ for each $z \in A$. Then $|f'(0)|\le 1$ and $|f(z)|\le |z|$ for each $z \in A$. If $|f'(0)| =1$ or there is a point $z_0$ other than $0$ in $A$ with $|f(z_0)| =|z_0|$, then there is a constant $c$ with $|c| =1$ and ${f(z) = cz}$ for all $z \in A$.

General Version

Let $f$ be an holomorphic and $M, R>0$ on the open set $A = B_R(0)$ with $f(0) = 0$ and each $|f(z)|\le M$ for each $z \in A$. Then $|f'(0)|\le M/R$ and $|f(z)|\le |z|M/R$ for each $z \in A$. If $|f'(0)| =M/R$ or there is a point $z_0$ other than $0$ in $A$ with $|f(z_0)| =|z_0|M/R$, then there is a constant $c$ with $|c| =1$ and ${f(z) = czM/R}$ for all $z \in A$.