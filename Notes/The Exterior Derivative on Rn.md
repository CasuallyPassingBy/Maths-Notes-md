---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Derivations]], [[The Gradient]], [[Stokes Theorem and Curl in R3]], [[Gauss's Theorem and Divergence in R3]]

To define the *exterior derivative* of a $\mathcal C^\infty$ $k$-form, we first define it for $0$-forms: the exterior derivative of $f \in \mathcal C^\infty (U)$ is defined to be the differential form $df \in \Omega^1(U)$, in terms of it's coordinates: $$df =  \frac{\partial f}{\partial x^i} dx^i$$
**Def:** For $k \ge 1$, if $\omega = \sum a_I dx^I \in \Omega^k(U)$, then $$d\omega =  da_I \wedge dx^I = \left(  \frac{\partial a_I}{\partial x^j}dx^j\right) \wedge dx^I \in \Omega^{k+1}(U)$$

**Prop:** 
- The exterior differentiation $d: \Omega^*(U) \to \Omega^*(U)$ is an [[Derivations#Graded Derivations|antiderivation]] of degree $1$: $$d(\omega \wedge \tau) = (d\omega) \wedge \tau + (-1) ^{\deg \omega} \omega \wedge d\tau$$
- $d^2 =0$
- If $f\in C^\infty(U)$ and $X \in \mathfrak (U)$ then $(df)(X) = Xf$

**Characterisation of the exterior derivative:** The three properties of the proposition above is uniquely characterise exterior differentiation on an open set $U$ in $\Bbb R^n$; that is, if $D:\Omega^*(U) \to \Omega^*(U)$ is
- An antiderivation of degree $1$
- $D^2 = 0$
- $(Df) (X) = Xf$ for $f\in C^\infty(U)$ and $X\in \mathfrak X(U)$
Then $D = d$.

# Closed and Exact Forms

**Def:** A $k$-form $\omega$ is *closed* if $d\omega = 0$; it is *exact* if there is a $(k-1)$-form $\tau$ such that $\omega = d\tau$ on $U.$ Since $d(d\tau) = 0$, every exact form is closed. 

**Def:** A collection of vector spaces $\{V_k \mid k < \omega\}$ with linear maps $d_k : V_k \to V_{k+1}$ such that $d_{k+1} \circ d_k = 0$ is called a *differential complex* or a *cochain complex*. For any open subset $U$ of $\Bbb R^n$, the exterior derivative $d$ makes the vector space $\Omega^*(U)$ into a cochain complex, called the *de Rham complex* of $U$: $$0 \longrightarrow \Omega^0(U) \stackrel{d}{\longrightarrow} \Omega^1(U) \stackrel{d}{\longrightarrow} \Omega^2(U) \stackrel{d}{\longrightarrow} \cdots$$The closed forms are precisely the elements of the kernel of $d$, and exact forms are the elements of the image of $d$. 

# Applications to Vector Analysis

In particular for every $\Bbb R^3$, we have that: 

Since every $1$-form on $U$ is a linear combination with function coefficients $dx$, $dy$ and $dz$, we can identify $1$-forms with vector fields on $U$ via $$P dx+ Qdy + Rdz \longleftrightarrow \begin{bmatrix}P \\ Q \\ R\end{bmatrix}$$
Similarly, $2$-forms on $U$ can also be identified with vector with vector fields on $U$: $$P dy \wedge dz + Qdx \wedge dz + dx \wedge dy \longleftrightarrow \begin{bmatrix}P \\ Q \\ R\end{bmatrix}$$and $3$-forms on $U$ can be identified with functions on $U$: $$f dx\wedge dy \wedge dz \longleftrightarrow f$$
In terms of these identifications, the exterior derivative of a $0$-form $f$ is: $$df = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy+ \frac{\partial f}{\partial z} dz \longleftrightarrow \text{grad } f$$
the exterior derivative of $1$-form is $$d(P dx+ Qdy + Rdz) = (R_y -Q_z) dy\wedge dz - (R_x - P_z)dz \wedge dx + (Q_x - P_y) dx\wedge dy $$this corresponds to the curl of $(P, Q, R)$.

The exterior derivative of a $2$-form is $$d(P dy\wedge dz + Q dz\wedge dx + R dx \wedge dy) = (P_x + Q_y + R_z) dx \wedge dy \wedge dz$$which corresponds to the divergence of $(P, Q, R)$.

Thus, after this identifications, the exterior derivatives $d$ on $0$-forms, $1$-forms, $2$-forms are simply the three operators: $\text{grad}, \text{curl}$, and $\text{div}$. In summary, on an open subset $U$ of $\Bbb R^3$, there are identifications:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts}
\usepackage{amsmath}
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\Omega^0(U) \arrow[d, "\simeq"'] \arrow[r, "d"] & 
\Omega^1(U) \arrow[d, "\simeq"'] \arrow[r, "d"] &
\Omega^2(U) \arrow[d, "\simeq"'] \arrow[r, "d"]  &
\Omega^3(U) \arrow[d, "\simeq"'] \\
\mathcal C^\infty(U) \arrow[r, , "\text{grad}"] & 
\mathfrak{X}(U) \arrow[r, , "\text{curl}"]& 
\mathfrak{X}(U) \arrow[r, , "\text{div}"]& 
\mathcal C^\infty(U)
\end{tikzcd}
\end{document}
```

From this commutative diagram we get some properties for free:
- $\text{curl }(\text{grad } f) = 0$ 
- $\text{div }(\text{curl } f) = 0$