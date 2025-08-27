---
tags:
  - GroupTheory
  - DifferentialGeometry
---
Subjects: [[Group Theory]], [[Differential Geometry]]
Links: [[Smooth or Differentiable Manifolds]], [[Smooth Functions on Smooth Manifolds]], [[Topological Groups]], [[Submersions, Immersions and Embeddings of Manifolds]]

**Def:** A *Lie group* is a $\mathcal C^\infty$ $G$ having a group structure such that the multiplication map: $$\mu : G\times G \to G, \qquad \mu(g,h)= gh $$and the inverse map $$\iota: G\to G, \qquad \iota(g)= g^{-1} $$ are both $\mathcal C^\infty$. 

**Def:** For $g \in G$, denote $\ell_g: G \to G$, $\ell_g(x) = \mu(g, x) = gx$, the operation of *left multiplication by $g$*, and $r_g: G \to G$, $r_a(x) = \mu(x, a) = xa$, the operation of the *right multiplication by $a$*. We also call left and right multiplications *left and right translations*. 

An important examples are:
- [[General Linear Group]]
- [[Special Linear Group]]
- [[Orthogonal Group]]
- [[Unitary Group]]
- [[symplectic group]]

**Prop:** For any $g \in G$ in a Lie group, then $\ell_g: G \to G$ is a diffeomorphism. 

**Prop:** The Cartesian product $G_1 \times G_2$ of two Lie groups $(G_1, \mu_1)$ and $(G_2, \mu_2)$ is a Lie group under coordinatewise multiplication $\mu_1 \times \mu_2$.

**Def:** A map $F: H \to G$ between two Lie groups $H$ and $G$ is a *Lie group homomorphism* if its a smooth map and a group homomorphism. 

The group homomorphism condition means that for all $g, h\in H$, $F(gh) = F(g)F(h)$. This can be written functionally as $F\circ \ell_g = \ell_{F(g)} \circ F$. 

**Cor:** The image of a Lie group homomorphism is a Lie group. 

**Def:** The *identity component $G_0$* of a Lie group $G$ is the connected component of the identity element $e$ in $G$. 

**Prop:** We have that $G_0$ is a normal Lie subgroup. 

**Def:** The quotient group $G/G_0$ is called the *component group* of $G$. Its elements are the connected component of $G$.

**Prop:** An open subgroup $H$ of a connected Lie group $G$ is equal to $G$.

Since $\mu$ and $\iota$ are $\mathcal C^\infty$ we can calculate the differential at $(e,e)$, $(a, b)$ and $e$, $a$ respectively, we get that for $X_e, Y_e\in T_e G$. 
- Then $d \mu_{(e, e)}: T_e G \times T_e G \to T_e G$ is $d\mu_{(e,e)} (X_e, Y_e) = X_e+ Y_e$. 
- Then $d \mu_{(a, b)}: T_a G \times T_b G \to T_ab G$ is $d\mu_{(a,b)} (X_a, Y_b) = d(r_b)_aX_a+ d(\ell_a)_b Y_b$
- Then $d\iota_e: T_e G \to T_e G$ is $d\iota_e (X_e) = -X_e$. 
- Then $d\iota_a: T_a G \to T_{a^{-1}} G$ is $d\iota_a (X_a) = -d(r_{a^{-1}})_e d(\ell_{a^{-1}})_a X_a$. 

**Prop:** Every Lie group is *parallelisable*.

We see know that $\ell_g: G\to G$ is a diffeomorphism with inverse $\ell_{g^{-1}}$. The diffeomorphism $\ell_g$ maps $e\mapsto g$, and induces an isomorphism of tangent spaces: $$d(\ell_g)_e = \ell_{g*}: T_e G \to T_g G$$Thus, if we can describe the tangent space $T_e G$ at the identity, then $\ell_g*[T_e G]$ will give a description of the tangent space $T_g G$ at any point $g\in G$. 

This gives rise to the concept of a [[Lie Algebra of a Lie Group]]

**Prop:** Let $F: G \to H$ be a Lie group homomorphism. The kernel of $F$ is an embedded Lie group of $G$, whose codimension is equal to the rank of $F$. 

**Existence of a Universal Covering Group:** Let $G$ be a connected Lie group. There exists a simply connected Lie group $\tilde G$ (called the universal covering group of $G$) and a smooth covering map $\pi: \tilde G\to G$ that is also a Lie group homomorphism.