---
tags:
  - Topology
  - DifferentialGeometry
---
Subjects: [[Topology]], [[Differential Geometry]]
Links: [[Hausdorff spaces]], [[Separable, First and Second Countable Spaces]]

**Def:** We say that if for each point $p$ has a neighbourhood $U$ which is homeomorphic to an open set $U'$ of $\Bbb R^n$, $n$ fixed. 

**Def:** A *manifold* $M$ of dimension $n$, or $n$-manifold, is a topological space with the following properties:
- $M$ is Hausdorff
- $M$ is locally Euclidean of dimension $n$
- $M$ is second countable

As a matter of notation $\dim M$ is used for the *dimension* of $M$. 

**Th:** A topological manifold $M$ is [[Locally Connectedness|locally connected]], [[Locally compactness|locally compact]], and a union of a countable collection of compact subsets; furthermore it is [[Normal Spaces|normal]] and [[Metrizable Spaces|metrizable]]

**Def:** Let $M \in \tau_M$, $U \in \tau_M$, $V\in \tau_{\Bbb R^n}$ where $n = \dim M$, and $\varphi: U \to V$ a homeomorphism. The pair $(U, \varphi)$ is called a *coordinate neighbourhood* to $q \in U$, or *chart*. We assign the $n$-coordinates $x^1(q), \dots, x^n(q)$ to the image of $\varphi(q) \in \Bbb R^n$ the $x^m$ is a real valued function on $U$, the $m$th coordinate function. 

**Obs:** If $q$ lies in two charts $(U, \varphi)$ and $(V, \psi)$, then it has coordinates $x^1(q), \dots, x^n(q)$ and $y^1(q), \dots, y^n(q)$, respectively. We define the homeomorphism $$\psi \circ \varphi^{-1} : \varphi[U \cap V]\subseteq \Bbb R^n \to \psi[U \cap V] \subseteq \Bbb R^n$$
In coordinates $\phi \circ \varphi^{-1}$ is given by the continuous functions $$y^m = h^m(x^1, \dots, x^n), \qquad m \in \{1 \dots, n\}$$
Similarly, $\varphi \circ \psi^{-1}$ gives the inverse mapping which expresses the $x$-coordinates as functions of the $y$-coordinates $$x^m = g^m(y^1, \dots, y^n) \qquad m \in \{1, \dots, n\}$$
We call $\varphi \circ \psi^{-1}$ to be a *transition map*. 

**Def:** An *atlas* is a collection of charts $\{(U_\alpha, \varphi_\alpha) \mid \alpha < \kappa\}$ such that $\{U_\alpha \mid \alpha < \kappa\}$ is an open cover of $M$. A *complete atlas* is a maximal. 