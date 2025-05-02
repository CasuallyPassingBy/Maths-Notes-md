---
tags:
  - Analysis
  - FunctionalAnalysis
---
Subjects: [[Metric and Normed Spaces]], [[Functional Analysis]]
Links: [[Metric Spaces]], [[Vector Spaces]], [[Rn]], [[Topological Vector Spaces]], [[Convex Hulls]], [[Complete Metric Spaces]]

Let $V$ be a vector space over $\Bbb R$. A _***norm**_ of $V$ is a function $\| \cdot\|: V \to \Bbb R$ that
N1) $\|v \| = 0$ iff $v = 0$
N2) $\|\lambda v \| = |\lambda | \| v\|$ for any $v \in V$, and $\lambda \in \Bbb R$
N3) $\|v+w\| \le \|v\| +\|w\|$ for any $v,w\in V$

A **normed space** is vector space $V$ with a norm $\|\cdot \|$, usually denoted as $(V, \|\cdot\|)$, or simply $V$ where we don’t need to specify the norm.



**Prop:** Every normed space $(V, \|\cdot\| )$ is a metric space with a metric given by$$ d(v,w) = \|v-w\| $$
We can see that every norm induces a metric, but a metric is not always induced by a metric, namely, the discrete metric. This metric is translation invariant, and absolutely homogenuous.

**Prop:** Let $X$ be a normed space. Then $|\|x\| - \|y\|| \le \|x-y\|$ whenever $x. y\in X$. Thus, the functions $x \mapsto \|x\|$ is continuous from $X$ into $\Bbb R$. 

**Prop:** Let $X$ be a normed vector space.
- Addition of vectors is a continuous operation from $X\times X$ into $X$.
- Multiplication of vectors by scalars is a continuous operation from $\Bbb F \times X$ into $X$.

**Cor:** Let $x_0$ be an element of a normed space $X$ and let $\alpha_0$ be a nonzero scalar. Then the maps $x \mapsto x +x_0$ and $x \mapsto \alpha_0 x$ are homeomorphism from $X$ to itself. Consequently, if $A$ is a subet of $X$ that is open, or closed, or compact, then $x_0 + A$ and $\alpha_0 A$ also have that property. If $A$ and $U$ are subsets of $X$ and $U$ is open, then $A+U$ is open.

**Cor:** Let $S$ be a topological space $X$ a normed space. Them the collection of all continuous functions from $S$ into $X$, usually denoted as $\mathcal C(S, X)$, is a vector space over $\Bbb F$ if sums and scalars multiples of functions are defined in the usual way.

**Th:** Let $X$ be a normed space.
- If $S$ is a subspace of $X$, then $\text{cl}_X(S)$ is a subspace of $X$.
- If $C$ is a convex subset of $X$, then $\text{cl}_X(C)$ and $\text{int}_X(C)$ are convex

We can see that [[Bases and Dimension|finite dimensional subspaces]] of a normed space $V$ are [[Topology on Metric Spaces|closed]]

In the context of topological vector spaces, we can define a couple of things. Let $X$ be a normed vector space and $A\subseteq X$. 
- We say that $A$ is *convex* if $ty + (1-t)x \in A$ whenever $x,y \in A$ and $t\in [0, 1]$.
- We say that $A$ is *balanced* if for every $|\alpha| \le 1$, then $\alpha A \subseteq A$.
- We say that $A$ is *absorbing* if, for every $x \in X$, there's $s >0$ such that $x \in tA$ for every $t > s$. 
Let us note something about this properties:
- Absorbing, and nonempty balanced sets contain $0$
- Arbitrary unions and intersections of balanced sets are balanced.
- Arbitrary intersections of convex sets are convex.
- Translates and scalar multiples of convex sets are convex.
- The set $A$ is convex iff $sA + tA = (s+t)A$ whenever $s, t >0$. 

With this in mind, we can define a couple of actions to get different sets: 
- $\langle A \rangle := \bigcap \{Y \subseteq X \mid Y \le X \land A\subseteq Y\}$
- $[A] := \bigcap \{Y \subseteq X\mid X\setminus Y \in \tau_X \land Y \le X \land A \subseteq Y\}$
- $\text{co}(A) := \bigcap \{Y \subseteq X \mid Y \text{ is convex }\land A \subseteq Y\}$
- $\overline{\text{co}}(Y) := \bigcap \{Y \subseteq X \mid Y \text{ is convex and closed}\land A \subseteq Y\}$ 

**Cor:** Let $A$ be a subset of a normed space. Then $[A] = \text{cl}_X({\langle A\rangle})$ and $\overline{\text{co}}(A) = \text{cl}_X(\text{co}(A))$. We also have that $\langle \text{cl}_X(A)\rangle \subseteq [A]$ and $\text{co}(\text{cl}_X(A)) \subseteq \overline{\text{co}}(A)$. 

**Prop:** Every ball in a normed space, whether open or closed, is convex.

**Prop:** Every ball centred at a the origin in normed space, whether open or closed, is balanced and absorbing. 

**Th:** Every closed, convex, absorbing subset of a Banach space includes a neighbourhood of the origin. 

**Prop:** If $Y \le X$ is a subspace with $\text{int}_X(Y) \neq \varnothing$, then $Y= X$.