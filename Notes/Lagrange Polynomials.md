---
tags:
  - NumericalAnalysis
  - SpecialPolynomials
---
Subjects: [[Numerical Analysis]], [[Special Polynomials]]

Let $\{x_0, x_1, \dots, x_n\}$, with must all be distinct $x_j \ne x_m$ for indices $j \ne m$, the Lagrange basis for polynomials of degree $\le n$ for those nodes in the set of polynomials $\{\ell_0(x), \ell_1(x), \dots, \ell_n(x)\}$ each of degree $k$ which take values $\ell_j(x_m) = \delta_{jm}$. Each element of the basis can be explicitly described by the product:

$$ \ell_j(x) = \prod_{\begin{smallmatrix}0\le m\le k\\ m\neq j\end{smallmatrix}} \frac{x-x_m}{x_j-x_m} $$

when we want to be explicit that it is used to interpolate $n+1$ points, then $L_{n,k} = \ell _k$.

If $\{x_0, x_1, \dots, x_n\}$ are distinct $n+1$ numbers and $f$ is a function whose values are given at this numbers, the unique polynomial $P$ of degree at most $n$ exists with

$$ f(x_k) = P(x_k)\qquad 0 \le k \le n $$

The polynomial is given by

$$ P(x)= \sum_{k = 0}^n f(x_k) L_{n, k}(x) $$
Which shows us how it is a basis for the polynomials that go at the points $\{x_1, \dots, x_n\}$

Suppose $\{x_0, x_1, \dots, x_n\}$ are distinct numbers in the interval $[a,b]$ and $f\in \cal{C}^{n+1}[a,b]$. Then, for each $x \in [a,b]$, a number $\xi(x)$ (generally unknown) between $\min\{x_0, x_1, \dots, x_n\}$ and $\max\{x_0, x_1, \dots, x_n\}$ and hence in $(a,b)$, exists with $$ f(x) = P(x) +\frac{f^{(n+1)}(\xi(x))}{(n+1)!}\prod_{k = 0}^n (x-x_k) $$
We can estimate the error of the polynomial, as
$$ \|f - P\|_\infty = \sup_{x\in [a,b]} |f(x)-P(x)| \le \sup_{x\in[a,b]}\frac{|f^{(n+1)}(x)|}{(n+1)!}\sup_{x \in [a,b]}\prod_{k = 0}^n|x-x_k| $$

This polynomials can have something called [[Runge's phenomenon]]