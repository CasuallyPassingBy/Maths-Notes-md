---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Mayer-Vietoris Theorem for Singular Homology]], [[Fundamental Group of the Circle]]

**Homology Groups on Spheres:** For $n \ge 1$, $\Bbb S^n$ has the following singular homology groups: $$H_p(\Bbb S^n) \cong \begin{cases}
\Bbb Z & p= 0 \text{ or } p = n,\\
0 & p\ne 0 \text{ and } p \ne n.
\end{cases}  $$

**Homology Groups of Punctured Euclidean Spaces:** For $n \ge 2$, $\Bbb R^n \setminus \{0\}$ has the following singular homology groups: $$H_p(\Bbb R^n\setminus \{0\}) \cong \begin{cases}
\Bbb Z & p= 0 \text{ or } p = n-1,\\
0 & p\ne 0 \text{ and } p \ne n-1.
\end{cases}  $$
# Degree Theory for Spheres

**Def:** Suppose $n \ge 1$. Because $H_n(\Bbb S^n)$ is infinite cyclic, if $f:\Bbb S^n \to\Bbb S^n$ is any continuous map, then $f_*: H_n(\Bbb S^n) \to H_n(\Bbb S^n)$ is multiplication by a unique integer, called the *degree of $f$* and denoted by $\deg f$.

**Prop:** Suppose $n \ge 1$, and $f,g :\Bbb S^n \to\Bbb S^n$ are continuous maps.
- $\deg(g\circ f) =(\deg g)(\deg f)$
- If $f\simeq g$, then $\deg f = \deg g$. 

If we look at the degree theory we did in the circle we have two notions of degree. We can call the degree 