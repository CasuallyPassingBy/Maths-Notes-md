---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]], [[Embedded Smooth Submanifolds]], [[Immersed Smooth Submanifolds]], [[Tangent Space for Manifolds]], [[Vector Fields on Smooth Manifolds]]

Let $M$ be a smooth manifold with or without boundary, and let $S\subseteq M$ be an immersed or embedded submanifold. Since the inclusion map $\iota:S \to M$ is a smooth immersion, at each point $p\in S$ we have the injective linear map $d\iota_p : T_p S \to T_p M$. We will adopt the convention *identifying* $T_p S$ with its image under this map, thereby thinking of $T_pS$ as a certain linear subspace of $T_p M$.

**Prop:** Suppose $M$ is a smooth submanifold with or without boundary, $S\subseteq M$ is an immersed or embedded submanifold, and $p\in S$. A vector $v\in T_pM$ is in $T_pS$ iff there is a smooth curve $\gamma: J \to M$ whose image is contained in $S$, and which is also smooth as a map into $S$, such that $0\in J$, $\gamma(0) = p$, and $\gamma'(0) = v$, 

**Prop:** Suppose $M$ is a smooth manifold with or without boundary, and $S\subseteq M$ is an embedded submanifold and $p\in S$. As a subspace of $T_pS$ is given by $$T_p S= \{X\in T_p M \mid\forall f\in \mathcal C^\infty (M) [f|_S = 0\implies Xf = 0]\}.$$
**Examples:**
- If $U \subseteq \Bbb R^n$ is open and $F: U \to \Bbb R^k$ is smooth, then the graph of $F$ is an embedded $n$-dimensional submanifold of $\Bbb R^{n+k}$.
- For any $n \in \Bbb N$, $\Bbb S^n$ is an embedded $n$-submanifold of $\Bbb R^{n+1}$.

**Def:** If $S \subseteq M$ is an embedded submanifold, a smooth map $\Phi: M \to N$ such that $S$ is a regular level set of $\Phi$ is called a *defining map* for $S$. In the special case $N = \Bbb R^{n-k}$, it is usually called a *defining function*. More generally, if $U$ is an open subset of $M$ and $\Phi: U \to N$ is a smooth map such that $S \cap U$ is a regular level set of $\Phi$, then $\Phi$ is called a *local defining map* or *local defining function* for $S$.

**Prop:** Suppose $S\subseteq M$ is an embedded submanifold. If $\Phi: U \to N$ is any local defining map for $S$, then $T_p S = \ker (d\Phi_p)$, where $\Phi_* = d\Phi_p : T_p M \to T_{\Phi(p)} N$ for each $p \in S \cap U$.  ^83d047

**Cor:** Suppose $S\subseteq M$ is a level set of a smooth submersion $\Phi = (\Phi^1,\dots. \Phi^k): M \to \Bbb R^k$. A vector $T_pM$ is tangent to $S$ iff $v\Phi^i = 0$ for all $i \in \{1,\dots, k\}$. 

**Def:** If $M$ is a smooth manifold with boundary. If $p\in \partial M$, a vector $X\in T_p M \setminus T_p\partial M$ is said to be *inward pointing* if for some $\varepsilon> 0$, there exists a smooth curve $\gamma: [0, \varepsilon) \to M$ such that $\gamma(0) = p$ and $\gamma'(0) = X$ , and it is *outward pointing* if there exists such a curve whose domain is $(-\varepsilon, 0]$. 

**Prop:** Suppose $M$ is a smooth $n$-dimensional manifold with boundary, $p\in \partial M$, and $(x^i)$ are smooth boundary coordinates defined on a neighbourhood of $p$. The inward pointing vectors in $T_pM$ are precisely those with positive $x^n$-component, the outward-pointing are the ones with negative $x^n$-component, and the ones tangent to $\partial M$ are those with zero $x^n$-component. Thus $T_p M$ is the disjoint union of $T_p \partial M$, the set of inward pointing and outward-pointing vectors, and $v\in T_p M$ is inward pointing iff $-v$ is outward pointing. 

**Def:** If $M$ is a smooth manifold, a *boundary defining* function for $M$ is a smooth function $f: M \to [0,\infty)$ such that $f^{-1}\{0\} = \partial M$ and $df_p \neq 0$ for all $p\in \partial M$. 

**Prop:** Every smooth manifold with boundary admits a boundary defining function. 

**Lagrange Multipliers:** Let $M$ be a smooth manifold, and let $C\subseteq M$ be an embedded submanifold that admits a global defining function $\Phi: M \to \Bbb R^k$. Let $f\in  \mathcal C^\infty(M)$, and suppose $p\in C$ is a point at which $f$ attains its maximum or minimum value among points in $C$. Them there are real numbers $\lambda_1,\dots, \lambda_k$ (called *Lagrange multipliers*) such that $$df_p = \sum_{n = 1}^k\lambda_n d\Phi^n|_p.$$
The proof of this relies on the fact $\{d\Phi^1|_p,\dots, d\Phi^l|_p\}$ forms a basis for the [[Dual Vector Spaces#^500dc6|annihilator]] of $T_p C$. A critical point of $f|_C$ must have a vanishing differential, then $d(f|_C)_p$ must be an element of the annihilator of $T_p C$ when seen as subspace of $T_pM$.  ^4260d8

# Vector Fields

If $S\subseteq M$ is an immersed or embedded submanifold with or without boundary, a vector field $X$ on $M$ does not necessarily restrict to a vector field on $S$, because $X_p$ may not lie on the subspace $T_p S \subseteq T_p M$ at a point $p\in S$. Given a point $p\in S$, a vector field $X$ on $M$ is said to be *tangent to $S$ at $p$* if $X_p \in T_p S\subseteq T_p M$. It is *tangent to $S$* if it is tangent to $S$ ar every point of $S$.

**Prop:** Let $M$ be a smooth manifold, $S\subseteq M$ be an embedded submanifold with or without boundary, and $X$ be a smooth vector field on $M$. Then $X$ is tangent to $S$ iff $(Xf)|_S = 0$ for every $f\in {\cal C}^\infty(M)$ such that $f|_S = 0$. 

**Restricting Vector Fields to Submaniolds:** Let $M$ be a smooth manifold, let $S\subseteq M$ be an immersed submanifold with or without boundary, and let $\iota: S \hookrightarrow M$ denote the inclusion map. If $Y\in {\frak X}(M)$ is tangent to X$, then there is a unique smooth vector field on $S$, denoted by $Y|_S$, that is $\iota$-related to $Y$. 

**Cor:** Let $M$ be a smooth manifold and let $S$ be an immersed submanifold with or without boundary in $M$. If $Y_1$ and $Y_2$ are smooth vector fields on $M$ that are tangent to $X$, then $[Y_1, Y_2]$ is also tangent to $S$. 

**Prop:** Let $M$ be a smooth manifold with boundary. There exists a global smooth vector field on $M$ whose restriction to $\partial M$ is everywhere inward-pointing, and one whose restriction to $\partial M$ is everywhere outward-pointing. 

**Extension Lemma for Vector Fields on Submanifolds:** Suppose $M$ is a smooth manifold and $S\subseteq M$ is an embedded submanifold with or without boundary. Given $X\in {\frak X}(S)$, there exists a smooth vector field $Y$ on a neighbourhood of $S$ in $M$ such that $X = Y|_S$. Additionally, every such vector fields extends to all of $M$ iff $S$ is properly embedded. 

This is a result of the [[Smooth Maps on and Between Submanifolds#Extending Functions from Submanifolds|Extension Lemma for Functions on Manifolds]].

