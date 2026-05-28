---
tags:
  - Topology
aliases:
  - Final Topologies
  - Co-Induced Topology
  - Inductive Topology
---
Subjects: [[Topology]]
Links: [[Continuous Functions and Homeomorphims]], [[Topological Spaces]], [[Bases, Subbases, and Local Basis for Topological Spaces]], [[Weak Topology]]

We would like to find the dual of the [[Weak Topology]]. 

**Prop:** Let $(Y, \tau)$ be a topological space, $X$ be a set and $f: X \to Y$. The set $$\;_f \tau := f^{-1}[\tau]$$is a topology on $X$. 

**Def:** The topology$\;_f \tau$ is called the *initial topology on $X$ defined by $f$ and $(Y, \tau)$*, or *the weak topology on $X$ induced by $f$*. 

**Prop:** The topology$\;_f \tau$ is the smallest (or weakest) of the topologies of $X$ that make the function $f$ continuous.

**Universal Property of the Weak Topology:** For any topological space $Z$, a function $g: Z \to (X, \,_f \tau)$ is continuous iff $g\circ f$ is continuous. 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
Z \arrow[dr,"f\circ g"'] \arrow[r, "g"] & (X, \,_f \tau) \arrow[d, "f"] \\ 
& Y
\end{tikzcd}
\end{document}
```

Additionally, $\,_f\tau$ is the only topology on $X$ that satisfies the condition above. 

We can generalise this to a family of functions and topological spaces. 

Let $\{(Y_\alpha, \kappa_\alpha) \mid \alpha < \kappa\}$ be a family of topological spaces and $\mathcal F = \{f_\alpha: X \to Y_\alpha \mid \alpha < \kappa\}$ be a family of functions defined on $X$. We may denote by $\,_{\mathcal F} \tau$ to be the smallest topology on $X$ that make each $f \in \mathcal F$ continuous.

**Th:**
- The family $\mathcal S = \{f^{-1}_\alpha[A] \mid \alpha <\kappa, A \in \tau_\alpha\} = \bigcup_{\alpha< \kappa} f^{-1}_\alpha[\tau_\alpha]$ is a subbase of the topology $\,_{\mathcal F} \tau$ 
- $\,_{\mathcal F} \tau$ is the unique topology that satisfies the following: for each topological space $Z$ and any function $g: Z \to (X,\,_\mathcal F \tau)$, $g$ is continuous iff $f\alpha \circ g$ is continuous for each $\alpha <\kappa$. 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
Z \arrow[dr,"f_\alpha \circ g"'] \arrow[r, "g"] & (X, \,_\mathcal F \tau) \arrow[d, "f_\alpha"] \\ 
& Y_\alpha
\end{tikzcd}
\end{document}
```

**Def:** Let $\mathcal C = \{ (X_\alpha, \tau_\alpha)\mid \alpha < \kappa\}$ be a collection of topological space, $X$ a set, and $\mathcal F = \{f_\alpha: X \to X_\alpha\mid \alpha<\kappa\}$ be a collection of functions. The topology $\,_{\mathcal F} \tau$ on $X$ is called *the weak topology* or *the initial topology induced by $\mathcal F$ (and $\mathcal C$).* 
