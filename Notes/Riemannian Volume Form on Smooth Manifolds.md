---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Orientations of Smooth Manifolds]], [[Riemannian Metrics on Smooth Manifolds]]

**Obs:** Let $(M, g)$ be an oriented Riemannian manifold of positive dimension. We know that there is a smooth orthonormal frame $(E_1,\dots, E_n)$ is a neighbourhood of each point of $M.$ By replacing $E_1$ by $-E_1$ if necessary, we can find an *oriented* orthonormal frame in a neighbourhood of each point.

**Prop:** Suppose $(M, g)$ is an oriented Riemannian $n$-manifold with or without boundary, and $n\ge 1$. There is a unique smooth orientation form $\omega_g \in \Omega^n(M)$, called the *Riemannian volume form,* that satisfies: $$\omega_g(E_1,\dots, E_n) = 1 $$for every local oriented orthonormal frame $(E_i)$ for $M$. 

**Prop:** Suppose $(M, g)$ and $(\widetilde M,\widetilde g)$ are positive-dimensional Riemannian manifolds with or without boundary, and $F: M \to \widetilde M$ is a local isometry. Then $F^*\widetilde \omega_g = \omega_g$. 

**Prop:** Let $(M, g)$ be an oriented Riemannian $n$-manifold with or without boundary, $n \ge 1$. If any oriented smooth coordinates $(x^i)$, the Riemannian volume form has the local coordinate expression $$\omega_g = \sqrt{\det(g_{ij}) } \; dx^1\wedge \dots \wedge dx^n,$$where $g_{ij}$ are the components of $g$ in these coordinates. 

## Hypersurfaces in Riemannian Manifolds

Let $(M, g)$ be an oriented Riemannian manifold with or without boundary, and suppose $S\subseteq M$ is an immersed hypersurface with or without boundary. Any unit normal vector along $S$ is nowhere tangent to $S$, so it determines an orientation of $S$.

**Prop:** Let $(M, g)$ be an oriented Riemannian manifold with or without boundary, let $S\subseteq M$ be an immersed hyperspace with or without boundary, and let $\widetilde g$ denote the induced metric on $S$. Suppose $N$ is a smooth unit normal vector field along $S$. With respect to the orientation of $S$ determined by $N$, the volume form of $(S, \widetilde g)$ is given by $$\omega_{\widetilde g} = \iota_S^*(N \; \lrcorner \; \omega _g). $$
**Prop:** Suppose $M$ is a Riemannian manifold with boundary. There is a unique smooth outward-pointing unit vector field $N$ along $\partial M$. 

**Cor:** If $(M, g)$ is an oriented Riemannian manifold with boundary, and $\widetilde g$ is the induced Riemannian metric on $\partial M$, then the volume form of $\widetilde g$ is $$\omega_{\widetilde g} = \iota_S^*(N \; \lrcorner \; \omega _g), $$where $N$ is the outward unit normal vector field along $\partial M$. 
