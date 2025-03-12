---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Derivations]], [[Module and Algebra (Structure)]]

**Def:** Let $K$ be a field. A *Lie Algebra* over $K$ is a vector space $L$ over $K$ together with the product $[\;, \;]: V \times V \to K$, is called the *bracket*, satisfying the following properties: for all $a, b\in K$ and $X, Y, Z \in L$, 
- $[aX + bY, Z] = a[X, Z] + b[Y, Z]$ 
- $[Y, X] = - [X, Y]$
- $[X, [Y, Z]] + [Y, [Z, X]] + [Z, [Y, X]] = 0$  (Jacobi identity)

**Def:** A *derivation* of a Lie algebra $L$ over a field $K$ is a $K$-linear map $D: L \to L$ satisfying the product rule: $$D[Y, Z] = [DY, Z] + [Y, DZ], \quad Y, Z\in L$$
**Example:** Let $L$ be a Lie algebra over a field $K$. For each $X \in L$, we define $\text{ad}_X: L \to L$ by $\text{ad}_X(Y) = [X, Y]$. We can write the Jacobi identity as $$[X, [Y, Z]] = [[X Y], Z] + [Y, [X, Z]]$$ or as $$\text{ad}_X[Y,Z] = [\text{ad}_XY, Z]+ [Y, \text{ad}_X Z]$$
**Def:** If $L$ is a Lie algebra, and for all $X, Y \in L$ satisfies $[X, Y] = 0$, then $L$ is called an abelian Lie algebra. 

**Obs:** If $A$ is any algebra over a field $K$, then the product $$[x, y] = xy - yx, \quad x,y \in A$$ makes $A$ into a Lie algebra over $K$. 

**Def:** A *Lie subalgebra* of a Lie algebra $\frak g$ is a vector subspace $\frak h \subseteq g$ that is closed under the bracket $[\; , \;]$.  