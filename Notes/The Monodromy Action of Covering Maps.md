---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Covering maps]], [[Fundamental Group of a Topological Space]], [[Group Actions]]

**The Monodromy Action:** Suppose $q:E \to X$ is a covering map and $x\in X$. There is a transitive right action of $\pi_1(X, x)$ on the fibre $q^{-1}\{x\}$, called the *monodromy action*, given by $e\cdot [f] = \widetilde f_e(1)$ for $e\in q^{-1}\{x\}$ and $[f]\in \pi_1(X, x)$. 

**Isotropy Groups of the Monodromy Action:** Suppose $q:E \to X$ is a covering map and $x\in X$. For each $e\in q^{-1}\{x\}$ the isotropy group of $e$ under the monodromy action is $q_*[\pi_1(E,e)] \subseteq \pi_1(X,x)$. 

**Cor:** Suppose $q:E \to X$ is a covering map. The monodromy action is free on each fiber of $q$ iff $E$ is simply connected.

**Cor:** Suppose $q:E \to X$ is a covering map and $E$ is simply connected. Then each fiber of $q$ has the same cardinality as the fundamental group of $X$. 

**Covering of Simply Connected Spaces:** If $X$ is a simply connected space, every covering map $q:E \to X$ is a homeomorphism. 

**Conjugacy Theorem:** Let $q: E \to X$ be a covering map. For any $x\in X$, as $e$ varies over the fiber $q^{-1}\{x\}$, the set of induced subgroups $q_*[\pi_1(E, e)]$ is exactly one conjugacy class in $\pi_1(X, x)$. 

**Def:** A covering map $q: E \to X$ is called a *normal covering* if the induced subgroup $q_*[\pi_1(E, e)]$ is a normal subgroup of $\pi_1(X, q(e))$ for some $e\in E$. 

**Characterisation of Normal Coverings:** Suppose $q: E \to X$ is a covering map. The following statements are equivalent.
- The subgroup $q_*[\pi_1(E, e)]$ is a normal for some $e\in E$, i.e, $q$ is normal.
- For some $x\in X$, the subgroups $q_*[\pi_1(E, e)]$ are the same for all $e\in q^{-1}\{x\}$.
- For every $x\in X$, the subgroups $q_*[\pi_1(E, e)]$ are the same for all $x\in q^{-1}\{x\}$. 
- The subgroup $q_*[\pi_1(E, e)]$ is normal for every $e\in E$. 

# Covering Homomorphisms

**Def:** Suppose $q_1: E_1 \to X$, $q_2: E_2\to X$ are two covering of the same topological space $X$. A *covering homomorphism from $q_1$ to $q_2$* is a continuous map $\varphi:E_1 \to E_2$ such that $q_2 \circ \varphi = q_1$: 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
E_1 \arrow[rr, "\varphi"] \arrow[dr, "q_1"] && E_2 \arrow[dl, "q_2"'] \\
& X
\end{tikzcd}
\end{document}
```
A covering homomorphism that is also a homeomorphism is said to be a *covering isomorphism*. We say two covering are *isomorphic* if there is a covering isomorphism between them; this is an equivalence relation on the class of coverings of $X$. 

**Properties of Covering Homomorphisms:** Let $q_1: E_1 \to X$, $q_2: E_2\to X$ be two covering of the same topological space $X$. 
- If two covering homomorphism from $q_1$ to $q_2$ agree at one point of $E_1$, then they are equal.
- Given $x\in X$, any covering homomorphism from $q_1$ to $q_2$ restricts to q $\pi_1(X, x)$ equivariant map from $q_1^{-1}\{x\}$ to $q_2^{-1}\{x\}$ (with respect to the monodromy action)
- Every covering homomorphism is itself a covering map. 

**Covering Homomorphism Criterion:** Let $q_1: E_1 \to X$, $q_2: E_2\to X$ be two covering of the same topological space $X$, and suppose $e_1\in E_1$ an $e_2\in E_2$ are base points such that $q_1(e_1) = q_2(e_2)$. There exists a covering homomorphism from $q_1$ to $q_2$ taking $e_1$ to $e_2$ iff $(q_1)_*[\pi_1(E_1, e_1)] \le (q_2)_*[\pi_1(E_2, e_2)]$. 

**Covering Isomorphism Criterion:** Suppose $q_1: E_1\to X$ and $q_2: E_2 \to X$ are two covering of the same space $X$.
- Given $e_1 \in E_1$ and $e_2 \in E_2$ such that $q_1(e_1) = q_2(e_2)$, there's a unique covering isomorphism from $q_1$ to $q_2$ taking $e_1$ to $e_2$ iff $(q_1)_*[\pi_1(E_1, e_1)] = (q_2)_*[\pi_1(E_2, e_2)]$. 
- The covering $q_1$ and $q_2$ are isomorphic off for some $x\in X$, the conjugacy classes of subgroups $\pi_1(X, x)$ induced by $q_1$ and $q_2$ are the same. If this is the case, these conjugacy classes are the same for every $x\in X$. 

# Universal Covering Space

**Universality of Simly Connected Coverings:**
- Let $q: E\to X$ be a covering map with $E$ simply connected. If $q': E'\to X$ is any covering map, there exists a covering map $Q: E \to E'$ such that the following diagram commutes: 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
E \arrow[rr, dashed, "Q"] \arrow[dr, "q"] && E' \arrow[dl, "q' "'] \\
& X
\end{tikzcd}
\end{document}
```
- Any two simply connected coverings of the same space are isomorphic. 

**Def;** Any covering of $X$ by a simply connected space $\widetilde X$ is called a *universal covering*, and $\widetilde X$ is called the *universal covering space of $X$.*

**Def:** We say that a space $X$ is *locally simply connected* if it admits a basis of simply connected open subsets. 

**Obs:** We see that locally simply connected spaces are locally path-connected. 

**Def:** If $X$ is a topological space, a subset $U\subseteq X$ is a *relatively simply connected* if the inclusion $U \hookrightarrow X$ induces the trivial homomorphism on the fundamental groups, and $X$ is *semilocally simply connected* if every point in $X$ has a relatively simply connected neighbourhood. 

**Existence of the Universal Covering Space:** Let $X$ be a topological space. $X$ has a universal covering space iff $X$ is  connected, locally path-connected, and semilocally simply connected. 

**Example:** Define a map $q: \Bbb S^n \to \Bbb{RP}^n$ by sending each point $x$ in the sphere to the line through the origin and $x$, thought of as a point in $\Bbb{RP}^n$. Then $q$ is a covering map, and the fiber over each point $\Bbb{RP}^n$ is a pair of antipodal points $\{\pm x\}$. Additionally, if $n\ge 2$, then $\Bbb S^n$ is simply connected, then $\Bbb S^n$ is a universal covering space of $\Bbb{RP}^n$. 