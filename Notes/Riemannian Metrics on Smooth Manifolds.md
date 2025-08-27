---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Tensor Bundles]], [[Correlations, Musical Isomorphisms]], [[Smooth Submanifolds]]

**Def:** A *Riemannian metric* on a smooth manifold $M$ is a $2$-tensor field $g\in \mathcal T^2(M)$ that is *symmetric*, and *positive definite*. A Riemannian metric thus determines an inner product on each tangent space $T_pM$, which is typically written $\langle X, Y \rangle := g(X, Y)$ for $X, Y \in T_p M$. A manifold together with a given Riemannian metric is called a *Riemannian manifold*. We often use the word 'metric' to refer to a Riemannian metric when there is no chance for confusion. 

**Prop:** Every smooth manifold can be given a Riemannian metric. 

If $p$ is a point in a Riemannian manifold $(M, g)$, we define the *length* of *norm* of any tangent vector $X \in T_p M$ to be $\|X \| = \langle X, X\rangle^{1/2}$. We define the *angle* between two nonzero vectors $X, Y\in T_p M$ to be the unique $\theta \in [0, \pi]$ satisfying $$\cos \theta = \frac{\langle X, Y \rangle}{\|X\| \|Y\|}.$$We say that $X$ and $Y$ are *orthogonal* if $\theta = \pi/2$ or $\langle X, Y \rangle =  0$. Vectors $E_1, \dots, E_k$ are called *orthornmal* if they are of length $1$ and pairwise orthogonal, or equivalently if $\langle E_i, E_j\rangle = \delta_{ij}$. 

**Def:** If $(M, g)$ and $(N, h)$ are Riemannian manifolds, a diffeomorphism $\varphi: M \to N$ is called an *isometry* if $\varphi^* h = g$. We are taking the pullback of the covariant tensor $h$ by $\varphi$. We can see thar being isometric is an equivalence relation on the class of Riemannian manifolds. 

**Def:** An isometry $\varphi: (M, g) \to (M, g)$ is called an *isometry* of $M$. the set of isometries of $M$ is a group, called the *isometry group* of $M$; it is denoted $\mathcal I(M)$. 

If $(E_1 \dots, E_n)$ is any smooth local frame for $TM$, and $(\phi^1 \dots, \phi^n)$ is its dual coframe a Riemannian metric can be written locally as $$g = g_{ij} \phi^i \otimes \phi^j.$$The coefficient matrix, defined by $g_{ij} = \langle E_i, E_j \rangle$, is symmetric in $i$ and $j$ and depends smoothly on $p\in M$. In a coordinate frame, $g$ has the form $$g = g_{ij} dx^i \otimes dx^j.$$
We are going to introduce the *symmetric product* of two $1$-forms $\omega$ and $\eta$, denoted by the juxtaposition with no product symbol: $$\omega \eta := \frac12 (\omega\otimes \eta + \eta \otimes \omega).$$ Using this and the symmetry of $g_{ij}$, $$g= g_{ij}dx^idx^j.$$
**Prop:** Let $p\in M$, $(M, g)$ a Riemannian $n$-manifold. There is always a local orthonormal frame near $p$, that is, a local frame $E_1, \dots, E_n$ defined on a neighbourhood of $p$ that forms an orthonormal basis for the tangent space at each point.

**Def:** Suppose that $(N, h)$ is a Riemannian manifold, and $\iota: M \to N$ is an immersed submanifold of $N$. The *induced metric* on $M$ is the $2$-tensor $g = \iota^* h$, which is just the restriction of $h$ to vectors tangent to $M$. 

The metric on $\Bbb R^n$ has the following form $$g= \sum_{i = 1}^n (dx^i)^2,$$meaning that $g_{ij} = \delta_{ij}$. 
 
Computations on a submanifold are usually most conveniently carried out in terms a *local parametrization*: this is an embedding of an open subset $U \subseteq \Bbb R^n$ into $N$, whose image is an open subset of $M$. 

**Example:** If $X: U \to \Bbb R^n$ is a parametrization of a submanifold $M \subseteq \Bbb R^n$ with the induced metric, the induced metric in standard coordinates $(u^1, \dots, u^n)$ on $U$ is just $$g = \sum_{i = 1}^n (dX^i)^2 = \sum_{i = 1}^n \left(\frac{\partial X^i}{\partial u^j} du^j\right)^2.$$
**Def:** If $(M_1, g_1)$ and $(M_2, g_2)$ are Riemannian manifolds, then product $M_1 \times M_2$ has a natural Riemannian metric $g = g_1 \oplus g_2$, called the *product metric*, defined by $$g(X_1 + X_2, Y_1 + Y_2) := g_1(X_1, Y_1) + g_2(X_2, Y_2),$$where $X_i, Y_i \in T_{p_i} M_i$, under the natural identification $T_{(p_1, p_2)}(M_1 \times M_2) = T_{p_1} M_1 \times T_{p_2} M_2$. 

**Obs:** Any local coordinates $(x^1, \dots, x^n)$ for $M_1$ and $(x^{n+1}, \dots, x^{n+m})$ for $M_2$ give coordinates $(x^1, \dots x^{n+m})$ for $M_1 \times M_2$. In terms of these coordinates the product metric has the local expression $g = g_{ij}dx^idx^j$, where $g_{ij}$ is a block diagonal matrix $$(g_ij) = \begin{pmatrix}
(g_1)_{ij} & 0 \\ 
0 & (g_2)_{ij} 
\end{pmatrix}$$
**Def:** Suppose $\pi: N \to M$ is a smooth covering map. A *covering transformation*, or *deck transformation* is a smooth map $\varphi: N \to N$ such that $\pi \circ \varphi = \pi$. If $g$ is Riemannian metric on $M$, then $h := \pi^* g$ is a Riemannian metric on $N$ that is invariant under all covering transformations. In this case $h$ is called a *covering metric*, and $\pi$ is called *Riemannian covering*. 