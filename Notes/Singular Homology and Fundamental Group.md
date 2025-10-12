---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Singular Homology]], [[Fundamental Group of a Topological Space]]

**Lemma:** Suppose $f_0$ and $f_1$ are paths in $X$, and $f_0 \sim f_1$. Then, considered as a singular chain, $f_0 - f_1$ is a boundary.

In this section, because we are dealing with various equivalnce relations on paths, we adopt the following notation. For any path in $X$ (not necessarily a loop), we let $[f]_\pi$ denote its equivalence class modulo path homotopy. Similarly, if $c$ is any $1$-chain we let $[c]_H$ denote its equivalence class modulo $B_1(X)$, so if $c$ is any cycle, then $[c]_H$ is an element of $H_1(X)$. We define a map $\gamma: \pi_1(X, p)\to H_1(X)$, called the *Hurewicz homomorphism*, by $$\gamma([f]_\pi) = [f]_H.$$
By the lemma above, $\gamma$ is well defined. 

If $f:X \to Y$ is a continuous, then the following diagram commutes:
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
\pi_1(X,p)\arrow[r, two heads, "f_*"] \arrow[d, "\gamma"]  & \pi_1(Y,f(p))\arrow[d, "\gamma"] \\
H_1(X) \arrow[r, "f_*"'] & H_1(Y)
\end{tikzcd}
\end{document}
```

**Th:** Let $X$ be a path-connected space, and let $p\in X$. Then $\gamma: \pi_1(X, p) \to H_1(X)$ is a surjective homomorphism whose kernel is the commutator of $\pi_1(X, p)$. Consequently, $H_1(X)$ is isomorphic to the abelianization of $\pi_1(X, p)$. 

**Cor:** The followinf spaces have the indicated first homology groups: $$\begin{align*}
H_1(\Bbb S^1) &\cong \Bbb Z \\
H_1(\Bbb S^n) &\cong 0, \ \text{if }n \ge 2 \\
H_1(\Bbb T^2\#\cdots \#\Bbb T^2) &\cong \Bbb Z^{2n} \\
H_1(\Bbb {RP}^2\#\cdots \#\Bbb {RP}^2) &\cong \Bbb Z^{n-1} \times \Bbb Z/2\Bbb Z 
\end{align*}$$

The Hurewicz homomorphism $\gamma_1(X, p) \to H_1(X)$ can be generalised to a homomorphism from $\pi_k(X, p)$ to $H_k(X)$ for any $k$. The relationship between higher homotopy and homology is not so simple, except in one important special case: the [[Hurewicz theorem]]. 

$(*)$ **Hurewicz Theorem:**  If $X$ is path-connected and $\pi_j(X, p)$ is trivial for $1 \le j \le k$, then $H_j(X)$ is trivial for the same values of $j$ and the Hurweicz homomorphism is an isomorphism from $\pi_k(X, p)$ to $H_k(X)$. 