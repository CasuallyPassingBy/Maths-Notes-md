---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Covering Maps]], [[Smooth Functions on Smooth Manifolds]], [[Proper Maps]], [[Covering maps]]

**Def:** If $N$ and $M$ are connected smooth manifolds, a *smooth covering map* $\pi: N \to M$ is a smooth surjective map with the property that every $p\in M$ has a connected neighbourhood $U$ such that each components of $\pi^{-1}[U]$ is mapped *diffeomorphically* onto $U$ by $\pi$. In this context we will say that $U$ is evenly covered. The manifold $M$ is called the *base* of the *covering*, and $N$ is called a *covering manifold*.

**Prop:**
- Any smooth covering map is a local diffeomorphism and an open map.
- Any injective smooth covering map is a diffeomorphism.
- A topological covering map is a smooth covering map iff it is a local diffeomorphism.

**Prop:** If $\pi_1: N_1 \to M_1$ and $\pi_1: N_2 \to M_2$ are smooth covering maps, then $\pi_1 \times \pi_2: N_1 \times N_2 \to M_1 \times M_2$ is a smooth covering map.

**Obs:** Let $\pi: N \to M$ is a smooth covering map. If $U\subseteq M$ is evenly covered in the topological sense, then $\pi$ maps each component of $\pi^{-1}[U]$ diffeomorphically onto $U$. 

**Def:** If $\pi: N \to M$ is any continuous map, a section of $\pi$ is a continuous map $\sigma: N \to N$ such that $\pi \circ \sigma = \text{id}_M$. A *local section* is a continuous map $\sigma: U \to N$ defined on some open set $U \subseteq M$ and satisfying the analogous relation $\pi \circ \sigma = \text{id}_U$.

**Local Section Theorem for Smooth Covering Maps:** Suppose $E$ and and $M$ are smooth manifolds with or without boundary, and $\pi: E \to M$ is a smooth covering map. Given any evenly covered open subset $U \subseteq M$, and any $q\in U$, and any $p$ in the fiber $\pi$ over $q$, there exists a unique smooth local section $\sigma: U \to E$ such that $\sigma(q) = p$. 

**Prop:** Suppose $\pi: N \to M$ is a smooth covering map and $L$ is any smooth manifold. A map $F: M \to L$ is smooth iff $F \circ \pi: N \to L$ is smooth:

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm] 
N \arrow[d,two heads, "\pi"'] \arrow[dr, "F \circ \pi"] \\ M \arrow[r, "F"'] & L
\end{tikzcd}
\end{document}
```

**Prop:** If $M$ is a connected smooth $n$-manifold and $\pi: N \to M$ is a topological covering map, then $N$ is a topological $n$-manifold, and it has a unique smooth structure such that $\pi$ is a smooth covering map. 

**Covering Spaces of Smooth Manifolds with Boundary:** Suppose $M$ is a connected smooth $n$-manifold with boundary, and let $\pi: E \to M$ is a topological covering map. Then $E$ is a topological $n$-manifold with boundary such that $\partial E = \pi ^{-1}[\partial M]$, and it has a unique smooth structure such that $\pi$ is a smooth covering map. 

**Existence of a Universal Covering Map:** If $M$ is a connected smooth manifold, there exists a simply connected smooth manifold $\widetilde M$, called the *universal covering manifold of $M$*, and a smooth covering map $\pi: \widetilde M \to M$. The universal covering manifold is unique in the sense: if $\widetilde M'$ is any other simply connected smooth manifold that admits a a smooth covering $\pi': \widetilde M' \to M$, then there exists a diffeomorphism $\Phi: \widetilde M \to \widetilde M'$ such that $\pi' \circ \Phi = \pi$. 

This is immediate from the [[The Monodromy Action of Covering Maps#Universal Covering Space|existence of a universal covering space]]. 

**Existence of a Universal Covering Map:** If $M$ is a connected smooth manifold with boundary, there exists a simply connected smooth manifold $\widetilde M$ with boundary, called the *universal covering manifold of $M$*, and a smooth covering map $\pi: \widetilde M \to M$ such that $\partial \widetilde M = \pi^{-1}[\partial M]$. The universal covering manifold is unique in the sense: if $\widetilde M'$ is any other simply connected smooth manifold that admits a a smooth covering $\pi': \widetilde M' \to M$, then there exists a diffeomorphism $\Phi: \widetilde M \to \widetilde M'$ such that $\pi' \circ \Phi = \pi$. 

**Existence of a Universal Covering Group:** Let $G$ be a connected Lie group. There exists a simply connected Lie group $\tilde G$ (called the universal covering group of $G$) and a smooth covering map $\pi: \tilde G\to G$ that is also a Lie group homomorphism.

**Prop:** Suppose $N$ and $M$ are connected smooth manifolds and $\pi: N \to M$ is a proper local diffeomorphism, then $\pi$ is a smooth covering map. 

**Prop:** Let $\pi:N \to M$ be a smooth covering map. With the discrete topology, the covering group $\mathcal C_\pi(N)$ is a zero dimensional [[Lie groups|Lie group]] [[Lie group Actions|acting]] smoothly, freely and properly on $N$. 

**Prop:** A covering map $\pi: N \to M$ is normal iff $\pi_*(\pi_1(N, p))$ is a normal subgroup of $\pi_1(M, \pi(p))$ for any $p\in N$. 