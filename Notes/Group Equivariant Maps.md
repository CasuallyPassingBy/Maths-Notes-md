---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Group Actions]]

Suppose $X$ and $Y$ are both $G$-sets. A map $F: X \to Y$ is said to be *equivariant* with respect to the given $G$-action if for each $g \in G$, $$F(g \cdot x) = g \cdot F(x).$$Equivalently, if $\theta$ and $\varphi$ are the given actions on $X$ and $Y$, respectively, $F$ is equivariant if the following diagram commutes for each $g \in G$: 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[r, "F"] \arrow[d, "\phi_g"'] & Y \arrow{d}{\phi_g} \\
X \arrow[r, "F"'] & Y
\end{tikzcd}
\end{document}
```

Equivariant maps are homomorphism in the [[Categories and Functors|category]] of $G$-sets (for a fixed $G$). Hence they are also known as $G$-morphisms, $G$-maps, or $G$-homomorphisms. Isomorphisms of $G$-sets are simply bijective equivariant maps. Note that the inverse of a $G$-isomorphism is another $G$-isomorphism

**Example:** Let $G$ and $H$ be groups, and $\phi: G \to H$ be a Lie group homomorphism. There is a natural action of $G$ on itself by left-translation. We define a left action $\theta$ of $G$ on $H$ by $$\theta(g, h) = F(g) h.$$ With respect to theses $G$-actions, $F$ is an equivariant. 

**Properties of $G$-Equivariant Maps:** Suppose $G$ is a group, and $X$, $Y$ are $G$-sets.
- If $G$ acts transitively on $X$, then any two $G$-equivariant maps from $X$ to $Y$ that agree on one element of $X$ are identical.
- If $X$ is nonempty, and $G$ acts transitively on $Y$, then every $G$-equivariant map from $X$ to $Y$ is surjective. 
- If $G$ acts transitively on $X$, then given $x\in X$ and $y\in Y$, there exists a (necessarily unique) $G$-equivariant map $\varphi:X\to Y$ satisfying $x\mapsto y$ iff $G_x \subseteq G_y$. 

**$G$-Set Isomorphism Criterion:** Suppose $X$ and $Y$ are $G$-sets with a transitive action. 
- Given $x\in X$ and $y\in Y$, there exists a necessarily unique $G$-isomorphism $\varphi:X \to Y$ taking $x \mapsto y$ iff $G_x = G_y$. 
- $X$ and $Y$ are $G$-isomorphic iff they have the same isotropy type. 

**Def:** If $X$ is a $G$-set, a $G$-isomorphism from $X$ to $X$ is called a *$G$-automorphism of $X$*. We know that the set of $G$-automorphisms from a group, see [[Automorphism Group|this]], and it is called the *$G$-automorphism group of $X$*, and it is denoted by $\text{Aut}_G(X)$. 

**Prop:** Suppose $X$ is transitive $G$-set. For any $x, y\in X$, there exists a necessarily unique $\varphi\in \text{Aut}_G(x)$ such that $x\mapsto y$ iff $G_x = G_y$.

**Characterisation of $G$-Automorphism Groups:** Let $X$ be a transitive $G$-set, and let $x\in X$. For each $g\in N_G(G_x)$, there is a unique $G$-automorphism $\varphi_g: X \to X$ such that $\varphi_g(x) = g\cdot x$. The map $g\mapsto \varphi_g$ is a surjective homomorphism from $N_G(G_x)$ to $\text{Aut}_G(X)$ whose kernel is $G_x$, and thus descends to an isomorphism $$N_G(G_x)/G_x \cong \text{Aut}_G(X),$$where $N_G(G_x)$ is the [[Cauchy and Sylow Theorems|normalizer]] of $G_x$ in $G$. 