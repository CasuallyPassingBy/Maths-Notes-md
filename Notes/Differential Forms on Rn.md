---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links:[[Tangent Vectors in Rn]], [[Vector Fields on Rn]], [[Dual Vector Spaces]], [[Exterior Algebra of Multicovectors]], [[Multi-index notation]]

# Differential $1$-forms

**Def:** The *cotangent space* to $\Bbb R^n$ at $p$, denoted by $T_p^*(\Bbb R^n)$ or $T_p^*\Bbb R^n$, is defined to be the dual space $(T_p\Bbb R^n)'$ of the tangent space $T_p(\Bbb R^n)$. In parallel with the definition of a [[Vector Fields on Rn|vector field]], a *covector field* or a *differential $1$-form* on an open subset $U$ of $\Bbb R^n$ is a function $\omega$ that assigns to each $p \in U$ a covector $\omega_p \in T_p^*(\Bbb R^n)$, $$\omega: U \to \bigcup_{p \in U} T^*_p(\Bbb R^n)$$Note that in the union $\bigcup_{p\in U} T^*_p(\Bbb R^n)$, the sets $T^*_p(\Bbb R^n)$ are all disjoint. We call a differential $1$-form a $1$*-form* for short.

From any $f\in \mathcal C^\infty(U)$ we can construct a $1$-form $df$, called the *differential of $f$*, as follows. For $p\in U$ and $X_p \in T_p U$, we defines $$(df)_p X_p := X_p f$$
The directional derivative of a function in the direction of a tangent vector at a point $p$ sets up a bilinear pairing: $$\begin{align*}T_p(\Bbb R^n) \times \; & \mathcal C_p^\infty (\Bbb R^n) \to \Bbb R  \\ &(X_p, f) \mapsto \langle X_p, f\rangle = X_p f\end{align*}$$
The tangent vector can be though of as a function of the second argument of the pairing: $\langle X_p, \;\cdot \;\rangle$. The differential $(df)_p$ at $p$ is function on the first argument of the pairing: $(df )_p = \langle \; \cdot \;, f\rangle$ 

**Prop:** If $x^1, \dots, x^n$ be the standard coordinates of $\Bbb R^n$, then at each point $p\in \Bbb R^n$, $\{(dx^1)_p, \dots, (dx^n)_p\}$ is the basis for the cotangent space $T_p (\Bbb R^n)$ dual to the basis $\left\{\left.\dfrac{\partial}{\partial x^1}\right\rvert_p, \dots, \left.\dfrac{\partial}{\partial x^n}\right\rvert_p\right\}$  for the tangents space $T_p(\Bbb R^n)$. 

If $\omega$ is a $1$-form on an open subset $U$ of $\Bbb R^n$, then at each point $p\in U$, we can write as a linear combination: $\omega_p = \sum a_i(p) (dx^i)_p$ for some $a_i(p)\in \Bbb R$. Similarly as we did for vector fields. The coefficients are functions on $U$ and we may write $$\omega = a_i dx^i$$
The covector field $\omega$ is said to be $\mathcal C^\infty$ if all the coefficient functions $a_i$ are $\mathcal C^\infty$ on $U$. 

**Prop:** If $f: U \to \Bbb R$ is a $\mathcal C^\infty$ function on an open set $U$ in $\Bbb R^n$, then $$df = \frac{\partial f}{\partial x^i} dx^i$$
# Differential $k$-forms

**Def:** More generally, a *differential form $\omega$ of degree $k$* of a $k$-form on an open subset $U$ of $\Bbb R^n$ is a function that assigns to each point $p$ in $U$ an alternating $k$-covector of the tangent space $T_p(\Bbb R^n)$, i.e., $\omega_p \in A_k(T_p\Bbb R^n; \Bbb R)$. 

We know that the basis for $A_k(T_p\Bbb R^n)$ is $$dx^I_p = dx_p^{i_1}\wedge \dots \wedge dx_p^{i_k}, \quad 1 \le i_1 < \dots < i_k \le n$$Therefore, a $k$-form $\omega$ on $U$ is a linear combination $$\omega_p = a_I dx^I$$with function coefficients $a_I : U \to \Bbb R$. We say that a $k$-form $\omega$ on $U$ is $\mathcal C^\infty$ if all the coefficients $a_I$ are $\mathcal C^\infty$ functions on $U$. 

**Def:** We denote by $\Omega^k(U)$ the vector space of $\mathcal C^\infty$ $k$-forms on $U$. A $0$-form on $U$ assigns to each point $p \in U$ an element of $A_0(T_p \Bbb R) = \Bbb R$. Thus, a $0$-form on  $U$ is simply a function $U$, and $\Omega^0(U) = \mathcal C^\infty(U)$. 

**Def:** The *wedge product* of a $k$-form $\omega$ and an $\ell$-form $\tau$ on an open set $U$ is defined pointwise: $$(\omega\wedge \tau)_p = \omega_p \wedge\tau_p, \quad p \in  U$$In terms of coordinates, if $\omega = \sum a_I dx^I$ and $\tau = b_J dx^J$, then $$\omega \wedge \tau =  (a_I b_J) dx^I \wedge dx^J$$
As a consequence, we have that the wedge product of two $\mathcal C^\infty$ forms is $\mathcal C^\infty$, and that the wedge product is a bilinear map: $$\wedge: \Omega^k (U) \times \Omega^\ell (U) \to \Omega^{k + \ell}(U)$$
The wedge product is anitcommutative and associtative. 

With the wedge product as multiplication and the degree of a form as the grading, and the direct sum $$\Omega^*(U) = \bigoplus_{k = 0}^\infty \Omega^k(U)$$becomes an anticommutative graded algebra over $\Bbb R$. Since one multiply $\mathcal C^\infty$ $k$-form by $\mathcal C^\infty$ functions, the set $\Omega^k(U)$ of is both a vector space over $\Bbb R$ and a module over $\mathcal C^\infty(U)$, and $\Omega^*(U)$ is also a module over the ring $\mathcal C^\infty(U)$. 

For the case of $\omega \in \Omega^1(U)$ and $X \in \mathfrak X(U)$, then we can write them in their coordinates: $\omega = \sum a_i dx^i$ and $X = \sum b^j \dfrac{\partial}{\partial x^j}$ so $$\omega(X) = a_i b^i$$
which shows that $\omega(X) \in \mathcal C^\infty(U)$. The only thing to note is that $\omega$ is linear over the ring $\mathcal C^\infty$, meaning that if $f\in \mathcal C^\infty(U)$, then $\omega(fX) = f\omega(X)$. 

