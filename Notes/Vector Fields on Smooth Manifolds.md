---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Local and Global Sections of Vector Bundles]], [[The Tangent Bundle]], [[Vector Fields on Rn]], [[Smooth Partitions of Unity for Manifolds]], [[Derivations]], [[Lie Algebra]], [[Submersions, Immersions and Local Diffeomorphism of Smooth Manifolds]]

**Def:** A *vector field* $X$ on a manifold $M$ is a function that assigns a tangent vector $X_p \in T_p M$ to each point $p\in M$. In terms of the tangent bundle, a vector field on $M$ is simply a section of the tangent bundle $\pi: TM \to  M$ and the vector field is *smooth* if it is a smooth map from $M$ to $TM$. 

**Lemma:** Let $(U, \phi) = (U, x^1, \dots, x^n)$ be a chart on a manifold $M$. A vector field $X = X^i \dfrac{\partial}{\partial x^i}$ on $U$ is smooth iff the coefficient functions $a^i$ are all smooth on $U$.  

**Prop:** Let $X$ be a vector field on a manifold $M$. The following are equivalent:
- The vector field $X$ is smooth on $M$.
- The manifold $M$ has an atlas such that any chart $(U, \phi) = (U, x^1, \dots, x^n)$ of the atlas, the coefficients $a^i$ of $X = X^i \dfrac{\partial}{\partial x^i}$ relative to the frame $\dfrac{\partial}{\partial x^i}$ are all smooth.
- On any chart $(U, \phi) = (U, x^1, \dots, x^n)$ on the manifold $M$, the coefficients $a^i$ of $X = X^i \dfrac{\partial}{\partial x^i}$ relative to the frame $\dfrac{\partial}{\partial x^i}$ are all smooth.

**Def:** Just as for the case of [[Vector Fields on Rn]], a vector field $X$ on a manifold $M$ induces a linear map on the algebra $\mathcal C^\infty (M)$ of smooth functions on $M$; for $f \in \mathcal C^\infty (M)$, define $Xf$ to be the function $$(Xf)(p) = X_p f, \qquad p \in M$$
**Cor:** Suppose $(U, x^1, \dots, x^n)$ and $(V, \dots, y^1, \dots, y^n)$ are two charts on $M$ with nonempty overlap. Then a smooth vector field $X$ on $U\cap V$ has two different local expressions: $$X = X^i \frac{\partial}{\partial x^i} = \tilde X^i \frac{\partial}{\partial y^i}.$$Then we see that $$X^k = \tilde X^i \frac{\partial x^k}{\partial y^i}$$
**Def:** The set of all smooth vector fields on $M$ is denoted as $\Gamma(M) = \mathfrak X(M)$ or $\text{Vect}(M)$, is clearly a $\Bbb R$-vector space, and a $\mathcal C^\infty(M)$-module. 

**Cor:** We have that $\mathfrak X(M) = \text{Der}(\mathcal C^\infty (M))$, by the case of real open sets. 

**Prop (Smoothness of a vector field in terms of functions):** A vector field $X$ on $M$ is smooth iff for every smooth function $f$ on $M$, the function $Xf$ is smooth on $M$.

**Cor:** Two smooth vector fields $X$ and $Y$ on a manifold $M$ are equal iff for every smooth function $f$ on $M$, we have $Xf = Yf$. 

**Prop:** Suppose $X$ is a smooth vector field defined on a neighbourhood $U$ of a point $p$ in a manifold $M$. Then there is a smooth vector field $\tilde X$ on $M$ that agrees with $X$ on some possibly smaller neighbourhood of $p$. 

# The Lie Bracket

Just as for derivations that the composition of two derivations it is usually not a derivation, we have the same problem for vector fields.

**Def:** Given two smooth vector fields $X$ and $Y$ on $U$ and $p\in U$, we define their *Lie bracket* $[X, Y]$ at $p$ to be $$[X, Y]_p f = (X_p Y - Y_p X) f$$
**Prop:** If $X$ and $Y$ are smooth vector fields on $M$, then the vector field $[X, Y]$ is also smooth on $M$.

**Prop:** We have that $(\mathfrak X(M), [ \; , \;])$ is a real Lie algebra. 

**Prop:** If $f$ and $g$ are smooth functions and $X$ and $Y$ are smooth vector fields on a manifold $M$, then $$[fX, gY] = fg[X, Y] + f(Xg)Y - g(Yf)X$$
**Prop:** Let $X$ and $Y$ be two smooth vector fields on $M$, with coordinate expressions for $X$ and $Y$ being $$X =  X^i \frac{\partial}{\partial x ^i}, \qquad \text{and} \qquad Y =  Y^j \frac{\partial}{\partial x ^j}$$in terms of some smooth local coordinates $(x^i)$ for $M$. Then $$[X, Y] =  \left(X^i \frac{\partial Y^j}{\partial x^i} -Y^i \frac{\partial X^j}{\partial x^i}\right)  \frac{\partial}{\partial x^j}$$
# Pushforward of Vector Fields

 **Def:** Let $F: N \to M$ be a smooth map of manifolds and let $dF_p: T_p N \to T_{F(p)} M$ be its differential at a point $p \in N$. If $X_p \in T_p N$, we call $F_* (X_p) = dF_p(X_p)$ the *pushforward* of the vector $X_p$ at $p$. 
  
This notion does not extend in general to vector fields, since if $X$ is a vector field on $N$ and $z = F(p) = F(q)$ for two distinct points $p, q \in N$, then $X_p$ and $X_q$ are both pushed forward to the tangent vectors at $z\in M$, there's no reason why $F_*(X_p)$ and $F_*(X_q)$ should be equal.

**Def:** If $F: N \to M$ is a diffeomorphism, then there's no ambiguity about the meaning of $(F_* X)_{F(p)} = dF_p(X_p)$, since $F$ is surjective, $F_* X$ is defined everywhere on $M$.

**Prop:** Let $F: N \to M$ be a smooth diffeomorphism of manifolds. If $g$ is a smooth function and $X$ a smooth vector field on $N$, then $$F_*(gX) = (g \circ F^{-1}) F_* X. $$
**Prop:** Let $F: N \to M$ be a smooth diffeomorphism of manifolds. If $X$ and $Y$ are smooth vector fields on $N$, then $$F_* [X, Y] = [F_* X, F_* Y]$$
**Cor:** Let $F: N \to M$ be a smooth diffeomorphism of manifolds, then $F_*: \mathfrak X(M) \to \mathfrak X(N)$ is a Lie algebra isomorphism. 

# Related Vector Fields

**Def:** Let $F: N \to M$ be a smooth map of manifolds. A vector field $X$ on $N$ is $F$-related to a vector field $\bar X$ on $M$ if for all $p \in N$, $$dF_p(X_p) = \bar X_{F(p)}$$
**Obs:** If $F: N \to M$ is a diffeomorphism and $X$ is vector field on $N$, then the pushforward $F_*X$ is defined, and the vector field $X$ is $F$-related to $F_*X$. 

**Prop:** Let $F: N \to M$ be a smooth map of manifolds. A vector field $X$ on $N$ and vector field $\bar X$ on $M$ are $F$-related iff for all $g\in \mathcal C^\infty (M)$. $$ X(g\circ F) = (\bar X g) \circ F.$$
**Prop:** Let $F: N \to M$ be a smooth map of manifolds. If the smooth vector fields $X$ and $Y$ are $F$-related to the smooth vector fields $\bar X$ and $\bar Y$, respectively, on $M$, then the Lie bracket $[X, Y]$ on $N$ is $F$-related to the Lie bracket $[\bar X, \bar Y]$ on $M$.

**Prop:** If $\pi: M \to N$ is a submersion and $X$ is a smooth vector field on $N$, then there is a smooth vector field on $M$, called a *lift of $X$*, that is $\pi$ to $X$.

**Cor:** Suppose $\pi: M \to N$ is a surjective submersion. If $X$ is a vector field on $M$ such that $\pi_* X_p = \pi_* X_q$ whenever $\pi(p) = \pi(q)$, then there exists a unique smooth vector field on $N$ that is $\pi$-related to $X$.