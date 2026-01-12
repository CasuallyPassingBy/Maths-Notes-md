---
tags:
  - DifferentialGeometry
  - OrdinaryDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Ordinary Differential Equations]]
Links: [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[Existence and Uniqueness of Solutions to Systems of Differential Equations]], [[Vector Fields on Smooth Manifolds]], [[Tangent Space for Manifolds]], [[Homotopy]]

**Boundary Flowout Theorem:** Let $M$ be a smooth manifold with nonempty boundary, and let $N$ b a smooth vector field $M$ that is inward pointing at each point of $\partial M$. There exists a smooth function $\delta: \partial M \to \Bbb R^+$ and a smooth embedding $\Phi: {\cal P}_\delta\to M$, where $${\cal P}_\delta := \{(t, p) \mid p\in \partial M, 0 \le t < \delta(p)\} \subseteq \Bbb R\times \partial M,$$such that $\Phi[{\cal P}_\delta]$ is a neighbourhood of $\partial M$, and for each $p\in \partial M$ the map $t \mapsto \Phi(t, p)$ is an integral curve of $N$ a starting at $p$. 

**Def:** Let $M$ be a smooth manifold with boundary. A neighbourhood of $\partial M$ is called a *collar neighbourhood* if it is the image of a  smooth embedding $[0, 1) \times \partial M \to M$ that restricts to the obvious identification $\{0\} \times \partial M \to \partial M$. 

**Collar Neighbourhood Theorem:** If $M$ is a smooth manifold with nonempty boundary, then $\partial M$ has a collar neighbourhood. 

**Th:** Let $M$ be a smooth manifold with nonempty boundary, and let $\iota: \text{Int }M \hookrightarrow M$ denote the inclusion. There exists a proper smooth embedding $R: M \to \text{Int }M$ such that $\iota \circ R: M \to M$ and $R\circ \iota: \text{Int }M\to \text{Int }M$ are smoothly homotopic maps. Therefore, $\iota$ is a homotopy equivalence.

The theorem above gives us a generalisation of the [[The Whitney Approximation Theorem]]. 

**Whitney Approximation for Manifold with Boundary:** If $M$ and $N$ are smooth manifolds with boundary, then every continuous map from $M$ to $N$ is homotopic to a smooth map.

**Attaching Smooth Manifolds Along Their Boundaries:** Let $M$ and $N$ be smooth $n$-manifolds with nonempty boundaries, and suppose $h: \partial N \to \partial M$ is diffeomorphism. Let $M \;\cup_h N$ be the adjunction space formed by identifying each $x\in \partial N$ with $h(x) \in \partial M$. Then $M\;\cup_h N$ is a topological manifold without boundary, and has a smooth estructure such that there are regular domains $M', N' \subseteq M\;\cup_h N$ diffeomorphic to $M$ and $N$, respectively, and satisfying
- $M' \cup N' = M\; \cup_h N$,
- $M'\cap N' = \partial M' = \partial N'$. 
If $M$ and $N$ are both compact, then $M \; \cup_h N$ is compact, and if they are both connected. then $M \;\cup_h N$ is connected.

**Cor:** Suppose $M$ and $N$ are smooth $n$-manifolds with boundary, $A\subseteq \partial M$ and $B \subseteq \partial N$ are nonempty subsets that are unions of components of the respective boundaries, and $h: B\to A$ is a diffeomorphism.  Let $M \;\cup_h N$ be the adjunction space formed by identifying each $x\in \partial N$ with $h(x) \in \partial M$. Then $M\;\cup_h N$ is a topological manifold with boundary, and has a smooth estructure such that there are regular domains $M', N' \subseteq M\;\cup_h N$ diffeomorphic to $M$ and $N$, respectively, and satisfying
- $M' \cup N' = M\; \cup_h N$,
- $M'\cap N' = \partial M' = \partial N'$. 
If $M$ and $N$ are both compact, then $M \; \cup_h N$ is compact, and if they are both connected. then $M \;\cup_h N$ is connected.

**Example:** 
- **Connected Sums:** Let $M_1$, $M_2$ be connected smooth manifold of dimension $n$. For $i = 1,2$, let $U_i$ be a regular coordinate ball centred at some point $p_i \in M_i$, and let $M_i' := M_i \setminus U_i$. We know that $M_i'$ is a smooth manifold whose boundary is diffeomorphic to $\Bbb S^{n-1}$. A *smooth connected sum $M_1$ an $M_2$*, denoted by $M_1\#M_2$, is a smooth manifold formed by choosing a diffeomorphism from $\partial M_1$ to $\partial M_2$ and attaching $M_1'$ and $M_2'$ along their boundaries. 
- **Double of a Smooth Manifold With Boundary:** Let $M$ be a smooth manifold with boundary. The *double of $M$* is the manifold $D(M) := M \cup_\text{id} M$; it is obtained from $M \sqcup M$ by identifying each boundary point in one copy of $M$ with the same boundary in the other. It is a smooth manifold without boundary, and contains two regular comains diffeomorphic to $M$. It is easy to check that $D(M)$ is compact iff $M$ is compact, and connected iff $M$ is connected. Sometimes it is useful to extend the definition to manifolds without boundary by defining $D(M) = M \sqcup M$ when $\partial M = \varnothing.$

**Lemma:** Suppose $M$ is a smooth manifold and $D\subseteq M$ is a regular domain. If $V$ is smooth vector field on $M$ that is tangent to $\partial M$, then every integral curve of $V$ that starts in $D$ remains in $D$ as long as it is defined. 

So Like this theorem tells us that the $\partial D$ splits the integral curves inside $D$ and outside $D$.

**Flows on Manifolds with Boundary:** Let $M$ be a smooth manifold with boundary and $V$ be a smooth vector field on $M$ that is tangent to $\partial M$. There is a unique smooth maximal flow $\theta: {\cal D}\to M$ whose infinitesimal generator is $V.$ This flow has the following properties:
- For each $p\in M$, the curve $\theta^{(p)}: {\cal D}^{(p)} \to M$ is the unique maximal integral curve of $V$ starting at $p$.
- If $s\in \mathcal D^{(p)}$, then $\mathcal D^{(\theta(s, p))}$ is the interval $\mathcal D^{(p)}-s$. 
- For each $t\in\Bbb R$, the set $M_t$ is open in $M$, and $\theta_t: M_t \to M_{-t}$ is diffeomorphism with inverse $\theta_{-t}$. 

**Canonical Form Near a Regular Point on the Boundary:** Let $M$ be a smooth manifold with boundary and let $V$ be a smooth vector field on $M$ that is tangent to $\partial M$. If $p\in \partial M$ is a regular point of $V$, there exists a smooth boundary coordinates $(s^i)$ on some neighbourhood of $p$ in which $V$ has coordinate representation $\dfrac{\partial}{\partial s^1}$. 