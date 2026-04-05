---
tags:
  - DifferentialGeometry
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Lie Group Actions]], [[Group Actions]], [[Continuous Actions of Groups]], [[Lie Groups]], [[Representations of Groups]],  [[Lie Algebra of a Lie Group]], [[Proper Actions of Groups]]

**Characterisations of Proper Actions:**  Let $M$ be a manifold, and let $G$ be a Lie group  acting continuously on $M$. The following are equivalent.
- The action is proper.
- If $(p_i)$ is a sequence in $M$ and $(g_i)$ is a sequence in $G$ such that both $(p_i)$ and $(g_i \cdot p_i)$ converges, then a subsequence of $(g_i)$ converges.
- For every compact subset $K\subseteq M$, the set $G_K := \{g\in G \mid (g \cdot K) \cap K \neq \varnothing\}$ is compact.

**Prop:** Any continuous action by a compact Lie group on manifold is proper.

**Orbits of Proper Actions:** Suppose $\theta$ is a proper smooth action of a Lie group $G$ on a smooth manifold $M$. For any point $p\in M$, the orbit map $\theta^{(p)}: G \to M$ is a proper map, and thus the orbit $G\cdot p = \theta^{(p)}[G]$ is closed in $M$. If in addition $G_p = \{e\}$, then $\theta^{(p)}$ is a smooth embedding, and the orbit is a properly embedded submanifold. 

**Cor:** If a Lie group $G$ acts properly on a manifold $M$, then each orbit is a closed subset of $M$, and each isotropy group is compact. 

# Quotient Manifold Theorem

**Quotient Manifold Theorem:** Suppose a Lie group $G$ acts smoothly, freely, and properly on a smooth manifold $M$. Then the *orbit space* $M/G$ is a topological manifold of dimension equal to $\dim M - \dim G$, and has a unique smooth structure with the property that the quotient map $\pi: M \to M/G$ is a smooth submersion. ^d7ed22

**Prop:** Suppose a Lie group acts smoothly on a manifold $M$. Each orbit is an immersed submanifold of $M$.

**Prop:** Suppose a connected Lie group $G$ acts smoothly on a discrete space $K$. Then this action is trivial. 

**Cor:** If $G$ is a connected Lie group, then every discrete normal subgroup of $G$ is central. 

**Cor:** Let $M$ be a smooth $n$-manifold, and suppose $V$ is a smooth vector field on $M$ such that every integral curve of $V$ is periodic with the same period. We define the relation on $M$ by saying $p\sim q$ if $p$ and $q$ are in the the image of the same integral curve of $V$. Let $M /\sim$ be the quotient space, and let $\pi: M \to M /\sim$ be the quotient map. $M/\sim$ is a topological $(n-1)$-manifold has a unique smooth structure such that $\pi$ is a smooth submersion. 

**Prop:** If a Lie group $G$ acts smoothly and freely on a smooth manifold $M$, and the orbit space $M/G$ has a smooth manifold structure such that the quotient map $\pi: M \to M/G$ is a smooth submersion, then $G$ acts properly. 

**Prop:** Suppose a Lie group $G$ acts smoothly, freely, and properly on a smooth manifold $M$. Then $M$ is the total space of a [[Fibre Bundles on Smooth Manifolds|smooth fibre bundle]] with base $M/G$, model fibre $G$, and projection equal to the quotient map $\pi: M \to M/G$. In particular, $M$ is compact iff both $G$ and $M/G$ are compact.

**Def:** Any fibre bundle obtained in this way is called a *principal $G$-bundle*

**Prop:** Suppose a Lie group $G$ acts smoothly, freely, and properly 

**Th:** Suppose $M$ is a connected smooth manifold, and $\Gamma$ is a discrete group acting smoothly, freely and properly on $M$. Then the quotient space $M/\Gamma$ is a topological manifold and has a unique smooth structure such that $\pi: M \to M/\Gamma$ is a [[Smooth Covering Maps|smooth]] [[Covering Maps#^06bb5b|normal]] covering map. ^2c0355

**Prop:** Let $\Gamma$ be a discrete group acting smoothly, freely, and properly on a connected smooth manifold $M$. If a [[Riemannian Metrics on Smooth Manifolds|Riemannian metric]] $g$ on $M$ is a pullback of a metric on $M$ by the quotient map $\pi: M\to M/\Gamma$ iff $\Gamma$ acts by isometry. 

**Prop:** Let $M$ be a smooth manifold, and let $\pi: E\to M$ be a smooth covering map. With the the discrete topology, the automorphism group $\text{Aut}_\pi(E)$ acts smoothly, freely, and properly on $E$.

**Cor:** Let $\pi: N \to M$ be a smooth normal covering map, then $M$ is diffeomorphic to the quotient manifold $N/\text{Aut}_\pi(N)$. 

**Prop:** Given that $\pi: \tilde G\to G$ is a universal covering map, then the covering group $\text{Aut}_\pi(\tilde G)$ is isomorphic to $\pi_1(G, e)$. Then we can prove that the fundamental group of a connected Lie group is abelian.

**Prop:** Let $M$ be a smooth manifold, and let $\pi: E \to M$ be a smooth vector bundle over $M.$ Suppose $\Gamma$ is a discrete group acting smoothly, freely and properly on both $E$ and $M$. Suppose further that $\pi$ is $\Gamma$-equivariant, and each $p\in M$ and each $g\in \Gamma$, the map $E_p$ to $E_{g\cdot p}$ is given by $v \mapsto g \cdot v$ is linear. Then $E/\Gamma$ can be given the structure of a smooth vector bundle over $M/\Gamma$ un such a way that the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
E \arrow{r}\arrow{d}& E/\Gamma \arrow{d} \\
M \arrow{r}& M/\Gamma
\end{tikzcd}
\end{document}
```
