---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[The Cotangent Bundle]], [[Vector Fields on Smooth Manifolds]], [[Tangent Space for Manifolds]], [[Dual Vector Spaces]]

**Def:** A *covector field*, a *differential $1$-form*, or more simply a $1$-*form* on $M$, is a function $\omega$ that assigns to each point $p$ in $M$ a covector $\omega_p$ at $p$. In this sense, it is dual to a vector field $M$. 

In terms of the cotangent bundle $T^*M$, a differential $1$-form is simply a section of the cotangent bundle $T^*M$. Meaning, it is a map $\omega: M \to T^*M$ such that $\pi \circ \omega: \text{id}_M$, the identity on $M$, where $\pi$ is the projection of the cotangent bundle $(T^*M, M, \pi)$. We say that a $1$-form $\omega$ is smooth if it is as a map $M \to T^* M$.  This is because the cotangent bundle is actually the dual of the tangent bundle, i.e. $T^*M := (TM)^*$. 

# Differential of a Function

**Def:** If $f$ is a smooth real-valued function on a manifold $M$, its *differential* is defined to be the $1$-form $df$ on $M$ such that for any $p \in M$, and $X_p\in T_p M$, $$(df)_p(X_p) := X_p f$$
**Prop:** If $f: M \to \Bbb R$ is a smooth function, then for $p \in M$ and $X_p \in T_p M$, $$ d(f)_p (X_p ) =f_*(X_p) = (df)_p (X_p) \left.\frac{d}{dt} \right\rvert_{f(p)}$$The first equality is refers to the difference in notation for the differential of a smooth function between manifolds. 

This shows that under the canonical identification of the tangent space $T_{f(p)} \Bbb R$ with $\Bbb R$ via $a \left.\dfrac{d}{dt}\right\rvert_{f(p)} \leftrightarrow a$, $d(f)_p = f_*$ is the same as $df$. For this reason we are justified in calling both of them the *differential* of $f$. In terms of the differential $df$, a smooth function $f: M \to\Bbb R$ has a [[Submersions, Immersions and Embeddings of Manifolds#^071ac1|critical point]] at $p\in M$ iff $(df)_p = 0$.

# Local Expression for a Differential $1$-form

Let $(U, \phi)= (U, x^1, \dots, x^n)$ be a coordinate chart on a manifold $M$. Then the differential $dx^1, \dots, dx^n$ are $1$-forms on $U$. 

**Prop:** At each point $p\in U$, the covectors $(dx^1)_p,\dots, (dx^n)_p$ form a basis for the cotangent space $T_p^*M$ dual to the basis $\left.\dfrac{\partial}{\partial x^1}\right\rvert_p, \dots, \left.\dfrac{\partial}{\partial x^n}\right\rvert_p$ for the tangent space $T_p M$. Meaning that $(dx^1)_p, \dots, (dx^n)_p$ is the coframe of $\left.\dfrac{\partial}{\partial x^1}\right\rvert_p, \dots, \left.\dfrac{\partial}{\partial x^n}\right\rvert_p$

**Obs:** Thus, every $1$-form $\omega$ on $U$ can be written as a linear combination $\omega = \sum a^i dx ^i$. 

**Cor:** Let $f$ be a smooth real-valued function on $M$ and if we restrict $df$ on $U$, then $$df = \frac{\partial f}{\partial x^i}dx^i.$$
# Characterisation of Smooth $1$-forms

**Def:** Let $\omega$ be a $1$-form on a manifold $M$ to be *smooth* if $\omega: M \to T^*M$ is smooth as a section of the cotangent bundle $\pi: T^*M \to M$. The set of all smooth $1$-forms on $M$ is denoted as $\Omega^1(M) := \Gamma(T^* M)$ is a $\Bbb R$-vector space and a $\mathcal C^\infty(M)$-module. 

**Lemma:** Let $(U, \phi)= (U, x^1, \dots, x^n)$ be a coordinate chart on a manifold $M$. A $1$-form $\omega = \sum a_i dx^i$ on $U$ is smooth iff the coefficient functions $a_i$ are all smooth.

**Prop (Smoothness of a $1$-form in terms of coefficients):** Let $\omega$ be a $1$-form on a manifold $M$. The following are equivalent:
- The $1$-form $\omega$ is smooth on $M$.
- The manifold has an atlas such that on any chart $(U, x^1, \dots, x^n)$ of the atlas, the coefficients $a_i$ of $\omega = a_i dx^i$ relative to the frame $dx^i$ are all smooth.
- On any chart $(U, x^1, \dots, x^n)$ on the manifold, the coefficients $a_i$ of $\omega = a_i dx^i$ relative to the frame $dx^i$ are all smooth.

**Cor:** If $f$ is a smooth function of a manifold $M$, then its differential $df$ is a smooth $1$-form on $M$.

Suppose $(U, x^1, \dots, x^n)$ and $(V, \dots, y^1, \dots, y^n)$ are two charts on $M$ with nonempty overlap. Then a smooth $1$-form $\omega$ on $U\cap V$ has two different local expressions: $$X =  X_i dx^i =  \tilde X_i dy^i.$$Then we see that $$X_k =  \tilde X_i \frac{\partial y^i}{\partial x^k}$$
**Def:** If $\omega$ is a $1$-form and $X$ is a vector field on the manifold $M$, we define a function $\omega(X)$ on $M$ by the formula $$\omega(X)_p := \omega_p(X_p)\in \Bbb R, \qquad p \in M.$$
**Prop (Linearity of a $1$-form over functions):** Let $\omega$ be a $1$-form on a manifold $M$. If $f$ is a function and $X$ is a vector field on $M$, then $\omega(fX) = f\omega(X)$. 

**Prop (Smoothness of a $1$-form in terms of vector fields):** A $1$-form $\omega$ on a manifold $M$ is smooth iff for every smooth vector field $X$ on $M$, the function $\omega(X)$ is smooth on $M$.

**Obs:** A $1$ form $\omega$ on $M$ defines a map $\mathfrak X(M) \to \mathcal C^\infty(M)$, and this map is $\Bbb R$-linear and $\mathcal C^\infty(M)$-linear.

# Pullback of $1$-forms

If $F: N \to M$ is a smooth map of manifolds then at each point $p \in N$ the differential $$dF_p= F_{*, p}: T_p N \to T_{F(p)} M$$is a linear map that pushes forward vectors at $p$ from $N$ to $M$. 

**Def:** The *codifferential* is the dual map of the differential: $$(dF_p)^\lor = (dF_p)^*: T_{F(p)}^* M \to T_p N$$reverses the arrow and pulls a back a covector at $F(p)$ from $M$ to $N$. Another notation for the codifferential is $F^* = (dF_p)^\lor$. By the definition of the dual, if $\omega_{F(p)}\in T_{F(p)}^* M$ is a covector at $F(p)$ and $X_p \in T_p N$ is a tangent vector at $p$, then $$F^*(\omega_{F(p)})(X_p) = ((dF_p)^*\omega_{F(p)})(X_p) = \omega_{F(p)}(dF_p X_p).$$We call $F^*(\omega_{F(p)})$ the *pullback* of the covector at $\omega_{F(p)}$ by $F$. Thus, the pullback of covectors is simply the codifferential. 

**Obs:** Unlike vector fields, which in general cannot be pushed forward under a smooth map, every covector field can be pulled back by a smooth map. 

**Def:** If $\omega$ is a $1$-form on $M$, its *pullback* $F^*\omega$ is the $1$-form on $N$ defined pointwise: $$(F^* \omega) = F^*(\omega_{F(p)}), \quad p \in N.$$This means that $$(F^* \omega)_p (X_p) = \omega_{F(p)}(F_*(X_p))$$for all $X_p \in T_p N$. 

**Def:** Let $F: N \to M$ be a map and $h$ be a function on $M$. The *pullback* of $h$ by $F$, denoted by $F^*h$, is the composite function $F^* h := h \circ F$. This is because if $h \in \mathcal C^\infty(M)$, then $F^* h \in \mathcal C^\infty (N)$.

**Prop:** Let $F: N \to M$ be a smooth map of manifolds. For any $h \in \mathcal C^\infty(M)$, $F^*(dh) = d(F^* h)$. 

**Prop:**  Let $F: N \to M$ be a smooth map of manifolds. Suppose $\omega, \tau \in \Omega^1(M)$ and $g\in \mathcal C^\infty(M)$. Then:
- $F^*(\omega + \tau) = F^*\omega+ F^*\tau$
- $F^*(g\omega) = (F^* g)(F^*\omega)$

**Prop:** The pullback $F^* \omega$ of a smooth $1$-form $\omega$ on $M$ under a smooth map $F: N \to M$ is a smooth $1$-form on $N$. 

# Restriction of $1$-Forms to an Immersed Submanifold

**Def:** Let $S\subseteq M$ be an immersed manifold and $i: S \to M$ the inclusion map. At any point $p \in S$, since the differential $i_* :T_p S \to T_p M$ is injective, then $T_p S$ can be interpreted as subspace of $T_p M$. If $\omega$ is a $1$-form on $M$, then the *restriction* of $\omega$ to $S$ is the $1$-form $\omega|_S$ defined by $$(\omega|_S)_p(v) = \omega_p (v), \qquad p \in S, v \in T_p S.$$**Prop:** If $i:S \hookrightarrow M$ is the inclusion map of an immersed submanifold $S$ and $\omega$ is a $1$-form on $M$, then $i^* \omega = \omega|_S$. 