---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth or Differentiable Manifolds]], [[Quotient Topology]], [[Grassmannian Spaces]], [[Smooth Submanifolds]]

We define an equivalence relation on $\Bbb R^{n+1}\setminus\{0\}$ by $$x \sim y \iff \exists t \in \Bbb R(y = tx)$$where $x, y \in \Bbb R^{n+1}\setminus \{0\}$. The *real projective space* $\Bbb {R P}^n$ or $\Bbb P_n(\Bbb R)$ is the quotient space of $\Bbb R^{n+1}\setminus\{0\}$ by this equivalence relation. We denote the equivalence class of a point $(a^0, \dots, a^n) \in \Bbb R^{n+1}\setminus\{0\}$ by $[a^0, \dots, a^n]$ and let $\pi: \Bbb R^{n+1}\setminus\{0\} \to \Bbb {R P}^n$ be the projection. We call $[a^0, \dots, a^n]$ *homogeneous coordinates* on $\Bbb {RP}^n$. 

Geometrically, two nonzero points in $\Bbb R^{n+1}$ are equivalent iff thy line in the same line through the origin, so $\Bbb {RP}^n$ can be interpreted as the set of all lines through the origin in $\Bbb R^{n+1}$. Each line through the origin in $\Bbb R^{n+1}$ meets the unit sphere $\Bbb S^n$ in a pair of antipodal points, and conversely, a pair of antipodal points on $\Bbb S^n$ determines a unique line through the origin. This suggest that we can define an equivalence relation $\sim$ on $\Bbb S^n$ by identifying antipodal points: $$x\sim y \iff x = \pm y, \qquad x, y\in \Bbb S^n$$We have the bijection $\Bbb {RP}^n \leftrightarrow \Bbb S^n/\sim$. 

Then we have that $\Bbb {RP}^n$ is compact.

**Prop:** The equivalence relation $\sim$ on $\Bbb R^{n+1}\setminus\{0\}$ in the definition of $\Bbb {RP}^n$ is an open equivalence relation. This can be seen as the [[Continuous Actions of Groups]] (scalar multiplication) on the topological space $\Bbb R^{n+1}\setminus\{0\}$. 

**Cor:** The real projective space $\Bbb {RP}^n$ is second countable

**Prop:** The real projective space $\Bbb {RP}^n$ is $T_2$. 

# The Standard $\mathcal C^\infty$ Atlas on a Real Projective Space

Let $[a^0, \dots, a^n]$ be homogeneous coordinates on the projective space $\Bbb {RP}^n$. $a^0$ is not a well-defined function $\Bbb {RP}^n$, the condition $a^0 \neq 0$ is independent of the choice of representative for $[a^0, \dots, a^n]$. With this condition, we can define: $$U_0 := \{[a^0, \dots, a^n]\in \Bbb {RP}^n \mid a^0\neq 0\}$$Similarly, for each $i\in \{1, \dots, n\}$, let $$U_i := \{[a^0, \dots, a^n]\in \Bbb {RP}^n \mid a^i \neq 0\}$$
We define the map: $\phi_i: U_i \to \Bbb R^n$ by $$[a^0, \dots, a^n] \mapsto \left(\frac{a^0}{a^i}, \dots, \hat{\frac{a^i}{a^i}}, \dots \frac{a^n}{a^i}\right)$$where the caret sign $\widehat \;$  over $a^i/ a^i$ means that entry is to be omitted. This proves that $\Bbb {RP}^n$ is locally Euclidean with the charts $(U_i, \phi_i)$ as charts.

Meaning that $\Bbb {RP}^n$ is a topological manifold of dimension $n$. 

It is easy to show that $\{(U_i, \phi_i)\mid i \in \{0, \dots, n\}\}$ is a $\mathcal C^\infty$ atlas for $\Bbb {RP}^n$, called the *standard atlas.* Meaning that $\Bbb {RP}^n$ is a smooth manifold.

# As CW Complex

If we consider the the usual inclusion $\Bbb R^{k+1} \subseteq \Bbb R^{n+1}$ for $k<n$, this allows us to consider $\Bbb{RP}^k$ as a subspace of $\Bbb{RP}^n$. Then $\Bbb{RP}^n$ has a CW decomposition with one cell in each dimension $0, \dots, n$ such that the $k$-skeleton is $\Bbb{RP}^k$ for $0 < k < n$. 

# As Quotient of a Zero Dimensional Lie Group

The two-element group $\{\pm 1\}$ acts on $\Bbb S^n$ by multiplication. This action is obviously smooth and free, and it is proper because the group is compact. This defines a smooth structure on $\Bbb S^n/\{\pm 1\}$. In fact, this quotient manifold is diffeomorphic to $\Bbb {RP}^n$ with smooth structure we defined above. Let $p: \Bbb S^n \to \Bbb {RP}^n$ be the smooth covering map obtained by restricting the canonical projection $\Bbb R^{n+1}\setminus \{0\}\to \Bbb {RP}^n$ to the sphere. This map makes the same identification as the quotient map $\pi: \Bbb S^n \to \Bbb S^n/\{\pm 1\}$. This $\Bbb S^n /\{\pm 1\}$ is diffeomorphic to $\Bbb {RP}^n$, and $\Bbb {RP}^n$ is a compact manifold. 

# Real Projective Varieties

On the projective space $\Bbb {RP}^n$ a homogeneous polynomial $F(x_0, \dots,x_n)$ of degree $k$ is not a function, since its value at a point $[a_0, \dots, a_n]$ is not unique. However, the zero set in $\Bbb {RP}^n$ of a homogeneous polynomial $F(x_0, \dots, x_n)$ is well defined, since $F(a_0, \dots, a_n) = 0$ if $$F(ta_0, \dots, ta_n) = t^kF(a_0, \dots, a_n) = 0, \qquad \forall t\in \Bbb R^\setminus\{0\}$$The zero set of finitely many homogeneous polynomials in % is called a *real projective variety*. A projective variety defined by a single homogeneous polynomial of degree $k$ is called a *hypersurface* of degree $k$. 

