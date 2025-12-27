---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Cotangent Bundle]], [[Differential 1-forms on Smooth Manifolds]], [[Local and Global Sections of Vector Bundles]], [[Exterior Algebra]], [[The Dual Functor and the Multicovector Functor]]

We consider the vector space ${\textstyle\bigwedge}^{\!k} (T_p^*M)$, the space of all alternating $k$-covectors on each tangent space $T_p M$. 

**Def:** A $k$-covector field on $M$ is a function $\omega$ that assigns to each point $p\in M$ a $k$-covector $\omega_p \in {\textstyle\bigwedge}^{\!k}(T_p^* M)$. $k$-covector field is also called a *differential $k$-form*, a *differential form of degree $k$*, or simply a $k$-form. A *top form* on a manifold is a differential form whose degree is the dimension of the manifold.

If $\omega$ is a $k$-form on the manifold $M$, and $X_1, \dots, X_k$ are vector fields on $M$, then $\omega(X_1, \dots, X_k)$ is the function on the manifold $M$ defined by: $$(\omega(X_1, \dots, X_k))(p) = \omega_p((X_1)_p, \dots, (X_k)_p).$$
**Cor:** Let $\omega$ be a $k$-form on a manifold $M$. For any vector fields $X_1, \dots, X_k$ and any function $h$ on $M$, $$\omega(X_1, \dots,  hX_i, \dots, X_k) = h \omega(X_1, \dots, X_i, \dots, X_k)$$
# Local Expression for a $k$-form

Since it is similar to $k$-vectors, we are going to use a set to simplify the notation: $$\mathcal I_{k, n} = \{I = (i_1, \dots, i_k) \mid 1 \le i_1 < \dots < i_k \le n\}$$be the set of all strictly ascending multi-indeces between $1$ and $n$ of length $k$. Using this notation if $I \in \mathcal I_{k, n}$, then $$dx^I := dx^{1_1}\wedge \dots \wedge dx^{i_k}$$
Let $(U, x^1, \dots, x^n)$ be a coordinate chart on a manifold. At each point $p\in U$, a basis for the tangent space $T_p U$ is $$\left.\frac{\partial}{\partial x^1}\right\rvert_p, \dots, \left.\frac{\partial}{\partial x^n}\right\rvert_p.$$We say that the basis for the cotangent space $T_p^* U$ is $$(dx^1)_p, \dots, (dx^n)_p.$$
We know that the basis for the alternating $k$-covectors in ${\textstyle\bigwedge}^{\!k} (T_p^*U)$ is $$\{(dx^I)_p\mid  I \in \mathcal I_{k, n}\}$$Meaning that we can write $\omega_p$ is a linear combination: $$\omega_p =  a_I (dx^I)_p.$$Lastly, If we consider $\omega$ in general, we get that $$\omega =  a_I dx^I.$$
**Obs:** On a coordinate chart $(U, x^1, \dots, x^n)$ of a manifold $M$. As shorthand, we write $\partial_i = \dfrac{\partial}{\partial x^i}$ for the $i$th coordinate vector field. We obtain the following equality on $U$, for $I, J \in \mathcal I_{k , n}$: $$dx^I (\partial_{j_1}, \dots, \partial_{j_k}) = \delta_J^I $$
**Wedge product of differentials in local coordinates:** Let $(U, x^1, \dots, x^n)$ be a chart on a manifold and $f^1, \dots, f^k$ smooth functions on $U$. Then $$ df^1 \wedge \dots \wedge df^k =  \frac{\partial(f^1, \dots, f^k)}{\partial x^I} dx^I,$$where: $$\frac{\partial(f^1, \dots, f^k)}{\partial x^I} := \frac{\partial(f^1, \dots, f^k)}{\partial (x^{i_1}, \dots, x^{i_k})}$$
**Cor:** Let $(U, x^1, \dots, x^n)$ be a chart on a manifold and $f^1, \dots, f^n$ smooth functions on $U$. Then
- ($1$-forms) $df = \sum (\partial f/\partial x^i) dx^i$
- (top forms) $df^1 \wedge \dots \wedge df^n = \det[\partial f^j/\partial x^i] dx^1\wedge \dots \wedge dx^n$

**Cor:** If $(U, x^1, \dots, x^n)$ and $(V, y^1, \dots, y^n)$ are two overlapping charts on a manifold $M$ on the intersection $U\cap V$, we get the transition formula for $k$-forms: $$dy^J =  \frac{\partial y ^J}{\partial x^I} dx^I,$$where: $$\frac{\partial y^J}{\partial x^ I} := \frac{\partial(y^{j_1}, \dots, y^{j_k})}{\partial (x^{i_1}, \dots, x^{i_k})}$$
**Cor:** If $(U, x^1, \dots, x^n)$ and $(V, y^1, \dots, y^n)$ are two overlapping charts on a manifold $M$ on the intersection $U\cap V$, and $\omega$ a $k$-form $$\omega =  a_I dx^I =  b_J dx^J.$$ Then we can calculate $$a_I =  b_J\frac{\partial y^J}{\partial x^ I}.$$
# Bundle Point of View

**Def:** A differential $k$-form is simply a section of the bundle $({\textstyle\bigwedge}^{\!k} (T^*M), M, \pi)$. A $k$-form is said to be smooth if it is smooth as a section of the bundle $\pi: {\textstyle\bigwedge}^{\!k} (T^*M) \to M$. 

**Def:** The vector space of all smooth $k$-forms on $M$ is usually denoted by $\Omega^k(M)$. Thus: $$\Omega^k(M) := \Gamma({\textstyle\bigwedge}^{\!k} (T^*M)) = \Gamma(M, {\textstyle\bigwedge}^{\!k} (T^*M))$$We get a special case where ${\textstyle\bigwedge}^{\!0} (T_p^*M) = \Bbb R$. Therefore, the bundle ${\textstyle\bigwedge}^{\!0} (T^*M) = M \times \Bbb R$, and $0$-from on $M$ is a function on $M$. A smooth $0$-form on $M$ is thus the same as a smooth function on $M$. In our new notation $$\Omega^0(M) := \mathcal C^\infty(M)$$
We define the vector space $\Omega ^*(M)$ of smooth differential forms on a manifold $M$ of dimension $n$ to be the direct sum $$\Omega^* (M) := \bigoplus _{k = 0}^n\Omega ^k(M).$$This means that $\Omega^*(M)$ is a graded vector space, the grading being the degree of the differential forms.
# Smoothness

**Lemma:** Let $(U, x^1, \dots, x^n)$ be a chart on a manifold $M$. A $k$-form $\omega = \sum a_I dx^I$ on $U$ is smooth if the coefficients $a_I$ are all smooth on $U$.

**Characterisation of a smooth $k$-form:** Let $\omega$ be a $k$-form on a manifold $M$. The following are equivalent:
- The $k$-form $\omega$ is smooth on $M$.
- The manifold has an atlas such that on any chart $(U, x^1, \dots, x^n)$ of the atlas, the coefficients $a_I$ of $\omega = \sum a_I dx^I$ relative to the frame $\{dx^I \mid I \in \mathcal I_{k, n}\}$ are all smooth.
- On any chart $(U, x^1, \dots, x^n)$ on the manifold, the coefficients $a_I$ of $\omega = \sum a_I dx^I$ relative to the frame $\{dx^I \mid I \in \mathcal I_{k, n}\}$ are all smooth.
- For any $k$ smooth vector fields $X_1, \dots, X_k$ on $M$, the function $\omega(X_1, \dots, X_k)$ is smooth on $M$.

**Prop:** Suppose $\tau$ is a smooth differential form defined on a neighbourhood $U$ of a point $p$ in a manifold $M$. Then there is a smooth form $\tilde \tau$ on $M$ that agrees with $\tau$ on a possibly smaller neighbourhood of $p$. 
# Pullbacks

We have defined pullback on $0$-forms on $1$-forms under a smooth map $F: N \to M$. For a smooth $0$-form on $M$, i.e., a smooth function on $M$, the pullback $F^*f$ is simple the composition $$N \stackrel{F}{\to} M \stackrel{f}{\to} \Bbb R, \quad F^* (f) = f \circ F \in \Omega^0(N).$$To generalise the pullback to $k$-forms for all $k \ge 1$, we need to recall the pullback of $k$-covectors, from [[The Dual Functor and the Multicovector Functor|here]]. 

Now suppose $F: N \to M$ is a smooth map of manifolds. At each point $p \in N$, the differential $$dF_p = F_{*, p}: T_p N \to T_{F(p)} M$$is a linear map of tangent spaces, and so there is a pullback map: $$ (dF_p)^*: A_k(T_{F(p)} M) \to A_k(T_p N)$$ We simplify the notation to $F^*$. Thus if $\omega_{F(p)}$ is a $k$-covector at $F(p)$ in $M$ then its *pullback* $F^*(\omega_{F(p)})$ is the $k$-covector at $p$ in $N$ defined by $$F^*(\omega_{F(p)})(v_1, \dots, v_k) = \omega_{F(p)}(dF_p v_1, \dots, dF_p v_k), \quad v_i \in T_p N.$$If $\omega$ is a $k$-form on $M$, then its *pullback* $F^*\omega$ is the $k$-form on $N$ defined pointwise by $(F^*\omega)_p = F^*(\omega_{F(p)})$, for all $p \in N$. Equivalently, $$(F^*\omega)_p(v_1, \dots, v_k) = \omega_{F(p)}(dF_p v_1, \dots, dF_p v_k), \quad v_i \in T_p N.$$The pullback of a $k$-form can be viewed as a composition: 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts}
\usepackage{amsmath}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
T_p N  \times \dots \times T_p N    \arrow[r, "F_* \times \dots \times F_*"] & 
T_{F(p)} M \times \dots \times T_{F(p)} M \arrow[r, "\omega_{F(p)}"] &
\Bbb R
\end{tikzcd}
\end{document}
```

**Linearity of the pullback:** Let $F: N \to M$ be a smooth map. If $\omega, \tau$ are $k$-forms on $M$ and $a$ is a real number, then:
- $F^*(\omega + \tau) = F^*\omega + F^*\tau$
- $F^*(a\omega) = aF^*\omega$

**Prop:** If $F: N \to M$ is a smooth map of manifolds and $\omega$ is a smooth $k$-form on $M$, then $F^*\omega$ is a smooth $k$-form on $N$. The proof of this relies on [[The Exterior Derivative on Manifolds]].

**Lemma:** In any smooth chart,  $$F^*(\omega_I dy^I ) = (\omega_I \circ F) d(y^{i_1} \circ F)\wedge\dots \wedge d(y^{i_k} \circ F)  $$
**Prop:** Let $F: M \to N$ be a smooth map between $n$-dimensional manifolds. If $(x^i)$ and $(y^j)$ are smooth coordinates on open sets $U \subseteq M$ and $V\subseteq N$, repectively, and $u$ is is a smooth real-valued function on $V$, then the following holds in $U \cap F^{-1}[V]$: $$F^*(u\, dy^1\wedge \dots \wedge dy^n) = (u \circ F)\left(\dfrac{\partial (F^1, \dots, F^n)}{\partial(x^1, \dots, x^n)}\right) \, dx^1\wedge \dots \wedge dx^n.$$
**Cor:** If $(U, (x^i))$ and $(V, (y^i))$ are overlapping smooth coordinate chart on $M$, then the following identity holds on $U \cap V$: $$dy^1\wedge \dots \wedge dy^n = \frac{\partial(y^1, \dots, y^n)}{\partial (x^1,\dots, x^n)}dx^1\wedge\dots \wedge dx^n $$

### Restrictions

**Def:** Let $S\subseteq M$ be an immersed manifold and $i: S \to M$ the inclusion map. At any point $p \in S$, since the differential $i_* :T_p S \to T_p M$ is injective, then $T_p S$ can be interpreted as subspace of $T_p M$. If $\omega$ is a $k$-form on $M$, then the *restriction* of $\omega$ to $S$ is the $k$-form $\omega|_S$ defined by $$(\omega|_S)_p(v_1, \dots, v_k) = \omega_p (v_1,\dots, v_k), \qquad p \in S, v_1,\dots, v_k \in T_p S.$$**Prop:** If $i:S \hookrightarrow M$ is the inclusion map of an immersed submanifold $S$ and $\omega$ is a $k$-form on $M$, then $i^* \omega = \omega|_S$. 

**Prop:** Let $F: N \to M$ be a smooth map of manifolds, $U$ is an open subset of $M$, $\omega \in \Omega^k(M)$, then $$\left(F|_{F^{-1}[U]}\right)^* (\omega|_U) = (F^* \omega)|_{F^{-1}[U]}$$
# Wedge Product

**Def:** For a $k$-form $\omega$ and $\ell$-form $\tau$ on $M$, we define their *wedge product* $\omega\wedge\tau$ to be the $(k+\ell)$-form on $M$ such that $$(\omega\wedge \tau)_p = \omega_p\wedge \tau_p$$at all $p \in M$. 

**Prop:** If $\omega$ and $\tau$ are smooth forms on $M$, then $\omega\wedge\tau$ is also smooth.

**Cor:** $\Omega^*(M)$ is a graded algebra, the grading being the degree of the differential forms. 

**Pullback of a wedge product:** If $F: N \to M$ is a smooth map of manifolds and $\omega$ and $\tau$ are differential forms on $M$, then $$F^*(\omega\wedge\tau) = F^*\omega\wedge F^*\tau$$