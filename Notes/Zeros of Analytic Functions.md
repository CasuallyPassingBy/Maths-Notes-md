---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]]

# Zeros of Functions

********Cor:******** Let $f: \Omega \to \Bbb C$ analytic and $z_0 \in \Omega$ such that $f(z_0) = 0$. If $f$ is not constant, then there’s $k\in \Bbb N$, such that $f^{(k)}(z_0) \ne 0$

********Def:******** Let $f: \Omega \to \Bbb C$ analytic and $z_0 \in \Omega$ such that $f(z_0) = 0$. If $f$ is not constant, then we can define the *******_order of $z_0$_ (as a zero of $f$) as the minmum $k \in \Bbb N$ such that $f^{(k)}(z_0) \ne 0$

**Prop:** Let $f:\Omega \to \Bbb C$ be a nonconstant analytic function such taht $f(z_0) = 0$. It follows that: $z_0$ is a zero of order $k \in \Bbb N$ of $f$ iff there’s $f_k :\Omega \to \Bbb C$ analytic such that

$$ f(z) = (z-z_0)^kf_k(z) $$

for all $z \in \Omega$ and $f_k (z_0) \ne 0$, sometimes we can denote it as $m(f, a) = k$

**Cor:** Let $f:\Omega \to \Bbb C$ be a nonconstant analytic function such taht $f(z_0) = 0$, then there’s a $r>0$ such that $f(z)\ne 0$ for all $z \in B_r(z_0) \setminus \{z_0\} \subseteq \Omega$

**Cor:** Let $f:\Omega \to \Bbb C$ be an analytic function and $Z_f= \{ z \in \Omega \mid f(z) = 0 \}$. If $z_0 \in \Omega$ is an accumulation point of $Z_f$, $z_0 \in Z'_f$, then $f$ is the constant $0$.

********Cor:******** Let $f, g:\Omega \to \Bbb C$ be analytic functions and $A = \{ z \in \Omega \mid f(z) = g(z) \}$. If $z_0 \in \Omega$ is an accumulation point of $A$, $z_0 \in A$, then $f= g$, or $A= \Omega$.

**L'Hôpital's Rules:**

Let $f, g:\Omega \to \Bbb C$ be nonconstant analytic functions and $z_0 \in \Omega$ such that $f(z_0) = 0 = g(z_0)$. If $n$ is the order of $z_0$ as zero of $f$, and $m$ is the order of $z_0$ as zero of $g$, and let $k = \min\{n, m\}$, then

- $n<m$, then
    
    $$ \lim_{z\to z_0}\frac{f(z)}{g(z)} =0 $$
    
- $n = m$, then
    
    $$ \lim_{z\to z_0}\frac{f(z)}{g(z)} = \frac{f^{(k)}(z_0)}{g^{(k)}(z_0)} $$
    
- $n> m$, then
    

$$ \lim_{z\to z_0}\frac{f(z)}{g(z)} = \infty $$
This is an analogue of [[L'Hôpital's Rules|L'Hôpitals Rules in R]]