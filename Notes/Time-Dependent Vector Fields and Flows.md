---
tags:
  - DifferentialGeometry
  - OrdinaryDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Ordinary Differential Equations]]
Links: [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[Existence and Uniqueness of Solutions to Systems of Differential Equations]]

Let $M$ be a smooth manifold. A *time-dependent vector field on $M$* is a continuous map $V: J \times M \to TM$, where $J \subseteq \Bbb R$ is an interval, such that $V(t, p) \in T_p M$ for each $(t, p)\in J \times M$. This means that for each $t\in J$, the map $V_t: M \to TM$ is defined by $V_t(p) = V(t, p)$ is a vector field on $M$. If $V$ is a time-dependent vector field on $M$, an *integral curve of $V$* is a differentiable curve $\gamma: J_0 \to M$, where $J_0$ is an interval contained in $J$, such that  $$\gamma'(t) = V(t, \gamma(t)), \quad \text{for all }t\in J_0.$$
Every ordinary vector field $X\in {\frak X}(M)$ determines a time-dependent vector field defined on $\Bbb R\times M$, just by setting $V(t, p) = X_p$. 

A time-dependent vector field might not generate flow, because two integral curves starting at the same point but different times might flow different paths, whereas all integral curves of a flow through a given point have the same image. 

**Fundamental Theorem on Time-Dependent Flows:** Let $M$ be a smooth manifold, let $J\subseteq \Bbb R$ be an open interval, and let $V: J \times M \to TM$ be a smooth time-dependent vector field on $M$. There exists an open subset ${\cal E} \subseteq J \times \times J \times M$ and a smooth map $\psi: {\cal E} \to M$ called the *time-dependent flow of $V$*, with the following properties:
- For each $t_0\in J$ and $p\in M$ the set ${\cal E}^{(t_0, p)} = \{t\in J \mid (t, t_0, p)\in {\cal E}\}$ is an open interval containing $t_0$, and the smooth curve $\psi^{(t_0, p)}: {\cal E}^{(t_0, p)} \to M$ defined by $\psi^{(t_0, p)} (t) := \psi(t, t_0, p)$ is the unique maximal integral curve of $V$ with initial condition $\psi^{(t_0, p)}(t_0) = p$. 
- If $t_1 \in {\cal E}^{(t_0, p)}$ and $q = \psi^{(t_0, p)} (t_1)$, then ${\cal E}^{(t_1, q)} = {\cal E}^{(t_0, p)}$ and $\psi^{(t_1, q)} = \psi^{(t_0, p)}$. 
- For each $(t_1, t_0)\in J \times J$, the set $M_{t_1, t_0} := \{p\in M \mid (t_1,t_0, p)\in {\cal E}\}$ is an open set in $M$, and the map $\psi_{t_1, t_0}: M_{t_1, t_0} \to M$ defined by $\psi_{t_1, t_0}(p) := \psi(t_1, t_0, p)$ is a diffeomorphism from $M_{t_1, t_0}$ onto $M_{t_0, t_1}$ with inverse $\psi_{t_0, t_1}$.
- If $p\in M_{t_1, t_0}$ and $\psi_{t_1, t_0}(p) \in M_{t_2, t_1}$, then $p\in M_{t_2, t_0}$ and $$(\psi_{t_2, t_1}\circ \psi_{t_1, t_0}) (p) = \psi_{t_2, t_0} (p). $$
