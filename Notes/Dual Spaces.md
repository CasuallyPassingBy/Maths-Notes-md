---
tags:
  - LinearAlgebra
---
Subjects: [[Linear Algebra]]

Links: [[Vector Spaces]], 

Suppose that $V$ is a vector space over the field $\mathbb F$. A _linear functional from $V$ ,_ is an element from $\cal L$$(V, \Bbb F)$.

The _dual of $V$,_ denoted as $V'$ is th vector space of all linear functionals, in other words $V' = \mathcal L(V, \Bbb F)$. In other contexts, it can be written as $V^*$, or $\widetilde V$. The elements of $V'$ can be called, duals, covectors or $1$-forms, depending of the context (Linear Algebra, Physics or Differential Geometry).

If $V$ is finite dimensional, then $V'$ is also finite dimensional and ${\dim V = \dim V'}$.

If $\{v_i\}_{i\in n}$ is a basis for $V$, then the _dual basis_ of $\{v_i\}$ is the list ${\{\varphi_i\}_{i\in n} \subseteq V'}$, such that for each $\varphi_j$ has the following property: $\varphi_j(v_i) = \delta_{ij}$, the Kronecker delta.

Suppose that $V$ is finite dimensional, then the dual basis of $V'$ is a a basis for $V'$.

Let $T\in \mathcal{L}(V,W)$, then _the dual map of $T$_ is the linear map $T' \in \mathcal{L}(W', V')$, defined by $T'(\varphi) = \varphi \circ T$.

The dual map has some algebraic properties:

- Let $S, T \in \mathcal{L}(V,W)$, then $(S +T)' = S' + T'$.
- Let $T \in \mathcal L (V,W)$, and $\lambda \in\Bbb F$, then$(\lambda T)'=\lambda T'$
- Let $T \in \mathcal L (U,V)$, and $S \in \mathcal L (V,W)$, then $(ST)' = T' S'$.

Let $U \subseteq V$, *the annihilator of $U$*denoted as $U^0$, is defined as the set:
$$ U^0=\{\phi \in V' \mid \phi(U) = \{0\}\} =\{\phi \in V' \mid U \subseteq N(\phi)\} $$

Suppose that $U\subseteq V$, then $U^0$ is a subspace of $V'$.

Let $U$ and $W$ be subsets of $V$ with $U \subseteq W$, then $W^0 \subseteq U^0$.

Let $U$ and $W$ be subspaces of $V$, a finite dimensional space, with ${W^0 \subseteq U^0}$ then ${U \subseteq W}$.

Let $V$ be a finite dimensional space and $U$ a subspace of $V$.

- $U = \{0\}$ iff $U^0 =V'$
- $U = V$ iff $U^0 = \{0\}$

Suppose $U, W$ are subspaces of $V$, then ${(U+W)^0= U^0\cap W^0}$, and ${U^0+W^0\subseteq (U\cap W)^0}$
Suppose $U, W$ are subspaces of $V$,a finite dimensional space, then ${(U\cap W)^0= U^0 + W^0}$.

Let $V$ a finite dimensional vector space, and $U$ is a subspace of $V$, then:

$$ \dim V= \dim U+ \dim U^0 $$

Let $T \in \mathcal L (U,V)$ with $U$ and $V$ being finite dimensional, considering the null space and range of $T'$, we get the following results:

- $N(T')= (R(T))^0$
- $R(T') = (N(T))^0$
- $\dim N(T') = \dim N(T) + \dim W -\dim V$
- $\dim R(T') = \dim R(T)$

Let $V$ and $W$ be finite dimensional vector spaces over the field $\Bbb F$, and ${T \in \mathcal L(V, W)}$, then:

- $T$ is surjective $\iff$$T'$ is injective
- $T$ is injective $\iff$$T'$ is surjective

Let’s consider the matrix representation of $T'$, then let $V$ and $W$ be finite dimensional vector spaces with $\beta$ and $\gamma$ as their basis respectively, and $\beta'$ and $\gamma'$ be dual basis for $V'$ and $W'$ respectively. Then:
$$ [T']_{\gamma'}^{\beta'}=([T]_\beta^\gamma)^\top $$

Where $([T]_\beta^\gamma)^\top$ is the transpose of $[T]_\beta^\gamma$. Similarly it has the following algebraic properties, let $A, B\in \mathcal M_{m\times n}(\Bbb F)$, $C\in \mathcal M_{n\times p}(\Bbb F)$, and $\lambda \in \Bbb F$:

- $(A+B)^\top = A^\top + B^\top$
- $(\lambda A)^\top=\lambda A^\top$
- $(AC)^\top = A^\top C^\top$

Even though that $V \cong V'$ for finite dimensional spaces, there’s a more natural isomorphism between $V$ and $V''$. Let $V$ be finite dimensional, ${\Lambda:V \to V''}$ defined by $\Lambda(x) = \widehat x \in V''$ , and $\widehat x(f) = f(x)$, for $f\in V'$. $\Lambda$ is more natural since it doesn’t depend in choosing a basis for $V$.
Suppose that $V$ is finite dimensional and $U$ is a subspace of $V$, then

$$ \Lambda[U] = U^{00} $$
where

$$ U^{00} = \{f\in V'' \mid \forall \phi\in U^0[f(\phi) = 0]\} $$
Suppose $U$ be a subspace of $V$. Let ${\pi:V\to V/U}$ be the usual quotient map. Then $(V/U)' \cong U^0$ and $\pi'$ is the isomorphism. This independent of base and dimension.