---
tags:
  - LinearAlgebra
  - CliffordAlgebra
---
Subjects: [[Linear Algebra]], [[Clifford Algebra (Subject)]]
Links: [[Bilinear Forms]], [[Correlations, Musical Isomorphisms]]

These are special $2$-forms that play a role in many applications of smooth manifolds to analysis and physics.

**Def:** A $2$-tensor $\omega$ on a finite dimensional real vector space $V$ is said to be *nondegenrate* if $\omega(u, v) = 0$ for all $Y\in V$ implies $X = 0$. 

**Prop:** Let $\omega$ be a $2$-tensor. The following are equivalent.
- $\omega$ is non-degenerate.
- The matrix $(\omega_{ij})$ representing $\omega$ in terms of any basis is nonsingular,
- The linear map $\widehat\omega: V \to V'$ defined by $\widehat\omega(u)(v) := \omega(u, v)$ is invertible. 

A nondegenerate alternating $2$-tensor is called a *symplectic tensor*. A vector space $V$ endowed with a specific symplect tensor is called a *symplectic vector space*. A symplectiv tensor is also called a 'symplectic form' because it is in particular a bilinear form. 

**Example:** Let $V$ be a vector space of dimension $2n$. We can choose any basis for $V$, and denote the basis by $(A_1, B_1,\dots, A_n, B_n)$ and the corresponding dual basis $(\alpha^1,\beta^1,\dots, \alpha^n, \beta^n)$. Let $\omega\in \bigwedge^2(V)$ be the $2$-covector defined by  $$\omega = \sum_{i = 1}^n \alpha^i \wedge \beta^i.$$Note that the action of $\omega$ on the basis vectors is given by
- $\omega(A_i, B_j) = -\omega(B_j, A_i) = \delta_{ij}$
- $\omega(A_i, A_j) = \omega(B_i, B_j) = 0$. 

**Def:** If $(V, \omega)$ is symplectic vector space and $S\subseteq V$ is any subspace, we define the *symplectic complement* of $S$, denoted by $S^\bot$, to be subspace $$S^\bot := \{v\in V \mid \omega(v, u) = 0 \text{for all }u \in S\}. $$
We see that the symplectic complement is analogous to the orthogonal complement in an inner product space. 

**Lemma:** Let $(V, \omega)$ be a symplectic vector space. For any subspace $S\le V$, $\dim S + \dim S^{\bot} = \dim V$. 

**Prop:** Let $(V, \omega)$ be a symplectic vector field and $S\subseteq V$ be a vector subspace. Then $(S^\bot)^\bot =S$.

Symplectic complements differ from orthogonal complements in one important respect: Although it is true that $S \cap S^\bot = \{0\}$ in an inner product space, this need not be true in a symplectic vector space. 

Subspaces of $V$ can be classified in the following way. A subspace $S\subseteq V$ is said to be:
- *symplectic* if $S \cap S^\bot = \{0\}$;
- *isotropic* if $S\subseteq S^\bot$;
- *coisotropic* if $S^\bot \subseteq S$;
- *Lagrangian* if $S= S^\bot$. 

**Prop:** Let $(V, \omega)$ be a symplectic vector space, and let $S\le V$.
- $(S^\bot)^\bot = S$.
- $S$ is symplectic if $\omega|_S$ is non-degenerate.
- $S$ is isotropic iff $\omega|_S = 0$.
- $S$ is Lagrangian iff $\omega|_S = 0$ and $\dim S = (\dim V)/2$. 

The symplectic tensor defined in the example turns out to be the prototype of all symplectic tensors. This can be viewed as a symplectic version of the [[Orthogonal Bases#Gram-Schmidt Process|Gram-Schmidt process]].

**Prop:** Let $(V, \omega)$ be a symplectic vector space of dimension $2n$. Then for each symplectic, isotropic, coisotropic, or Lagrangian subspace $S\subseteq V$, there exists a basis $(A_i, B_i)$ for $V$ with the following property
- If $S$ is symplectic, $S = \text{span}\{A_1, B_1,\dots, A_k, B_k\}$ for some $k\le n$.
- If $S$ is isotropic, $S = \text{span}\{A_1,\dots, A_k\}$ for some $k\le n$.
- If $S$ is coisotropic, $S = \text{span}\{A_1,\dots, A_n, B_1,\dots, B_k\}$ for some $k\le n$.
- If $S$ is Lagrangian, $S = \text{span}\{A_1,\dots, A_n\}$. 

**Canonical Form for a Symplectic Tensor:** Let $\omega$ be a symplectic tensor on an $m$-dimensional vector space $V$. Then $V$ has an even dimension $m = 2n$, and there exists a basis for $V$ in which $\omega$ has the form $$\omega = \sum_{i = 1}^n \alpha^i \wedge \beta^i. $$
Because of this proposition, if $(V, \omega)$ is a symplectic vector space, a basis $(A_1, B_1,\dots, A_n, B_n)$ for $V$ is called a *symplectic basis* if
- $\omega(A_i, B_j) = -\omega(B_j, A_i) = \delta_{ij}$
- $\omega(A_i, A_j) = \omega(B_i, B_j) = 0$. 
hold, which is equivalent to $\omega$ being given by $\omega = \sum_{i = 1}^n \alpha^i \wedge \beta^i$ in terms of the dual basis. The proposition above tells us that every symplectic vector space has a symplectic basis.

**Prop:** Suppose $V$ is a $2n$-dimensional vector space and $\omega\in {\textstyle \bigwedge}^{\!2}(V')$. Then $\omega$ is a symplectic tensor iff $\omega^n \neq  0$. 