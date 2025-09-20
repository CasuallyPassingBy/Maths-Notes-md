---
tags:
  - CategoryTheory
---
Subjects: [[Category Theory]]
Links: [[Categories and Functors]], [[Product Topology]], [[Direct Product of Groups]],  [[Product of Rings]], [[Product of Measures]], [[Cartesian Product]]

# Product

**Def:** Let $(X_\alpha)_{\alpha \in A}$ be an indexed family of objects in a category $\sf C$. An object $P\in \text{Ob}(\mathsf C)$ together with a family of morphisms $\pi_\alpha: P \to X_\alpha$, called *projections*, is said to be the *product* of the family of objects $(X_\alpha)_{\alpha \in A}$ if given any object $Y \in \text{Ob}(\mathsf C)$ and morphisms $f_\alpha: Y \to X_\alpha$, there exists a unique morphism $f: W \to P$ such the following diagram commutes for each $\alpha$:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
&  P\arrow[d, "\pi_\alpha"] \\
Y \arrow[ur, dashed, "f"] \arrow[r, "f_\alpha"'] & X_\alpha
\end{tikzcd}
\end{document}
```

The product may or may not exist in a given category, for example in $\sf Field$ 

**Th:** If a product exists in a category, it is unique up to unique isomorphism that respects projections. More precisely, $(P, (\pi_\alpha))$ and $(P', (\pi'_\alpha))$ are both product of the family $(X_\alpha)$, there is a unique isomorphism $f: P \to P'$ satisfying $\pi'_\alpha \circ f= \pi_\alpha$ for each $\alpha$.

**Examples:**
- The product of a family of sets in $\sf Set$ is just their [[Cartesian product]]. 
- In the category $\sf Top$, the product of family of spaces $(X_\alpha)$ is the space $\prod_\alpha X_\alpha$ with the [[product topology]]. 
- In the category $\sf Top_*$, the product of family of pointed spaces $(X_\alpha, x_\alpha)$ is the pointed space $\left(\prod_\alpha X_\alpha, x\right)$ with the [[product topology]], and $x(\alpha) := x_\alpha$ for each $\alpha$.
- The product of groups $(G_\alpha)_{\alpha\in A}$ in $\sf Grp$ is their [[Direct Product of Groups|direct product group]] $\prod_\alpha G_\alpha$. 
- The product of rings $(R_\alpha)_{\alpha\in A}$ in $\sf Rng$ is their [[Product of Rings]] $\prod_\alpha R_\alpha$, where the operations are componentwise. 
- The product of vector spaces $(V_\alpha)$ in $\mathsf{Vect}_K$, $\prod_\alpha V_\alpha$ is the [[product of vector spaces]].

# Coproduct

**Def:** Let $(X_\alpha)_{\alpha \in A}$ be an indexed family of objects in a category $\sf C$. An object $S\in \text{Ob}(\mathsf C)$ together with a family of morphisms $\iota_\alpha: X_\alpha \to S$, called *injections*, is said to be the *corproduct* or *categorical sum* of the family of objects $(X_\alpha)_{\alpha \in A}$ if given any object $Y \in \text{Ob}(\mathsf C)$ and morphisms $f_\alpha:X_\alpha\to Y$ , there exists a unique morphism $f: S \to Y$ such the following diagram commutes for each $\alpha$:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
S \arrow[dr, dashed, "f"] & \\
X_\alpha \arrow[u, "\iota_\alpha"] \arrow[r, "f_\alpha"'] & Y
\end{tikzcd}
\end{document}
```

**Th:** If a coproduct exists in category, it is unique up to isomorphism that respects the injections. 

**Examples:**
- The product of a family of sets in $\sf Set$ is just their disjoint union. 
- In the category $\sf Top$, the product of family of spaces $(X_\alpha)$ is the space $\coprod_\alpha X_\alpha$ with the [[sum topology]]. 
- In the category $\sf Top_*$, the product of family of pointed spaces $(X_\alpha, x_\alpha)$ is the pointed space $\left(\bigvee_\alpha X_\alpha, x\right)$ with the [[wedge sum topology]], and $x(\alpha) := x_\alpha$ for each $\alpha$.
- The product of groups $(G_\alpha)_{\alpha\in A}$ in $\sf Grp$ is their [[Free product of Groups|free product of groups]]  $*_\alpha G_\alpha$. 
- The product of rings $(R_\alpha)_{\alpha\in A}$ in $\sf Rng$ is their [[Sum of Rings]] $\bigoplus_\alpha R_\alpha$, where the operations are componentwise. 
- The product of vector spaces $(V_\alpha)$ in $\mathsf{Vect}_K$, $\bigoplus_\alpha  V_\alpha$ is the [[Vector Subspaces#^2b44bd|direct sum]].

