---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Functions on Smooth Manifolds]], [[Tangent Space for Manifolds]], [[The Rank of a Matrix and Matrix Inverses]], [[Submersions, Immersions and Local Diffeomorphism of Smooth Manifolds]], [[The Cotangent Bundle]]

**Def:** Suppose $M$ and $N$ are smooth manifolds with or without boundary and $p\in M$, we define a *rank of $F$ at $p$* to be the rank of the linear map $dF_p : T_pM \to T_{F(p)}N$; it is the rank of the Jacobian matrix of $F$ in any smooth chart, or the dimension of $\text{Im } dF_p \le T_{F(p)} N$. If $F$ has the same rank $r$ at every point, we say that it has *constant rank,* and write $\text{rank }F = r$. 

We see that the rank of $F$ is bounded above by $\min \{\dim M, \dim N\}$. If the rank of $dF_p$ is equal to this upper bound, we say that *$F$ has full rank at $p$*, and if $F$ has full rank everywhere, we say that $F$ has full rank. 

**Rank Theorem for Manifolds:** Suppose $M$ and $N$ are smooth manifolds of dimension $m$ and $n$, respectively, and $F: M \to N$ is a smooth map with constant rank $r$. For each $p\in M$ there exists a smooth coordinates $(U, (x^1, \dots, x^m))$ centred at $p$ and $(V, (y^1, \dots, y^n))$ centred at $F(p)$ such that $F[U] \subseteq V$, in which $F$ has the coordinate representation $$F(x^1, \dots, x^m) = (x^1, \dots, x^k, 0, \dots, 0).$$In particular, if $F$ is a smooth submersion, this becomes $$F(x^1,\dots, x^n,\dots, x^m) = (x^1,\dots, x^n)$$and if $F$ is a smooth immersion, it is $$ F(x^1, \dots, x^m) = (x^1, \dots, x^m, 0, \dots, 0).$$
This is just the [[Inverse Function Theorem in Rn#Straightening-Out Theorem|Straightening-Out Theorem]]. 

**Cor:** Let $M$ and $N$ be smooth manifolds, let $F: M \to N$ be a smooth map, and suppose $M$ is connected. Then the following are equivalent: ^815841
- For each $p\in M$ there exist smooth charts near $p$ and $F(p)$ in which the coordinate representation of $F$ is linear.
- $F$ has constant rank.

We see that the following theorem is a special case for $F$ is a full rank smooth map between smooth manifolds with the same dimension:

**Inverse Function Theorem for Manifolds:** Suppose $M$ and $N$ are smooth manifolds, and $F:M \to N$ is a smooth map. If $p\in M$ is a point such that $dF_p$ is invertible, then there are connected neighbourhoods $U_0$ of $p$ and $V_0$ of $F(p)$ such that $F|_{U_0}: U_0 \to V_0$ is a diffeomorphism,.

**Coordinate Selection Lemma:** Suppose $M$ is a smooth manifold, $p \in M$ and $y^1, \dots, y^n$ are smooth real-valued functions defined on a neighbourhood $p$ of $M$.
- If $dy^1|_p, \dots, dy^n|_p$ form a basis for $T^*_pM$, then $(y^1, \dots, y^n)$ are smooth coordinates for $M$ in some neighbourhood.
- If $dy^1|_p, \dots, dy^n|_p$ are independent, then are real valued functions $y^{n+1}, \dots, y^m$ such that $(y^1, \dots, y^m)$ are smooth coordinates for $M$ in some neighbourhood of $p$.
- If $dy^1|_p, \dots, dy^n|_p$ span $T_p^*M$, then there are indices $i_1, \dots, i_k$ such that $(y^{i_1}, \dots, y^{i_k})$ are smooth coordinates for $M$ in some neighbourhood of $p$.