---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Fundamental Group of a Topological Space]], [[Compact Surfaces]], [[The Seifert-Van Kampen Theorem]], [[Fundamental Group of CW Complexes]]

**Fundamental Groups and Polygonal Presentations:** Let $M$ be a topological space with a polygonal presentation $\langle a_1,\dots, a_n \mid W\rangle$ with one face, in which all vertices identified with a single point. Then $\pi_1(M)$ has the presentation $\langle a_1,\dots, a_n\mid W\rangle$. 

**Fundamental Groups of Compact Surfaces:** The fundamental groups of compact connected surfaces have the following presentations:
- $\pi_1(\Bbb S^2)\cong \langle \varnothing \mid \varnothing\rangle$ 
- $\pi_1(\mathbb{T^2 \# \cdots \# T^2}) \cong \langle \beta_1, \gamma_1,\dots, \beta_n,\gamma_n \mid \beta_1 \gamma_1\beta_1^{-1}\gamma_1^{-1}\cdots\beta_n \gamma_n\beta_n^{-1}\gamma_n^{-1} = 1\rangle$ 
- $\pi_1(\mathbb{RP^2\#\cdots \# RP^2})\cong \langle \beta_1\dots, \beta_n\mid \beta_1^2\cdots \beta_n^2 = 1\rangle$ 

Note that $\pi_1(\Bbb T^2) \cong \langle\beta,\gamma\mid \beta \gamma = \gamma\beta\rangle \cong \Bbb Z^2$, and $\pi_1(\Bbb{RP}^2) \cong \langle \beta\mid \beta^2 = 1\rangle \cong \Bbb Z/2\Bbb Z$.

**Prop:** The fundamental groups of compact surfaces have the following abelianizations: $$\begin{align*}\pi_1(\Bbb S^2)^\text{ab} &= \{e\} \\\pi_1(\mathbb{T^2 \# \cdots \# T^2})^\text{ab} &\cong \Bbb Z^{2n} \\
 \pi_1(\mathbb{RP^2\#\cdots \# RP^2})^\text{ab} &\cong  \Bbb Z^{n-1}\times \Bbb Z/2\Bbb Z\end{align*}$$
 **Classification of Compact Surfaces, Part II:** Every nonempty, compact, connected $2$-manifold is homeomorphic to exactly one the surfaces $\Bbb S^2$, $\mathbb{T^2 \# \cdots \# T^2}$ or $\mathbb{RP^2\#\cdots \# RP^2}$. 

**Cor:** A connected sum of projective planes is not orientable.

**Cor:** Orientability of compact surface is a topological invariant. 

**Cor:** The Euler characteristic of a surface presentation is a topological invariant. 

**Def:** If $M$ is a compact surface, we can define the *Euler characteristic of $M$*, denoted by $\chi(M)$, to be the Euler characteristic of the presentation of that surface. 

**Lemma:** Suppose $M$ and $N$ are nonempty, compact, connected $2$-manifolds. $M$ and $N$ are homeomorphic iff they have isomorphic fundamental groups.

**Prop:** Suppose $M$ and $N$ are nonempty, compact, connected $2$-manifolds. Any two connected sums of $M$ and $N$ are homeomorphic. 