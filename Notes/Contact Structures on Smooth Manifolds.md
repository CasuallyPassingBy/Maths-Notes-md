---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Symplectic Forms on Smooth Manifolds]], [[Tangent Distributions and Involutivity on Smooth Manifolds]]. [[The Lie Derivative]], [[Hamiltonian Vector Fields]]

**Def:** Suppose $M$ is a smooth manifold of odd dimension $2n+1$. A *contact form* on $M$ is a nonvanishing smooth $1$-form $\theta$ with the property that for each $p\in M$, the restriction of $d\theta_p$ to the subspace $\ker \theta_p \subseteq T_p M$ is nondegenerate, which is to say it is a symplectic tensor. A *contact structure on $M$* is a smooth distribution $H\subseteq TM$ of rank $2n$ with the property that any smooth local defining form $\theta$ for $H$ is a contact form. A *contact manifold* is a smooth manifold $M$ together with a contact structure on $M$. If $(M, H)$ is a contact manifold, any (local or global) defining form for $H$ is called a *contact form for $H$*. 

It was proved in 1971 by Jean Martinet that every oriented compact smooth $3$-manifold admits a contact structure; but the question of which higher-dimensional manifolds admit contact structure is still unresolved.

**Prop:** A smooth $1$-form $\theta$ on a $(2n+1)$-manifolds is a contact form iff $\theta\wedge d\theta^n$ is nonzero everywhere on $M$, where $d\theta^n$ represents the $n$-fold wedge product $d\theta\wedge \dots\wedge d\theta.$ 

**Prop:** Suppose $H$ is a contact structure on a smooth manifold $M$. If $\theta_1$ and $\theta_2$ are two local contact forms for $H$, then on their common domain there is a smooth nonvanishing function $f$ such that $\theta_2 = f\theta_1$. 

We see that the codimension-$1$ distribution $H\subseteq TM$ is integrable iff any local defining form $\theta$ satisfies $\theta\wedge d\theta = 0$. If $H$ is a contact structure, by contrast, not only $\theta\wedge d\theta$ nonzero everywhere on $M$, but it remains nonzero after taking $n-1$ more wedge products with $d\theta$. Thus, a contact structure is, in a sense, a 'maximally nonintegrably distribution.'

**The Reeb Field:** Let $(M, H)$ be a contact manifold, and suppose $\theta$ is a contact for $H$. There is a unique vector field $T\in {\frak X}(M)$, called the *Reeb field of $\theta$*, that satisfies the following two conditions: $$T \; \lrcorner\; d\theta = 0, \qquad \theta(T) = 1. $$
**Prop:** Let $\theta$ be a contact form and $T$ be its Reeb field. Then $\mathcal L_T\theta = 0$.  This is immediate by Cartan's Magic Formula.

**Contact Darboux Theorem:** Suppose $\theta$ is a conctact form on a $(2n+1)$-dimensional manifold $M$. For each $p\in M$, there are smooth coordinates $(x^1,\dots, x^n, y^1,\dots, y^n, z)$ centred at $p$ in which $\theta$ has the form  $$\theta = dz - \sum_{i = 1}^n y^i dx^i.$$
**Prop:** Suppose $(M, H)$ is a contact manifold and $\theta$ is a contact form for $H$. For any function $f\in \mathcal C^\infty(M)$, is a unique vector field $X_f$ called the *contact Hamiltonian vector field of $f$*, that satisfies $\theta(X_f) = f$ and $(X_f \; \lrcorner \; d\theta)|_H = -df|_H$. 

**Def:** Suppose $(M, H)$ is a contact manifold. A smooth vector field $X\in {\frak X}(M)$ is called a *contact vector field* if its flow $\theta$ preserves the contact structure, in the sense, that $d(\theta_t)_p (H_p) = H_{\theta_t(p)}$ for all $(t, p)$ in the domain of $\theta$.

**Characterisation of Contact Vector Fields:** If $(M, H)$ is a contact manifold and $\theta$ is a contact form for $H$, then a smooth vector field on $M$ is a contact vector field iff it is a contact Hamiltonian vector field.

**Def:** If $(M, H)$ is a contact manifold, a submanifold $S\subseteq M$ is said to be *isotropic* if $TS \subseteq H$, or equivalently if $\iota^*\theta  = 0$ for any contact form $\theta$, where $\iota: S \hookrightarrow M$ is inclusion. If $S\subseteq M$ is isotropic, then $\iota^*d\theta = d(\iota^*\theta) = 0$. This implies that for $p\in S$, the tangent space $T_p S$ is an isotropic subscpace of the symplectic vector space $H_p$, and thus its dimension cannot be larger than $n$, where $2n+1$ is the dimension of $M$. An isotropic submanifold of the maximum possible dimension $n$ is called *Legendrain submanifold.*

**Contact Flowout Theorem:** Suppose $(M , H)$ is a contact manifold, $F\in \mathcal C^\infty(M)$, $\Gamma$ is an embedded isotropic submanifold of $M$ that is contained in the zero set of $F$, and the contact Hamiltonian vector field $X_F$ is nowhere tangent to $\Gamma$. If $\cal S$ is a flowout from $\Gamma$ along $X_F$, then $\cal S$ is also isotropic and contained in the zero set of $H$.