---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Power Series in R]]

Let $f$ be $N+1$ differentiable, then

$$ S_N(x) = \sum_{n = 0}^N \frac{f^{(n)}(a)}{n!}(x-a)^n $$

$S_N(x)$ is $N$th Taylor polynomial centered at $a$, and $E_N(x) = f(x) -S_N(x)$ is the error function of our approximation.

### Lagrange Remainder Theorem

Let $f$ be differentiable $N+1$ times on $(-R,R)$. Given $x \neq 0$ in $(-R, R)$, there exists a point $c$ in between $a$ and $x$

$$ E_N(x) = \frac{f^{(N+1)}(c)}{(N+1)!} x^{N+1} = \frac{1}{N!}\int_a^x f^{(N+1)}(t)(x-t)^N \,dt $$

### Weak Lagrange Remainder Theorem

Let $f$ be differentiable $N+1$ times on , and $f^{(N+1)}$ be bounded between $a$ and $x$, then:

$$ |E_N(x) | \le \frac{M}{(N+1)!}|x-a|^{N+1} $$

for some $M>0$.

### Cauchy Remainder Theorem

Let $f$ be differentiable $N+1$ times on $(-R,R)$. Given $x \neq 0$ in $(-R, R)$, there exists a point $c$ in between $a$ and $x$

$$ E_N(x) = \frac{f^{(N+1)}(c)}{N!} (x-c)^{N}(x-a) $$

### Weak Cauchy Remainder Theorem

Let $f$ be differentiable $N+1$ times on , and $f^{(N+1)}$ be bounded between $a$ and $x$, then:

$$ |E_N(x) | \le \frac{M}{N!}|x-a|^{N+1} $$

for some $M>0$.