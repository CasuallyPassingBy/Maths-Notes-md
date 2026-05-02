---
tags:
  - FunctionalAnalysis
---
Subjects: [[Linear Algebra]], [[Functional Analysis]]
Links: [[Lattices]], [[Vector Spaces]], [[Orderings]], [[Pre-orderings]], [[Ordered Groups]], [[Ordered Vector Spaces]], [[Ordered Fields]]

**Def:** A *preordered vector lattice* is a preordered vector space $E$ in which every pair of elements has a supremum. More explicitely, a *preordered vector lattice* is a vector space endowed with a preorder, $\le$, such that $x, y, z\in E$:
1. *Translation invariance:* If $x\le y$, then $x+z \le y+z$.
2. *Positive Homogeneity:* For any scalar $0 \le a$, if $x\le y$, then $ax\le ay$.
3. For any two vectors $x, y\in E$, there exists a supremum, denoted $x\vee y$, in $E$ with respect to the $\le$-preorder.
The preorder, together with conditions $1.$ and $2.$, which make it compatible with the vector  space structure, maje $E$ a preordered vector space. Condition $3.$ says that the preorder is a join semilattice. 

**Prop:** The following conditions are equivalent for a preordered vector space $E$.
- $E$ is a preordered vector lattice.
- For any $x, y\in E$, their supremum exists in $E$.
- For any $x,y\in E$, their infimum exists in $E$.
- For any $x,y\in E$, their infimum and supremum exist in $E$.
- For any $x\in E$, $\sup \{x, 0\}$ exists in $E$.

**Def:** A *Riesz space* or a *vector lattice* is a preordered vector lattice whose preorder is a partial order. Meaning, that it is an [[Ordered Vector Spaces|ordered vectors space]] for which the ordering is a lattice. 

**Prop:** If $E$ is an ordered vector space over $\Bbb R$ whose positive cone $C$ is such that $E = C-  C$, and if for every $x, y\in C$ either $\sup\{x, y\}$ or $\inf\{x, y\}$ exist, then $E$ is a vector lattice. 

**Examples:**
- Let $X$ be a topological space, then $\mathcal C(X)$ is a Riesz space.
- If $(X, {\scr A}, \mu)$ be a measure space, then $L^p(X, {\scr A}, \mu, \Bbb R)$ for $1\le p \le \infty$ are Riesz spaces.