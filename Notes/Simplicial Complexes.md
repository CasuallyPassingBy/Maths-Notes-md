---
tags:
  - Topology
---
TSubjects: [[Topology]]
Links: [[Cell Complexes and CW Complexes]], [[Affine Spaces of Rn]], [[Convex Hulls]]

**Def:** Let $\{v_0, \dots, v_k\}$ be an affinely independent set of $k+1$ points in $\Bbb R^n$. The *simplex*, spanned by them, denoted by $[v_0, \dots, v_k]$, is the set $$[v_0,\dots, v_k] := \left\{\left.\sum_{i = 0}^k t_i v_i \; \right \rvert\; t_i \ge 0 \land \sum_{i = 1}^k t_i \right\},$$with the subspace topology. For any point $x = \sum_{i = 0}^k t_i v_i\in [v_0, \dots, v_k]$, the numbers $t_i$are called the *barycentric coordinates of $x$* with respect to $[v_0, \dots, v_k]$. Each of the points $v_i$ is called a *vertex* of the simplex. The integer $k$ is called its *dimension*; a $k$-dimensional simplex is often called a *$k$-simplex*. 

**Def:** Let $\Delta_k := [e_0, \dots, e_k] \subseteq \Bbb R^k$, where $e_0 = 0$, and $e_i$ is the standard basis. We call $\Delta_k$ the *standard $k$-simplex*. 

**Obs:** We see that $[v_0, \dots, v_k] = \text{conv}(v_0, \dots, v_k)$, meaning that the $[v_0, \dots, v_k]$ is the convex hull of its vertices. 

**Prop:** Every $k$-simplex is a closed $k$-cell. This is because every $k$-simplex is homeomorphic to the standard $k$-simplex, and the standard $k$-simplex is a closed $k$-cell.

**Def:** Let $\sigma$ be a $k$-simplex. Each simplex spanned by a nonempty subset of vertices of $\sigma$ is called a *face of $\sigma$*. The faces that are not equal to $\sigma$ itself acre called its *proper faces*. The $0$-dimensional faces of $\sigma$ are just its vertices, and the $1$-dimensional faces are called its *edges.* The $(k-1)$-dimensional faces of a $k$-simplex are called its *boundary faces*. 

We define the *boundary of $\sigma$* to be the union of its boundary faces, which is equal to the union of all its proper faces, and it is is equal to its manifold boundary.  Additionally, we define the *interior of $\sigma$* to be the set of all points with positive barycentric coordinates.

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

We see that a polyhedron is compact iff it associated simplicial complex is finite, and its connected iff the polyhedron of its $1$-skeleton is connected.

**Examples:**
- Any $n$-simplex together with all of its faces is a simplicial complex whose polyhedron is homeomorphic to $\bar{\Bbb B}^n$.
- The set of proper faces of an $n$-simplex constitutes an $(n-1)$-simplicial complex whose polyhedron is homeomorphic to $\Bbb S^{n-1}$. 

**Def:** If $X$ is a topological space, a homeomorphism between $X$ and the polyhedron of some simplicial complex is called a *triangulation of $X$*. Any space that admits a triangulation is said to be *triangulable*.  ^dbc61e

**Prop:** All $1$-dimensional manifolds with and without boundary are triangulable. 

$(*)$ **Triangulation Theorem for $2$-Manifolds:** Every $2$-manifold is homeomorphic to the polyhedron of a $2$-dimensional simplicial complex, in which every $1$-simplex is a face of exactly two $2$-simpleces. ^e0f03b

$(*)$ **Triangulation Theorem for $3$-Manifolds:** Every $3$-manifold is triangulable. 

$(*)$ **Manolescu's Theorem:** There exists non-triangulable $n$-dimensional topological manifolds for every $n \ge 5$.

**Def:** Suppose $\sigma = [v_0, \dots, v_k]$ is a simplex in $\Bbb R^n$ and $w\in \Bbb R^n$. If $\{w, v_0, \dots, v_k\}$ is affinely independent set, we say that $w$ is *affinely independent of $\sigma$*. In this case the simplex $[w, v_0, \dots, v_k]$ is denoted by $w*\sigma$ and is called the *cone on $\sigma$*. More generally, suppose $K$ is finite Euclidean simplicial complex and $w$ is a point in $\Bbb R^n$ that is affinely independent of every simplex in $K$. We define the *cone on $K$* to be the following collection of simplices in $\Bbb R^n$:  $$w*K := K \cup\{w*\sigma\mid \sigma \in K\}. $$
We see that $w*K$ is homeomorphic to $CK$, the cone of $K$.

# Simplicial Maps

**Prop:** Let $\sigma = [v_0, \dots, v_k]$ be a $k$-simplex in $\Bbb R^n$. Given $k+1$ points $w_0, \dots, w_k\in \Bbb R^m$, there is a unique map $f: \sigma \to \Bbb R^m$ that is the restriction of an affine map that takes $v_i$ to $w_i$ for each $i$. 

In this situation, we say that $f: \sigma\to \Bbb R^m$ is the *affine map determined by the vertex map* $v_i \mapsto w_i$ for $i \in \{0,\dots, k\}$. 

**Def:** Suppose $K$ and $L$ are simplicial complexes, and let $K_0$ and $L_0$ denote their respective $0$-skeletons. A *simplicial map from $K$ to $L$* is a continuous map $f: |K| \to |L|$ whose restriction to each simplex $\sigma \in K$ agrees with an affine map taking $\sigma$ onto some simplex in $L$. The restriction to $K_0$ yields a map $f_0: K_0 \to L_0$ called the *vertex map of $f$*. A simplicial map is called a *simplicial isomorphism* if it is also a homeomorphism. 

**Simplicial Maps Are Determined by Vertex Maps:** Let $K$ and $L$ be simplicial comlpexes. Suppose $f_0: K_0\to L_0$ is any map with the property that whenever $\{v_0,\dots, v_k\}$ are the vertices of a simplex of $K$, $\{f_0(v_0), \dots, f_0(v_k)\}$ are the vertices of a simplex of $L$ (possibly with repetitions). Then there is a unique simplicial map $f: |K| \to |L|$ whose vertex map is $f_0$. 

Additionally, it is a simplicial isomorphism iff $f_0$ is a bijection satisfying the following additional condition: $\{v_0, \dots, v_k\}$ are the vertices of a simplex $K$ iff $\{f_0(v_0), \dots, f_0(v_k)\}$ are the vertices of a simplex of $L$. 

**Def:** If $K$ is a Euclidean simplicial complexa *subdivision of $K$* is a simplicial complex $K'$ such that each simplex $K'$ is contained in a simplex of $K$, and each simplex of $K'$ is the union of simpleces of $K'$. We see that $|K| = |K'|$. 

