---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Compactness]], [[Continuous Functions and Homeomorphims]], [[Convergence of Sequences]] [[Open and Closed Functions]]

**Def:** If $X$ and $Y$ are topological spaces, a map $f:X \to Y$ is said to be *proper* if for every compact set $K \subseteq N$, the inverse image $f^{-1}[K]$ is compact. 

**Lemma:** Suppose $X$ is a compact space and $Y$ is Hausdorff space. Then every continuous map $f:X \to Y$ is proper.

**Def:** A subset $A\subseteq X$ is said to be saturated with respect to a map $f:X \to Y$ if $A = f^{-1}[f[A]]$.

**Lemma:** Suppose $f: X \to Y$ is a proper map between topological spaces, and $A \subseteq M$ is any subsets that is saturated with respect to $F$. Then $F|_A :A \to F[A]$ is proper.

**Lemma:** Let $F: X \to Y$ be a continuous map between Hausdorff spaces. If there exists a continuous left inverse for $F$, then $F$ is proper. 

**Prop:** Suppose $X$ and $Y$ are topological spaces, and $f:X \to Y$ is a continuous map.
- If $f$ is a closed and compact map, then $f$ is proper.
- If $f$ is a topological embedding, then $f$ is proper.

**Sequential Characterisation of Proper Maps:** If $X$ is a second countable $T_2$ space and $F$ is continuous map that takes sequences diverging to infinity in $X$ to sequences diverging to infinity in $Y$, then $F$ is proper.

**Cor:** Suppose $M$ and $N$ are topological manifolds. A continuous map $F: M \to N$ is proper iff for every sequence $(x_n)_{n <\omega}$ in $M$ that escapes to infinity, $(F(x_n))_{n<\omega}$ escapes to infinity in $N$.

**Proper Maps are Closed:** Suppose $X$ is any topological space, $Y$ is [[compactly generated]] $T_2$ space, and $f:X \to Y$ a proper continuous map. Then, $f$ is a closed map.

**Cor:** If $X$ is a topological space and $Y$ is a compactly generated Hausdorff space, an embedding $f:X\to Y$ is proper iff it has closed image.

**Cor:** Suppose $f$ is a proper continuous map from a topological space to a compactly generated $T_2$ space.
- If $f$ is surjective, it is a quotient map.
- If $f$ is injective, it is a topological embedding.
- If $f$ is bijective, it is a homeomorphism.
