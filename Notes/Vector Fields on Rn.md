---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Tangent Vectors in Rn]], [[Derivations]]

**Def:** A *vector field* $X$ on an open subset $U\subseteq \Bbb R^n$ is a function that assigns to each point $p$ in $U$ a tangent vector $X_p \in T_p(\Bbb R^n)$. Meaning that $$X: U \to \bigcup_{p\in U} T_p(\Bbb R^n)$$Note that in the union $\bigcup_{p\in U} T_p(\Bbb R^n)$, the sets $T_p(\Bbb R^n)$ are all disjoint. Since $T_p(\Bbb R^n)$ has a basis $\left\{\left.\dfrac{\partial}{\partial x^i}\right\rvert_p\right\}$ , the vector $X_p$ is a linear combination: $$X_p = \sum a^i(p) \left.\frac{\partial}{\partial x^i}\right\rvert_p$$ Omitting $p$, we may write $X = \sum a^i\dfrac{\partial}{\partial x^i}$, where $a^i$ are now functions on $U$. We say that the vector field $X$ is $\mathcal C^\infty$ *on $U$* if each coefficient functions $a^i$ are all $\mathcal C^\infty$ on $U$. 

We can identify vector fields on $U$ with column vectors of $\mathcal C^\infty$ functions on $U$: $$X = \sum a^i \frac{\partial}{\partial x^i} \longleftrightarrow \langle a^1, \dots, a^n\rangle$$
Multiplication of vector fields by functions on $U$ is defined pointwise: $$(f X)_p = f(p) X_p, \qquad p \in U$$
then we get that $fX = \sum (fa^i) \dfrac{\partial}{\partial x^i}$ is a $\mathcal C^\infty$ vector field. The set of all $\mathcal C^\infty$ vector fields on $U$, denoted by $\mathfrak X(U)$ or as $\text{Vect}(U)$, is not only a vector space over $\Bbb R$, but also a [[Module and Algebra (Structure)|module]] over the ring $\mathcal C^\infty(U)$. 

## Derivations

If $X$ is a $\mathcal C^\infty$ vector field on an open subset $U$ of $\Bbb R^n$ and $f$ is a $\mathcal C^\infty$ function we define a new function $Xf$ on $U$ by $$(Xf) (p) = X_p f, \qquad p \in U$$
writing $X = \sum a^i \dfrac{\partial}{\partial x^i}$, then $$(Xf)(p) = \sum a^i \frac{\partial f}{\partial x^i}(p)$$or $$Xf = \sum a^i \frac{\partial f}{\partial x^i}$$which shows that $Xf \in \mathcal C^\infty(U)$. Thus, a $\mathcal C^\infty$ vector field $X$ gives rise to an $\Bbb R$-linear map: $X: \mathcal C^\infty(U) \to \mathcal C^\infty(U)$. 

**Leibniz rule for a vector field:** If $X$ is a $\mathcal C^\infty$ and $f, g\in \mathcal C^\infty(U)$, then $X(fg)$ satisfies the *Leibniz Rule*: $$X(fg)  = (Xf) g+ f(Xg)$$
We have a map: $\varphi: \mathfrak X(U) \to \text{Der}(\mathcal C^\infty(U))$ then $X \mapsto (f \mapsto Xf)$. 

Thus we have that $\mathfrak X(U) \subseteq \text{Der}(\mathcal C^\infty(U))$, meaning that the set of all smooth vector fields are a $\mathcal C^\infty(U)$-submodule of $\text{Der}(\mathcal C^\infty (U))$. 

**Key Lemma:** Let $D \in \text{Der}(\mathcal C^\infty(U))$, $f\in \mathcal C^\infty(M )$, and suppose that $V$ is an open set such that $f|_V = 0$, then $(Df)|_V = 0$. 

**Cor:** Let $D \in \text{Der}(\mathcal C^\infty(U))$, $f\in \mathcal C^\infty(U)$,and $p\in M$. Then $(Df)(x)$ only depends on $D$ and the germ $[f]_p \in \mathcal C^\infty_p(U)$. 

**Def:** Given $D \in \text{Der}(\mathcal C^\infty(U))$, and $p\in M$, $D_x: \mathcal C^\infty_p(U) \to \Bbb R$ is given by $$D_p([f]_p) = (Df)(x)$$where $f\in \mathcal C^\infty_p(U)$. 

**Prop:** If Let $D \in \text{Der}(\mathcal C^\infty(U))$, and $p\in M$, then $D_p \in T_p M$.

**Th:** The equality $\mathfrak X(U) = \text{Der}(\mathcal C^\infty(U))$. Means that every derivation of $\mathcal C^\infty (U)$ is a smooth vector field and viceversa.

Just as tangent vectors at a point $p$ can de identified with the point-derivations of $\mathcal C_p^\infty$, so the vector fields on the open subset $U$ can be identified with the derivations of the algebra $\mathcal C^\infty(U)$: meaning that $\varphi$ is a vector space isomorphism. 