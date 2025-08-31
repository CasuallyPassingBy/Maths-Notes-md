---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth or Differentiable Manifolds]], [[Submersions, Immersions and Embeddings of Manifolds]]

**Def:** If $U$ is an open subset of $\Bbb R^n$, a *$k$-slice* of $U$ is any subset of the form $$S = \{(x^1, \dots, x^k, x^{k+1}, \dots,x^n)\in U \mid x^{k+1} =c^{k+1}, \dots, x^n = c^n\}.$$
**Def:** Let $M$ be a smooth $n$-manifold, and $(U, \varphi)$ be a smooth chart on $M$. If $S$ is a subset of $U$ such that $\varphi[S]$ is a $k$-slice of $\varphi[U]$, then we say simply that $S$ is a $k$-slice of $U$. A subset $S\subseteq M$ is called an *embedded submanifold of dimension $k$* (or *embedded $k$-submanifold*) if for each point $p \in S$ there exists a smooth chart $(U, \varphi)$ for $M$ such that $p\in  U$ and $U \cap S$ is a $k$-slice of $U$. In this situation we call the chart $(U, \varphi)$ a *slice chart for $S$ in $M$*, and the corresponding coordinates $(x^1, \dots, x^n)$ are called *slice coordinates*. If the dimension of $S$ is understood or irrelevant, we will just call $S$ an *embedded submanifold*. Embedded submanifolds are also called *regular manifolds.*

We call a chart $(U, \phi)$ in $N$ an *adapted chart* relative to $S$. On $U \cap S$, $\phi = (x^1, \dots, x^k, 0,\dots, 0)$. Let $$\phi_S : U \cap S \to \Bbb R^k$$be the restriction of the first $k$ componentes to $\phi$ to $U \cap S$, that is $\phi_S = (x^1, \dots, x^k)$. Note that $(U \cap S, \phi_S)$ is a chart for $S$ in the subspace topology. 

**Def:** If $S$ is an embedded submanifold of $M$, the difference $\dim M- \dim S$ is called the *codimension* of $S$. An *embedded  hypersurface* is an embedded submanifold of codimension $1$.  

**Lemma:** Let $M$ be a smooth manifold and let $S$ be subset of $M$. Suppose that for some $k$, every point $p \in S$ has a neighbourhood $U\subseteq M$ such that $U \cap S$ is an embedded $k$-submanifold of $U$. Then $S$ is an embedded $k$-submanifold of $M$.

**Prop:** Let $S$ be a embedded submanifold of $N$ and $\mathfrak U$ a collection of compatible charts that covers $S$. Then $\{U \cap S, \phi_S) \mid (U, \phi) \in \mathfrak U\}$. is an atlas for $S$. Therefore, a embedded submanifold is itself a manifold. If $N$ has dimension $n$ and $K$ is locally defined by the vanishing of $n-k$ coordinates, then $\dim S = k$. 

**Th:** The image of a smooth embedding is an embedded manifold.

**Cor:** Embedded submanifolds are precisely the images of smooth embeddings.

Let $M$ be a smooth manifold, and let $S\subseteq M$ be an embedded submanifold. Since the inclusion map $\iota:S \to M$ is a smooth embedding, at each point $p\in S$ we have the injective linear map $\iota_* = d\iota_p : T_p S \to T_p M$. We will adopt the convention *identifying* $T_p S$ with its image under this map, thereby thinking of $T_pS$ as a certain linear subspace of $T_p M$

**Prop:** Suppose $S\subseteq M$ is an embedded submanifold and $p\in S$. As a subspace of $T_pS$ is given by $$T_p S= \{X\in T_p M \mid\forall f\in \mathcal C^\infty (M) [f|_S = 0\implies Xf = 0]\}.$$
**Examples:**
- If $U \subseteq \Bbb R^n$ is open and $F: U \to \Bbb R^k$ is smooth, then the graph of $F$ is an embedded $n$-dimensional submanifold of $\Bbb R^{n+k}$.
- For any $n \in \Bbb N$, $\Bbb S^n$ is an embedded $n$-submanifold of $\Bbb R^{n+1}$.

**Cor:** If $S\subseteq M$ is an embedded submanifold and $\gamma: J \to M$ is a smooth curve whose image happens to lie in $S$, then $\gamma'(t)$ is in the subspace $T_{\gamma(t)}S$ of $T_{\gamma(t)} M$ for all $t\in J$. 

**Prop:** An embedded submanifold is closed iff if the inclusion is [[Proper Maps|proper]].


# Levels Sets of a Function

**Def:** A *level set* of a map $F: N \to M$ is a subset $F^{-1}\{c\}$ for some $c\in M$. The value $c \in M$ is called the *level* of the level set $F^{-1}\{c\}$. If $F: N\to \Bbb R^n$, then $Z(F) := F^{-1}\{0\}$ is the *zero set* of $F$. 

**Constant-Rank Level Set Theorem:** Let $M$ and $N$ be smooth manifolds, and let $\Phi: M \to N$ be a smooth map with constant rank equal to $k$. Each level set of $\Phi$ is a closed embedded submanifold of codimension $k$ in $M$. 

**Cor (Submersion Level Set Theorem):** If $\Phi: M \to N$ is a submersion, then each level set of $\Phi$ is a closed embedded submanifold whose codimension is equal to the dimension of $N$. ^c2a3b8

**Def:** Let us consider the smooth map $F:N \to M$. A point $p$ in $N$ is a *critical point* of $F$ if the differential $dF_p: T_pN \to T_{F(p)} M$ fails to be surjective. It is a *regular point* of $F$ if the differential $dF_p$ is surjective, i.e., $F$ is a submersion at $p$. A point $c \in M$ is a *critical value* if some point in the preimage $F^{-1}\{c\}$ is a critical point. A point $c$ in the image of $F$ is regular value iff *every* point in the preimage $F^{-1}\{c\}$ is a regular point. Additionally, 
The inverse image image $F^{-1}\{c\}$ of a regular value $c$ is called a *regular level set*. If the zero set $F^{-1}\{0\}$ is a regular set of $F:N \to \Bbb R^m$, it is called a *regular zero set*.

**Lemma:** Let $F: N \to \Bbb R^m$ be a $\mathcal C^\infty$ map on a manifold $N$ of dimension $n$ and let $S$ be the level set $F^{-1}\{0\}$. If relative to some coordinate chart $(U, x^1, \dots, x^n)$ about $p\in S$, the Jacobian determinant $\dfrac{\partial (F^1, \dots, F^m)}{\partial(x^{j_1}, \dots, x^{j_m})}(p)$ is nonzero, then in some neighbourhood of $p$ one may replace $x^{j_1}, \dots, x^{j_m}$ by $F^1, \dots, F^m$ to obtain an adapted chart for $N$ relative to $S$. 

**Regular Level Set Theorem:** Every regular level set of a smooth map is a closed embedded submanifold whose codimension is equal to the codimension of the range. 

**Prop:** For a real-valued function $f:M \to \Bbb R$, a point $p\in M$ is critical point iff relative to some chart $(U, x^1, \dots, x^n)$ containing $p$, all the partial derivatives satisfy $$\frac{\partial f}{\partial x^j} (p) = 0, \qquad j\in \{1, \dots, n\}$$
**Prop:** Let $S$ be a subset of a smooth $n$ manifold $M$. Then $S$ is an embedded $k$-submanifold of $M$ iff every point $p\in S$ has a neighbourhood $U$ in $M$ such that $U \cap S$ is a level set of submersion $\Phi: U \to \Bbb R^{n-k}$. 

**Def:** If $S \subseteq M$ is an embedded submanifold, a smooth map $\Phi: M \to N$ such that $S$ is a regular level set of $\Phi$ is called a *defining map* for $S$. In the special case $N = \Bbb R^{n-k}$, it is usually called a *defining function*. More generally, if $U$ is an open subset of $M$ and $\Phi: U \to N$ is a smooth map such that $S \cap U$ is a regular level set of $\Phi$, then $\Phi$ is called a *local defining map* or *local defining function* for $S$.

**Lemma:** Suppose $S\subseteq M$ is an embedded submanifold. If $\Phi: U \to N$ is any local defining map for $S$, then $T_p S = \ker (d\Phi_p)$, where $\Phi_* = d\Phi_p : T_p M \to T_{\Phi(p)} N$ for each $p \in S \cap U$.  ^83d047

**Lagrange Multipliers:** Let $M$ be a smooth manifold, and let $C\subseteq M$ be an embedded submanifold that admits a global defining function $\Phi: M \to \Bbb R^k$. Let $f\in  \mathcal C^\infty(M)$, and suppose $p\in C$ is a point at which $f$ attains its maximum or minimum value among points in $C$. Them there are real numbers $\lambda_1,\dots, \lambda_k$ (called *Lagrange multipliers*) such that $$df_p = \sum_{n = 1}^k\lambda_n d\Phi^k|_p.$$
**Def:** Suppose $\Phi: M \to N$ is a smooth map and $S\subseteq M$ is an embedded submanifold. We say that $\Phi$ is *transverse to S* if for every $p\in \Phi^{-1}[S]$, the spaces $T_{\Phi(p)}S$ and $\Phi_* T_p M$ together span $T_{\Phi(p)} N$, i.e., $$T_{\Phi(p)} S + d\Phi_p[ T_p M] = T_{\Phi(p)}N. $$We denote this relation as $\Phi \pitchfork Z$. 

**Transversality Theorem:** A $\mathcal C^\infty$ map $\Phi: M \to N$ is transversal to a embedded submanifold $S$ of codimension $k$ in $M$, then $\Phi^{-1}[S]$ is embedded submanifold of codimension $k$ in $M$. 

**Def:** Two embedded submanifold $S_1, S_2 \subseteq M$ are said to be *transverse*, or to *intersect transversly*, if for each $p\in S_1 \cap S_2$, the tangent spaces $T_p S_1$ and $T_p S_2$ together span $T_p M.$ I am going to denote it as $S_1 \pitchfork S_2$. 

**Prop:** If $S_1$ and $S_2$ are transverse, then $S_1\cap S_2$ is en embedded submanifold of $M$ of dimension $\dim S_1 + \dim S_2- \dim M$. 

# Immersed Submanifolds

**Def:** Let $M$ be a smooth manifold. An *immersed submanifold of dimension $k$*, or *immersed $k$-submanifold* of $M$ is a subset $S \subseteq M$ endowed with a $k$-manifold topology together with a smooth structure such that the inclusion map $\iota:S \to M$ is a smooth immersion. As for embedded submanifolds, we define the *codimension of $S$ in $M$* to be $\dim M - \dim S$.

We see that every embedded submanifold is an immersed submanifold, but the converse is not necessarily true.

Immersed submanifolds arise in a fairly natural way. Let $F: N \to M$ be an injective immersion, we can give the set image $F[N]$ a unique manifold topology and smooth structure such that $F:N \to F[N]$ is a diffeomorphism. We define that a set $U \subseteq F[N]$ is open iff $F^{-1}[U] \subseteq N$ is open, and take the smooth coordinates maps on $F[N]$ to be the maps of the form $\phi \circ F^{-1}$, where $\phi$ is a smooth coordinate map for $N$. Lastly, the map $\iota: F[N] \to M$ is an injective immersion, 

**Prop:** Immersed submanifolds are precisely the images of injective immersions. 

**Lemma:** Let $F: N \to M$ be an immersion. Then $F$ is locally an embedding, i.e., for any $p\in N$, there exists a neighbourhood $U$ of $p$ in $N$ such that $F|_U: U \to M$ is a smooth embedding. 

**Def:** If $S \subseteq M$ is an immersed $k$-submanifold, we define a *local parametrization* of $S$ to be a smooth embedding $X: U \to M$ whose domain is an open subset $U\subseteq \Bbb R^k$, whose image is an open subset of $S$, and that is a smooth as a map into $S$.

**Lemma:** Let $S\subseteq M$ be an immersed submanifold. Every point $p\in S$ is the image of a local parametrization of $S$. If $X:U \to M$ is any such local parametrization, there is uniquely determined smooth coordinate chart $(V, \varphi)$ for $S$ such that $X = \iota \circ \varphi^{-1}$, where $\iota: S \to M$ is the inclusion.

# Submanifolds of Manfolds with Boundary

The definition naturally can be extended to manifolds with boundary. If $M$ and $N$ are smooth manifolds with boundary, a smooth map $F: M \to N$ is said to be an immersion if $F_*$ is injective at each point, a submersion if $F_*$ is surjective at each point, and a smooth embedding if it is an immersion and a topological embedding.

A subset $S\subseteq M$ is said to be an *immersed submanifold* of $M$ if $S$ is endowed with a smooth manifold structure such that the inclusion map is an immersion, and an *embedded submanifold* if in addition $S$ has the subspace topology. 

More generally, an immersed or embedded *submanifold with boundary* in $M$ is defined in exactly the same way, except that now $S$ itself is allowed to be a manifold with boundary,

**Prop:** Let $M$ be a smooth $n$-manifold with boundary. Then $\partial M$ is a topological $(n-1)$-manifold (without boundary), and it has a unique smooth structure such that the inclusion $\iota: \partial M \to M$ is a smooth embedding. This means that $\partial M$ is an embedded hypersurface of $M$. 

# Restricting Maps

**Prop:** If $F: M \to N$ is a smooth map and $S\subseteq M$ is an (immersed or embedded) submanifold, then $F|_S: S\to N$ is smooth.

**Prop:** Let $S\subseteq N$ be an immersed submanifold, and let $F:M \to N$ be a smooth map whose image is contained in $S$. IF $F$ is continuous as a map from $M$ to $S$, then $F: M \to S$ is smooth. 

**Cor:** Let $S\subseteq N$ be an embedded submanifold. Then any smooth map $F: M \to N$ whose image is contained in $S$ is also smooth as a map from $M$ to $S$. 

## Vector and Covector Fields

**Lemma:** Let $M$ be a smooth manifold, and let $S\subseteq M$ be an embedded submanifold, and let $X$ be a smooth vector field on $M$. $Y$ is tangent to $S$ iff $Yf = 0$ on $S$ for every $f\in \mathcal C^\infty (M)$ such that $f|_S  = 0$.

**Prop:** Let $S\subseteq M$ be an immersed submanifold, and let $\iota: S\to M$ denote de inclusion map. If $Y \in \mathfrak X(M)$ is tangent to $S$, then there is a unique smooth vector filed on $S$, denoted by $Y|_S$, that is $\iota$-related to $Y$.

**Cor:** Let $M$ be a smooth manifold and let $S$ be an immersed submanifold. If $Y_1$ and $Y_2$ are smooth vector fields on $M$ that are tangent to $S$, then $[Y_1, Y_2]$ is tangent to $S$ as well.

For covector fields, we only need to consider the pullback of that covector field. 