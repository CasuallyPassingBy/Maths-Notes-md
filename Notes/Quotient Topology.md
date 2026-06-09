---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Strong Topology]], [[Equivalence Relations and Partitions]]

**Def:** Let $(X, \tau)$ is a topological space, $Y$ a set, and $q: X \to Y$ a surjective function. The pair $(Y, \tau_q)$, where $\tau_q$ is the [[Strong Topology]] on $Y$ defined by $q$ and $(X,\tau)$, we called the *quotient space* determined by $(X, \tau)$ and $q$. By the definitions of the final topology we get that $$\tau_q = \{A \subseteq Y \mid q^{-1}[A] \in\tau\}.$$
**Th:** If $(Y, \tau_q)$ is the quotient space determined by $q: (X, \tau) \to Y$, then $\tau_q$ is the finest topology on $Y$ that makes $q$ continuous, and is the unique topology on $Y$ that satisfy: for any topological space $Z$ and any $g:(Y, \tau_q) \to Z$, $g$ is continuous iff $g \circ q$ is continuous: 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[dr,"g\circ q"'] \arrow[r, "q"] & (Y, \tau_q) \arrow[d, "g"] \\ 
& Z
\end{tikzcd}
\end{document}
```

Given a continuous surjective function $q$ with domain $(X, \tau_X)$ and codomain $(Y, \tau_Y)$. Then we get that $\tau_Y \subseteq \tau_q$. So a natural question is when $\tau_Y = \tau_q$. 

**Def:** If $\tau_Y = \tau_q$ we say that $q$ is a *quotient function* or *identification*. 

**Prop:** Let $X$ and $Y$ be topological space and $q:X \to Y$ be a function and surjective. If $q$ is an open or closed function, then the topology of $Y$ coincides with the final topology on $Y$ defined by $q$.

**Remainder:**
- Let $\mathcal D$ be a partition of a set $X$. The map $q: X \to \mathcal D$  where $q$ maps each $x\in X$ to the unique element of $D$ that contains it, is called the *natural projection associated with $\mathcal D$.*

**Def:** Let $\mathcal D$ be a partition of a topological space $(X, \tau)$. Consider the set $\mathcal D$ with the topology $\tau_\mathcal D$ defined as follows: $A \in \tau_\mathcal D$ iff $\bigcup A\in \tau$. The $(\mathcal D, \tau_\mathcal D)$ is called the *partition space of $X$.*

**Prop:** For any partition $\mathcal D$ of a topological space $(X, \tau)$ is the quotient topology defined by the natural projection $q: X  \to \mathcal D$.

**Prop:** Let $\mathcal D$ be a partition of the topological space $(X, \tau)$, then the natural projection $q: X \to \mathcal D$ has a continuous inverse.

We can also consider equivalence relations since there's a natural bijection between the two.

**Th:** If $Y$ has the quotient topology induced by the continuous and surjective function $f: X \to Y$, then there's a homeomorphism $h$ to $Y$ to the partition space $\mathcal D := \{f^{-1}\{y\} \mid y \in Y\}$. Furthermore, $h \circ f$ is equal to the natural projection $q: X \to \mathcal D$. 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[dr,"q = h\circ f"'] \arrow[r, "f"] & (Y, \tau_f) \arrow[d, "h", "\cong"'] \\ 
& (\mathcal D, \tau_\mathcal D)
\end{tikzcd}
\end{document}
```

**Passing to the Quotient:** Suppose $q:X \to Y$ is a quotient map, $Z$ is a topological space, and $f:X \to Z$ is any continuous that is constant on the fibres of $q$. Then there exists a unique continuous map $\tilde f:Y \to Z$ such that $f = \tilde f\circ q$
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[dr,"f"'] \arrow[r, "q"] & Y \arrow[d,dashed, "\tilde f"] \\ 
& Z
\end{tikzcd}
\end{document}
```
In this situation, we say that $f$ *passes to the quotient* or *descends to the quotient*. 

**Prop:** Suppose $P$ is a second countable space and $M$ is a quotient space of $P$. If $M$ is locally euclidean, then it is second countable. Thus if $M$ is locally Euclidean and $T_2$, then it is a manifold. 

**Prop:** Suppose $q:X \to Y$ is an open quotient map. Then $Y$ is Hausdorff iff the set $\{(x_1, x_2)\in X \times X \mid q(x_1) = q(x_2)\}$ is closed in $X\times X$

**Cor:** Suppose $\sim$ is an equivalence relation on a space $X$. If the quotient map $X \to X/\sim$ is an open map, then $X/\sim$ is Hausdorff iff $\sim$ is closed in $X\times X$. 

**Def:** Suppose $q:X \to Y$ is a map. A subset $U \subseteq X$ is said to be *saturated with respect to $q$* if $U = q^{-1}[V]$ for some $V\subseteq Y$.

**Prop:** Let $q:X \to Y$ be any map. For any subset $U \subseteq X$. the following are equivalent:
- $U$ is saturated
- $U = q^{-1}[q[U]]$
- $U$ is the union of fibres
- if $x\in U$, then every point $y\in X$ such that $q(x) = q(y)$ is also in $U$.

**Prop:** A continuous surjective map $q:X \to Y$ is quotient map iff it takes saturated open sets to open subsets, or saturated closed subsets to closed sets.

**Properties of Quotient Maps:**
- Any composition of quotient maps is a quotient maps.
- An injective quotient map is a homeomorphism.
- If $q:X \to Y$ is a quotient map, a subset $K \subseteq Y$ is closed iff $q^{-1}[K]$ is closed in $X$.
- If $q:X \to Y$ is a quotient map and $U\subseteq X$ is a saturated open or closed subsets, then the restriction $q|_U: U \to q[U]$ is a quotient map.
- If $\{q_\alpha:X_\alpha \to Y_\alpha \mid \alpha < \kappa\}$ is an indexed family of quiteint maps, then the map $q: \coprod_{\alpha < \kappa} X_\alpha \to\coprod_{\alpha < \kappa} Y_\alpha$ whose restriction to each $X_\alpha$ is equal to $q_\alpha$ is a quotient map.

**Prop:** If $q:X\to Y$ is a surjective continuos maps that is also open or closed, then it is a quotient map. 
# Cones

If $X$ is any topological space the quotient $(X\times [0, 1])/(X \times \{0\})$ obtained from the 'cylinder' $X\times I$ by collapsing one end point to a point is called the *cone on $X$*, and is denoted by $CX$. 

We can identify $X$ and $X \times \{1\}$, thus we consider $X$ as a subspace of $CX$.

If $X$ is topological space, then
- $CX$ is path connected.
- $CX$ is locally connected iff $X$ is locally path connected iff $X$ is connected.