---
tags:
  - DifferentialGeometry
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Homogeneous Spaces]], [[Lie Group Actions]], [[Lie Groups]]

**Def:** A smooth manifold endowed with a transitive smooth action by a group $G$ is called a a *homogeneous $G$ space*, *homogeneous space* or *homogeneous manifold.*

**Examples:**
- The natural action $\text{O}(n)$ on $\Bbb S^{n-1}$ is transitive. So is this natural action $\text{SO}(n)$ on $\Bbb S^{n-1}$ when $n \ge 2$. Thus $n \ge 2$, $\Bbb S^{n-1}$ is a homogeneous space of either $\text{O}(n)$ or $\text{SO}(n)$.
- The natural action of $\text E(n)$ on $\Bbb R^n$ is transitive. So is this natural action $\text{SE}(n)$ on $\Bbb R^n$, thus $\Bbb R^n$ is a a homogeneous space of either $\text{E}(n)$ or $\text{SE}(n)$.
- The group $\text{SL}(2, \Bbb R)$ acts smoothly and transitively on the upper half plane $\Bbb H = \{z\in \Bbb C \mid \Im z > 0\}$, by the formula $$\begin{pmatrix} a & b \\ c & d\end{pmatrix} \cdot z := \frac{az +b}{cz+d}.$$The resulting complex-analytic transformations of $\Bbb H$ are called *Möbius transformations.*
- The natural action $\text{U}(n)$ on $\Bbb S^{2n-1}$ is transitive. So is this natural action $\text{SU}(n)$ on $\Bbb S^{n-1}$ when $n \ge 2$. Thus $n \ge 2$, $\Bbb S^{2n-1}$ is a homogeneous space of either $\text{U}(n)$ or $\text{SU}(n)$.

**Homogeneous Space Construction Theorem:** Let $G$ be a Lie group and let $H$ be closed Lie subgroup of $G$. The left coset space $G/H$ has a unique smooth manifold structure such that the quotient map $\pi: G \to G/H$ is a smooth submersion. The left action of $G$ on $G/H$ given by $$g_1 \cdot (g_2 H) =(g_1g_2)H$$ turns $G/H$ into a homogeneous $G$-space.

This is mainly a corollary of the [[Lie Group Actions#^d7ed22|Quotient Manifold Theorem]]. 

**Lemma:** If $M$ is a smooth $G$-space, then for each $p\in M$, the stabiliser group $G_p$ is closed, embedded Lie subgroup of $G$. 

**Homogeneous Space Characterisation Theorem:** Let $M$ be a homogeneous $G$-space, and let $p$ be any point of $M$. Then the map $F: G/G_p \to M$ defined by $F(gG_p) = g\cdot p$ is an equivariant diffeomorphism. 

This theorem shows that the study of homogeneous spaces can be reduced to the problem of understanding closed Lie subgroups of Lie groups. 

**Examples:**
- If we consider again the natural action of $\text O(n)$ on $\Bbb S^{n-1}$. If we choose our base point to be the north pole $N= (0, \dots, 0, 1)$, then we see that the stabiliser group is $\text{O}(n-1)$, thought of as the orthogonal transformations of $\Bbb R^n$ that fix the last variable. Thus $\Bbb S^{n-1}$ is diffeomorphic to $\text O(n)/\text O(n-1)$. We get something similar for the case of $\text{SO}(n)$, and see that $\Bbb S^{n-1}$ is diffeomorphic to $\text {SO}(n)/\text {SO}(n-1)$.
- Because the group $\text E(n)$ acts smoothly and transitively on $\Bbb R^n$, and the stabiliser group of the origin is the subgroup $\text O(n)$, then $\Bbb R^n$ is diffeomorphic to $\text{E}(n)/\text{O}(n)$, and to $\text{SE}(n)/\text{SO}(n)$.
- We consider the transitive action of $\text{SL}(2, \Bbb R)$ on the upper plane by Möbius transformations. If we calculate the stabiliser of $i$, we get that it is $\text{SO}(2)$. We get the following diffeomorphism $\Bbb H \cong \text{SL}(2, \Bbb R)/\text{SO}(2)$. 
- Lastly, we get that $\Bbb S^{2n-1} \cong \text{U}(n)/\text{U}(n-1) \cong \text{SU}(n)/\text{SU}(n-1)$. 

**Obs:** Any discrete subgroup of a Lie groups is a closed zero-dimensional Lie subgroup.

**Prop:** If $G$ is a connected Lie group and $\Gamma \le G$ is a discrete subgroup, then the quotient map $\pi: G \to G/\Gamma$ is a smooth covering map.

**Prop:** The image of a Lie group homomorphism is a Lie group

**Prop:** Suppose $G$ is a Lie group.
- If $K\subseteq G$ is a closed normal Lie group, then $G/K$ is a Lie group and the quotient map $\pi: G \to G/K$ is a Lie group homomorphism.
- If $F: G \to H$ is a Lie group homomorphism, then $F$ descends to a Lie group isomorphism $\tilde F: G/\ker F \to \text{Im}(F)$. 

Meaning that we get that the true analogue of a normal subgroup for Lie groups is actually just closed normal Lie subgroups, and now we get an analogue of [[Group Homomorphisms and Isomorphisms#^ff5e58|Noether's First Isomorphism Theorem]] but for Lie groups.

**Prop:** Let $G$ and $H$ be connected Lie groups with Lie algebras $\frak g$ and $\frak h$, respectively. For any Lie group homomorphism $F: G \to H$ the following are equivalent.
- $F$ is surjective and has a discrete kernel.
- $F$ is a smooth covering map.
- The induced Lie algebra homomorphism $F_*: \frak g \to h$ is an isomorphism.
- $F$ is a local diffeomorphism.

**Prop:** Suppose $X$ is a set, and we are given a transitive action of a Lie group $G$ on $X$ such that the stabiliser group of a point $p\in X$ is a closed Lie subgroup of $G$. Then $X$ has a unique smooth manifold structure such that the given structure is smooth. 

Meaning that we can give a set a smooth structure if there's a nice enough action from a Lie group. 

**Prop:** Suppose a  Lie group $G$ acts smoothly, freely, and properly on a manifold $M$. If $G$ and $M/G$ are connected, then $M$ is connected.