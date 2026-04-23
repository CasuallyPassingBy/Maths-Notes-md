---
tags:
  - Topology
  - Topology/AlgebraicTopology
---
Subjects: [[Topology]], [[Algebraic Topology]]
Links: [[Continuous Functions and Homeomorphims]], [[Topological Connectedness]], [[Path Connectedness]], [[Local Path Connectedness]], [[Homotopy]], [[Fundamental Group of a Topological Space]], [[Proper Maps]]

**Def:** Let $E$ and $X$ be topological spaces, and let $q: E \to X$ be a continuous map. An open subset $U\subseteq X$ is said to be *evenly covered by $q$* if $q^{-1}[U]$ is a disjoint union of connected open subsets of $E$, called the *sheets of the covering over $U$*, each of which is mapped homeomorphically onto $U$ by $q$. 

Note that the sheets are connected, disjoint and open implies that they are components of $q^{-1}[U]$, and the fact $q$ restricts to a homeomorphism from each sheet to $U$ implies $U$ is connected. 

**Def:** A *covering map* is a continuos surjective map $q:E \to X$ such that $E$ is connected and locally path-connected, and every point of $X$ has an evenly covered neighbourhood. If $q:E\to X$ is a covering map, we call $E$ a *covering space of $X$,* and $X$ the *base of the covering.*

**Obs:** We see that if $q:E \to X$ is a covering map, then $X$ and $E$ are path-connected, and $X$ is locally path-connected. 

**Elementary Properties of Covering Maps:**
- Every covering map is a local homeomorphism, an open map, and a quotient map.
- An injective covering map is a homeomorphism.
- A finite product of covering maps is a covering map.
- The restriction of a covering map to a saturated, connected, open subset is a covering map onto its image. 
- If $q: E\to X$ is a covering map and $A\subseteq X$ is a locally path-connected subset, then the restriction of $A$ to each component of $q^{-1}[A]$ is a covering map onto its image. 

**Prop:** Suppose $q: E \to X$ is a covering map.
- If $X$ is $T_2$, then $E$ is too.
- If $X$ is an $n$-manifold, then $E$ is too.
- If $E$ is an $n$-manifold and $X$ is Hausdorff, then $X$ is an $n$-manifold. 

**Prop:** Let $X$ be a CW complex, and let $q: E \to X$ be a covering map. $E$ has CW decomposition for which each cell is mapped homeomorphically by $q$ onto a cell of $X$. 

**Prop:** A proper local homomorphism between connected, locally path-connected, and compactly generated Hausdorff spaces is a covering map.

**Def:** If $q:X \to Y$ is any surjective continuous map, a *section of $q$* is a continuous map $\sigma: Y \to X$ such that $q\circ \sigma = \text{Id}_Y$. If $U\subseteq Y$ is any open subset, a *local section of $q$ over $U$* is continuous map $\sigma: U \to X$ such that $q\circ \sigma =\text{Id}_U$. 

**Existence of Local Sections:** Let $q: E \to X$ be a covering map. Given any evenly covered map subset $U\subseteq X$, any $x\in I$, and any $e_0$ in the fiber over $x$, there exists a local section $\sigma: U \to E$ such that $\sigma(x) = e_0$. 

**Prop:** For every covering map $q:E\to X$, the cardinality of the fibres $q^{-1}\{x\}$ is the same for all fibres. 

If $q:E \to X$ us a covering map, the cardinality of any fiber is called the *number of sheets of the covering*. 

**Prop:** A covering map is proper iff it is finite-sheeted. 

**Prop:** Let $q:E \to X$ is a covering map. $E$ is compact iff $X$ is compact and $q$ is finite-sheeted. 

**Prop:** Let $M$ and $N$ be connected manifolds of dimension $n$, and suppose $\widetilde M\to M$ is a $k$-sheeted covering map. There is a connected sum $M \# N$ that admits a $k$-sheeted covering by a manifold $\widetilde M \# N \#\cdots \# N$ (connected sum of $\widetilde M$ with $k$ disjoint copies of $N$)

**Prop:** Every nonorientable compact surface of genus $n \ge 1$ has a two sheeted covering by an orientable one of genus $n-1$. 

**Prop:** Let $X$ be a CW complex, and $q:E \to X$ be a covering map. Then $E$ has CW decomposition for which each cell is mapped homeomorphically by $q$ onto the cell $X$. 

# Lifting Properties

**Def:** If $q:E \to X$ is a covering map and $\varphi: Y \to X$ is any continuous map, a *lift of $\varphi$* is a continuous map $\widetilde \varphi: Y\to E$ such that $q\circ\widetilde \varphi = \varphi$: 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
     & E\arrow[d,"q"] \\
     Y\arrow[r,"\varphi"']\arrow[ur,dashed,"\widetilde\varphi"] & X
   \end{tikzcd}
\end{document}
```

**Unique Lifting Property:** Let $q: E \to X$ be a covering map. Suppose $Y$ is connected, $\varphi: Y \to X$ is continuous, and $\widetilde \varphi_1, \widetilde \varphi_2: Y\to X$ are lifts of $\varphi$ that agree at some point in $Y$. Then $\widetilde \varphi_1$ is equal to $\widetilde \varphi_2$.

**Homotopy Lifting Theorem:** Let $q:E \to X$ be a covering map, and let $Y$ be a locally connected space. Suppose $\varphi_0, \varphi_1: Y\to X$ are continuous functions, $H: Y\times I \to X$ is a homotopy from $\varphi_0$ to $\varphi_1$, and $\widetilde \varphi_0: Y\to E$ is any lift of $\varphi_0$. Then there exists a unique lift $\widetilde H$ satisfying $\widetilde H_0 = \widetilde \varphi_0$. If $H$ is stationary on some subset $A\subseteq Y$, then so is $\widetilde H$. 

**Path Lifting Property:** Let $q:E\to X$ be a covering map. Suppose $f:I \to X$ is any path, and $e\in q^{-1}\{f(0)\}$. Then there exists a unique lift $\widetilde f:I \to E$ such that $\widetilde f_e(0) = e$. 

Whenever $q:E \to X$ is a covering map, we use the following notation for lifts of paths: if $f:I\to X$ is a path and $e\in q^{-1}\{f(0)\}$, then $\widetilde f_e: I \to E$ is the unique lift of $f$ such that $\widetilde f_e(0) =e$. 

**Monodromy Theorem:** Let $q: E \to X$ be a covering map. Suppose $f$ and $g$ are paths in $X$ with the same initial point and same terminal point, and $\widetilde f_e$, $\widetilde g_e$ are lifts with the same initial point $e\in E$. Then:
- $\widetilde f_e \sim \widetilde g_e$ iff $f \sim g$
- If $f\sim g$, then $\widetilde f_e(1) \sim \widetilde g_e(1)$. 

**Injectivity Theorem:** Let $q:E \to X$ be a covering map. For any point $e\in E$, the induced homomorphism $q_*: \pi_1(E, e) \to \pi_1(X, q(e))$ is injective. 

**Def:** The injectivity theorem shows that the fundamental group of a covering space is isomorphic to a certain subgroup of the fundamental group of the base. We call this the *subgroup induced by the covering*. 

# The General Lifting Problem

A natural problem arises when considering covering maps, and that is when a function has a lift, this is called as the *lifting problem*. 

**Lifting Criterion:** Suppose $q:E \to X$ is a covering map. Let $Y$ be a connected and locally path-connected space, and let $\varphi: Y \to X$ be a continuous map. Given any points $y_0\in Y$ and $e_0\in E$ such that $q(e_0) = \varphi(y_0)$, the map $\varphi$ has a lift $\widetilde \varphi: Y\to E$ satisfying $\widetilde \varphi(y_0) = e_0$ iff the subgroup $\varphi_*[\pi_1(Y, y_0)]$ of $\pi_1(X, \varphi(y_0))$ is contained in $q_*[\pi_1(E, e_0)]$, i.e., $\varphi_*[\pi_1(Y, y_0)] \le q_*[\pi_1(E, e_0)]\le \pi_1(X, \varphi(y_0))$. 

**Obs:** If $\varphi: Y \to X$ has a lift $\widetilde \varphi:Y \to E$, then we get that $\varphi_*[\pi_1(Y, y_0)] \le q_*[\pi_1(E, e_0)]$, without the additional hypothesis about $Y$.

**Lifting Maps from Simply Connected Spaces:** If $q:E \to X$ is a covering map and $Y$ is a simply connected and locally path-connected space, then every continuous function $\varphi: Y\to X$ has a lift to $E$. Given any point $y_0\in Y$, the lift can be chosen to take $y_0$ to any point in the fiber over $\varphi(y_0)$. 
 
**Lifting Maps to Simply Connected Spaces:** Suppose $q:E\to X$ is a covering map and $E$ is simply connected. For any connected and locally path-connected space $Y$, a continuous map $\varphi: Y \to X$ has a lift to $E$ iff $\varphi_*$ is the zero homomorphism from some base point $y_0\in Y$. If this is the case, then the lift can be chosen to take $y_0$ to any point in the fiber over $\varphi(y_0)$. 

# Interesting Theorems

**Borsuk-Ulam Theorem $2$-dimensional Version:** For any continuous map $F: \Bbb S^2\to \Bbb R^2$, there is a point $x\in \Bbb S^2$ such that $F(x) = F(-x)$. We get the nice corollary, there are antipodal points on earth with the same temperature and atmospheric pressure. 

**Ham Sandwich Theorem in $\Bbb R^3$:** Given three disjoint, bounded, connected open subsets $U_1, U_2, U_3\subseteq \Bbb R^3$, there exists a plane that simultaneously bisects all three, in the sense that the plane divides $\Bbb R^3$ into two half-spaces $H^+$ and $H^-$ such that for each $i$, $U_i \cap H^+$ has the same [[Lebesgue Measure|Lebesgue measure]] as $U_i \cap H^-$. 

# Generalisation

**Def:** If $N$ and $M$ are topological spaces, et us say that a map $\pi: N \to M$ is a *generalised covering map* if it satisfies all the requirements of a covering map except that $N$ might not be connected: this means that $N$ is locally path-connected, $\pi$ is surjective and continuous, and each point $p\in M$ has a neighbourhood that is evenly covered by $\pi$. 

**Lemma:** Suppose $N$ and $M$ are topological spaces and $\pi: N \to M$ is a generalised covering map. If $M$ is connected, then the restriction of $\pi$ to each component fo $N$ is a covering map. 