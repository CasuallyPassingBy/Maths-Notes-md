---
tags:
  - SpecialPolynomials
---
Subjects: [[Special Polynomials]]
Links: [[Rectifiable Curves in Rn]]
A Bernstein polynomial is a polynomial of the form:

$$ b_{\nu, n}(x) = \binom{n}{\nu}x^\nu(1-x)^{n-\nu} $$

The set $\{b_{\nu, n}\}_{\nu = 0}^n$ is a basis for $P_n(\Bbb R) = \Pi_n$ or the polynomials with real coefficients of at most degree $n$, then: 

$$ p(x) = \sum_{\nu= 0}^n \beta_\nu b_{\nu, n}(x) $$

is the _Bernstein form_ of the polynomial $p(x)$, the coefficietns are called *Bernstein coefficients* or *Bézier coefficients*.

Given a collection of points $\{P_k\}_{k=0}^n$, then the Bézier Curve with $P_k$ as its control points it’s:
$$ {B}(t) = \sum_{k=0}^n P_k b_{k,n}(t) $$
and $t\in [0,1]$.
In particular it has a neat property, that for any $n\in \Bbb N$:

$$ \sum _{\nu = 0}^n b_{\nu, n} = 1 $$

### Properties

$b_{\nu, n} (x) = 0$ if $\nu < 0$ or $\nu >n$

$b_{\nu, n} (x) \ge 0$, for $x \in [0,1]$

$b_{\nu, n} (1-x) = b_{n-\nu, n}(x)$

$b_{\nu, n} (0) = \delta_{\nu, 0}$ and $b_{\nu, n} (1) = \delta_{\nu, n}$, where $\delta_{ij}$ is the Kronecker delta

$b_{\nu, n} (x)$ has a root with multiplicity $\nu$ at $x=0$, if $\nu =0$, then there’s no root

$b_{\nu, n} (x)$ has a root with multiplicity $n-\nu$ at $x=1$, if $\nu =n$, then there’s no root

$b'_{\nu, n} (x) = n(b_{\nu-1, n-1}(x) - b_{\nu, n-1}(x))$

If $n \ne 0$, then $b_{\nu, n} (x)$ has a unique local maximum on $[0,1]$ at $x = \dfrac{\nu}{n}$, with the value

$$ \nu^\nu n^{-n}(n-\nu)^{n-\nu} {n \choose \nu} $$

We can show that

$$ \sum_{\nu = 0}^n \nu b_{\nu, n}(x) =nx \\ \;\\ \sum_{\nu = 0}^n \nu(\nu-1) b_{\nu, n}(x) =n(n-1)x^2 $$

The antiderivative of $b_{\nu, n}$ is given by

$$ \int b_{\nu, n}(x)\, dx = \frac{1}{n+1} \sum_{j = \nu+1}^{n+1} b_{j, n+1}(x) $$

the integral over $[0,1]$ of $b_{\nu, n}$ is

$$ \int_0^1 b_{\nu, n}(x) \, dx = \frac{1}{n+1} $$

The transformations of Berstein Polynomials to monomials is

$$ b_{\nu, n}(x) = {n\choose \nu }\sum_{k = 0}^{n-\nu}{n-\nu \choose k}(-1)^{n-\nu-k } x^{\nu+k} = \sum_{k =\nu}^n{n \choose k}{k \choose \nu} (-1)^{k-\nu} x^k $$

using the inverse binomial transformation we get that

$$ x^k = \sum_{i = 0}^{n-k} {n-k \choose i}\frac{1}{n \choose i} b_{n-i, n}(x) =\frac{1}{n\choose k} \sum_{j = k}^n {j \choose k} b_{j, n}(x) $$