---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Fundamental Group of a Topological Space]], [[Homotopy]]

**Def:** Let $\varphi: X \to Y$ be a continuous map. We say that another continuous map $\psi: Y \to X$ is a *homotopy inverse for $\varphi$* if $\psi \circ \varphi \simeq \text{Id}_X$ and $\varphi \circ \psi \simeq \text{Id}_Y$. If there exists a homotopy inverse for $\varphi$, then $\varphi$ is called a *homotopy equivalence*. In this case, we say that $X$ is *homotopy equivalent* to $Y$, or $X$ has the *same homotopy type* as $Y$, and we write $X\simeq Y$. 

Properties that are preserved by homotopy equivalences are called *homotopy invariants*.

**Prop:** Homotopy equivalence is an equivalence relation on the class of all topological spaces. 

**Prop:** The Möbius band is homotopy equivalent to $\Bbb S^1$. 

**Def:** Suppose $X$ is a topological space, $A$ is a subspace of $X$, and $r:X \to A$ is a retraction. We say that $r$ is a *deformation retraction* if $\iota_A \circ r$ is homotopic to the identity map of $X$, where $\iota_A:A \hookrightarrow X$ is the inclusion map. If there exists a deformation retraction from $X$ to $A$, then $A$ is said to be a *deformation retract* of $X$. 

A retraction $r:X \to A$ is called a *strong deformation retraction* if $\text{Id}_X$ is homotopic to $\iota_A \circ r$ relative to $A$, which means that there is a homotopy from $\text{Id}_X$ to $\iota_A\circ r$ that is stationary on $A$. In this case, we say that $A$ is a *strong deformation retract* of $X$.

We see that a subspace $A\subseteq X$ and $H:X \times I \to X$ a homotopy such that
1. $H(x, 0) = x$ for all $x\in X$.
2. $H(x, 1) \in A$ for all $x\in X$,
3. $H(a,1) = a$ for all $a\in A$,
4. $H(a, t) = a$ for all $a\in A$ and all $t\in [0, 1]$. 
$A$ is a deformation retract of $X$ iff it satisfies conditions $(1)-(3)$. Additionally, $A$ is strong deformation retract of $X$ iff it satisfies conditions $(1)-(4)$. 

**Prop:** For any $n \ge 1$, $\Bbb S^{n-1}$ is a strong deformation retract of $\Bbb R^n\setminus\{0\}$ and of $\bar{\Bbb B}^n\setminus \{0\}$.

**Cor:** For $n \ge 3$, both $\Bbb R^n \setminus\{0\}$ and $\bar{\Bbb B}^n\setminus\{0\}$ are simply connected.

**Def:** Let $X$ be any space. If the identity map of $X$ is homotopic to a constant map, we say that $X$ is *contractible*. 

**Prop:** Let $X$ be a topological space. The following statements are equivalent.
- $X$ is contractible.
- $X$ is homotopy equivalent to a one-point space.
- Each point of $X$ is a deformation retract of $X$. 

Since a one-point space is simply connected, wee that every contractible space is simply connected. 

**Cor:** [[Conservative Fields#^525c9d|Star shaped]] subset of $\Bbb R^n$ is contractible.

**Prop:** Let $X$ and $Y$ be topological spaces. If either $X$ or $Y$ is contractible, then every continuous map from $X$ to $Y$ is homotopic to a constant map. 

**Lemma:** Suppose $\varphi, \psi:X \to Y$ are continuous, and $H: \varphi \simeq \psi$ is a homotopy. For any $p\in X$, let $h$ be the path in $Y$ from $\varphi(p)$ and $\psi(p)$ defined by $h(t):= H(p, t)$, and let $\Phi_h: \pi_1(Y, \varphi(p)) \to \pi_1(Y, \psi(p))$ be an isomorphism defined by $\Phi_h([f]) := [\bar h] \cdot [f]\cdot [h]$, then the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
& \pi_1(X, p)\arrow[dl, "\varphi_*"']\arrow[dr, "\psi_*"]& \\
\pi_1(Y, \varphi(p))\arrow[rr, "\Phi_h"'] && \pi_1(Y, \psi(p)) 
\end{tikzcd}
\end{document}
```

**Homotopy Invariance of $\pi_1$:** If $\varphi:X \to Y$ is a homotopy equivalence, then for any point $p\in X$, $\varphi_*: \pi_1(X, p) \to \pi_1(Y. \varphi(p))$ is an isomorphism.

**Def:** Let $X$ and $Y$ be topological spaces, and let $f:X \to Y$ be a continuous map. Define the *mapping cylinder* $Z_f$ of $f$ to be the adjunction space $Y \cup_\varphi (X \times I)$ where the attaching map $\varphi: X\times\{0\} \to Y$ is given by $\varphi(x,0) := f(x)$. 

We see that the subspace $X \times \{1\}\subseteq Y \sqcup (X \times I)$ is a saturate closed subset homeomorphic to $X$. The restriction of this quotient map $q: Y \sqcup (X \times I) \to Z_f$ to this subset is an embedding of $X$. The image of the embedding is denoted by $\bar X$. Similarly, for $Y$, and $\bar Y$.

**Prop:** With notation as above, if $f$ is a homotopy equivalence, then $\bar Y$ and $\bar X$ are deformation retracts of $Z_f$. Thus two spaces are homotopy equivalent iff they are both homeomorphic to deformation retracts of a single space. 