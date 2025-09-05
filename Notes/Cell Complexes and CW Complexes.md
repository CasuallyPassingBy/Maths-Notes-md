---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Continuous Functions and Homeomorphims]], [[Adjunction Topology]], [[Hausdorff Spaces]], [[Spheres in Rn]]

**Def:** An *open $n$-cell* is any topological space that is homeomorphic to the open unit ball $\Bbb B^n$, and a *closed $n$-cell* is any space homeomorphic to $\bar{\Bbb B}^n$. 

**Prop:** If $D\subseteq \Bbb R^n$ is a compact convex subset with nonempty interior, then $D$ is a closed $n$-cell and its interior is an open $n$-cell. In fact, given any point $p\in \text{int}(D)$, there exists a homeomorphism $F: \bar{\Bbb B^n} \to D$ that sends $0$ to $o$ and $\Bbb B^n$ to $\text{int}(D)$, and $\Bbb S^{n-1}$ to $\partial D$.

**Obs:** Let $D$ be a closed $n$-cell. Note that $D$ is a manifold with boundary. We use the notation $\partial D$ and $\text{Int}D$ to denote the images of $\Bbb S^{n-1}$ and $\Bbb B^n$, respectively under some homeomorphism $f:\bar {\Bbb B}^n \to D$. 

## Cell Decompositions

Suppose $X$ is a nonempty topological space, $\{D_\alpha \mid \alpha<\kappa\}$ is an indexed collection of closed $n$-cells for some fixed $n\ge 1$, and for each $\alpha$, we are given a continuos map $\varphi_\alpha: \partial D_\alpha \to X$. Letting $\varphi: \coprod_\alpha\partial D_\alpha \to X$ be the map those whose restrictions to each $\partial D_\alpha$ is $\varphi_\alpha$, we can form the adjunction space $$X\; \cup_\varphi \coprod_{\alpha <\kappa} \partial D_\alpha.$$

Any space homeomorphic to such an adjunction space is said to be obtained from $X$ by *attaching $n$-cells to $X$*. 

**Def:** If $X$ is a nonempty topological space, a *cell decomposition of $X$* is a partition $\cal E$ of $X$ unto subspaces that are open cells of various dimensions, such that the following condition is satisfied. For each cell $e\in \cal E$ of dimension $n \ge 1$, there exists a continuous map $\varphi_e$ from some closed $n$-cell $D$ into $X$, called the *characteristic map for $e$*, that restricts to a homeomorphism from $\text{Int}(D)$ onto $e$ and maps $\partial D$ into the union of all cells of $\cal E$ of dimension strictly less than $n$. 

**Def:** A *cell complex* is a $T_2$ space $X$ together with a specific cell decomposition of $X$. We usually write a cell complex as a pair $(X, \mathcal E)$. Given a cell complex $(X, \mathcal E)$, the open cells in $\cal E$ are typically just called *cells of $X$*. 

**Def:** A *finite cell complex* is one whose cell decomposition has only finitely many cells. A cell complex is *locally finite* if the collection of open cells is locally finite. 

# CW complexes

**Def:** Suppose $X$ is a topological space, and $\cal B$ is any family of subspaces of $X$ whose union is $X$. To say that the topology of $X$ is *coherent with $\cal B$* means that a subset $U\subseteq X$ is open in $X$ iff its intersection with each $B\in \cal B$ is open in $B$. The same applies for closed sets. 

We see that [[compactly generated]] spaces are coherent with the family of compact subsets. 

**Prop:** Suppose $X$ is a topological space whose topology is coherent with a family $\cal B$ of subspaces.
- If $Y$ is another topological space, then a map $f:X\to Y$ is continuous iff $f|_B$ is continuous for each $B\in \cal B$.
- The map $\coprod_{B\in \cal B} B \to X$ induced by the inclusion of each set $B \hookrightarrow X$ is a quotient map. 

**Def:** A *CW complex* is a cell complex $(X, \mathcal E)$ satisfying the following additional conditions:
- $(C)$ The closed of each cell is contained in a union of finitely many cells.
- $(W)$ The topology of $X$ is coherent with the family of closed subspaces $\overline{\cal E}$. 
A cell decomposition of a space $X$ satisfying the conditions above is called a *CW decomposition of $X$*. The letters $C$ and $W$ come from these two conditions: 
- condition $C$ was called *closure finiteness*.
- condition $W$ was called the [[Weak Topology|weak topology]] associated with the subspaces $\overline {\cal E}$ 

**Prop:** Let $X$ be a $T_2$ space, and let $\cal E$ be a cell decomposition of $X$. If $\cal E$ is locally finite, then it is a CW decomposition.

**Def:** Suppose $X$ is a CW complex. If there is an integer $n$ such that all of the cells of $X$ have dimension at most $n$, them we say $X$ is *finite-dimensional*; otherwise, it is *infinite-dimensional*. If it is finite dimensional, the *dimension of $X$* is the largest $b$ such that $X$ contains an at least one $n$-cell.

A finite complex is always finite dimensional.

**Def:** A CW complex of dimension less than or equal to $1$ is called a *graph*. Each $0$-cell of the complex is called a *vertex*, and each $1$-cell is called an *edge*. A graph is said to be *finite* if its associated CW complex is finite. 

**Prop:** Suppose $X$ is an $n$-dimensional CW complex. Then every $n$-cell of $X$ is an open subset of $X$. 

**Def:** A *subcomplex* of $X$ is a subspace $Y\subseteq X$ that is a union of cells of $X$, such that if $Y$ contains a cell, it also contains its closure. 

We see that the union and the intersection of any collection of subcomplexes are themselves subcomplexes.

**Def:** For each nonnegative integer $n$, we define the *$n$-skeleton of $X$* to the subspace $\text{skel}_n(X) \subseteq X$ consisting to all the cells of dimensions less than or equal to $n$; it is an $n$-dimensional subcomplex of $X$: $$\text{skel}_n(X) := \bigcup\{e\in \mathcal E\mid \dim e \le n\} $$
**Th:** Suppose $X$ is a CW complex and $Y$ is a subcomplex of $X$. Then $Y$ is closed in $X$, and with the subspace topology and the cell decomposition that it inherits from $X$ it is a CW complex. 

**Prop:** If $X$ is any CW complex, the topology of $X$ is coherent with the collection of subspaces $\{X_n \mid n \ge 0\}$.

**Def:** An open cell $e\subseteq X$ is called a *regular cell* if it admits a characteristic map that is a homeomorphism onto $\overline e$. For a regular cell, we can always take the inclusion map $\overline e \hookrightarrow X$ as a characteristic map.

**Def:** A CW complex is called a *regular CW complex* or *regular complex cell* if each of its cells is regular, and the closure of each cell is finite subcomplex. 

**Examples:** 
- We will construct a regular cell decomposition of $\Bbb S^n$. Since $\Bbb S^0$ is a finite discrete space is already a regular $0$-dimensional cell complex with two cells. We will proceed by induction. Let us suppose that we have constructed a regular cell decomposition of $\Bbb S^n$ with two cells in each dimension. Now consider $\Bbb S^n$ as a subspace of $\Bbb S^{n+1}$ (the subset where $x_{n+2} = 0$), we can see that the open upper and lower hemispheres of $\Bbb S^{n+1}$ are regular $n$-cells whose boundaries lie in $\Bbb S^{n}$. We get the regular cell decomposition of $\Bbb S^n$ with exactly two cells in each dimension $0$ through $n$. Lastly, for $k\le n$, the $k$-skeleton of this complex of $\Bbb S^k$. 
- We can decompose $\Bbb S^n$ in another way, with only one $0$-cell and $n$-cell and no others. The $0$-cell is the north pole $N= (0,\dots, 0, 1)$, and the characteristic map for the $n$-cell is map $q:\bar {\Bbb B}^n\to \Bbb S^n$ which collapses $\partial \bar{\Bbb B}^n$. 
- A regular cell decomposition of $\Bbb R$ is obtained by defining the $0$-cells to be the integers, and the $1$-cells to be intervals $(n,n+1)$ for $n \in \Bbb Z$, with characteristic maps $\varphi_n:[n, n+1] \to\Bbb R$ given by inclusion. Since the collection of cells is locally finite, then it satisfies conditions C and W.

## Topological Properties

**Th:** For a CW complex $X$, the following are equivalent.
- $X$ is path connected.
- $X$ is connected.
- The $1$-skeleton of $X$ is connected.
- Some $n$-skeleton of $X$ is connected.

**Lemma:** In any CW complex, the closure of each cell is contained in a finite subcomplex.

**Lemma:** Let $X$ be a CW complex. A subset of $X$ is discrete iff its intersection with each cell is finite. 

**Th:** Let $X$ be a CW complex. A subset of $X$ is compact iff it is closed in $X$ and contained in a finite subcomplex.

**Cor:** A CW complex is compact iff it is a finite complex.

**Prop:** A CW complex is locally compact iff it is locally finite.

## Inductive Construction

**Lemma:** Suppose $X$ is a CW complex, $\{e_\alpha \mid \alpha < \kappa\}$ is the collection of cells of $X$, and for each $\alpha <\kappa$, $\varphi_\alpha: D_\alpha \to X$ is a characteristic map for the cell $e_\alpha$. Then the map $\varphi: \coprod_{\alpha} D_\alpha \to \coprod_\alpha \overline{e}_\alpha$ whose restriction to each $D_\alpha$ is $\varphi_\alpha$ is quotient map.

**Prop:** Let $X$ be a CW complex. Each skeleton $\text{skel}_n(X)$ is obtained from $\text{skel}_{n-1}(X)$ by attaching a collection of $n$-cells.