---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Smooth Manifolds]], [[Embedded Smooth Submanifolds]], [[Immersed Smooth Submanifolds]]

**Def:** If $M$ is a smooth manifold with or without boundary, a *smooth submanifold with boundary in $M$* is a subset $\subseteq M$ endowed with a topology and smooth structure making it into a smooth manifold with boundary such that the inclusion map is a smooth immersion. If the inclusion map is an embedding it is called an *embedded submanifold with boundary*; in the general case, it is an *immersed submanifold with boundary*. The terms *codimension* and *properly embedded* are defined just as in the submanifold case.

One particular type of submanifold with  boundary is particularl important. If $M$ is a smooth manifold with or without boundary, a *regular domain in $M$* is a properly embedded codimension $0$-submanifold with boundary. 

**Prop:** Suppose $M$ is a smooth manifold without boundary and $D\subseteq M$ is a regular domain. The topological interior and boundary of $D$ are equal to its manifold interior and boundary, respectively. 

**Prop:** Suppose $M$ is a smooth manifold and $f\in \mathcal C^\infty(M)$
- For each regular value $b$ of $f$, the subset $f^{-1}[(-\infty, b]]$ is a regular domain in $M$.
- If $a$ and $b$ are two regular values of $f$ with $a< b$, then $f^{-1}[[a,b]]$ is a regular domain in $M$. 

**Def:** A set of the form $f^{-1}[(-\infty, b]]$ for regular value of $f$ is called a *regular sublevel of $f$*. If $D\subseteq M$ is a regular domain and $f\in\mathcal C^\infty(M)$ is a smooth function such that $D$ is a regular subleve set of, then $f$ is called a *defining function for $D$.*

**Th:** If $M$ is a smooth manifold and $D\subseteq M$ is a regular domain, then there exists a defining function for $D$. if $D$ is compact, then $f$ can be taken to be a smooth exhaustion function fo $M$. 

**Properties of Submanifolds with Boundary:** Suppose $M$ is smooth manifold with or without boundary.
- Every open subset of $M$ is an embedded codimension-$0$ submanifold, with (posiibly empty) boundary.
- If $N$ is a smooth manifold with boundary and $F:N \to M$ is a smooth embedding, then with the subspace topology $F[N]$ is a topological manifold with boundary, and it has a smooth structure making it into an embedded submanifold with boundary in $M$.
- An embedded submanifold with boundary in $M$ is properly embedded iff it is closed.
- If $S\subseteq M$ is an immersed submanifold with boundary, then for each $p\in S$ there exists a neighbourhood $U$ of $p$ in $S$ that is embedded in $M$. 

**Def:** Suppose $M$ is a smooth manifold (without boundary). If $(U, (x^i))$ is a chart for $M$, a $k$*-dimensional half-slice of $U$* is a subset of the following for some constants $c^{k+1}, \dots,c^n$: $$\{(x^1,\dots, x^n) \in U\mid x^{k+1} = c^{k+1}, \dots x^n = c^n, \text{ and }x^k \ge 0\}.$$We say that a subset $S\subseteq M$ satisfies the *local $k$-slice condition for submanifolds with boundary* if each point of $S$ is contained in the codomain of a smooth chart $(U, (x^i))$ such that $S\cap U$ is either an ordinary $k$-dimensional slice or a $k$-dimensional half-slice. In the former, case the chart is called an *interior slice chart for $S$ in $M$*, and the latter, it is a *boundary slice chart for $S$ in $M$,*

**Th:** Let $M$ be a smooth $n$-manifold without boundary. If $S\subseteq M$ is an embedded $k$-dimensional submanifold with boundary, then $S$ satisfies the local $k$-slice condition for manifolds with boundary. Conversely, if $S\subseteq M$ is a subset that satisfies the local $k$-slice condition for submanifolds with boundary, and it has smooth structure making it into an embedded submanifold with boundary in $M$.

**Th:** Suppose $M$ and are smooth manifold with boundary and $S\subseteq M$ is an embedded submanifold with boundary.
- If $F:M \to N$ is a smooth map, then $F|_S: S \to N$ is smooth.
- If $\partial M= \varnothing$ and $F: N \to M$ is a smooth map whose image is contained in $S$, then $F$ is a smooth map from $N$ to $S$. 

We can actually strengthen this theorem using [[Flows and Flowouts on Manifold with Boundary|flows]], since we can get the following: 

**Th:** Suppose $M$ and are smooth manifold with boundary and $S\subseteq M$ is an embedded submanifold with boundary. If $F: N  \to M$ is a smooth map whose image is contained in $S$, then $F$ is a smooth map from $N$ to $S$. 

**Prop:** Suppose $M$ is a smooth manifold with boundary, $N$ is a smooth manifold and $F: M \to N$ is a smooth map. Let $S := F^{-1}\{c\}$, where $c\in N$ is a regular value for both $F$ and $F|_{\partial M}$. Then $S$ is a smooth submanifold with boundary in $M$, with $\partial S = S \cap \partial M$.  