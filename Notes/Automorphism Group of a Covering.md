---
tags:
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]]
Links: [[Covering Maps]], [[The Monodromy Action of Covering Maps]], [[Automorphism Group]], 

**Def:** Suppose $q:E \to X$ is a covering map. An *automorphism of $q$* is a covering isomorphism from $q$ to itself, that is a homeomorphism $\varphi: E \to E$ such that $q \circ\varphi = q$: 
```tikz
\usepackage{tikz-cd}
\begin{document}
\begin{tikzcd}[row sep=2cm, column sep=2cm]
E \arrow[rr, "\varphi"] \arrow[dr, "q"] && E \arrow[dl, "q"'] \\
& X
\end{tikzcd}
\end{document}
```
Covering automorphisms are also variously known as *deck transformations* or *covering transformations*. 

Let $\text{Deck}(E/X) = \text{Aut}_q(E)$ denote the set of all automorphisms of the covering $q:E \to X$. Thus $\text{Aut}_q(E)$ is a group, called the *automorphism group of the covering*, or the *covering group.* It acts on $E$ in a natural way, and the definition of covering map isomorphisms implies that each orbit is a subset of a single fiber. 

**Properties of the Covering Group:** Let $q:E \to X$ be a covering map.
- If two automorphisms of $q$ agree at one point, they are identical, 
- Given $x\in X$, each covering automorphism restricts to a $\pi_1(X, x)$-automorphism of the fiber $q^{-1}\{x\}$ (with respect to the monodromy action). 
- For any evenly covered open subset $U\subseteq X$, each covering automorphism permutes the components of $q^{-1}[U]$.
- The group $\text{Aut}_q(E)$ acts freely on $E$ by homeomorphism. 

**Examples:** 
- For the covering map $\varepsilon: \Bbb R \to \Bbb S^1$, the integral translations $x \mapsto x+k$ for $k\in \Bbb Z$ are automorphisms. We can prove that $\text{Aut}_\varepsilon (\Bbb R)\cong \Bbb Z$. We can generalise this further to $\varepsilon^n: \Bbb R^n \to \Bbb T^n$, then $\text{Aut}_{\varepsilon^n}(\Bbb R^n) \cong \Bbb Z^n$. 
- If $q: \Bbb S^n \to \Bbb{RP}^n$ is the natural covering map, then the antipodal map $\alpha: \Bbb S^n \to \Bbb S^n$ defined by $\alpha(x) =-x$ is an automorphism. The covering automorphism group is the two element $\{\text{Id}, \alpha\} \cong \Bbb Z/2\Bbb Z$.

**Orbit Criterion for Covering Automorphisms:** Let $q:E\to X$ be a covering map. If $e_1, e_2\in E$ are two points in the same fiber $q^{-1}\{x\}$, there exists a covering automorphism taking $e_1$ to $e_2$ iff the induced subgroups $q_*[\pi_1(E, e_1)]=q_*[\pi_1(E, e_2)] \le \pi_1(X, x)$.

**Normal Coverings Have Transitive Automorphism Groups:** If $q:E \to X$ is a covering map, then $\text{Aut}_q(E)$ acts transitively on each fiber iff $q$ is a normal covering. 

**Th:** Suppose $q:E \to X$ is a covering map and $x\in X$. The restriction map $\varphi \mapsto \varphi|_{q^{-1}\{x\}}$ is a group isomorphism between $\text{Aut}_q(E)$ and the group $\text{Aut}_{\pi_1(X, x)}(q^{-1}\{x\})$ of $\pi_1(X, x)$-automorphism of $q^{-1}\{x\}$. 

**Covering Group Structure Theorem:** Suppose $q:E \to X$ is a covering map, $e\in E$, and $x = q(e)$. Let $G = \pi_1(X, x)$ and $H = $q_*[\pi_1(E, e)] \le \pi_1(X, x)$. For each path class $\gamma \in N_G(H)$ (the [[normaliser]] of $H$ in $G$), there is a unique covering automorphism $\varphi_\gamma\in \text{Aut}_q(E)$ that satisfies $\varphi_\gamma(e) = e \cdot \gamma$. The map $\varphi \mapsto \varphi_\gamma$ is a surjective homomorphism from $N_G(H)$ to $\text{Aut}_q(E)$ with kernel equal to $H$, so it descends to an isomorphism from $N_G(H)$ to $\text{Aut}_q(E)$:
$$\text{Aut}_q(E) \cong \frac{N_{\pi_1(X, x)}(q_*[\pi_1(E, e)])}{q_*[\pi_1(E, e)]}.$$

**Normal Case:** If $q:E \to X$ is a normal covering, then for any $x\in X$ and any $e\in q^{-1}\{x\}$, the map $\gamma\mapsto \varphi_\gamma$ of the theorem above induces an isomorphism from $\pi_1(X, x)/ q_*[\pi_1(E, x)]$ to $\text{Aut}_q(E)$. 

**Simply Connected Case:** If $q: E \to X$ is a covering map and $E$ is simply connected, then the automorphism group of the covering map is isomorphic to the fundamental group of $X$. In fact, for any $x\in X$ and $e\in q^{-1}\{x\}$, the map $\gamma \mapsto \varphi_\gamma$ of the theorem above is an isomorphism from $\pi_1(X, x)$ to $\text{Aut}_q(E)$. 

# Classification Theorem

**Classification Theorem:** Let $X$ be a topological space that has a [[The Monodromy Action of Covering Maps#^84e006|universal covering space]], and let $x_0\in X$ be any base point. there is a one-to-one correspondence between isomorphism classes of coverings of $X$ and conjugacy classes of subgroups of $\pi_1(X, x_0)$. The correspondence associates each covering $\widehat q: \widehat E\to X$ with the conjugacy class of its induced subgroup.