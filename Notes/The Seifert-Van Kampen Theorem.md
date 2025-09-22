---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Fundamental Group of a Topological Space]], [[Categories and Functors]], [[Free Product of Groups]], [[Wedge Sums]]

**Seifert-Van Kampen Theorem:** Let $X$ be a topological space. Suppose that $U, V \subseteq X$ are open subsets whose union is $X$, with $U, V$, and $U \cap V$ path-connected, and $p\in U \cap V$. The four inclusion maps
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}
& U\arrow[dr, "k"] & \\
U \cap V\arrow[ur, "i"]\arrow[dr, "j"] && X \\
&V\arrow[ur,"\ell"']&
\end{tikzcd}
\end{document}
```
induce fundamental group homomorphisms
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}
& \pi_1(p,U)\arrow[dr, "k_*"] & \\
\pi_1(p,U \cap V)\arrow[ur, "i_*"]\arrow[dr, "j_*"] && \pi_1(p,X) \\
&\pi_1(p,V)\arrow[ur,"\ell_*"']&
\end{tikzcd}
\end{document}
```
Then, 
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
& \pi_1(U, p)\arrow[dr, "k_*"]\arrow[d, hook] & \\
\pi_1(U \cap V, p)\arrow[ur, "i_*"]\arrow[dr, "j_*"] &\pi_1(U, p) \ast \pi_1(V, p)\arrow[r, "\Phi"] & \pi_1(X,p) \\
&\pi_1(V, p)\arrow[ur,"\ell_*"']\arrow[u, hook]&
\end{tikzcd}
\end{document}
```
Where $\Phi: \pi_1(U, p) \ast \pi_1(V, p) \to\pi_1(X, p)$ is a surjective homomorphism. If $$C := \{(i_*(\gamma)) (j_*(\gamma))^{-1} \mid \gamma\in \pi_1(U\cap V, p)\}, $$then $\ker \Phi$ is the normal closure of $C$, finally, getting that $$\pi_1(X, p)\cong (\pi_1(U, p) \ast \pi_1(V, p))/\overline C.$$Meaning, that $\pi_1(U, p) \ast_{\pi_1(U\cap V, p)} \pi_1(V, p) \cong \pi_1(X, p)$, where $\pi_1(U, p) \ast_{\pi_1(U\cap V, p)} \pi_1(V, p)$ is an the amalgamated free product along ${\pi_1(U\cap V, p)}$, and this diagram commutes
```tikz
\usepackage{tikz-cd}
\usepackage{amsfonts, amsmath, amssymb}

\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
& \pi_1(U, p)\arrow[dr, "k_*"]\arrow[d, hook] & \\
\pi_1(U \cap V, p)\arrow[ur, "i_*"]\arrow[dr, "j_*"] &\pi_1(U, p) \ast_{\pi_1(U\cap V, p)} \pi_1(V, p)\arrow[r, "\cong"] & \pi_1(X,p) \\
&\pi_1(V, p)\arrow[ur,"\ell_*"']\arrow[u, hook]
\end{tikzcd}
\end{document}
```

**Cor:** Let $X$ be a topological space. Suppose that $U, V \subseteq X$ are open subsets whose union is $X$, with $U, V$, and $U \cap V$ path-connected, and $p\in U \cap V$. If $U \cap V$ is simply connected. Then $\pi_1(U, p) \ast \pi_1(V, p) \cong \pi_1(X, p)$. 

**Cor:** Let $X$ be a topological space. Suppose that $U, V \subseteq X$ are open subsets whose union is $X$, with $U, V$, and $U \cap V$ path-connected, and $p\in U \cap V$. If $U$ is simply connected, then $\ell: V \hookrightarrow X$ induces an isomorphism $$\pi_1(X, p) \cong \pi_1(V,p) /\overline{(j_*[\pi_1(U \cap V, p)])},$$where $\overline{(j_*[\pi_1(U \cap V, p)])}$ is the normal closure of ${(j_*[\pi_1(U \cap V, p)])}$ in $\pi_1(V, p)$. If the fundamental groups of $V$ and $U\cap V$ have finite representation $$\begin{align*}
\pi_1(V, p)&\cong \langle\beta_1,\dots, \beta_n \mid \sigma_1, \dots, \sigma_s\rangle  \\ 
\pi_1(U \cap V) &\cong \langle \gamma_1, \dots, \gamma_p\mid \tau_1, \dots, \tau_t\rangle,
\end{align*}$$then $\pi_1(X, p)$ has the presentation $$\pi_1(X, p) \cong \langle \beta_1, \dots \beta_n\mid \sigma_1,\dots, \sigma_s,v_1,\dots, v_p\rangle $$where the generators are represented by the same loops as in the presentation of the fundamental group of $V$; but considered as loops in $X$; and each $v_a$ is an expression for $j_*(\gamma_a)\in \pi_1(V, p)$ in terms its generators. 

# Applications

**Lemma:** Suppose $p_i \in X_i$ is a [[Homotopy Equivalence#^85d060|nondegenerate base point]] for $i = 1,\dots, n$. Then $\ast$ is a nondegenerate base point in $X_1 \vee \dots \vee X_n$. 

**Th:** Let $X_1, \dots, X_n$ be spaces with nondegenerate base points $p_j\in X_j$. Then map $$\Phi: \pi_1(X_1, p_1) \ast\dots\ast\pi_1(X_n,p_n) \to \pi_1(X_1\vee\dots\vee X_n, \ast)$$induced by $(\iota_j)_\ast: \pi_1(X_j, p_j) \to \pi_1(X_1\vee\dots\vee X_n, \ast)$ is an isomorphism. 

**Cor:** A bouquet of circles $\Bbb S^1\vee\dots\vee \Bbb S^1$ of $n$ circles has a fundamental group isomorphic to $\Bbb Z\ast\dots\ast\Bbb Z$, which is a free group of $n$ generators. If $\omega_i$ denotes the standard loop in the $i$th copy of $\Bbb S^1$, then the fundamental group of the bouquet is just the free group $F([\omega_1], \dots, [\omega_n])$.

This means that under special circumstances, we get that the functor $\pi_1: \sf Top_* \to Grp$ also preserves coproducts. 

**Lemma:** Suppose $M$ is a connected manifold of dimension of at least $3$, and $p\in M$. Then the inclusion $M \setminus \{p\} \hookrightarrow M$ induces an isomorphism $\pi_1(M\setminus \{p\}) \cong \pi_1(M)$. 

**Prop:** Suppose $M$ and $N$ connected $n$-manifolds with $n\ge 3$. Then the fundamental group of $M \# N$ is isomorphic to $\pi_1(M) \ast \pi_1(N)$. 