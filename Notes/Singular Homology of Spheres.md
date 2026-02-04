---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Mayer-Vietoris Theorem for Singular Homology]], [[Fundamental Group of the Circle]], [[Singular Homology]]

**Homology Groups on Spheres:** For $n \ge 1$, $\Bbb S^n$ has the following singular homology groups: $$H_p(\Bbb S^n) \cong \begin{cases}
\Bbb Z & p= 0 \text{ or } p = n,\\
0 & p\ne 0 \text{ and } p \ne n.
\end{cases}  $$

**Homology Groups of Punctured Euclidean Spaces:** For $n \ge 2$, $\Bbb R^n \setminus \{0\}$ has the following singular homology groups: $$H_p(\Bbb R^n\setminus \{0\}) \cong \begin{cases}
\Bbb Z & p= 0 \text{ or } p = n-1,\\
0 & p\ne 0 \text{ and } p \ne n-1.
\end{cases}  $$
# Degree Theory for Spheres

**Def:** Suppose $n \ge 1$. Because $H_n(\Bbb S^n)$ is infinite cyclic, if $f:\Bbb S^n \to\Bbb S^n$ is any continuous map, then $f_*: H_n(\Bbb S^n) \to H_n(\Bbb S^n)$ is multiplication by a unique integer, called the *degree of $f$* and denoted by $\deg f$. We can call this definition to the *homological degree* of a function.

**Prop:** Suppose $n \ge 1$, and $f,g :\Bbb S^n \to\Bbb S^n$ are continuous maps.
- $\deg(g\circ f) =(\deg g)(\deg f)$
- If $f\simeq g$, then $\deg f = \deg g$. 

If we look at the degree theory we did in the circle we have two notions of degree.

**Def:** If $\varphi: \Bbb S^1 \to \Bbb S^1$ is a continuous map, we define the *degree of $\varphi$* to be the winding number of the loop $\varphi \circ \omega$. This integer is denoted by $\deg \varphi$. We can call this to be the *homotopic degree*. 

**Prop:** The homological degree and homotopic degree of a continuous map $f: \Bbb S^1\to\Bbb S^1$ are equal. 

**Degrees of Some Common Maps of Spheres:**
- The identity map of $\Bbb S^n$ has degree $1$.
- Any constant map $\Bbb S^n \to\Bbb S^n$ has degree $0$
- The *reflection maps* $R_i: \Bbb S^n \to\Bbb S^n$ given by $$R_i(x_1,\dots, x_i,\dots,x_{n+1}) := (x_1,\dots, -x_i, \dots, x_{n+1}) $$have degree $-1$.
- The anitpodal map $\alpha:\Bbb S^n\to\Bbb S^n$ given by $\alpha(x) = -x$ has degree $(-1)^{n+1}$. 

**Th:** Let $\varphi: \Bbb S^n \to\Bbb S^n$ be continuous. If $\deg \varphi \neq 0$, then $\varphi$ is surjective.

**Th:** Let $\varphi: \Bbb S^n \to\Bbb S^n$ be continuous. If $\deg \varphi \ne (-1)^{n+1}$, then $\varphi$ has a fixed point. 

**Prop:** The antipodal map $\alpha:\Bbb S^n \to\Bbb S^n$ is homotopic to the identity map iff $n$ is odd.

**Def:** A *vector field* on $\Bbb S^n$ is a continuous map $V: \Bbb S^n \to\Bbb R^{n+1}$ such that for each $x\in \Bbb S^n$, $V(x)$ is tangent to $\Bbb S^n$ at $x$, or in other words the Euclidean dot product $V(x) \cdot x = 0$. 

**The Hairy Ball Theorem:** There exists a nowhere vanishing vector field on $\Bbb S^n$ iff $n$ is odd.

The proof of this fact can also be done using [[Stokes's Theorem and Smooth Manifolds with Corners#^ed5f49|Stokes's Theorem on Manifolds]], which is a little wild. 

$(*)$ **Th:** Two continuous maps from $\Bbb S^n$ to itself are homotopic iff they have the same degree. 

(I have to read Hatcher, so i am gonna leave it be for a bit).

**[[Topological Manifolds#^ca2c82|Invariance of Dimension]]:** If $m \ne n$, then a nonempty topological space cannot be both an $m$-dimensional manifold and an $n$-dimensional manifold

**[[Topological Manifolds#^cd5f36|Invariance of the Boundary]]:** Suppose $M$ is an $n$-manifold with boundary. A point of $M$ cannot be a boundary point and an interior point. 

**Prop:** If $f: \Bbb S^n \to \Bbb S^n$ is a continuous map that has a continuous extension $F: \bar{\Bbb B}^{n+1}\to \Bbb S^n$, then $f$ has degree $0$. 

**Brouwer Fixed Point Theorem:** For each integer $n \ge 0$, every continuous map $f: \bar{\Bbb B}^{n}\to \bar{\Bbb B}^{n}$ has a fixed point.  ^374dde

**Prop:** If $n$ is even, then $\Bbb Z/2\Bbb Z$ is the only nontrivial group that can act freely on $\Bbb S^n$ by homeomorphism. 