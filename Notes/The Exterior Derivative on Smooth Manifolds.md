---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Differential Forms on Smooth Manifolds]], [[Derivations]], [[Stokes's Theorem and Curl in R3]], [[Green's Theorem and Curl in R2]], [[Divergence Theorem in R2]], [[Gauss's Theorem and Divergence in R3]]

We first define the exterior derivative for Euclidean space.

**Def:** The definition of $d$ Euclidean space is straightforward: if $\omega = \omega_J \; dx^J$ is a smooth $k$-form on an open subset $U\subseteq \Bbb R^n$ or $\Bbb H^n$, we define its *exterior derivative* $d\omega$ to be the following $(k+1)$-form $$d(\omega_J \; dx^J) :=  d\omega_j \wedge dx^J,$$where $d\omega_J$ is the differential of the function $\omega_J$. In somewhat more detail this becomes $$d(\omega_J \; dx^J) =\left(\frac{\partial \omega_J}{dx^i} dx^i\right) \wedge dx^J.$$
**Properties of the Exterior Derivative on $\Bbb R^n$:**
- $d$ is linear over $\Bbb R^n$.
- If $\omega$ is a smooth $k$-form and $\eta$ is smooth $l$-form on an open subset $U\subseteq \Bbb R^n$ or $\Bbb H^n$, then $$d(\omega\wedge\eta) = d\omega \wedge\eta + (-1)^k\omega\wedge d\eta. $$
- $d \circ d = 0$.
- $d$ commutes with pullbacks: If $U$ is an open subset of $\Bbb R^n$or $\Bbb H^n$, $V$ is an open subset of $\Bbb R^m$ or $\Bbb H^m$, $F: U \to V$ is a smooth map, and $\omega\in \Omega^k(V)$, then $$F^*(d\omega) = d(F^*\omega). $$
**Existence and Uniquenes of Exterior Differentiation:** Suppose $M$ is a smooth manifold with or without boundary. There are unique operators $d: \Omega^k(M) \to \Omega^{k+1}(M)$ for all $k$, called *exterior differentiation,* satisfying the following properties:
- $d$ is linear over $\Bbb R$.
- If $\omega\in \Omega^k(M)$ and $\eta\in \Omega^l(M)$, then  $$d(\omega\wedge\eta) = d\omega \wedge\eta + (-1)^k\omega\wedge d\eta.  $$
- $d\circ d = 0$.
- For $f\in \Omega^0(M) = \mathcal C^\infty(M)$, $df$ is the differential, given by $df(X) = Xf$.
In any smooth chart, $d$ is given by  $$d(\omega_J \; dx^J) :=  d\omega_j \wedge dx^J. $$
**Obs:** The differential on functions extend uniquely to an antiderivation of $\Omega^*(M)$ of degree $+1$ whose square is $0$. 

**Naturality of the Exterior Derivative:** If $F: M \to N$ is a smooth map, then for each $k$ the pullback map $F^*: \Omega^k(N) \to \Omega^k(M)$ commutes with $d$: for all $\omega\in \Omega^k(N)$, $$F^*(d\omega) = d(F^*\omega). $$
**Def:** We say that a smooth differential form $\omega\in \Omega^k(M)$ is *closed* if $d\omega = 0$, and *exact* if there exists a $(k-1)$-form $\eta$ on $M$ such that $\omega = d\eta$. 

We see that every exact form is closed, but the converse might not not be true. 

# Relationship with Vector Calculus in $\Bbb R^3$

**Example:** Let us work out the exterior derivatives of arbitrary $1$-forms and $2$-forms in $\Bbb R^3$. Any smooth $1$-form can be written as$$\omega = P\;dx + Q\; dy+ R\; dz$$for some smooth functions $P, Q, R$. We can compute the its exterior derivative to get that $$
\begin{align*}
d\omega &= dP \wedge dx + dQ \wedge dy + dR\wedge dz \\
&= \left(\frac{\partial Q}{\partial x}- \frac{\partial P}{\partial y}\right) dx \wedge dy + \left(\frac{\partial R}{\partial x}- \frac{\partial P}{\partial z}\right) dx \wedge dz + \left(\frac{\partial R}{\partial z}- \frac{\partial Q}{\partial y}\right) dy \wedge dz.
\end{align*}
$$
An arbitrary $2$-form on $\Bbb R^3$ can be written as $$\eta  = u\; dx \wedge dy + v\; dx \wedge dz + w\; dy\wedge dz.$$A similar calculation whose that $$d\eta = \left(\frac{\partial u}{\partial x}- \frac{\partial v}{\partial y}-\frac{\partial w}{\partial x}\right)\; dx\wedge dy \wedge dz. $$
We see a remarkable similarity between the the componentes of the $2$-form $d\omega$ with the componentes of the curl of a vector field with components $(P, Q, R)$. Similarly, but for signs and ordering of terms, there is a strong analogy between the formula of $d\eta$ and the divergence of a vector fields. Obviously, since $\Bbb R^3$ is a Riemannian manifold, there's also the obvious analogy between $\text{grad }f$ and $df$, also in great part to the metric.

The Euclidean metric on $\Bbb R^3$ yields an index-lowering isomorphism $\flat: {\frak X}(\Bbb R^3) \to \Omega^1(\Bbb R^3)$. Interior multiplication yields another map $\beta: {\frak X}(\Bbb R^3) \to \Omega^2(\Bbb R^3)$ as follows: $$\beta (X) := X \; \lrcorner\; (dx\wedge dy\wedge dz). $$It is easy to check that $\beta$ is linear over $\mathcal C^\infty(\Bbb R^3)$, so it corresponds to a smooth bundle homomorphism from $TM$ to ${\textstyle \bigwedge}^2(T^*\Bbb R^3)$. It is a bundle isomorphism because it is injective and both $TM$ and ${\textstyle \bigwedge}^2(T^*\Bbb R^3)$ are bundles of rank $3$. Similarly, we can define a bundle isomorphism $* : \mathcal C^\infty(\Bbb R^3) \to \Omega^3(\Bbb R^3)$ by $$*(f) := f\; dx\wedge dy\wedge dz. $$
The relationships among all these operators are summarised in the following diagram:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]

\mathcal C^\infty(\mathbb R^3) \arrow[r, "\text{grad}"] \arrow[d, "\text{Id}"] & 
{\frak X}(\mathbb R^3) \arrow[r, "\text{curl}"] \arrow[d, "\flat"] & 
{\frak X}(\mathbb R^3) \arrow[r, "\text{div}"]\arrow[d, "\beta"]  & 
\mathcal C^\infty(\mathbb R^3)\arrow[d, "*"]  \\

\Omega^0(\mathbb R^3) \arrow[r, "d"']& \Omega^1(\mathbb R^3)\arrow[r, "d"'] & \Omega^2(\mathbb R^3) \arrow[r, "d"']& \Omega^3(\mathbb R^3) 


\end{tikzcd}
\end{document}
```

**Obs:** We see that the diagram commutes. This actually gives us some nice proofs for $\text{grad }\circ \text{curl } = 0$ and $\text{curl }\circ \text{div } = 0$ on $\Bbb R^3$. 

The need to generalise this operations of vector calculus from $\Bbb R^3$ to higher dimensions was one to the main motivations for developing differential forms. The curl makes sense as an operator on vector fields only in dimension $3$, whereas the exterior derivative expresses the same information but makes sense in all dimensions. 

## Invariant Formula for the Exterior Derivative

**Exterior Derivative of a $1$-Form:** For any smooth $1$-form $\omega$ and smooth vector fields $X$ and $Y$, $$d\omega(X, Y) = X(\omega(Y))- Y(\omega(X)) - \omega([X, Y]). $$
**Prop:** Let $M$ be a smooth $n$-manifold with or without boundary, let $(E_i)$ be a smooth local frame for $M$, and let $(\varepsilon^i)$ be the dual coframe. For each $i$, let $b^i_{jk}$ denote the component functions of the exterior derivative of $\varepsilon^i$ in this frame, and for each $j,k$, let $c^i_{jk}$ be the component functions of the Lie bracket $[E_j, E_k]$: $$d\varepsilon^i = \sum_{j < k} b^i_{jk} \varepsilon^i\wedge \varepsilon^k; \qquad [E_j, E_k] = c ^i_{jk} E_i.$$Then $b^i_{jk} = - c^i_{jk}$.

**Invariant Formula for the Exterior Derivative:** Let $M$ be a smooth manifold with or without boundary, and $\omega\in \Omega^k(M)$. For any smooth vector fields $X_1,\dots, X_{k+1}$ on $M$, $$\begin{align*} d\omega(X_1,\dots, X{k+1}) &= \\
& \sum_{i = 1}^{k+1} (-1)^{i-1}X_i(\omega(X_1,\dots, \widehat{X_i}, \dots, X_{k+1})) \\ & + \sum_{1 \le i <j \le k+1} (-1)^{i+j}\omega([X_i, X_j], X_1,\dots, \widehat{X_i},\dots, \widehat{X_j},\dots, X_{k+1}),
\end{align*} $$where the hats indicate omitted arguments.

**Prop:** Suppose $M$ is a smooth manifold, $V\in {\frak X}(M)$, and $\omega, \eta\in \Omega^*(M)$. Then $$\mathcal L_V(\omega\wedge \eta) = (\mathcal L_V \omega) \wedge \eta + \omega\wedge (\mathcal L_V \eta). $$
**Cartan's Magic Formula:** On a smooth manifold, for any vector field $V$ and any smooth differential form $\omega$,  $$\mathcal L_V \omega = V \;\lrcorner\; (d\omega) + d(V\; \lrcorner\; \omega). $$**The Lie Derivative Commutes with $d$:** If $V$ is a smooth vector field and $\omega$ is a differential form, then $$\mathcal L_V(d\omega) = d(\mathcal L_V\omega) = d(V \; \lrcorner \; d\omega). $$

**Prop:** For each nonnegative integer $k$, there is a contravariant functor $\Omega^k: \sf Diff \to Vec_\Bbb R$, which to each smooth manifold $M$ assigns the vector space $\Omega^k(M)$ and to each smooth $F$ the pullback $F^*$. We see that the exterior derivative is a natural transformation from $\Omega^k$ to $\Omega^{k+1}$.

**Prop:** Let $M$, $N$ be smooth manifolds, and suppose $\pi:M \to N$ is a surjective smooth submersion with connected fibres. Suppose $\omega\in \Omega^k(M)$. There exists $\eta\in \Omega^k(N)$ such that $\omega = \pi^*\eta$ iff $v\; \lrcorner\;\omega_p = 0$ and $v \; \lrcorner\; d\omega_p = 0$ for every $p\in M$ and every [[Vector Fields on Smooth Manifolds#^3c9489|vertical vector]] $T_p M$. 

# Codifferential

Let $(M ,g)$ be an oriented Riemannian manifold. 

**Def:** For $1\le k \le n$, define a map $d^*: \Omega^k(M) \to \Omega^{k-1}(M)$ by $$d^*\omega:= (-1)^{n(k+1)+1}\star d \star \omega,  $$where $\star$ si the Hodge star operator. We extend this definition to $0$-forms by defining $d^*\omega = 0$ for $\omega\in \Omega^0(M)$.

**Def:** Just as we have exact forms, we call differential forms such that $d^*\omega = 0$ *co-closed.* Similarly, if $\omega$ is and $k$-form, and there is an $k+1$-form $\eta$, such that $d^*\eta = \omega$, then $\omega$ is called *co-exact.*

**Properties of the codifferential:** 
- $d^* \circ d^* = 0$. 