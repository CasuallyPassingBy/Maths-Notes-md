---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[The Monodromy Action of Covering Maps]], [[Covering Maps]], [[Compact Surfaces]], [[Fundamental Group of Compact Surfaces]], [[Möbius Transformations]], [[Group Actions]], [[Continuous Actions of Groups]], [[Geodesics in Riemannian Geometry]], [[Topology of Metric Spaces]]

The idea of this note to determine the universal covering of all compact surfaces. We consider that $\Bbb B^2 \subseteq \Bbb C$. 

**Def:** There's a special metric on the disk. For $z_1, z_2 \in \Bbb B^2$, defined as $$d(z_1, z_2) = \cosh^{-1}\left(1+ \frac{2|z_1-z_2|^2}{(1-|z_1|^2)(1-|z_2|^2)}\right).$$This metric is called the *hyperbolic metric*. 

The disk with the metric, called the *hyperbolic disk*, is one model of non Euclidean plane geometry. The geodesics in this geometry, called *hyperbolic geodesics*, are the intersections with the disk of Euclidean circles and lines meeting the unit circle orthogonally. 

An important feature of the hyperbolic metric is that is preserved by a transitive group action. 

Let $\alpha,\beta\in\Bbb C$ with $|\alpha|^2 - |\beta|^2 >0$, and define $$\varphi(z) = \frac{\alpha z + \beta}{\overline \beta z + \overline \alpha}.$$We see that actually $\varphi: \Bbb B^2 \to \Bbb B^2$ is an isometry. We calle this type of maps a *Möbius transformations of the disk*, and the set $\cal M$ of all such maps is a group under composition called the *Möbius group* of the disk. Each Möbius transformations is determined by a matrix of the form $\begin{pmatrix}\alpha & \beta \\ \overline \beta & \overline\alpha \end{pmatrix}$, and the composition of two Möbius transformations correspond to the multiplication of matrices. Two such matrices determine the same Möbius transformations iff they differ by a real scalar multiple, so we can identify $\cal M$ with the quotient of the group of all matrices $\begin{pmatrix}\alpha & \beta \\ \overline \beta & \overline\alpha \end{pmatrix}$ modulo the subgroup of matrices $\begin{pmatrix}\lambda & 0 \\ 0 & \lambda \end{pmatrix}$ with $\lambda \in\Bbb R\setminus \{0\}$; with the quotient topology, it is a topological group acting continuously on $\Bbb B^2$.

Any Möbius transformation that takes the origin to itself must be of the form $\varphi(z) = (\alpha/\overline\alpha) z$. Additionally, if we observe that the hyperbolic distance of $z$ to the origin only depends on $|z|$, thus each metric ball $B(0, r)$ about the origin is actually a Euclidean disk centred at $0$, and its boundary is the Euclidean circle. We know by the properties of Möbius transformations that they take circles of the Riemann sphere to circles of the Riemann spheres. Additionally, we know that isometries take geodesics to geodesics. We see that every metric ball is a Euclidean disk (the centre of the Euclidean ball can be different from the centre of the metric ball). Hence, the hyperbolic metric generates the Euclidean topology. 

We see that the action of $\cal M$ on $\Bbb B^2$ is transitive because for any $w\in\Bbb B^2$ is carried to $0$ by the Möbius transformation $$\varphi(z) = \frac{z-w}{1-\overline wz}.$$

**Prop:** Given two pairs of points $z_0, z_1$ and $w_0, w_1$ such that $d(z_0, z_1) = d(w_0, w_1)$, there is a unique Möbius transformation taking $z_0 \mapsto w_0$ and $z_1 \mapsto w_1$. 

We see that Möbius maps on the disk are conformal, meaning they preserve angles between tangent vectors. 

Let $M$ be a compact orientable surface of genus $n \ge 2$. We would like to be a discrete subgroup $\Gamma\subseteq \cal M$ whose action on $\Bbb B^2$ is a covering space action such that $M$ is homeomorphic to $\Bbb B^2 /\Gamma$. Then we would see that $\Bbb B^2$ is the universal covering space.

We know that the standard polygonal presentation of $M$ as a quotient of a polygonal region with $4n$ sides whose edges are identified pairs. We will realise $M$ as a quotient of a compact region in $\Bbb B^2$ bounded by a *geodesic polygon*, that is, the union of finitely many geodesic segments.

We begin by constructing a $4n$-sided regular, geodesic polygon, whose edges have the equal lengths and meet at equal angles. We start with $4n$ points $(z_0, z_1, \dots, z_{4n} = z_0)$ equally spaced on some circle about the origin. Since the hyperbolic metric is invariant under rotations, the geodesic segments $z_j$ and $z_{j+1}$ for $j = 0, \dots, 4n-1$ all have the same length and meet at equal angles, so their union is a regular geodesic polygon. We can define small regular geodesic polygons whose interior angles are very close to what they would be in the Euclidean case, namely $\pi - \pi/2n$. As the points get farther from the origin, the arcs become nearly tangent with each other, getting geodesic polygons with interior angles very near $0$. By continuity, there is a polygon whose interior angles are exactly $\theta = \pi/2n$, for $n \ge 2$. 

Let $P$ be the compact subset of $\Bbb B^2$ consisting of this regular geodesic polygon together with the bounded component of its complement. We choose a vertex $v_0$, and label the edges $a_1, b_1, a_1^{-1}, b_1^{-1}, \dots, a_n, b_n, a_n^{-1}, b_n^{-1}$ in counterclockwise order starting from $v_0$. For each edge $a_j$, $a_j^{-1}$, there is a unique Möbius transformation $\alpha_j$ that takes the edge labeled $\alpha_j^{-1}$ onto the labeled $a_j$, with initial vertex of going to the initial vertex of the other. Similarly, let $\beta_j$ be the transformation taking $b_j$ to $b_j^{-1}$ and respecting the initial and terminal vertices. Let $\Gamma \subseteq \cal M$ be the subgroup generated by $\{\alpha_j, \beta_j \mid j = 1, \dots, 4n\}$. We call the generators $\alpha_j, \beta_j$, and their inverses *edge pairings transformations.*

**Obs:** If $\sigma$ is any edge pairing transformations, then $P \cap \sigma(P)$ consists of exactly one edge of $P$.

**Th:** The group $\Gamma$ is discrete and its action on $\Bbb B^2$ is a covering space action whose quotient $\Bbb B^2/\Gamma$ is homeomorphic to $M$. The restriction of this quotient map to $P$ is $q$. 

**Th:** Let $M$ be a compact surface. The universal covering space of $M$ is homeomorphic to:
- $\Bbb S^2$ if $M\cong \Bbb S^2$ or $\Bbb{RP}^2$
- $\Bbb R^2$ if $M \cong \Bbb T^2$ or $\Bbb{RP}^2 \#\Bbb{RP}^2$
- $\Bbb B^2$ if $M$ is any other surface. 