---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]]

**Def:** If $G$ is a group and $X$ is a set, a *left action* of $G$ on $X$ is a map $\alpha: G\times X \to X$, often written $(g, p) \mapsto g\cdot p$, that satisfies for all $x\in X$ and $g_1, g_2\in G$:
- $g_1 \cdot (g_2 \cdot x) = (g_1g_2) \cdot x$
- $e\cdot x =x$ 

We call $X$ a *$G$-set.* If $X$ has a left action of $G$ on $X$, $(X, \alpha)$.

**Def:** For any $x\in X$, the *orbit* of $x$ under the action is the set $$\text{Orb}_\alpha(x) = G \cdot x := \{g\cdot x \mid g\in G\},$$the set of all images of $x$ under the action by elements of $G$.

**Def:** Given $x\in X$, the *isotropy group* of $x$ or the *stabiliser of $x$*, denoted by $G_x$, is the set of elements $g\in G$ that fix $x$: $$G_x := \{g\in G \mid g\cdot x =x\} $$ 

# Types of Actions

The action is *transitive* if for any two points $x, y \in X$, there is a group element $g\in G$ such that $\alpha(g, x) = y$, or equivalently if the orbit of any point is all of $X$

The action is said to be *free* if the only element of $G$ that fixes any element of $X$ is the identity: $\alpha(g, x) = x$ implies that $g = e$. This is equivalent to the requirement that $G_x = \{e\}$ for every $p\in X$. 

# Equivariant Maps

Suppose $X$ and $Y$ are both $G$-sets. A map $F: X \to Y$ is said to be *equivariant* with repect to the given $G$-action if for each $g \in G$, $$F(g \cdot x) = g \cdot F(x).$$Equivalently, if $\theta$ and $\varphi$ are the given actions on $X$ and $Y$, respectively, $F$ is equivaraint if the following diagram commutes for each $g \in G$: 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[r, "F"] \arrow[d, "\phi_g"'] & Y \arrow{d}{\phi_g} \\
X \arrow[r, "F"'] & Y
\end{tikzcd}
\end{document}
```

Equivariant maps are homomorphism in the [[Categories and Functors|category]] of $G$-sets (for a fixed $G$). Hence they are also known as $G$-morphisms, $G$-maps, or $G$-homomorphisms. Isomorphisms of $G$-sets are simply bijective equivariant maps. 

**Example:** Let $G$ and $H$ be groups, and $\phi: G \to H$ be a Lie group homomorphism. There is a natural action of $G$ on itself by left-translation. We define a left action $\theta$ of $G$ on $H$ by $$\theta(g, h) = F(g) h.$$ With respect to theses $G$-actions, $F$ is an equivariant. 