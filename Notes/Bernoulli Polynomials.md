---
tags:
  - SpecialPolynomials
---
Subjects: [[Special Polynomials]]
Links: [[Bernoulli numbers]]

We define the *Bernoulli polynomials* $B_n(x)$ by the formula $$\frac{ze^{xz}}{e^z-1}= \sum_{n = 0}^\infty \frac{B_n(x)}{n!}z^n$$
The functions $B_n(x)$ are polynomials in $x$ and $$B_n(x) = \sum_{k = 0}^n {n \choose k}B_k x^{n-k}$$
Some examples are: 
- $B_0(x) = 1$
- $B_1(x) = x-1/2$
- $B_2(x) = x^2-x+1/6$
- $B_3(x) = x^3-3/2+1/2x$

For $n\ge 1$, then $$\Delta B_n(x) = B_n(x+1)-B_n(x) = nx^{n-1}$$for $n \ge 2$, then $$B_n(0) = B_1(0) = B_n$$
With this we have we can calculate $$\sum_{k = 1}^n k^p = \frac1{p+1}(B_{p+1}(n+1) - B_{p+1}) $$
If we simplify then we get the *Faulhaber's formula*

We have that: 
- $B_0(x) = 1$
- $B_n'(x) = nB_{n-1}(x)$ for $n \ge 1$
$$\int_x^{x+1}B_n(t)\, dt = x^n$$
# Periodic Bernoulli Polynomials

We can make periodic versions of the original polynomials only considering $x\in (0,1)$, usually denoted with $P_n$ as the $n$th Periodic Bernoulli polynomial, then $$P_1(x) = -\frac1{\pi}\sum_{k = 1}^\infty \frac{\sin(2\pi k x)}{k}$$
Integrating we have that $$B_{2n}(x) = (-1)^{n+1}\frac{2(2n)!}{(2\pi)^{2n}}\sum_{k = 1}^\infty \frac{\cos(2\pi k x)}{k^{2n}}$$and $$B_{2n+1}(x) = (-1)^{n+1}\frac{2(2n+1)!}{(2\pi)^{2n+1}}\sum_{k = 1}^\infty \frac{\cos(2\pi k x)}{k^{2n+1}}$$
In general we have that $$B_n(x) = - \frac{n!}{(2\pi i)^n}\sum_{k \ne 0} \frac{e^{2\pi i k x}}{k^n}$$