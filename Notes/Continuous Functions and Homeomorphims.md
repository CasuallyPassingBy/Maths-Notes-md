---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Continuity on R]], [[Continuity on Metric Spaces]] [[Limits and Continuity of real valued functions of Rm]], [[Limits and Continuity of Vector valued functions of Rn]], [[Topological Spaces]]

## Continuous Functions

Let $f:X\to Y$, where $X$ and $Y$ are topological spaces
- We say that $f$ is *continuous* at the point $x_0\in X$ if for any open subset $A$ of $Y$ that contains $f(x_0)$, there's a open subset $B$ of $X$ that contains $x_0$ and that satisfies $f[B] \subseteq A$
- In the case where $f$ is *continuous* on all the points of $X$, we say that $f$ is continuous
- $f$ is discontinuous (on $x_0\in X$) if it is not continuous (on $x_0\in X$)

The continuity of any function can be checked using topological bases.

If $f$ is a function from a topological space $X$ into the topological space $Y$, then the following are equivalent
- $f$ is continuous
- For any open set $U$ of $Y$, $f^{-1}[U]$ is open in $X$
- For any closed set $F$ of $Y$, $f^{-1}[F]$ is closed in $X$
- For any $A\subseteq X$, we have that $f[\text{cl}_X(A)] \subseteq \text{cl}_Y(f[A])$ 
- For any $B \subseteq Y$, we have that $\text{cl}_X(f^{-1}[B]) \subseteq f^{-1}[\text{cl}_Y(B)]$ 

If $f:X\to Y$ be a function between topological spaces, then the following are equivalent
- $f:X \to Y$ is continuous
- For each $Z \subseteq Y$ such that $\text{Im }f \subseteq Z$, the function $f:X\to Z$ is continuous where $Z$ contains the subspace topology with respect to $Y$

If $\cal B$ and $\cal S$ are a base and a subbase of $Y$ respectively, then the following are equivalent
- $f$ is continuous
- $f^{-1}[B]$ is open in $X$ for each $B\in \cal B$
- $f^{-1}[S]$ is open in $X$ for each $S\in \cal S$

Let $f:(X, \tau_1) \to (Y, \tau_2)$ be continuous. If $\tau_1'$ and $\tau_2'$ are two topologies defined on $X$ and $Y$, respectively, that satisfy $\tau_2' \le \tau_2$ and $\tau_1\le \tau_1'$, then $f:(X, \tau_1') \to (Y, \tau'_2)$ is also continuous. 

If the functions $f: X\to Y$ and $g:Y\to Z$ are continuous, then the composition $g\circ f$ is also continuous

If $f:X\to Y$ is a continuous function and $A$ is a subspace of $X$, then the function $f|_A :A\to Y$ is continuous.

Let $(X, \tau)$ be a topological space and $f, g:X \to \Bbb R$ continuous functions. Then the functions $P, Q, R, S:X\to \Bbb R$ and $\Delta: X\to \Bbb R^2$ defined by
- $P(x) = f(x) \cdot g(x)$
- $Q(x) = |f(x)|$
- $R(x) = -f(x)$ 
- $S(x) = f(x)+g(x)$
- $\Delta(x) = (f(x), g(x))$
for all $x\in X$, are continuous. Additionally, the function $D(x) = 1/f(x)$, defined on $\{x\in X\mid f(x) \ne 0\}$ is also continuous

Let $f, g:X \to \Bbb R$ be continuous functions, then the function $\min\{f, g\}, \max\{f, g\}: X\to \Bbb R$  are continuous

## Homoemorphisms

The bijective function $\varphi$ defined over the topological space $X$ and with values in the space $Y$, it is called a *homeomorphism* if $\varphi$ is continuous with continuous inverse.
The topological spaces $X$ and $Y$ are called *homeomorphic* if there's a homeomorphism between them. The expression $X\cong Y$ signifies that the spaces $X$ and $Y$ are homeomorphic

A property $P$ is topological if for each space $X$ with the property $P$, then any homeomorphic space to $X$ also has the property $P$

Let $f$ be a function from that topological space $X$ to the topological space $Y$
- $f$ is an *open function* if the image under $f$ of any open subset of $X$ is an open subset of $Y$
- $f$ is an *closed function* if the image under $f$ of any closed subset of $X$ is an closed subset of $Y$

$f$ is open iff $f[B]$ is open on $Y$ for each $B\in \cal B$, where $\cal B$ is a base for $X$. Similarly, $f$ is closed iff $f[C]$ is open on $Y$ for each $C\in \cal C$, where $\cal C$ is a closed base for $X$. 

If $f$ is a bijective function between the topological space $X$ and $Y$, then the following are equivalent
- $f^{-1}$ is continuous
- $f$ is open
- $f$ is closed
In particular, a continuous bijective function $f:X\to Y$ is a homeomorphism if it satisfies any of the above conditions.

If $Y$ is a subspace of $X$, then the inclusion $\iota:Y\to X$ is closed/open iff the set $Y$ is closed/open on $X$

