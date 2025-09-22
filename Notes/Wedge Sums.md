---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Sum Topology]], [[Quotient Topology]], [[Categorical Product and Coproduct]]

**Def:** Let $\{(X_\alpha, p_\alpha) \mid \alpha < \kappa\}$ be a collection of pointed spaces. The *wedge sum* of $\{(X_\alpha, p_\alpha) \mid \alpha <\kappa\}$, denoted by $\bigvee_{\alpha<\kappa} (X_\alpha, p_\alpha)$, is defined as the quotient of $\coprod_{\alpha<\kappa} X_\alpha$, and collapsing $\{(p_\alpha, \alpha)\mid \alpha < \kappa\}$ to a point, this point is denoted as $\ast$. 

We can define $\iota_\alpha: (X_\alpha, p_\alpha) \to (\bigvee_\alpha X_\alpha, \ast)$ as the composition of the inclusion $X_\alpha \hookrightarrow \coprod_\alpha X_\alpha$, and the projection from $\coprod_\alpha X_\alpha \to \bigvee_\alpha X_\alpha$. Note that $\iota_\alpha$ is an embedding. 

**Characteristic Property of the Wedge Sum:** Let $\{(X_\alpha, p_\alpha) \mid \alpha < \kappa\}$ be a collection of pointed spaces. For any pointed space $(Y, y)$ and any collection of continuous maps $\varphi_\alpha: (X, p_\alpha) \to (Y, y)$, there exists a unique continuous map $\Phi: (\bigvee_\alpha X_\alpha, \ast) \to (Y, y)$ such for each $\alpha$ the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\left(\bigvee_{\alpha< \kappa} X_\alpha, \ast\right) \arrow[dr, dashed, "\Phi"] & \\
(X_\alpha,p_\alpha) \arrow[u, hook,"\iota_\alpha"] \arrow[r, "\varphi_\alpha"'] & (Y,y)
\end{tikzcd}
\end{document}
```

**Cor:** The wedge sum is the coproduct in the category $\mathsf{Top}_*$. 

**Cor:** The wedge sum is the unique pointed space (up to homeomorphism) satisfying the characteristic property. 

**Example:** $\Bbb R \vee \Bbb R$ is homeomorphic to the union of the $x$ axis and $y$ axis in the plane.

**Def:** A wedge sum of finitely many copies of $\Bbb S^1$ is sometimes called a *bouquet of circles*. 