---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Tangent Vectors in Rn]], [[Smooth or Differentiable Manifolds]], [[Module and Algebra (Structure)]], [[Derivations]], [[Smooth Functions on Smooth Manifolds]], [[Partial Derivatives on Manifolds]], [[Matrix Representation of Linear Transformations]], [[Differentiability of Vector valued functions of Rn]]

# Tangent Space at a Point

Just as for $\Bbb R^n$, we define a *germ* of a $\mathcal C^\infty$ function at $p$ in $M$ to be an equivalence class of $\mathcal C^\infty$ function defined in a neighbourhood of $p\in M$, two such functions being equivalent if they agree on some neighbourhood of $p$. the set of all germs of $\mathcal C^\infty$ real-valued functions at $p\in M$ is denoted by $\mathcal C^\infty_p(M)$. The addition and multiplication of functions make $\mathcal C^\infty_p(M)$ into a ring: with scalar multiplication of real numbers, $\mathcal C^\infty_p(M)$ becomes an algebra over $\Bbb R$. 

Generalising a derivation at a point in $\Bbb R^n$, we define a *derivation at a point* in a manifold $M$, or a *point-derivation* of $\mathcal C^\infty_p(M)$, to be the linear map $D: \mathcal C^\infty_p(M) \to \Bbb R$ such that $$D(fg) = (Df)g(p) + f(p) Dg$$
**Def:** A *tangent vector* at a point $p$ in a manifold $M$ is a derivation at $p$. 

The tangent vectors form a vector space $T_p(M)$, called the *tangent space of $M$ at $p$.* We also write $T_pM$ instead of $T_p(M)$. 

**Obs:** If $U$ is an open set containing $p$ in $M$, then the algebra $\mathcal C^\infty_p(U)$ of germs of $\mathcal C^\infty$ in $U$ at $p$ is the same as $\mathcal C^\infty_p(M)$. Hence $T_p U = T_pM$. 

# Differential of a Map

**Def:** Let $F: N\to M$ be a $\mathcal C^\infty$ map between two manifolds. At each point $p\in N$. the map $F$ induces a linear map of tangent spaces called its *differential at $p$,* $$F_* =dF_p: T_pN \to T_{F(p)} M$$as follows. If $X_p \in T_p N$, then $dF_p(X_p)$ is the tangent vector in $T_{F(p)} M$ defined by $$(F_*(X_p))f =(dF_p(X_p))f := X_p(f \circ F) \in \Bbb R,\qquad f\in \mathcal C^\infty_{F(p)}(M) $$It doesn't really matter the distinction between using a germ or a representative function for the germ, when evaluating the differential. Sometimes we use $F_*$ to be make emphasis on as a *pushforward*. 

**Prop:** $dF_p: T_pN \to T_{F(p)} M$ is linear and $dF_p(X_p)$ is a derivation. 

To make the dependence on $p$ explicit we sometimes write $F_{*, p}$ instead of $F_*$ 

**Prop:** Let $M$ and $N$ be manifolds, let $\pi_M: M \times N \to M$ and $\pi_N: M\times N \to N$ be the two projections. Then for any $(p, q)\in M \times N$, $$(d(\pi_M)_{(p, q)}, d(\pi_N)_{(p, q)} : T_{(p, q)}(M \times N) \to T_p M \times T_q N $$is a vector space isomorphism.

# Chain Rule

Let $F: N \to M$ and $G: M \to P$ be smooth maps of manifolds, and $p\in N$. The differentials of $F$ at $p$ and $G$ at $F(p)$ are linear maps: 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts}
\usepackage{amsmath}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
T_p N      \arrow[r, "dF_p"] & 
T_{F(p)} M \arrow[r, "dG_{F(p)}"] &
T_{G(F(p))} P
\end{tikzcd}
\end{document}
```
**Th:** If $F: N \to M$ and $G: M \to P$ are smooth maps of manifolds and $p\in N$, then $$d(G\circ F)_{ p} = dG_{ F(p)} \circ dF_{p}$$
**Obs:** The differential of the identity map $\text{id}_M : M \to M$ at any $p$ in $M$ is the identity map $d (\text{id}_M)_p = \text{id}_{T_p M}: T_p M\to T_p M$.  

**Cor:** If $F: N \to M$ is a diffeomorphism of a manifolds and $p\in N$, then $dF_p: T_p N \to T_{F(p)} M$ is an vector space isomorphism.

**Cor: (Invariance of dimension)** If an open set $U \subseteq \Bbb R^n$ is diffeomorphic to an open set $V\subseteq \Bbb R^m$, then $n = m$. 

# Bases for the Tangent Space

Let $(U, \phi)$ be a chart about a point $p$ in a manifold $M$ of dimension $n$, $r^1, \dots, r^n$ be the standard coordinates of $\Bbb R^n$, we set $x^i = r^i \circ \phi$. We see that $\phi: U \to \phi[U]$ is a diffeomorphism, then we get that $d\phi_p : T_p M \to T_{\phi(p)} \Bbb R^n$ is a vector isomorphism. 

**Cor:** The tangents space $T_p M$ has the same dimension as the manifold $M$

**Prop:** Let $(U, \phi) = (U, x^1, \dots, x^n)$ be a chart about a point $p$ in a manifold $M$. Then $$d\phi_p\left(\left.\frac{\partial}{\partial x^i}\right\rvert_p\right) = \left. \frac{\partial}{\partial r^i}\right\rvert_{\phi(p)}$$ **Prop:** If $(U, \phi) = (U, x^1, \dots, x^n)$ is a chart containing $p$, then the tangent space $T_p M$ has a basis $$\left.\frac{\partial}{\partial x^1}\right\rvert_p, \dots, \left.\frac{\partial}{\partial x^n}\right\rvert_p$$
**Prop (Transition matrix for coordinate vectors):** Suppose $(U, x^1, \dots, x^n)$ and $(V, y^1,\dots, y^n)$ are two coordinate charts on a manifold $M$. Then $$\frac{\partial}{\partial x^j} = \sum \frac{\partial y^i}{\partial x^j} \frac{\partial}{\partial y^j}$$on $U \cap V$. 

# Local  Expression for the Differential

**Prop:** Given a smooth map $F: N \to M$ of manifolds and a point $p\in N$, let $(U, x^1,\dots, x^n)$ and $(V, y^1, \dots, x^m)$ be coordinate charts about $p$ in $N$ and $F(p)$ in $M$ respectively. Relative to the bases $\left\{\left.\dfrac{\partial}{\partial x^j}\right\rvert_p\right\}$ for $T_p N$ and $\left\{\left.\dfrac{\partial}{\partial y^i}\right\rvert_{F(p)}\right\}$ for $T_{F(p) }M$ the differential $dF_{p} : T_p N \to T_{F(p)} M$ is represented by the matrix $\left[\dfrac{\partial Fi}{\partial x^j}\right]$ where $F^i = y^i \circ F$ is the $i$th component of $F$.

# Curves in a Manifold

A *smooth curve*on a manifold $M$ is by definition a smooth map $c: (a, b) \to M$ from some open interval $(a, b)$ into $M$. We usually assume that $0 \in (a, b)$ and we say that $c$ is a *curve starting at $p$* if $c(0) = p$. The *velocity vector* $c'(t_0)$ of a curve $c$ at time $t_0 \in (a, b)$ is defined to be $$c'(t_0):= dc_{c(t_0)} \left(\left.\frac{d}{dt}\right\rvert_{t_0}\right) \in T_{c(t_0)} M. $$We also say that $c'(t_0)$ is the velocity vector of $c$ at the point $c(t_0)$. 

Since, $c'(t)$ in this context means a tangent vector, but also can mean the derivative of $c$, i am going to use Newton's notation for $\dot c$ to refer to the derivative so it is not confused with tangent vector. 

**Prop (Velocity of a curve in local coordinates):** Let $c:(a, b) \to M$ be a smooth curve, and let $(U, x^1, \dots, x^n)$ be a coordinate chart about $c(t)$. Write $c^i = x^i \circ c$ for the $i$ component of $c$ in the chart. Then $c'(t)$ is given by $$c'(t) = \sum_{i = 1}^n \dot c^i(t) \left.\frac{\partial}{\partial x^i} \right\rvert_{c(t)}.$$
Every smooth curve $c$ at $p$ in a manifold $M$ gives rise to a tangent vector $c'(0)$ in $T_p M$.

**Prop (Existence of a curve with a given initial vector):** For any point $p$ in a manifold $M$ and any tangent vector $X_p \in T_p M$, there are $\varepsilon >0$ and a smooth curve $c:(-\varepsilon, \varepsilon) \to M$ such that $c(0) = p$ and $c'(0) = X_p$.

**Prop:** Suppose $X_p$ is a tangent vector at a point $p$ of a manifold $M$ and $f\in \mathcal C^\infty_p(M)$. If $c: (-\varepsilon, \varepsilon) \to M$ is a smooth curve starting at $p$ with $c'(0) = X_p$, then $$X_p f = \left.\frac{d}{dt}\right\rvert_0 (f \circ c)$$
**Prop:** Let $F: N \to M$ be a smooth map of manifolds, $p\in N$, and $X_p\in T_p N$. If $c$ is a smooth curve starting at $p$ in $N$ with velocity $X_p$ at $p$, then: $$dF_{p}(X_p) = \left.\frac{d}{dt}\right\rvert_0 (F\circ c) (t)$$In other words, $F_{*, p}(X_p)$ is the velocity vector of the image curve $F\circ c$ at $F(p)$. 

# The Tangent Space to a Manifold with Boundary

Suppose $M$ is an $n$-dimensional manifold with boundary, and $p$ is a boundary point of $M$. We would like to preserve as much as possible, with this in mind we still define $T_p M$ as the space of all derivations of $\mathcal C^\infty(M)$ at $p$. 

**Lemma:** If $M$ is an $n$-dimensional manifold with boundary, and $p$ is a boundary point of $M$, then $T_p M$ is an $n$-dimensional vector space, with basis given by the coordinate vectors $\left\{\left.\dfrac{\partial}{\partial x^j}\right\rvert_p\right\}$ in any smooth chart. 