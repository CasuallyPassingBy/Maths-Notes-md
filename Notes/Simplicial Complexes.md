---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Cell Complexes and CW Complexes]], [[Affine Spaces of Rn]], [[Convex Hulls]]

**Def:** Let $\{v_0, \dots, v_k\}$ be an affinely independent set of $k+1$ points in $\Bbb R^n$. The *simplex*, spanned by them, denoted by $[v_0, \dots, v_k]$, is the set $$[v_0,\dots, v_k] := \left\{\left.\sum_{i = 0}^k t_i v_i \; \right \rvert\; t_i \ge 0 \land \sum_{i = 1}^k t_i \right\},$$with the subspace topology. For any point $x = \sum_{i = 0}^k t_i v_i\in [v_0, \dots, v_k]$, the numbers $t_i$are called the *barycentric coordinates of $x$* with respect to $[v_0, \dots, v_k]$. Each of the points $v_i$ is called a *vertex* of the simplex. The integer $k$ is called its *dimension*; a $k$-dimensional simplex is often called a *$k$-simplex*. 

**Def:** Let $\Delta_k := [e_0, \dots, e_k] \subseteq \Bbb R^k$, where $e_0 = 0$, and $e_i$ is the standard basis. We call $\Delta_k$ the *standard $k$-simplex*. 

**Obs:** We see that $[v_0, \dots, v_k] = \text{conv}(v_0, \dots, v_k)$, meaning that the $[v_0, \dots, v_k]$ is the convex hull of its vertices. 

**Prop:** Every $k$-simplex is a closed $k$-cell. This is because every $k$-simplex is homeomorphic to the standard $k$-simplex, and the standard $k$-simplex is a closed $k$-cell.

**Def:** Let $\sigma$ be a $k$-simplex. Each simplex spanned by a nonempty subset of vertices of $\sigma$ is called a *face of $\sigma$*. The faces that are not equal to $\sigma$ itself acre called its *proper faces*. The $0$-dimensional faces of $\sigma$ are just its vertices, and the $1$-dimensional faces are called its *edges.* The $(k-1)$-dimensional faces of a $k$-simplex are called its *boundary faces*. 

We define the *boundary of $\sigma$* to be the union of its boundary faces, which is equal to the union of all its proper faces, and it is is equal to its manifold boundary. Since the boundary of $\sigma$ as a simplex is the same as the one as a manifold, we can use the notation $\partial \sigma$ without fear of confusion. Additionally, we define the *interior of $\sigma$* to be $\sigma \setminus \partial \sigma$. 

An *open $k$-simplex* is the interior of a $k$-simplex. It consists of the set points with positive barycentric coordinates. 

**Def:** A (Euclidean) *simplicial complex* is a collection $K$ of simplices if some Euclidean space $\Bbb R^n$, satisfying the following conditions.
- If $\sigma \in K$, then every face of $\sigma$ is in $K$.
- The intersection of any two simplices in $K$ is either empty or a face of each.
- $K$ is a locally finite collection.
If $K$ is a simplicial complex in $\Bbb R^n$, the *dimension of $K$* is defined to be the maximum of the simplices in $K$; it is obviously no greater than $n$. A subset $L \subseteq K$ is said to be a *subcomplex of $K$* if whenever $\sigma \in L$, every face of $\sigma$ is in $L$. 

Note that a subcomplex is a simplicial complex on its own. 

For any $k \le n$, the set of all simplices of $K$ of dimension of at most $k$ is subcomplex called the *$k$-skeleton of $K$*, denoted as $\text{skel}_k(K)$.

Given a simplicial complex $K$ in $\Bbb R^n$, the union of all the simplices in $K$, with the subspace topology inherited from $\Bbb R^n$, is a topological space denoted by $|K|$ and called the *polyhedron of $K$*.

**Prop:** If $K$ is Euclidean simplicial complex, then the collection of the interiors of the simplices of $K$ is a regular CW decomposition of $|K|$. 