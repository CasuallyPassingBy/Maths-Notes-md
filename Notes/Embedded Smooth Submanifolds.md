---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]], [[Submersions, Immersions and Local Diffeomorphism of Smooth Manifolds]], [[The Whitney Embedding Theorem]]

**Def:** An *embedded submanifold of $M$* is subset $S\subseteq M$ that is a manifold (with or without boundary) in the subspace topology, endowed with a smooth structure with respect to which the inclusion map $S \hookrightarrow M$ is a smooth embedding. Embedded submanifolds are also called *regular submanifolds*.

**Def:** If $S$ is an embedded submanifold of $M$, the difference $\dim M-\dim S$ is called the *codimension of $S$ in $M$*, and the containing submanifold is called the *ambient manifold* for $S$. An *embedded hypersurface* is an embedded submanifold of codimension $1$. The empty set is an embedded submanifold of any dimension.

The easiest embedded submanifold to understand are those of codimension $0$. For any smooth manifold we define an *open submanifold of $M$* to be any open set with the subspace topology and with the smooth charts obtained by restricting those of $M$.

**Prop:** Suppose $M$ is a smooth manifold. The embedded submanifolds if codimension $0$ in $M$ are exactly the open submanifolds. 

**Prop:** Suppose $M$ is a smooth manifold with or without boundary, $N$ is a smooth manifold, and $F: N \to M$ is a smooth embedding. Let $S := F[N]$. With the subspace topology $S$ is a topological manifold, and it has a unique smooth structure making it into an embedded submanifold of $M$ with the property that $F$ is a diffeomorphism onto its image. 

**Cor:** Embedded submanifolds are precisely the images of smooth embeddings.

**Prop:** Suppose $M$ and $N$ are smooth manifold. For each $p\in N$, the subset $M \times \{p\}$, called a *slice of the prodcut manifold*, is an embedded manifold that is diffeomorphic to $M$.

**Prop:** Suppose $M$ is a smooth $m$-manifold (without boundary), $N$ is a smooth $n$ submanifold with or without boundary, $U\subseteq M$ is open and $f: U \to N$ is a smooth map. If we define $\Gamma(f)\subseteq M \times N$ denote the graph of $f$:  $$\Gamma(f) =\{(x, f(x))\in M \times N\mid x\in U\},  $$then $\Gamma(f)$ is an embedded $m$-dimensional submanifold of $M \times N$. 

**Def:** An embedded manifold $S\subseteq M$ is said to be *properly embedded* if the injection $S \hookrightarrow M$ is a proper map.

**Prop:** Suppose $M$ is a smooth manifold with or without boundary and $S\subseteq M$ is an embedded submanifold. Then $S$ is properly embedded iff it is a closed subset of $M$. 

**Cor:** Every compact embedded submanifold is properly embedded.

**Global Graphs are Properly Embedded:** Suppose $M$ is a smooth manifold, $N$ is a smooth manifold with or without boundary, and $f: M \to N$ is a smooth map. With the smooth manifold structure $\Gamma(f)$ is properly embedded in $M \times N$. 

### Slice Charts for Embedded Submanifolds

**Def:** If $U$ is an open subset of $\Bbb R^n$ and $k\in \{0,\dots, n\}$, a *$k$-dimensional slice of $U$* is any subset of the form $$S = \{(x^1, \dots, x^k, x^{k+1}, \dots,x^n)\in U \mid x^{k+1} =c^{k+1}, \dots, x^n = c^n\}.$$for some constants $c^{k+1},\dots,c^n$. Note that when $k = n$, then $S= U$. 

**Def:** Let $M$ be a smooth $n$-manifold, and $(U, \varphi)$ be a smooth chart on $M$. If $S$ is a subset of $U$ such that $\varphi[S]$ is a $k$-slice of $\varphi[U]$, then we say simply that $S$ is a $k$-slice of $U$. A subset $S\subseteq M$ is called an *embedded submanifold of dimension $k$* (or *embedded $k$-submanifold*) if for each point $p \in S$ there exists a smooth chart $(U, \varphi)$ for $M$ such that $p\in  U$ and $U \cap S$ is a $k$-slice of $U$. In this situation we call the chart $(U, \varphi)$ a *slice chart for $S$ in $M$*, and the corresponding coordinates $(x^1, \dots, x^n)$ are called *slice coordinates*. 

**Local Slice Criterion for Embedded Submanifolds:** Let $M$ be a smooth $n$-manifold. If $S\subseteq M$ is an embedded $k$-dimensional submanifold, then $S$ satisfies the local $k$-slice condition. Conversely, if $S\subseteq M$ is a subset that satisfies the local $k$-slice condition, then with the subspace topology, $S$ is a topological manifold of dimension $k$, and it has a smooth structure it into a $k$-dimensional embedded submanifold of $M$. 

We call a chart $(U, \phi)$ in $N$ an *adapted chart* relative to $S$. On $U \cap S$, $\phi = (x^1, \dots, x^k, 0,\dots, 0)$. Let $$\phi_S : U \cap S \to \Bbb R^k$$be the restriction of the first $k$ componentes to $\phi$ to $U \cap S$, that is $\phi_S = (x^1, \dots, x^k)$. Note that $(U \cap S, \phi_S)$ is a chart for $S$ in the subspace topology. 

**Th:** If $M$ is a smooth $n$-manifold with boundary, then with the subspace topology, $\partial M$ is a topological $(n-1)$-submanifold (without boundary), and has a smooth structure that is properly embedded submanifold of $M$ 

 happens to lie in $S$, then $\gamma'(t)$ is in the subspace $T_{\gamma(t)}S$ of $T_{\gamma(t)} M$ for all $t\in J$. 

# Levels Sets of a Function

**Def:** A *level set* of a map $F: N \to M$ is a subset $F^{-1}\{c\}$ for some $c\in M$. The value $c \in M$ is called the *level* of the level set $F^{-1}\{c\}$. If $F: N\to \Bbb R^n$, then $Z(F) := F^{-1}\{0\}$ is the *zero set* of $F$. 

**Constant-Rank Level Set Theorem:** Let $M$ and $N$ be smooth manifolds, and let $\Phi: M \to N$ be a smooth map with constant rank equal to $k$. Each level set of $\Phi$ is a closed embedded submanifold of codimension $k$ in $M$. 

**Cor (Submersion Level Set Theorem):** If $\Phi: M \to N$ is a submersion, then each level set of $\Phi$ is a closed embedded submanifold whose codimension is equal to the dimension of $N$. ^c2a3b8

**Def:** Let us consider the smooth map $F:N \to M$. A point $p$ in $N$ is a *critical point* of $F$ if the differential $dF_p: T_pN \to T_{F(p)} M$ fails to be surjective. It is a *regular point* of $F$ if the differential $dF_p$ is slurjective, i.e., $F$ is a submersion at $p$. A point $c \in M$ is a *critical value* if some point in the preimage $F^{-1}\{c\}$ is a critical point. A point $c$ in the image of $F$ is regular value iff *every* point in the preimage $F^{-1}\{c\}$ is a regular point. Additionally, 
The inverse image image $F^{-1}\{c\}$ of a regular value $c$ is called a *regular level set*. If the zero set $F^{-1}\{0\}$ is a regular set of $F:N \to \Bbb R^m$, it is called a *regular zero set*.

**Lemma:** Let $F: N \to \Bbb R^m$ be a $\mathcal C^\infty$ map on a manifold $N$ of dimension $n$ and let $S$ be the level set $F^{-1}\{0\}$. If relative to some coordinate chart $(U, x^1, \dots, x^n)$ about $p\in S$, the Jacobian determinant $\dfrac{\partial (F^1, \dots, F^m)}{\partial(x^{j_1}, \dots, x^{j_m})}(p)$ is nonzero, then in some neighbourhood of $p$ one may replace $x^{j_1}, \dots, x^{j_m}$ by $F^1, \dots, F^m$ to obtain an adapted chart for $N$ relative to $S$. 

**Regular Level Set Theorem:** Every regular level set of a smooth map between smooth manifolds is a properly embedded submanifold whose codimension is equal to the codimension of the codomain. 

**Prop:** For a real-valued function $f:M \to \Bbb R$, a point $p\in M$ is critical point iff relative to some chart $(U, x^1, \dots, x^n)$ containing $p$, all the partial derivatives satisfy $$\frac{\partial f}{\partial x^j} (p) = 0, \qquad j\in \{1, \dots, n\}$$
**Prop:** Let $S$ be a subset of a smooth $n$ manifold $M$. Then $S$ is an embedded $k$-submanifold of $M$ iff every point $p\in S$ has a neighbourhood $U$ in $M$ such that $U \cap S$ is a level set of submersion $\Phi: U \to \Bbb R^{n-k}$. 

**Th:** Suppose $M$ is a smooth manifold and $S\subseteq M$ is an embedded submanifold. The subspace topology on $S$ and the smooth structure given by the $k$-slice condition, for some $k$, are the only topology and smooth structure with respect to which $S$ is an embdedded or immersed submanifold. 