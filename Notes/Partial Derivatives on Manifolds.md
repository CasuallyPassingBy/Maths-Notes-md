---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Functions on Smooth Manifolds]], [[Smooth Manifolds]], [[Differentiability of Vector valued functions of Rn]], [[Inverse Function Theorem in Rn]]

**Def:** On a manifold $M$ of dimension $n$, let $(U, \phi)$ be a chart and $f$ a $\mathcal C^\infty$ function as a function into $\Bbb R^n$, and $\phi$ has $n$ components $x^1, \dots, x^n$. The means that if $r^1, \dots, r^n$ are the standard coordinates on $\Bbb R^n$, then $x^i = r^i \circ \phi$. For $p\in U$, we define the *partial derivative* $\dfrac{\partial f}{\partial x^i}$ of $f$ with respect to $x^i$ at $p$ to be: $$\left.\frac{\partial}{\partial x^i}\right\rvert_p f:= \frac{\partial f}{\partial x^i} (p) := \frac{\partial(f\circ \phi^{-1})}{\partial r^i}(\phi(p)) := \left.\frac{\partial}{\partial r^i}\right\rvert_{\phi(p)}(f \circ \phi^{-1}) $$Since $p = \phi^{-1})\phi(p)$, this equation may be written in the form $$ \frac{\partial f}{\partial x^i} (\phi^{-1}(\phi(p)) = \frac{\partial (f \circ \phi^{-1})}{\partial r^i})(\phi(p))$$Thus, as functions $\phi[U]$, $$\frac{\partial f}{\partial x^i} \circ \phi^{-1} = \frac{\partial (f\circ \phi^{-1})}{\partial r^i}$$The partial derivative $\dfrac{\partial f}{\partial x^i}$ is $\mathcal C^\infty$ on $U$ because the composition $\left(\dfrac{\partial f}{\partial x^i}\right) \circ \phi^{-1}$ is $\mathcal C^\infty$ on $\phi[U]$. 

**Prop:** Suppose $(U, x^1, \dots, x^n)$ is chart on a manifold. Then $\dfrac{\partial x^i}{\partial x^j} = \delta^i_j$. 

**Def:** Let $F: N \to M$ be a smooth map, and let $(U, \phi) = (U, x^1, \dots, x^n)$ and $(V, \psi) = (V, y^1, \dots, y^m)$ be charts on $N$ and $M$ respectively such that $F[U] \subseteq V$. Denote by $$F^i := y^i \circ F = r^i \circ \psi \circ F: U \to \Bbb R$$the $i$th component of $F$ in the chart $(V, \psi)$. The the matrix $\left[\dfrac{\partial F^i}{\partial x^j}\right]$ is called the *Jacobian matrix* of $F$ relative to the charts $(U, \phi)$ and $(V, \psi)$. In the case $N$ and $M$ have the same dimension, the determinant $\det \left[\dfrac{\partial F^i}{\partial x^j}\right]$ is called the *Jacobian determinant* of $F$ to the two charts. The Jacobian determinant is also written as $\dfrac{\partial (F^1, \dots, F^n)}{\partial(x^1, \dots, x^n)}$. This is a clear generalisation from the Jacobian matrix from calculus.

**Example:** Let $(U, \phi) = (U, x^1, \dots, x^n)$ and $(V, \psi) = (V, y^1, \dots, y^n)$ be overlapping charts on a manifold $M$. The transition map $\psi \circ \phi^{-1}: \phi[U\cap V] \to \psi[U \cap V]$ is a diffeomorphism of open subsets of $\Bbb R^n$, and that $J(\psi \circ \phi^{-1})$ at $\phi(p)$ is the matrix $\left[\dfrac{\partial y^i}{\partial x^j}\right]$ of partial derivatives at $p$.

# Inverse Function Theorem

**Def:** We say that a $\mathcal C^\infty$ map $F:N \to M$ is *locally invertible* or a *local diffeomorphism* at $p\in N$ If $p$ has a neighbourhood $U$ on which $F|_U: U \to F[U]$ is a diffeomorphism. 

**Inverse function Remainder:** Let $F:W \to \Bbb R^n$ be a $\mathcal C^\infty$ map defined on an open subset $W$ of $\Bbb R^n$. For any point $p \in W$, the map $F$ is locally invertible at $p$ iff the Jacobian determinant $\det \left[\dfrac{\partial F^i}{\partial r^j}(p)\right]$ is nonzero.
#### Inverse Function Theorem for Manifolds
Let $F: N\to M$ be a $\mathcal C^\infty$ map between two manifolds of the same direction, and $p\in N$. Suppose for some charts $(U, \phi) = (U, x^1, \dots, x^n)$ about $p$ in $N$ and $(V, \psi) = (V, y^1, \dots, y^n)$ about $F(p)$ in $M$, $F[U] \subseteq V$. Set $F^i = y^i \circ F$. Then $F$ is locally invertible at $p$ iff the Jacobian determinant $\det \left[\dfrac{\partial F^i}{\partial x^j}(p)\right]$ is nonzero. 

Using the notion of [[Tangent Space for Manifolds#Local Expression for the Differential|differentials on manifolds]], we can rephrase this theorem as: A $\mathcal C^\infty$ map $F:N \to M$ between two manifolds on the same dimension is locally invertible at a point $p\in N$ iff its differential $dF_{p}: T_p N \to T_{F(p)} M$ at $p$ is an isomorphism. 

**Cor:** Let $N$ be a manifold of dimension $n$. A set of $n$ smooth functions $F^1, \dots, F^n$ defined on the coordinate neighbourhood $(U, x^1, \dots, x^n)$ of a point $p\in N$ forms a coordinate system about $p$ iff the iff Jacobian determinant $\det \left[\dfrac{\partial F^i}{\partial x^j}(p)\right]$ is nonzero. 