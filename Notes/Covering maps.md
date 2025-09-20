---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Continuous Functions and Homeomorphims]], [[Topological Connectedness]]

**Def:** Let $\pi: X \to Y$ be a continuous surjective map between connected, locally path connected spaces with the property that every point $y\in Y$ has a neighbourhood $V$ that is *evenly covered*, meaning that $U$ is connected and each component of $\pi^{-1}[U]$ us mapped homoemorphically onto $U$ by $\pi$. If $\pi$ satisfies this, is called a covering map. 

**Def:** Let $X$ and $Y$ be topological spaces, and let $\pi X \to Y$ be a covering map. A *covering transformation* or *deck transformation* of $\pi$ is a homemorphism $\varphi: X \to X$ such that $\pi \circ \varphi = \pi$
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
X \arrow[rr, "\varphi"] \arrow[dr, "\pi"] && X \arrow[dl, "\pi"'] \\
& Y
\end{tikzcd}
\end{document}
```
The set $\mathcal C_\pi(X)$ of all covering transformations, called the *covering group* of $\pi$, is a group under composition, acting on $X$ on the left. The covering group is the key to constructing smooth manifolds covered by $X$. ^78c0a4

**Def:** A covering map $\pi: X \to Y$ is said to be *normal* if the covering group $\mathcal C_\pi(X)$ acts transitively on the fibres of $\pi$. ^06bb5b