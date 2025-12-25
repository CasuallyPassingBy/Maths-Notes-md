---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Tensor Bundles]], [[Correlations, Musical Isomorphisms]], [[Smooth Submanifolds]]

**Def:** A *Riemannian metric* on a smooth manifold $M$ is a $2$-tensor field $g\in \mathcal T^2(M)$ that is *symmetric*, and *positive definite*. A Riemannian metric thus determines an inner product on each tangent space $T_pM$, which is typically written $\langle X, Y \rangle_g := g(X, Y)$ for $X, Y \in T_p M$. A manifold together with a given Riemannian metric is called a *Riemannian manifold*. We often use the word 'metric' to refer to a Riemannian metric when there is no chance for confusion. 

**Prop:** Every smooth manifold can be given a Riemannian metric. 

If $p$ is a point in a Riemannian manifold $(M, g)$, we define the *length* of *norm* of any tangent vector $X \in T_p M$ to be $\|X \|_g := \langle X, X\rangle^{1/2}$. We define the *angle* between two nonzero vectors $X, Y\in T_p M$ to be the unique $\theta \in [0, \pi]$ satisfying $$\cos \theta = \frac{\langle X, Y \rangle_g}{\|X\|_g \|Y\|_g}.$$We say that $X$ and $Y$ are *orthogonal* if $\theta = \pi/2$ or $\langle X, Y \rangle =  0$. Vectors $E_1, \dots, E_k$ are called *orthornmal* if they are of length $1$ and pairwise orthogonal, or equivalently if $\langle E_i, E_j\rangle = \delta_{ij}$. 

If $\gamma:[a,b] \to M$ is a piecewise smooth curve segment, the *length of $\gamma$* is $$L_g(\gamma) = \int_a^b \|\gamma'(t)\|_g\, dt.$$Because $\|\gamma(t)\|_g$ is continuous at all but finitely any value of $t$, and has a well-defined left and right-handed limits, at those points the integral is well-defined. 

**Prop:** If $\gamma:[a,b] \to M$ is a piecewise smooth curve segment and $a<c<b$, then $$L_g(\gamma) = L_g(\gamma|_{[a,c]}) + L_g(\gamma|_{[c,b]}).$$
**Parameter Independence of Length:** Let $(M,g)$ be a Riemannian manifold, and let $\gamma:[a,b]\to M$ be a piecewise smooth curve segment. If $\widetilde\gamma$ is a reparametrisation of $\gamma$, then $L_g(\widetilde \gamma) = L_g(\gamma)$. 

**Def:** If $(M, g)$ and $(N, h)$ are Riemannian manifolds, a diffeomorphism $\varphi: M \to N$ is called an *isometry* if $\varphi^* h = g$. We are taking the pullback of the covariant tensor $h$ by $\varphi$. We can see that being isometric is an equivalence relation on the class of Riemannian manifolds. More generally, $F$ is called a *local isometry* if every point $p\in M$ has a neighbourhood $U$ such that $F|_U$ is an isometry of $U$ onto an open subset of $N$. A metric $g$ on $M$ is said to be *flat* if every point $p\in M$ has a neighbourhood $U\subseteq M$ such that $(U, g|_U)$ is isometric to an open subset of $\Bbb R^n$ with the Euclidean metric. 

**Prop:** Let $(M, g)$ be a Riemmanian manifold. The following statements are equivalent:
- Each point of $M$ has a smooth coordinate neighbourhood in which the coordinate frame is orthonormal.
- $g$ is flat. 

**Def:** An isometry $\varphi: (M, g) \to (M, g)$ is called an *isometry* of $M$. the set of isometries of $M$ is a group, called the *isometry group* of $M$; it is denoted $\mathcal I(M)$. 

**Prop:** Let $(M, g)$ and $(\widetilde M, \widetilde g)$ be Riemannian manifolds. If $F: M \to \widetilde M$ is an isometry and $\gamma:[a,b] \to M$ is a piecewise smooth curve segment, then $L_{\widetilde g}(F \circ\gamma) = L_g(\gamma)$. 

If $(E_1 \dots, E_n)$ is any smooth local frame for $TM$, and $(\phi^1 \dots, \phi^n)$ is its dual coframe a Riemannian metric can be written locally as $$g = g_{ij} \phi^i \otimes \phi^j.$$The coefficient matrix, defined by $g_{ij} = \langle E_i, E_j \rangle$, is symmetric in $i$ and $j$ and depends smoothly on $p\in M$. In a coordinate frame, $g$ has the form $$g = g_{ij} dx^i \otimes dx^j.$$
We are going to introduce the *symmetric product* of two $1$-forms $\omega$ and $\eta$, denoted by the juxtaposition with no product symbol: $$\omega \eta := \frac12 (\omega\otimes \eta + \eta \otimes \omega).$$ Using this and the symmetry of $g_{ij}$, $$g= g_{ij}dx^idx^j.$$
**Prop:** Let $p\in M$, $(M, g)$ a Riemannian $n$-manifold. There is always a local orthonormal frame near $p$, that is, a local frame $E_1, \dots, E_n$ defined on a neighbourhood of $p$ that forms an orthonormal basis for the tangent space at each point.

## The Riemannian Distance Function

If $(M, g)$ is a connected Riemannian manifold and $p,q \in M$, the *Riemannian disctance* between $p$ and $q$, denoted by $d_g(p,q)$, is defined to be the infimum of $L_g(\gamma)$ over all piecewise smooth curve segments $\gamma$ from $p$ to $q$. Because any pair of points in a connected smooth manifold can be joined by a piecewise smooth curve segment, this is well defined. 

**Prop:** If $(M, g)$ and $(\widetilde M, \widetilde g)$ are connected Riemannian manifolds and $F:M \to \widetilde M$ is an isometry, then $d_{\widetilde g}(F(p), F(q)) = d_g(p,q)$ for all $p, q\in M$. 

**Prop:** Let $(M, g)$ is a compact Riemannian manifold and $p,q\in M$, If there is a piecewise smooth curve segment connecting $p$ and $q$, then there exists a piecewise smooth curve segment $\gamma$ joining $p$ and $q$ that satisfy$$L_g(\gamma) = d_g(p, q).$$In other words, the infimum in the definition of the Riemannian distance is attained. 

This is as result from analysis, see [[Rectifiable Curves]]. 

We will see that Riemannian distance function turn $M$ into a metric space whose topology is the same as the given manifold. We will need a technical lemma, which shows that any Riemannian metric is locally comparable to the Euclidean metric in coordinates. 

**Lemma:** Let $g$ be any Riemannian metric on an open set $U\subseteq \Bbb R^n$. For any compact $K\subseteq U,$ then there exists positive constants $c, C$ such that for all $x\in K$ and all $v\in T_x\Bbb R^n$, $$c\|v\|_{\overline g}\le  \|v\|_g \le C\|v\|_{\overline g}, $$where $\overline g$ is the Euclidean metric. 

**Riemannian Manifolds as Metric Spaces:** Let $(M, g)$ be a connected Riemannian manifold. With the Riemannian distance function, $M$ is a metric space whose metric topology is the same as the original manifold topology. 

**Existence of Riemannian Metrics:** Every smooth manifold admits a Riemannian metric. 

There are two proofs of this fact, one that relies on [[Smooth Partitions of Unity for Manifolds]], and the other on the [[The Whitney Embedding Theorem]], which the latter is far less elementary, but still fun. 

# Submanifolds

**Def:** Suppose that $(N, h)$ is a Riemannian manifold, and $\iota: M \to N$ is an immersed submanifold of $N$. The *induced metric* on $M$ is the $2$-tensor $g = \iota^* h$, which is just the restriction of $h$ to vectors tangent to $M$. 

The metric on $\Bbb R^n$ has the following form $$g= \sum_{i = 1}^n (dx^i)^2,$$meaning that $g_{ij} = \delta_{ij}$. 
 
Computations on a submanifold are usually most conveniently carried out in terms a *local parametrization*: this is an embedding of an open subset $U \subseteq \Bbb R^n$ into $N$, whose image is an open subset of $M$. 

**Prop:** Let $(M, g)$ and $(\widetilde M, \widetilde g)$ be Riemannian manifolds. If $F: M \to \widetilde M$ is a smooth map such that $F^*\widetilde g = g$, then $F$ is an immersion. 

**Example:** If $X: U \to \Bbb R^n$ is a parametrization of a submanifold $M \subseteq \Bbb R^n$ with the induced metric, the induced metric in standard coordinates $(u^1, \dots, u^n)$ on $U$ is just $$g = \sum_{i = 1}^n (dX^i)^2 = \sum_{i = 1}^n \left(\frac{\partial X^i}{\partial u^j} du^j\right)^2.$$
Suppose $(M, g)$ is a Riemannian manifold and $S\subseteq M$ is a Riemannain submanifold. For any $p\in S$, a vector $N\in T_pM$ is said to be *normal to $S$* if $N$ is orthogonal to $T_pS$ with respect to $g$. The set $N_pS := (T_p S)^\bot$ inside $T_pM$, and we call it the normal space to $S$ at $p.$ We are using [[Orthogonal Complements]] to define the normal space.

A local orthonormal frame $(E_1,\dots, E_n)$ for $M$ on an open set $U\subseteq M$ is said to be *adapted to $S$* if the first $k$ vectors $(E_1|_p,\dots, E_k|_p)$ span $T_pS$ at each $p\in U \cap S$. It is immediate that $(E_{k+1}|_p,\dots, E_n|_p)$ span $N_pS$. 

**Existence of Adapated Orthonormal Frames:** Let $S\subseteq M$ be an embedded Riemannian submanifold of a Riemannian manifold $(M, g)$. For each $p\in  S$, there is a smooth adapted orthonormal frame on a neighbourhood $p$ in $M$. 

**Def:** If $S\subseteq M$ is a Riemannian submanifold, we define the *normal bundle* to $S$ as $$NS := \coprod_{p\in S} N_p S. $$
**Obs:** Let us note that for each $p\in M$ we have that $T_p S \oplus N_p S = T_p M$. This is actually giving us something more general that the $N_p S$ must be the missing dimensions of $T_pS$, which tells us emphatically that normal bundle cannot be realised without an ambient space unlike the tangent and cotangent bundle.

**Prop:** If $S\subseteq M$ is an embedded Riemannian submanifold, then $NS$ is a [[Vector Bundles on Smooth Manifolds|smooth vector bundle]] over $S$ whose rank is equal to the codimension of $S$ in $M$. 

**Def:** If $(M_1, g_1)$ and $(M_2, g_2)$ are Riemannian manifolds, then product $M_1 \times M_2$ has a natural Riemannian metric $g = g_1 \oplus g_2$, called the *product metric*, defined by $$g(X_1 + X_2, Y_1 + Y_2) := g_1(X_1, Y_1) + g_2(X_2, Y_2),$$where $X_i, Y_i \in T_{p_i} M_i$, under the natural identification $T_{(p_1, p_2)}(M_1 \times M_2) = T_{p_1} M_1 \times T_{p_2} M_2$. 

**Obs:** Any local coordinates $(x^1, \dots, x^n)$ for $M_1$ and $(x^{n+1}, \dots, x^{n+m})$ for $M_2$ give coordinates $(x^1, \dots x^{n+m})$ for $M_1 \times M_2$. In terms of these coordinates the product metric has the local expression $g = g_{ij}dx^idx^j$, where $g_{ij}$ is a block diagonal matrix $$(g_{ij}) = \begin{pmatrix}
(g_1)_{ij} & 0 \\ 
0 & (g_2)_{ij} 
\end{pmatrix}$$
**Def:** Suppose $\pi: N \to M$ is a smooth covering map. A *covering transformation*, or *[[Automorphism Group of a Covering|deck transformation]]* is a smooth map $\varphi: N \to N$ such that $\pi \circ \varphi = \pi$. If $g$ is Riemannian metric on $M$, then $h := \pi^* g$ is a Riemannian metric on $N$ that is invariant under all covering transformations. In this case $h$ is called a *covering metric*, and $\pi$ is called *Riemannian covering*. 

# The Tangent-Cotangent Isomorphism

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