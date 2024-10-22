---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Contour Integrals in C]], [[Analytic Functions]]

### Goursat’s Theorem (Cauchy’s Theorem for Rectangles)

Let $f: \Omega\subseteq \Bbb C \to \Bbb C$ be holomorphic on $\Omega$ and $R = [a,b] \times [c,d] \subseteq \Omega$. If $\Gamma = \partial R$, and with $\gamma$ being a counterclockwise parametrization of $\Gamma$, then

$$ \oint_\gamma f =0 $$

### Local Version of Cauchy’s Theorem (Marsden)

Suppose $f:D \to \Bbb C$ is holomorphic on $D= B_\rho(z_0)\subseteq \Bbb C$, then

- $f$ has an primitive on $D$; that is, there is a function $F:D\to \Bbb C$ is holomorphic on $D$ and satisfies $F' =f$ on $D$
    
- If $\Gamma$ is a closed piecewise smooth curve in $D$ then
    
    $$ \oint_\Gamma f =0 $$
    

This tells us that if a function is holomorphic , then there’s a local primitive on an open neighborhood of $z_0$.

**********Lemma:********** Suppose $R$ is a rectangle with sides parallel to the axes, that $f$ is a function defined on an open set $G$ containing $R$, $f$ is holomorphic in $G\setminus \{z_1, \dots, z_n\}$, and let $z_1, \dots, z_m \not\in\partial R$. Suppose that at $z_1$, the function $f$ satistisfies $\lim_{z\to z_j}(z-z_j)f(z) =0$ for $1 \le j \le n$. Then

$$ \oint_{\partial R} f =0 $$

This lemma holds under any of the following situations:

- $f$ is bounded in a deleted neighborhood of $z_1, \dots, z_n$
- $f$ is continuous on $G$
- If $\lim_{z\to z_1}f(z)$ exists

**************Lemma:************** Suppose $R$ is a rectangle with sides parallel to the axes, that $f$ is a continuous function defined on an open set $G$ containing $R$, $f$ is holomorphic in $G\setminus \{z_1, \dots, z_n\}$. Then

$$ \oint_{\partial R} f =0 $$

### Strengthened Local Version of Cauchy’s Theorem

Suppose $f:D \to \Bbb C$ , where $D= B_\rho(z_0)\subseteq \Bbb C$ and holomorphic on $D\setminus \{z_1, \dots, z_n\}$ for some fixed points in $D$, with

$$ \lim_{z \to z_j} (z-z_j)f(z) =0 \quad \text{for }j \in \{1, \dots, n\} $$

- If $\gamma$ is a closed piecewise smooth curve in $D\setminus \{z_1, \dots, z_n\}$ then
    
    $$ \oint_\gamma f =0 $$