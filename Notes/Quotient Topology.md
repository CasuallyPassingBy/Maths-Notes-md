---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Final Topology]], [[Equivalence Relations and Partitions]]

**Def:** Let $(X, \tau)$ is a topological space, $Y$ a set, and $q: X \to Y$ a surjective function. The pair $(Y, \tau_q)$, where $\tau_q$ is the [[final topology]] on $Y$ defined by $q$ and $(X,\tau)$, we called the *quotient space* determined by $(X, \tau)$ and $q$. By the definitions of the final topology we get that $$\tau_q = \{A \subseteq Y \mid q^{-1}[A] \in\tau\}.$$
**Th:** If $(Y, \tau_q)$ is the quotient space determined by $q: (X, \tau) \to Y$, then $\tau_q$ is the finest topology on $Y$ that makes $q$ continuous, and is the unique topology on $Y$ that satisfy: for any topological space $Z$ and any $g:(Y, \tau_q) \to Z$, $g$ is continuous iff $g \circ q$ is continuous: 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
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
\begin{tikzcd}
X \arrow[dr,"q = h\circ f"'] \arrow[r, "f"] & (Y, \tau_f) \arrow[d, "h", "\cong"'] \\ 
& (\mathcal D, \tau_\mathcal D)
\end{tikzcd}
\end{document}
```
