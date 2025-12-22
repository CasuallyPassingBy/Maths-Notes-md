---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]

There are quite a few methods of interpolation of data, using polynomials:

One of the reason, we know we can approximate continuous functions with polynomials is by the [[Stone-Weierstrass Theorem|Weiestrass Approximation Theorem]]

**Unisolvence Theorem:** Given a set of $n+1$ data points $(x_0,y_0),\dots, (x_n, y_n)$, with no $x_j$ the same, a polynomial function $p(x) = a_0+ \dots +a_n x^n$ is said to interpolate the data if $p(x_j) = y_j$ for each $j\in \{0,\dots, n\}$. There is a unique polynomial of degree $n$ that interpolates $n+1$ data points. 

- [[Neville's Method]]
	- [[Lagrange Polynomials]]
- [[Newton's Divided Difference]]
- [[Hermite Interpolation]]
- [[Cubic Spline Interpolation]]
- [[Parametric Curves]]