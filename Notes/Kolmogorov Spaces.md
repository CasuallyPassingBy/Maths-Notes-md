---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Topological Subspaces]], [[Topological Indistinguishability]], [[Quotient Topology]], [[Product Topology]]

**Def:** A topological space $(X, \tau)$ is called a $T_0$ *space* (we also say that $\tau$ is a *$T_0$ topology*) if any two points $x, y \in X$, there's a $U \in \tau$ such that $U$ contains $x$ or $y$, but only one of them. In other words, any two points $x, y \in X$ there's a $U\in \tau$ such that $|U \cap \{x, y\}| = 1$. 

Not every space is $T_0$. 
- Pseudometric spaces
- Seminormed spaces

**Prop:** $T_0$ is a topological property, meaning invariant under homeomorphisms. 

**Prop:** Every subspace of a $T_0$ space is $T_0$. $T_0$ is a hereditary property. 

**Obs:** $T_0$ is a topological property that is preserved under refinement the topology. This means that if $(X, \tau_1)$ is $T_0$ and $\tau_1 \subseteq \tau_2$ topologies then $(X,\tau_2)$ is $T_0$. 

**Th:** For every $T_0$ space we have $|X| \le 2^{w(X)}$.  

**Prop:** If $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ is a family of nonempty $T_0$ spaces, then the product $\prod_{\alpha < \kappa} X_\alpha$ is a $T_0$ space iff for each $\alpha < \kappa$, $X_\alpha$ is a $T_0$ space. 

**Prop:** If $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ is a family of nonempty $T_0$ spaces, then the sum $\bigoplus_{\alpha < \kappa} X_\alpha$ is a $T_0$ space iff for each $\alpha < \kappa$, $X_\alpha$ is a $T_0$ space. 

**Th:** A topological space $(X, \tau)$ os a $T_0$ space iff for each $x, y \in X$ with $x \neq y$ we have that $\text{cl}(\{x\}) \neq \text{cl}(\{y\})$. 

**Cor:** A topological space $(X, \tau)$ os a $T_0$ space iff all point are topologically distinguishable

**Prop:** Topological indistinguishability of points is an equivalence relation. Then if we make denote the quotient of topological space $X$ with respect to this equivalence relation, the quotient space is always $T_0$. 

**Def:** If we denote $\sim$ to be denote topological indistinguishability of points, then $KQ(X)$ or $KX$ is called the *Kolmogorov quotient*, and it is defined as $X/\sim$.  ^93759c

**Universal Property:** For any continuous map $f: X \to Y$ to a $T_0$-space $Y$ there exists a unique $f': KQ(X) \to Y$ such that $f' \circ \pi = f$ where $\pi$ is the natural projection of $X$ onto $KQ(X)$. 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[dr,"f"'] \arrow[r, "\pi"] & KQ (X) \arrow[d, dashed,"f'"] \\ 
& Y
\end{tikzcd}
\end{document}
```
