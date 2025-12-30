---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links:  [[Smooth Manifolds]], [[Module and Algebra]], [[Derivations]], [[Smooth Functions on Smooth Manifolds]], [[Partial Derivatives on Manifolds]], [[Matrix Representation of Linear Transformations]], [[Differentiability of Vector valued functions of Rn]]

# Preliminaries
Given a point $a\in \Bbb R$, we define (momentarily) the *geometric tangent space to $\Bbb R^n$ to $a$,* denoted by $\Bbb R^n_a$, to be the set $\{a\}\times \Bbb R^n$. A *geometric tangent vector* in $\Bbb R^n$ is an element of $\Bbb R^n_a$ for some $a\in \Bbb R^n$. We are gonna abbreviate $(a,v)$ to $v_a$ or $v|_a$. The set $\Bbb R^n_a$ is a real vector space under the natural operations: $$v_a+ w_a := (v+w)_a \qquad c(v_a) := (cv)_a.$$The vectors $e_i|_a$ for $i = 1,\dots, n$ are a basis for $\Bbb R_a^n$. Even more $\Bbb R^n_a$ and $\Bbb R$ are basically identical, but $\Bbb R^n_a$ and $\Bbb R^n_b$ are different spaces, if $a$ and $b$ are different.

The only things we have to work with on smooth manifolds so far are smooth function, smooth maps, and smooth coordinate charts. The geomeetric tangent vector provides is a means of taking direcional derivatives of functions. Any geometric tangent vector $v_a\in \Bbb R^n_a$
yields a map $D_v|_a: \Bbb C^\infty(\Bbb R^n) \to \Bbb R,$ which takes teh directional derivative in the direction $v$ at $a$: $$D_v|_a f := D_v f(a) = \left.\frac{d}{dt}\right\rvert_{t= 0} f(a+tv).$$This operation is linear over $R$ and satisfies the product rule $$D_v|_a (fg) = f(a)D_v|_ag + g(a)D_v|_af.$$
We see that $v_a = v^i e_i|_a$ in terms of the standard basis, then by the chain rule $D_v|_af$ can be written more concretely as $$D_v|_a f = v^i \frac{\partial f}{\partial x^i}(a).$$
If $a$ is point of $\Bbb R^n$, a map $w: \mathcal C^\infty(\Bbb R^n) \to \Bbb R$ is called a *derivation at $a$* if it is linear over $\Bbb R$ and satisfies the product rule $$w(fg) = f(a) w g+ g(a)wf.$$
Let $T_a \Bbb R^n$ denote the set of all derivations of $\mathcal C^\infty(\Bbb R)$ at $a$. Clearly, $T_a\Bbb R^n$ is a vector space, with the obvious operations.

**Lemma:** Suppose $a\in \Bbb R^n$, $w\in T_a\Bbb R^n$ and $f,g\in\mathcal C^\infty(\Bbb R^n)$.
- If $f$ is a constant function, then $wf = 0$
- If $f(a) = g(a) = 0$, then $w(fg) = 0$.

**Prop:** Let $a\in \Bbb R^n$.
- For each geometric vector $v_a\in \Bbb R^n_a$, the map $D_v|_a: \mathcal C^\infty(\Bbb R^n)\to \Bbb R$ is a derivation at $a$.
- The map $v_a \mapsto D_v|_a$ is an isomorphism from $\Bbb R^n_a$ onto $T_a\Bbb R^n$. 

**Cor:** For $a\in \Bbb R^n$, then $n$ derivations $$\frac{\partial}{\partial x^1},\dots, \frac{\partial}{\partial x^n} $$form a basis for $T_a\Bbb R^n$, which is therefore has dimension $n$. 

# Tangent Vectors on Manifolds

**Def:** Let $M$ be a smooth manifold with or without boundary, and let $p\in M$. A linear map $v: \mathcal C^\infty(M) \to \Bbb R$ is a called a *derivation at $p$* if it satisfies $$v(fg) = f(p) vg + g(p) vf$$for all $f, g\in \mathcal C^\infty(M)$. The set of all derivations of $C^\infty(M)$ at $p$, denoted by $T_pM$, is a vector space called the *tangent space to $M$ at $p$*. An element of $T_pM$ is called a *tangent vector at $p$.*

**Lemma:** Suppose $M$ is a smooth manifold with or without boundary, $p\in M$, $v\in T_pM$ and $f,g\in \mathcal C^\infty(M)$. 
- If $f$ is a constant function, then $vf = 0$
- If $f(a) = g(a) = 0$, then $v(fg) = 0$.

# Differential of a Map

**Def:** Let $F: N\to M$ be a $\mathcal C^\infty$ map between two manifolds with or without boundaries. At each point $p\in N$. the map $F$ induces a linear map of tangent spaces called its *differential at $p$,* $$F_* =dF_p: T_pN \to T_{F(p)} M$$as follows. If $X_p \in T_p N$, then $dF_p(X_p)$ is the tangent vector in $T_{F(p)} M$ defined by $$(F_*(X_p))f =(dF_p(X_p))f := X_p(f \circ F) \in \Bbb R,\qquad f\in \mathcal C^\infty_{F(p)}(M) $$It doesn't really matter the distinction between using a germ or a representative function for the germ, when evaluating the differential. Sometimes we use $F_*$ to be make emphasis on as a *pushforward*. 

**Prop:** $dF_p: T_pN \to T_{F(p)} M$ is linear and $dF_p(X_p)$ is a derivation. 

To make the dependence on $p$ explicit we sometimes write $F_{*, p}$ instead of $F_*$ 

**Prop:** Let $M$ and $N$ be manifolds, let $\pi_M: M \times N \to M$ and $\pi_N: M\times N \to N$ be the two projections. Then for any $(p, q)\in M \times N$, $$(d(\pi_M)_{(p, q)}, d(\pi_N)_{(p, q)} : T_{(p, q)}(M \times N) \to T_p M \times T_q N $$is a vector space isomorphism.

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

**Cor:** If $F: N \to M$ is a diffeomorphism of a manifolds and $p\in N$, then $dF_p: T_p N \to T_{F(p)} M$ is an vector space isomorphism, with $(dF)_p^{-1} = d(F^{-1})_p$. 

**Cor: (Invariance of dimension)** If an open set $U \subseteq \Bbb R^n$ is diffeomorphic to an open set $V\subseteq \Bbb R^m$, then $n = m$. 


# Bases for the Tangent Space

**Prop** Let $M$ be a smooth manifold with or without boundary, $p\in M$ and $v\in T_pM$. If $f,g \in \mathcal C^\infty(M)$ agree on some neighbourhood of $p$, then $vf = vg$. 

**Prop:** Let $M$ be a smooth manifold with or without boundary, let $U\subseteq M$ be an open subset, and let $\iota: U \hookrightarrow M$ be the inclusion map. For every $p\in U$, the differential $d\iota_p: T_p U \to T_p M$ is an isomorphism. 

Let $(U, \phi)$ be a chart about a point $p$ in a manifold $M$ of dimension $n$, $r^1, \dots, r^n$ be the standard coordinates of $\Bbb R^n$, we set $x^i = r^i \circ \phi$. We see that $\phi: U \to \phi[U]$ is a diffeomorphism, then we get that $d\phi_p : T_p M \to T_{\phi(p)} \Bbb R^n$ is a vector isomorphism. 

**Cor:** The tangents space $T_p M$ has the same dimension as the manifold $M$

**Lemma:** Let $\iota: \Bbb H^n \to \Bbb R^n$ denote the inclusion map. For every $a\in\Bbb H^n$, the differential $d\iota_a: \Bbb H^n \to T_a\Bbb R^n$ is an isomorphism. 

**Prop:** Suppose $M$ is n $n$-dimensiona smooth manifold with boundary. For each $p\in M$ $T_pM$ is an $n$-dimensional vector space. 

**Prop:** Suppose $V$ is a finite-dimensional real vector space with its standard smooth structure. For each point $a\in V$, the map $v\mapsto D_v|_a$ is a canonical isomorphism from $V$ to $T_aV$, such that the linear map $L: V \to W$, the following diagram commutes 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
     V\arrow[d, "L"']\arrow[r, "\cong"] & T_a V\arrow[d ,"dL_a"] \\
     W\arrow[r, "\cong"] & T_{La} W
   \end{tikzcd}
\end{document}
```

**Prop:** Let $M_1,\dots, M_k$ be smooth manifolds, and for each $j$, let $\pi_j: M_1\times \dots \times M_k \to M_j$ be the projection onto the $M_j$ factor. For any point $p = (p_1,\dots, p_k)\in M_1\times \dots \times M_k$, the map $$\alpha: T_p (M_1\times \dots \times M_k) \to T_{p_1} M \oplus \dots \oplus T_{p_k}M_k $$defined by  $$\alpha (v) = \left(d(\pi_1)_p (v), \dots, d(\pi_k)_p(v)\right)  $$is an isomorphism. The same is true if one of the spaces $M_i$ is a smooth manifold with boundary. 

**Prop:** Let $(U, \phi) = (U, x^1, \dots, x^n)$ be a chart about a point $p$ in a manifold $M$. Then $$d\phi_p\left(\left.\frac{\partial}{\partial x^i}\right\rvert_p\right) = \left. \frac{\partial}{\partial r^i}\right\rvert_{\phi(p)}$$ **Prop:** If $(U, \phi) = (U, x^1, \dots, x^n)$ is a chart containing $p$, then the tangent space $T_p M$ has a basis $$\left.\frac{\partial}{\partial x^1}\right\rvert_p, \dots, \left.\frac{\partial}{\partial x^n}\right\rvert_p$$
**Prop (Transition matrix for coordinate vectors):** Suppose $(U, x^1, \dots, x^n)$ and $(V, y^1,\dots, y^n)$ are two coordinate charts on a manifold $M$. Then $$\frac{\partial}{\partial x^j} = \frac{\partial y^i}{\partial x^j} \frac{\partial}{\partial y^j}$$on $U \cap V$. 

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


# Alternative Definitions of the Tangent Space

### Tangent Vectors as Derivations of the Space of Germs

**Def:** A *smooth function element* on $M$ is an ordered pair $(f, U)$ where $U$ is an open smooth subset of $M$ and $f: U \to \Bbb R$ is a smooth function. Given a point $p\in M$, let us define an equivalence relation on the set of all smooth function elements whose domain contain $p$ by setting $(f, U) \sim (g, V)$ if $f = g$ on some neighbourhood $p$. The equivalence class of a function element $(f, U)$ is called a *germ of $f$ at $p$*. The set of all germs of smooth functions at $p$ is denoted by $\mathcal C^\infty_p(M)$. It is a real vector space and an associative algebra under the operations $$
\begin{align*}
c[(f, U)] &= [(cf, U)] \\
[(f, U)] + [(g, V)] &= [(f+g, U \cap V)] \\
[(f, U)] [(g, V)] &= [(fg, U \cap V)]
\end{align*}
$$
Let us denote the germ at $p$ of the function element $(f, U)$ simply by $[f]_p$. To say that two germs $[f]_p$ and $[g]_p$ are equal is simply to say that $f = g$ on some neighbourhood of $p$.

A *derivation at $\mathcal C^\infty_p (M)$* is a linear map $v: \mathcal C^\infty_p(M) \to \Bbb R$ satisfying the following product rule $$v[fg]_p = f(p) v[g]_p + g(p) v[f]_p.$$
It is common to define the tangent space to $M$ at $p$ as as the vector space $\mathcal D_p M$ of the derivations of $\mathcal C^\infty_p(M)$.  

The germ definition has a number of advantages. One of the most significant it makes the local nature of the tangent space clearer, without requiring the use of bump functions. Since analytic bump functions, the germ definition of tangent vectors is the only avaialble on real-analytic or complex-analytic manifolds.

### Tangent Vectors as Equivalence Classes of Curves

Suppose $p$ is a point of $M$. We wish to define an equivalence relation on the set of all smooth curves of the form $\gamma: J \to M$, where $0\in J$ and $\gamma(0) = p$. Given two such curves $\gamma_1: J_1 \to M$ and $\gamma_2: J_2\to M$, let us say that $\gamma_1\sim \gamma_2$ if $(f\circ\gamma_1)'(0) = (f\circ \gamma_2)'(0)$ for every smooth real-valued function $f$ defined on a neighourhood of $p$. Let $\mathcal V_p M$ denote the set of equivalence classes. The tangent space to $M$ at $p$ is often defined to be the set $\mathcal V_p M.$

It is very easy define the differential of a map $F: M \to N$ as the map $[\gamma]\in \mathcal V_p M$ to $[F\circ \gamma]\in \mathcal V_p N$. Velocity vectors of smooth curves are almost as easy to define. We see that $\mathcal V_p M$ is isomorphic to $T_p M$.

### Tangent Vectors as Equivalence Classes of $n$-Tuples

One defines a tangent vector at a point $p\in M$ to be a rule that assigns an ordered $n$-tuple $(v^1,\dots, v^n) \in\Bbb R^n$ to each smooth coordinate chart containing $p$, with the property that the $n$-tuples assigned to overlapping charts transform according  to$$\frac{\partial}{\partial x^j} = \frac{\partial y^i}{\partial x^j} \frac{\partial}{\partial y^j}.$$
In this approach, the velocity of a curve is defined by the usual Euclidean formula in coordinates, and the differential of $F: M \to N$ is defined as the linear map determined by the Jacobian matrix of $F$ in coordinates. By black magic of tedious computations we see that these operations are well defined, independently of choices of coordinates.

