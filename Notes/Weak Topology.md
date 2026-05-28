---
tags:
  - Topology
aliases:
  - Initial Topology
  - Induced Topology
  - Projective Topology
---
Subjects: [[Topology]]
Links: [[Strong Topology]], [[Continuous Functions and Homeomorphims]], [[Topological Spaces]], [[Bases, Subbases, and Local Basis for Topological Spaces]]

We would like to find the dual of the [[Strong Topology]].

Let's consider $X$ a topological space, $Y$ a set, and $f:X \to Y$. We would like to construct the the finest topology of $Y$ that makes $f$ continuous, denoted as $\tau_f$, and we satisfies the property:
- For any topological space $Z$, a function $g: Y \to Z$ is continuous iff $g\circ f$ is continuous

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[dr,"g\circ f"'] \arrow[r, "f"] & Y \arrow[d, "g"] \\ 
& Z
\end{tikzcd}
\end{document}
```

We propose a candidate for $\tau_f$ as $\{E \subseteq Y \mid f^{-1}[E] \in \tau\}$. 

**Th:**
- The family $\tau_f$ is a topology on $Y$.
- The function $f:(X, \tau) \to (Y, \tau_f)$ is continuous and $\tau_f$ is the finest topology on $Y$ that satisfy this property
- $\tau_f$ is the only topology on $Y$ satisfies the property above.

We can generalise this technique, in an analogue way as we did with the initial topology. Let $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ be a family of nonempty topological spaces and $\mathcal F = \{f_\alpha: X_\alpha \to Y\mid \alpha < \kappa\}$, we can define the collection of subsets $\tau_\mathcal F$ of all subsets of $Y$ that satisfy $f_\alpha^{-1}[E] \in \tau_\alpha$ for each $\alpha < \kappa$. 

**Th:**
- The collection $\tau_\mathcal F$ is a topology on $Y$.
- Each $f_\alpha: (X_\alpha, \tau_\alpha) \to (Y, \tau_\mathcal F)$ is continuous for each $\alpha < \kappa$, and $\tau_\mathcal F$ is the finest topology of $Y$ with this property.
- $\tau_\mathcal F$ is the unique topology on $Y$ that satisfies: For any topological space $Z$, a function $g: (Y, \tau_\mathcal F) \to Z$ is continuous iff $g\circ f_\alpha$ is continuous for each $\alpha < \kappa$. 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X_\alpha \arrow[dr,"g\circ f_\alpha"'] \arrow[r, "f_\alpha"] & (Y, \tau_\mathcal F) \arrow[d, "g"] \\ 
& Z
\end{tikzcd}
\end{document}
```

**Def:** A topology $\tau_\mathcal F$ is called the *strong topology* or the *final topology*,on $Y$ defined by the family of functions $\mathcal F$ and the family of topological spaces $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$. 