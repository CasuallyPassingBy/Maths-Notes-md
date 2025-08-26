---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Compactness]], [[Continuous Functions and Homeomorphims]], [[Convergence of Sequences]]

**Def:** If $X$ and $Y$ are topological spaces, a map $f:X \to Y$ is said to be *proper* if for every compact set $K \subseteq N$, the inverse image $f^{-1}[K]$ is compact. 

**Lemma:** Suppose $X$ is a compact space and $Y$ is Hausdorff space. Then every continuous map $f:X \to Y$ is proper.

**Def:** A subset $A\subseteq X$ is said to be saturated with respect to a map $f:X \to Y$ if $A = f^{-1}[f[A]]$.

**Lemma:** Suppose $f: X \to Y$ is a proper map between topological spaces, and $A \subseteq M$ is any subsets that is saturated with respect to $F$. Then $F|_A :A \to F[A]$ is proper.

**Lemma:** Let $F: X \to Y$ be a continuous map between Hausdorff spaces. If there exists a continuous left inverse for $F$, then $F$ is proper. 

**Sequential Characterisation of Proper Maps:** Suppose $M$ and $N$ are topological manifolds. A continuous map $f: M \to N$ is proper iff for every sequence $(x_n)_{n <\omega}$ in $M$ that escapes to infinity, $(F(x_n))_{n<\omega}$ escapes to infinity in $N$.

**Prop:** Suppose $f: M \to N$ is a proper continuous map between topological manifolds, then $f$ is closed.