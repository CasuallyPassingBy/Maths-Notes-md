---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Derivations]], [[Module and Algebra]]

**Def:** Let $K$ be a field. A *Lie Algebra* over $K$ is a vector space $L$ over $K$ together with the product $[\;, \;]: V \times V \to K$, is called the *bracket*, satisfying the following properties: for all $a, b\in K$ and $X, Y, Z \in L$, 
- $[aX + bY, Z] = a[X, Z] + b[Y, Z]$ 
- $[Y, X] = - [X, Y]$
- $[X, [Y, Z]] + [Y, [Z, X]] + [Z, [Y, X]] = 0$  (Jacobi identity)

**Def:** A *derivation* of a Lie algebra $L$ over a field $K$ is a $K$-linear map $D: L \to L$ satisfying the product rule: $$D[Y, Z] = [DY, Z] + [Y, DZ], \quad Y, Z\in L$$
**Example:** Let $L$ be a Lie algebra over a field $K$. For each $X \in L$, we define $\text{ad}_X: L \to L$ by $\text{ad}_X(Y) = [X, Y]$. We can write the Jacobi identity as $$[X, [Y, Z]] = [[X Y], Z] + [Y, [X, Z]]$$ or as $$\text{ad}_X[Y,Z] = [\text{ad}_XY, Z]+ [Y, \text{ad}_X Z]$$
**Def:** If $L$ is a Lie algebra, and for all $X, Y \in L$ satisfies $[X, Y] = 0$, then $L$ is called an abelian Lie algebra. 

**Obs:** If $A$ is any algebra over a field $K$, then the product $$[x, y] = xy - yx, \quad x,y \in A$$ makes $A$ into a Lie algebra over $K$. 

**Def:** A *Lie subalgebra* of a Lie algebra $\frak g$ is a vector subspace $\frak h \subseteq g$ that is closed under the bracket $[\; , \;]$.  

**Prop:** Given $K$-Lie algebras $\frak g$ and $\frak h$, then the direct sum $\frak g \oplus h$ is a Lie algebra with the bracket defined by $$[(X, Y),(X', Y')] := ([X, X'], [Y, Y']). $$

**Def:** Let $\frak g$ be a Lie algebra. A vector subspace $\frak h \le g$ is a called an *ideal of $\frak g$* if $[X, Y]\in \frak h$ whenever $X\in \frak h$ and $Y\in \frak g$.

**Basic Properties of Ideals:** 
- It $\frak h$ is an ideal in $\frak g$, then the quotient space $\frak g/h$ has a unique Lie algebra structure such that the projection $\pi: \frak g\to g/h$ is a Lie algebra homomorphism.
- A subspace $\frak h \le g$ is an ideal iff it is the kernel of a Lie algebra homomorphism. 

This is directly analogous to idea of an [[Ring Ideals and Quotient Rings|ideal in rings]]. 

**Def:** If $\frak g$ is a Lie algebra, the *centre of $\frak g$* is the set of all $X\in {\frak g}$ such that $[X, Y] = 0$ for all $Y\in \frak g$. 