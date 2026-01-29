---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Integration of Differential Forms on Smooth Manifolds]], [[Stokes's Theorem and Smooth Manifolds with Corners]], [[Riemannian Volume Form on Smooth Manifolds]], [[Orientations of Smooth Manifolds]], [[Divergence Theorem in R2]], [[Gauss's Theorem and Divergence in R3]], [[Stokes's Theorem and Curl in R3]], [[The Tangent-Cotangent Bundle Isomorphism for Riemannian Manifolds]], [[The Exterior Derivative on Smooth Manifolds]]

## Integration of Functions on Riemannian Manifolds

**Def:** Suppose $(M, g)$ is an oriented Riemannian manifold with or without boundary and let $\omega_g$ denote its Riemannian volume form. If $f$ is a compactly supported continuous real-valued function on $M$, then $f\omega_g$ is compactly supported $n$-form, so we can define the *integral of $f$ over $M$* to be $\int_M f\omega_g$. If $M$ is itself compact, we define the *volume of $M$* by $$\text{Vol}(M) := \int_M \omega_g.$$
Because of these definitions, the Riemannian volume form is often denoted by $dV_g$, or $dA_g$ or $ds_g$ in the $2$-dimensional or $1$-dimensional case, respectively. Then the integral of $f$ over $M$ is written $$\int_M f\; dV_g := \int_M f\omega_g ,$$and the volume of $M$ as $$\int_M dV_g.$$We just interpret $dV_g$ to be notational convenience, not to mean that it is the exterior derivative of a $(n-1)$-form.

**Prop:** Let $(M, g)$ be a nonempty oriented Riemannian manifold with or without boundary, and suppose $f$ is a compactly supported continuous real-valued function on $M$ satisfying $f\ge 0$. Then $$\int_M f\; dV_g \ge0,$$with equality iff $f = 0$. 

**Cor:** Let $(M, g)$ be a nonempty oriented Riemannian manifold with or without boundary, and suppose $f$ is a compactly supported continuous real-valued function on $M$. Then $$\left|\int_M f\; dV_g \right| \le \int_M |f| \; dV_g. $$
## The Divergence Theorem

**Def:** Let $(M, g)$ be an oriented Riemannian $n$-manifold with or without boundary. Multiplication by the Riemannian volume form defines a smooth bundle isomorphism $*:\mathcal C^\infty(M) \to \Omega^n(M)$: $$*f := f\; dV_g.$$In addition, we define a smooth bundle isomorphism $\beta: {\frak X}(M) \to \Omega^{n-1}(M)$ as follows$$\beta (X) := X\; \lrcorner \; dV_g. $$
**Lemma:** Let $(M, g)$ be an oriented Riemannian manifold with or without boundary. Suppose $S\subseteq M$ is an immersed hypersurface with the orientation determined by a unit normal vector field $N$, and $\widetilde g$ is the induced metric on $S$. If $X$ is any vector field along $S$, then $$\iota_S^*(\beta(X)) = \langle X, N\rangle_g \; dV_{\tilde g}. $$
**Def:** The *divergence operator* $\text{div}: {\frak X}(M) \to \mathcal C^\infty (M)$ by $$\text{div }X := *^{-1}d(\beta(X)),  $$or equivalently, $$d(X\; \lrcorner\; dV_g) = (\text{div }X)\;dV_g.$$
**Prop:** Let $(M,g )$ be a Riemannian manifold with or without boundary. In any smooth local coordinates $(x^i)$, then $$\text{div}\left(X^i\frac{\partial}{\partial x^i}\right) = \frac1{\sqrt{\det g}} \frac{\partial}{\partial x^i} \left(X^i \sqrt{\det g}\right),$$where $\det g= \det(g_{kl})$ is the determinant of the component matrix of $g$ in these coordinates.

**Prop:** We can write the the divergence using the Hodge star operator to be $$\begin{align*}
X \; \lrcorner \; dV_g &= \star X^\flat, \\
\text{div }X &=\star d \star X^\flat. 
\end{align*}
$$
**Prop:** Let $(M,g )$ be a Riemannian manifold with or without boundary. The divergence operator satisfies the following product rule for $f\in \mathcal C^\infty(M)$, $X\in {\frak X}(M)$:$$\text{div}(fX) = f \text{ div }X+\langle \text{grad }f, X\rangle_g. $$
**The Divergence Theorem:** Let $(M, g)$ be an oriented Riemannian manifold with boundary, for any compactly supported smooth vector field $X$ on $M$, $$\int_M (\text{div }X)\; dV_g = \int_{\partial M} \langle X, N\rangle_g \; dV_{\widetilde g},$$where $N$ is the outward-pointing unit normal vector field along $\partial M$ and $\widetilde g$ is the induced Riemannian metric on $\partial M$. 

**The Integration by Parts:** Let $(M, g)$ be a compact oriented Riemannian manifold with boundary, for any $f\in \mathcal C^\infty(M)$, $X\in {\frak X}(M)$  $$\int_M \langle \text{grad }f, X\rangle_g\; dV_g = \int_{\partial M} f\langle X, N \rangle \;dV_{\widetilde g} -\int_M (f \text{ div }X)\; dV_g.   $$where $N$ is the outward-pointing unit normal vector field along $\partial M$ and $\widetilde g$ is the induced Riemannian metric on $\partial M$. 

**Def:** A [[Integral Curves, Flows and Flowouts on Smooth Manifolds|smooth flow]] $\theta$ on $M$ is said to be *volume-preserving* if for every compact regular domain $D$, we have $\text{Vol}(\theta_t[D]) = \text{Vol}(D)$ whenever the domain $\theta_t$ contains $D$. It is called *volume-increasing, volume-decreasing, volume-nonincreasing* or *volume-nondecreasing* if for every such $D$, $\text{Vol}(\theta_t[D])$ is strictly increasing, strictly decreasing, nonincreasing, nondecreasing, respectively, as a function of $t$. 

Note that the properties of flow domains ensure that if $D$ is contained in the domain of $\theta_t$  for some $t$, then the same is true for all times between $0$ and $t$.

**Geometric Interpretation of the Divergence:** Let $M$ be an oriented Riemannian manifold, let $X\in {\frak X}(M)$, and let $\theta$ be the flow of $X$. Then $\theta$ is
- volume preserving iff $\text{div }X = 0$ everywhere on $M$.
- volume-nondecreasing iff $\text{div X}\ge 0$ everywhere on $M$.
- volume-nonincreasing iff $\text{div X}\le 0$ everywhere on $M$.
- volume-increasing iff $\text{div }X > 0$ on a dense subset of $M$.
- volume-decreasing iff $\text{div }X < 0$ on a dense subset of $M$.

The proof needs [[Differentiation under the integral sign]], which needs to be slightly adapted. 

**Def:** We can define an inner product on $k$-forms for compact oriented Riemannian manifolds. For any $\omega, \eta\in \Omega^k(M)$ the inner product is defined as $$\langle\!\langle \omega,\eta \rangle\!\rangle_g := \int_M \langle \omega,\eta\rangle_g\; dV_g.$$

**Prop:** Let $\omega\in \Omega^k(M)$ and $\eta\in \Omega^{k+1}$, then $$\langle\!\langle d\omega,\eta \rangle\!\rangle  = \langle\!\langle \omega,  d^*\eta\rangle\!\rangle.$$Meaning that the codifferential is the adjoint of the differential with respect to this inner product. 

### Surface Integral

**Def:** Let $(M, g)$ be an oriented Riemannian $3$-manifold. Define the *curl operator* denoted by $\text{curl}: \mathfrak X(M)\to \mathfrak X(M)$, by $$\text{curl }X := \beta^{-1} d(X^\flat),$$where $\beta: \mathfrak X(M)\to \Omega^2(M)$ is the already defined smooth bundle isomorphism. Unwinding the definitions, we see that this is equivalent to  $$(\text{curl }X)\; \lrcorner \; dV_g = d(X^\flat).$$
**Prop:** We can write the the curl using the Hodge star operator to be $$\text{curl }X = (\star dX^\flat)^\sharp.$$
The operators $\text{div}$, $\text{grad}$ and $\text{curl}$ on an oriented Riemannian $3$-manifold $M$ are related by the following commutative diagram: 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]

\mathcal C^\infty(M) \arrow[r, "\text{grad}"] \arrow[d, "\text{Id}"] & 
{\frak X}(M) \arrow[r, "\text{curl}"] \arrow[d, "\flat"] & 
{\frak X}(M) \arrow[r, "\text{div}"]\arrow[d, "\beta"]  & 
\mathcal C^\infty(M)\arrow[d, "*"]  \\

\Omega^0(M) \arrow[r, "d"']& \Omega^1(M)\arrow[r, "d"'] & \Omega^2(M) \arrow[r, "d"']& \Omega^3(M) 


\end{tikzcd}
\end{document}
```

The identities $\text{curl} \circ \text{grad} = 0$ and $\text{div}\circ\text{curl} = 0$ follow from $d \circ d = 0$, just as they do for the Euclidean case. The curl operator is defined only in dimension $3$ because it is only in the case that ${\textstyle \bigwedge}^{\!2}(T^*M)$ is isomorphic to $TM$, via the map $X \mapsto X\; \lrcorner\; dV_g$. 

Note that the if the orientation of $M$ changes, then also $\text{curl }X$ changes, by gaining a minus sign.

**Def:** Now suppose $S\subseteq M$ is a compact $2$-dimensional submanifold with or without boundary, and $N$ is a smooth unit normal vector along $S$. Let $dA$ be denote the Riemannian volume form on $S$ with respect to the induced metric $\iota_S^*g$ and the orientation determined by $N$, so that $dA := \iota_S^*(N\; \lrcorner \; dV_g)$. For any smooth vector field $X$ define on $M$, the *surface integral of $X$ over $S$* is defined as $$\int_S \langle X, N\rangle_g\; dA. $$
**Stokes's Theorem for Surface Integrals:** Suppose $M$ is an oriented Riemannian $3$-manifold with or without boundary, and $S$ is a compact oriented $2$-dimensional smooth manifold with boundary in $M$. For any smooth vector field $X$ on $M$, $$\int_S \langle \text{curl }X, N\rangle_g\, dA = \int_{\partial S} \langle X, T\rangle_g \, ds,  $$where $N$ is the smooth unit normal vector field along $S$ that determines its orientation, $ds$ is the Riemannian volume form for $\partial S$, with respect to the metric and orientation induced from $S$, and $T$ is the unique positively oriented unit tangent vector field on $\partial S$. 

