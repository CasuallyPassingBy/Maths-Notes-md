---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Homotopy Cauchy's Theorem]], [[Homology Cauchy's Theorem]], [[Analytic Functions]]

**Def:** Let $\gamma$ be a closed curve in $\Bbb C$ and $z_0 \in \Bbb C$ be a point not on $\gamma$. Then, the _**index**_ of $\gamma$ with respect to $z_0$ (also called the _**winding number**_ of $\gamma$ with respect to $z_0$) is defined to be

$$ n(\gamma; z_0) = \frac{1}{2\pi i} \oint_\gamma \frac{dz}{z-z_0} $$

we say that $\gamma$ ************_winds around $z_0$, $n(\gamma, z_0)$_ times.

**Prop:**
- The circle $\gamma(t) = z_0 +re^{it}$, with $r >0$ is the radius and the parameter $0\le t \le 2\pi n$, has an index of $n$ with respect to $z_0$; while the circle $\gamma^-(t) = z_0+e^{-it}$, where $0\le t \le 2\pi n$, has an index of $-n$
- If $z_0$ does not lie on either $\tilde \gamma$ or $\gamma$, and if $\tilde \gamma$ and $\gamma$ are homotopic in $\Bbb C \setminus \{ z_0\}$, then

$$ n(\tilde \gamma; z_0) = n(\gamma; z_0) $$

********Th:******** Let $\gamma: [a,b] \to \Bbb C$ be a piecewise smooth closed curve and $z_0$ a point not on $\gamma$; then $I(\gamma;z_0)$ is an integer.

Let $\gamma:[a,b] \to \Bbb C$ be a piecewise smooth closed curve.

- If $z_0 \in \Bbb C$ and $\delta>0$ such that $\gamma \subseteq B_\delta (z_0)$, then $n(\gamma; w) =0$ for all $w \not \in B_\delta(z_0)$
- If $z, w\in \Bbb C$ belong to the same connected component of $\Bbb C\setminus \gamma$, then $n(\gamma; z) = n(\gamma;w)$
- If $z \in \Bbb C$ belongs to the unbounded connected component of $\Bbb C\setminus \gamma$, then $n(\gamma; z) = 0$
### Cauchy’s Integral Formula (for disks)

Let $z_0 \in \Bbb C$, $r>0$ and $f:B_r(z_0) \to \Bbb C$. If $f$ is analytic on $B_r(z_0)$ and $\gamma\subseteq B_r(z_0)$ a be a piecewise smooth closed curve, then
$$ f(z_0) \cdot n(\gamma; z_0) = \frac{1}{2\pi i}\oint_\gamma \frac{f(z)}{z-z_0}\, dz $$

### Homotopy Cauchy's Integral Formula
Let $f$ be analytic on a region $A$. Let $\gamma$ be closed curve in $A$ that is homotopic to a point, let $z_0 \in A$ be a point not on $\gamma$. Then

$$ f(z_0) \cdot n(\gamma; z_0) = \frac{1}{2\pi i}\oint_\gamma \frac{f(z)}{z-z_0}\, dz $$

If we say that $\gamma$ is a simple closed curve, and $z_0$ is “inside” of $\gamma$. Then $I(\gamma;z_0) =1$, so the formula is

$$ f(z_0) = \frac{1}{2\pi i}\oint_\gamma \frac{f(z)}{z-z_0}\, dz $$

There’s a more powerful version where $f$ is continuous on $\gamma$, and holomorphic on the “inside” of $\gamma$, and the formula is still valid. The inside of the curve is defined using the [[Jordan Curve Theorem]]
### Homology Cauchy Integral Formula
Let $f: \Omega \subseteq \Bbb C\to \Bbb C$ analytic in the region $\Omega$ and $\gamma\subseteq \Omega$ a cycle such that $\gamma \sim0\pmod \Omega$. If $z_0 \in \Omega \setminus \gamma$, then
$$ n(\gamma;z_0) f(z_0) =\frac{1}{2\pi i} \oint_\gamma \frac{f(z)}{z-z_0} $$
Let the function $f$ be holomorphic in the closure of a compact domain $D$ that is bounded by a finite number of continuous curves. Then the function f at any point $z ∈ D$ may be represented as

$$ f(z)= \frac{1}{2\pi i} \int_{\partial D} \frac{f(\zeta)}{\zeta -z} \, d\zeta $$

where $∂D$ is the oriented boundary of $D$.

### Generalized Cauchy’s Integral Formula
Let $f$ be a complex function with continuous [[Wirtinger derivatives]] in a closure of a compact region $D$ bounded by by a finite number of piecewise smooth curves. Then we have
$$ f(z)= \frac{1}{2\pi i} \oint _{\partial D} \frac{f(\zeta)}{\zeta -z} \, d\zeta -\frac{1}{\pi} \int_A \frac{\partial f / \partial \overline \zeta}{\zeta -z}\,dA(\zeta, \overline \zeta) $$

We are using the [[Contour Integrals in C#Green's Theorem Analogue|Green's Theorem analogue but for contour integrals]] 