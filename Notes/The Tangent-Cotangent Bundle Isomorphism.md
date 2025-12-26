---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Riemannian Metrics on Smooth Manifolds]], [[Correlations, Musical Isomorphisms]], [[Dual Vector Spaces]]

An inner product determines a canonical isomorphism between a vector space and its dual, by [[Orthogonal Bases#Riesz Representation Theorem|Riesz' Representation Theorem]]. Given a Riemannian metric $g$ on a manifold $M$, we define $\widetilde g: TM \to T^*M$ as follows. For each $p\in M$ and each $X_p\in T_pM$, we let $$\widetilde g(X_p)(Y_p) := g_p(X_p, Y_p)$$for all $Y_p\in T_pM$. 

Since $\widetilde g(X)(Y)$ is linear over $\mathcal C^\infty(M)$ as a function of $Y$, we know that $\widetilde g(X)$ is a smooth covector field; and because $\widetilde g(X)$ is linear $\mathcal C^\infty(M)$ as a function of $X$, this define $\widetilde g$ as a smooth bundle map. We are going to use the same symbol to refer to the bundle map $\widetilde g:TM \to T^*M$ and the linear map on section $\widetilde g: \mathcal T(M) \to \mathcal T^*(M)$. 

We see that $\widetilde g$ is injective at each point, because $\widetilde g(X_p) = 0$, implies that $\widetilde g(X_p)(X_p) = \langle X_p,X_p\rangle_p$, which implies that $X_p = 0$. Thus we see that $\widetilde g$ is bijective, so it is a bundle isomorphism.

If $X$ and $Y$ are smooth vector fields, in smooth coordinates we can write$$\widetilde g(X)(Y) = g_{ij} X^iY^j, $$which imples that the covector field $\widetilde g(X)$ has the coordinate expression $$\widetilde g(X) = g_{ij}X^idy^j.$$
In other words, $\widetilde g$ is the bundle map whose matrix with respect to the coordinate frames for $TM$ and $T^*M$ is the same as the matrix of $g$ itself. It is costumary to denote the components of the covector field $\widetilde g(X)$ by $$ X_j = g_{ij}X^j,$$so that $$\widetilde g(X) = X_j dy^j.$$
Because of this, we say that $\widetilde g(X)$ is obtained from $X$ by *lowering an index*. The notation $X^\flat$ is frequently used for $\widetilde g(X)$, because $\flat$ typically is used in musical notation to indicate that a tone is lowered. 

The matrix of the inverse $\widetilde g^{-1}: T_p*M \to T_p M$ is thus the inverse of $(g_{ij})$. We let $(g^{ij})$ denote the matrix-valued function whose value at $p\in M$ is the inverse of the matrix $(g_{ij}(p))$, so that$$g^{ij}g_{jk} = g_{jk}g^{ij} = \delta^i_k. $$
Thus for a covector field $\omega\in \mathcal T^*M$, $\widetilde g^{-1}(\omega)$ has the coordinate representation$$\widetilde g^{-1}(\omega) = \omega^i \frac{\partial }{\partial x^i} = g^{ij}\omega_j \frac{\partial }{\partial x^i}.$$We use the notation $\omega^\sharp$ for $\widetilde g^{-1}(\omega)$, and say that $\omega^\sharp$ is obtained from $\omega$ is *raising an index*. 

This is just the vector bundle versions of the [[Correlations, Musical Isomorphisms|musical isomorphisms]].

The most important use of the sharp operation is to reinstate the [[The Gradient|gradient]] as vector field on Riemannian manifolds. For any smooth real-valued function $f$ on a Riemannian manifold $(M, g)$, we define the vector field called the *gradient* of $f$ by $$\text{grad }f := (df)^\sharp= \widetilde g^{-1}(df).$$We see that for any $X\in\mathcal T(M)$ it satisfies $$\langle \text{grad }f, X\rangle _g = df (X) = Xf, $$equivalently, $$\langle \text{grad }f, \cdot \rangle_g = df.$$
In smooth coordinates, $\text{grad }f$ has the expression $$\text{grad }f = g^{ij} \frac{\partial f}{\partial x^i} \frac{\partial}{\partial x^i}.$$
**Prop:** Let $(M,g)$ be a Riemannian manifold, and let $f\in\mathcal C^\infty(M)$. 
- For any $p\in M$, among all unit vectors $X\in T_pM$, the directional derivative $Xf$ is greatest when $X$ points in the same direction as $\text{grad }f|_p$, and the length of $\text{grad }f|_p$ is equal to the value of the directional derivative in that direction.
- If $p$ is a regular point of $f$, then $\text{grad }f|_p$ is normal to the level set of $f$ through $p$. 

**Prop:** Let $(M,g)$ be a Riemannian manifold. If $S\subseteq M$ is a regular level set of a smooth function $\Phi: M \to \Bbb R^k$, then the normal bundle $NS$ is trivial. 

The way we actually build the global frame is fairly simple. since $d\Phi_p: T_p M \to T_{\Phi(p)} \Bbb R^k$ is surjective then we know that the the differential of the component functions $d\Phi_1,\dots, d\Phi_k$ actually behaves as the basis for the annihilator of $T_pS$, and thus $\text{grad }\Phi_1|_p,\dots, \text{grad }\Phi_k|_p$ is a linearly independent that spans $N_pS$. We can turn this into a global frame $p\mapsto (\text{grad }\Phi_1|_p,\dots, \text{grad }\Phi_k|_p)$, which is what we wanted. 

The proof highlights that [[Smooth Submanifolds#^f347ae|Lagrange multipliers for manifolds]] is equivalent to a regular level set of a smooth manifold has a trivial normal bundle. 

**Prop:** For any smooth manifold $TM$ and $T^*M$ are isomorphic as vector bundles. There doesn't exists a rule that assigns every smooth manifold to a bundle isomorphism $\lambda_M: TM \to T^*M$ in such a way that every diffeomorphism $F: M \to N$, the following diagram commute: 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
TM \arrow[d,"\lambda_M"'] \arrow[r, "\tilde F_*"] & TN\arrow[d, "\lambda_N"]\\
T^*M  & T^*N\arrow[l, "F^*"']
\end{tikzcd}
\end{document}
```
This actually telling us that there is no *natural* or *canonical* vector bundle isomorphism between them, and we can use [[Natural Transformations]] to be a little bit more precise in that statement. 

Let $\sf SM$ and $\sf VB$ denote the categories of smooth manifolds and smooth vector bundles, respectively, and let $\mathcal {T, T^*} ; \sf SM \to VB$ be the functors defined by
- $\mathcal T(M) = TM$ and $\mathcal T(f) = f_*$.
- $\mathcal T^*(M) = T^*$ and $\mathcal T^*(f) = f^*$.
Then there is no natural transformation from $\cal T$ to $\cal T^*$. 

This is a a consequence that given the [[Dual Vector Spaces|dual functor]] from $\mathsf {Vect}_K$ to itself there's no natural transformation to $\text{id}_{\mathsf{Vect}_K}$. 