---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Local and Global Sections of Vector Bundles]], [[The Tangent Bundle]], [[Smooth Partitions of Unity for Manifolds]], [[Derivations]], [[Lie Algebras]], [[Submersions, Immersions and Local Diffeomorphism of Smooth Manifolds]]

**Def:** If $M$ is a smooth manifold with or without boundary, a *vector field on $M$* is a continuous section of the map $\pi: TM \to M$. More concretely, a vector field is a continuous map $X:M \to TM$, usually written $p\mapsto X_p$, with the property $$\pi \circ X = \text{id}_M,$$or equivalently, $X_p\in T_pM$ for each $p\in M$. 

We are primarily interested in *smooth vector fields,* that ones that are smooth as maps from $M$ to $TM$. In addition, for some purposes it is useful to consider maps from $M$ to $TM$ that would be a vector fields except they might not be continuous. A *rough vector field on $M$* is a map $X: M \to TM$, such that $\pi \circ X = \text{id}_M$. Just as for functions, if $X$ is a vector field on $M$, the *support of $X$* is defined to be the closure of the set $\{p\in M \mid X_p \neq 0\}$. A vector field is said to be *complactly supported* if its support is a compact set. 

Suppose $M$ is a smooth $n$-manifold with or without boundary. If $X: M \to TM$ is a rough vector field and $(U, (x^i))$ is any smooth coordinate chart for $M$, we can write the value of $X$ on $U$ in terms the coordinate basis vectors: $$X = X^i \left.\frac{\partial}{\partial x^i}\right\rvert_p. $$This defines $n$ functions $X^i:U \to \Bbb R$, called the *component functions of $X$* in the given chart.

**Smoothness Criterion for Vector Fields:** Let $M$ be a smooth manifold with or without boundary, and let $X: M \to TM$ be a rough vector field. If $(U, (x^i))$ is any smooth coordinate chart on $M$, then the restriction of $X$ to $U$ is smooth iff its component functions with respect to this chart are smooth. 

**Prop:** Let $X$ be a vector field on a manifold $M$. The following are equivalent:
- The vector field $X$ is smooth on $M$.
- The manifold $M$ has an atlas such that any chart $(U, \phi) = (U, x^1, \dots, x^n)$ of the atlas, the coefficients $X^i$ of $X = X^i \dfrac{\partial}{\partial x^i}$ relative to the frame $\dfrac{\partial}{\partial x^i}$ are all smooth.
- On any chart $(U, \phi) = (U, x^1, \dots, x^n)$ on the manifold $M$, the coefficients $X^i$ of $X = X^i \dfrac{\partial}{\partial x^i}$ relative to the frame $\dfrac{\partial}{\partial x^i}$ are all smooth.

If $M$ is a smooth manifold with or without boundary and $A \subseteq M$ is an arbitrary subset, a *vector field along $A$* is a continuous map $X: A \to TM$ satisfying $\pi \circ X = \text{id}_A$. We call it s a *smooth vector field along $A$* if for each $p\in A$, there is a neighbourhood $V$ of $p$ in $M$ and a smooth vector field $Y$ on $V$ that agrees with $X$ on $V \cap A$.

**Extension Lemma for Vector Fields:** Let $M$ be a smooth manifold with or without boundary, and let $A\subseteq M$ be a closed subset. Suppose $X$ is a smooth vector space along $A.$ Given any open subset $U$ containing $A$, there exists a smooth global vector field $Y$ on $M$ such that $Y|_A =X$ and $\text{supp } Y \subseteq U$. 

**Prop:** Let $M$ be a smooth manifold with or without boundary. Given $p\in M$ and $v\in T_pM$, there is a smooth global vector field $X$ on $M$ such that $X_p = v$.

**Cor:** Suppose $(U, x^1, \dots, x^n)$ and $(V, \dots, y^1, \dots, y^n)$ are two charts on $M$ with nonempty overlap. Then a smooth vector field $X$ on $U\cap V$ has two different local expressions: $$X = X^i \frac{\partial}{\partial x^i} = \tilde X^i \frac{\partial}{\partial y^i}.$$Then we see that $$X^k = \tilde X^i \frac{\partial x^k}{\partial y^i}.$$
**Def:** The set of all smooth vector fields on $M$ is denoted as $\Gamma(M) = \mathfrak X(M)$ or $\text{Vect}(M)$, is clearly a $\Bbb R$-vector space, and a $\mathcal C^\infty(M)$-module. 

**Prop:** If $M$ is a smooth manifold, then ${\frak X}(M)$ is a infinite dimensional vector space. 

# Local and Global Frames

**Def:** Suppose $M$ is a smooth $n$-manifold with or without boundary. An ordered $k$-tuple $(X_1,\dots,X_k)$ of vector fields defined on some subset $A\subseteq M$ is said to be *linearly independent* if $(X_1|_p,\dots, X_k|_p)$ is linearly independent $k$-tuple in $T_pM$ for each $p\in A$, and is said to *span the tangent bundle* if the $k$-tuple $(X_1|_p,\dots, X_k|_p)$ spans $T_p M$ at each $p\in A$. A *local frame for $M$* is an ordered $n$-tuple of vector fields $(E_1,\dots, E_n)$ define on an open subset $U\subseteq M$ that is linearly independent and spans the tangent bundle; thus the vectors $(E_1|_p,\dots, E_n|_p)$ form a basis for $T_p M$ at each $p\in U$. It is called a *global frame* if $U =M$, and a *smooth frame* if each of the vector fields $E_i$ is smooth. We often use the shorthand notation $(E_i)$ to denote the frame $(E_1,\dots, E_n)$. If $M$ has dimension $n,$ then to check that the ordered $n$-tuple of vector fields $(E_1,\dots, E_n)$ is a local frame, it suffices to check that either that is linearly independent or that it spans the tangent bundle.

**Completion of Local Frames:** Let $M$ be a smooth $n$ manifold with or without boundary.
- If $(X_1,\dots, X_k)$ is a linearly independent $k$-tuple of smooth vector fields on an open subset $U\subseteq M$, with $1 \le k < n$, then for each $p\in U$ there exist smooth vector fields $X_{k+1},\dots, X_n$ in a neighbourhood $V$ of $p$ such that $(X_1,\dots, X_n)$ is a smooth local frame for $M$ on $U\cap V$.
- If $(v_1,\dots, v_k)$ is linearly independent $k$-tuple of vectors in $T_p M$ for some $p\in M$, with $1\le k \le n$ then there exists a smooth local frame $(X_i)$ on a neighbourhood $p$ such that $X_i|_p$ for $i =1,\dots, k$.
- If $(X_1,\dots, X_n)$ is a linearly independent $n$-tuple of smooth vector fields along a closed subset $A\subseteq M$, then there exists a smooth local frame $(\tilde X_1,\dots, \tilde X_n)$ on some neighbourhood of $A$ such that $\tilde X_i|_A = X_i$ for $i =1,\dots, n$. 

**Def:** Let $(M, g)$ be a Riemannian manifold. A $k$-tuple of vector fields $(E_1,\dots, E_k)$ defined on some subset $A\subseteq M$ is said to be *orthonormal* if for each $p\in A$, the vectors $(E_1|_p,\dots, E_k|_p)$ is orthonormal with respect to the inner product $g(\cdot, \cdot)$. A (local or global) frame consisting of orthonormal vector fields is called an *orthonormal frame*. 

**Gram-Schmidt Algorithm for Frames:** Suppose $(M, g)$ is a Riemannian manifold and $(X_i)$ is a smooth local frame $TM$ over an open subset $U\subseteq M$. Then there id a smooth orthonormal frame $(E_j)$ over $U$ such that $\text{span} (E_1|_p,\dots, E_j|_p) = \text{span} (X_1|_p,\dots, X_j|_p)$ for $j= 1,\dots, n$ for each $p\in U$. 

# Vector Fields as Derivations of $\mathcal C^\infty(M)$

**Def:** If $X\in \mathfrak X(M)$ and $f$ is a smooth real-valued function defined on an open subset $U\subseteq M$, we obtain a new function $Xf: U\to \Bbb R$, defined by  $$(Xf)(p) = X_p f.$$Because the action of a tangent vector field on a function is determined by the values of the function in an arbitrarily small neighbourhood, it follows that $Xf$ us locally determined. In particular, for any open subset $V\subseteq U$, $$(Xf)|_V = X(f|_V).$$

**Prop.** Let $M$ be a smooth manifold with or without boundary, and let $X: M \to TM$ be a rough vector field. The following are equivalent:
- $X$ is smooth. 
- For every $f\in \mathcal C^\infty(M)$, the function $Xf$ is smooth on $M$.
- For every open subset $U\subseteq M$ and every $f\in \mathcal C^\infty(U)$, the function $Xf$ is smooth on $U$. 

One consequence of the preceding proposition is that a smooth vector field $X\in\mathfrak X(M)$ defines a map from $\mathcal C^\infty(M)$ to itself by $f\mapsto Xf$. This map is linear over $\Bbb R$. Moreover, we see that satisfies the following equality: $$X(fg) = f Xg+ g Xf,$$for all $f, g\in \mathcal C^\infty(M)$.

**Prop:** Let $M$ be a smooth manifold with or without boundary. A map $D: \mathcal C^\infty(M) \to \mathcal C^\infty(M)$ is a derivation iff is of the form $Df = Xf$ for some smooth vector field $X\in \mathfrak X(M)$. 

**Cor:** We have that $\mathfrak X(M) \cong \text{Der}(\mathcal C^\infty (M))$. 

**Prop (Smoothness of a vector field in terms of functions):** A vector field $X$ on $M$ is smooth iff for every smooth function $f$ on $M$, the function $Xf$ is smooth on $M$.

**Cor:** Two smooth vector fields $X$ and $Y$ on a manifold $M$ are equal iff for every smooth function $f$ on $M$, we have $Xf = Yf$. 

**Prop:** Suppose $X$ is a smooth vector field defined on a neighbourhood $U$ of a point $p$ in a manifold $M$. Then there is a smooth vector field $\tilde X$ on $M$ that agrees with $X$ on some possibly smaller neighbourhood of $p$. 

# The Lie Bracket

Just as for derivations that the composition of two derivations it is usually not a derivation, we have the same problem for vector fields.

**Def:** Given two smooth vector fields $X$ and $Y$ on $U$ and $p\in U$, we define their *Lie bracket* $[X, Y]$ at $p$ to be $$[X, Y]_p f = (X_p Y - Y_p X) f$$
**Prop:** If $X$ and $Y$ are smooth vector fields on $M$, then the vector field $[X, Y]$ is also smooth on $M$.

**Prop:** We have that $(\mathfrak X(M), [ \; , \;])$ is a real Lie algebra. 

**Prop:** If $f$ and $g$ are smooth functions and $X$ and $Y$ are smooth vector fields on a manifold $M$, then $$[fX, gY] = fg[X, Y] + (fXg)Y - (gYf)X$$
**Prop:** Let $X$ and $Y$ be two smooth vector fields on $M$, with coordinate expressions for $X$ and $Y$ being $$X =  X^i \frac{\partial}{\partial x ^i}, \qquad \text{and} \qquad Y =  Y^j \frac{\partial}{\partial x ^j}$$in terms of some smooth local coordinates $(x^i)$ for $M$. Then $$[X, Y] =  \left(X^i \frac{\partial Y^j}{\partial x^i} -Y^i \frac{\partial X^j}{\partial x^i}\right)  \frac{\partial}{\partial x^j}$$
**Cor:** Let $M$ be a smooth manifold. If  $(U, (x^i))$ be a chart on that manifold, then $$\left[\frac{\partial}{\partial x^i}, \frac{\partial}{\partial x^j}\right] = 0$$
**Prop:** Let $M$ and $N$ be smooth manifolds. Given a vector fields $X\in {\frak X}(M)$ and $Y\in {\frak X}(N)$, we can define a vector field $X \oplus Y$ on $M\times N$ by  $$(X\oplus Y)_{(p,q)} := (X_p, Y_q), $$where we think of the right hand side as an element of $T_p M \oplus T_q N$, which is naturally identified with $T_{p,q} (M \times N)$. Then $X \oplus Y$ is smooth, and $[X_1 \oplus Y_1, X_2\oplus Y_2] = [X_1\oplus X_2] \oplus [Y_1\oplus Y_2]$. 

# Related Vector Fields

**Def:** Suppose $F: M\to N$ is smooth and $X$ is a vector field on $M$, and suppose there happens to be a vector field $Y$ on $N$ with the property that for each $p\in M$ $dF_p (X_p) = Y_{F(p)}$. In this case, we say that the vector fields $X$ and $Y$ are $F$*-related*, 

**Prop:** Suppose $F:M \to N$ is a smooth map between manifolds with or without boundary, $X\in {\frak X}(M)$ and $Y\in {\frak X}(M)$. Then $X$ and $Y$ are $F$-related iff for every real valued function $f$ defined on an open subset of $N$,  $$X(f \circ F) = (Yf)\circ F $$
**Prop:** Suppose $M$ and $N$ are smooth manifold with or without boundary, and $F: M \to N$ is a diffeomorphism. For every $X\in {\frak X}(M)$, there is a unique smooth vector field $N$ that is $F$-related to $X$. 

In this situation we denote the unique vector field that is $F$-related to $X$ by $F_*X$, and call it the *pushforward of $X$ by $F$*. Remember, it is only when $F$ is a diffeomorphism that $F_*X$ is defined. The explicit formula of $F_*X$ is $$(F_* X)_q := dF_{F^{-1}(q)}(X_{F^{-1}(q)}). $$As long as the inverse map $F^{-1}$ can be computed explicitly, the pushforward of a vector field can be computed from this formula. 

**Cor:** Suppose $F: M \to N$ is a diffeomorphism and $X\in {\frak X}(M)$. For any $f\in {\cal C}^\infty (N)$, $$((F_* X)f)\circ F = X(f\circ F). $$

**Prop:** Let $F: N \to M$ be a smooth diffeomorphism of manifolds. If $g$ is a smooth function and $X$ a smooth vector field on $N$, then $$F_*(gX) = (g \circ F^{-1}) F_* X. $$

**Prop:** Let $F: N \to M$ be a smooth map of manifolds. If the smooth vector fields $X$ and $Y$ are $F$-related to the smooth vector fields $\bar X$ and $\bar Y$, respectively, on $M$, then the Lie bracket $[X, Y]$ on $N$ is $F$-related to the Lie bracket $[\bar X, \bar Y]$ on $M$.

**Prop:** Let $F: N \to M$ be a smooth diffeomorphism of manifolds. If $X$ and $Y$ are smooth vector fields on $N$, then $$F_* [X, Y] = [F_* X, F_* Y]$$
**Cor:** Let $F: N \to M$ be a smooth diffeomorphism of manifolds, then $F_*: \mathfrak X(M) \to \mathfrak X(N)$ is a Lie algebra isomorphism. 

**Prop:** Let $M$ be a smooth manifold with or without boundary, and $N$ be a smooth manifold, and let $f:M \to N$ be a smooth map. If $F: M \to M \times N$ by $F(x) := (x, f(x)),$ then for every $X\in {\frak X}(M)$, there is a smooth vector fields on $M\times N$ that is $F$-related to $X$

**Def:** Suppose $F: M \to N$ is a smooth submersion, where $M$ and $N$ are positive dimensional smooth manifolds. Given $X\in {\frak X}(M)$ and $Y\in {\frak}(N)$, we say that $X$ is the *lift of $Y$* if $X$ and $Y$ are $F$-related. A vector field $V\in {\frak X}(M)$ is said to be *vertical*, if $V$ is everywhere tangent to the fibres of $F$, or equivalently, if $V$ is $F$-related to the zero vector field on $N$. 

**Properties of Lifts:** Let $F: M \to N$ be a smooth submersion between manifold, where $M$ and $N$ are positive dimensional manifolds.
- If $\dim M = \dim N$, then every smooth vector field on $N$ has a unique lift. 
- If $\dim M \neq \dim N$, then $\dim M >\dim N$, then every smooth vector field on $N$ has a lift, but that is not unique.
- If $F$ is surjective, and given $X\in {\frak X}(M)$ is a lift of a smooth vector field on $N$ iff $dF_p (X_p) = dF_q(X_q)$ whenever $F(p)= F(q)$. Additionally, then $X$ is a lift of a *unique* smooth vector field.
- If $F$ is a surjective and with connected fibres, then a vector field $X\in {\frak X}(M)$ is a lift of a smooth vector field on $N$ iff $[V, X]$ is vertical whenever $V\in {\frak X}(M)$ is vertical. 
