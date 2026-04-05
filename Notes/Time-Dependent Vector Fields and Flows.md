---
tags:
  - DifferentialGeometry
  - OrdinaryDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Ordinary Differential Equations]]
Links: [[Integral Curves, Flows and Flowouts on Smooth Manifolds]], [[Existence and Uniqueness of Solutions to Systems of Differential Equations]], [[Lie Derivative]], [[The Tensor Bundles]]

Let $M$ be a smooth manifold. A *time-dependent vector field on $M$* is a continuous map $V: J \times M \to TM$, where $J \subseteq \Bbb R$ is an interval, such that $V(t, p) \in T_p M$ for each $(t, p)\in J \times M$. This means that for each $t\in J$, the map $V_t: M \to TM$ is defined by $V_t(p) = V(t, p)$ is a vector field on $M$. If $V$ is a time-dependent vector field on $M$, an *integral curve of $V$* is a differentiable curve $\gamma: J_0 \to M$, where $J_0$ is an interval contained in $J$, such that  $$\gamma'(t) = V(t, \gamma(t)), \quad \text{for all }t\in J_0.$$
Every ordinary vector field $X\in {\frak X}(M)$ determines a time-dependent vector field defined on $\Bbb R\times M$, just by setting $V(t, p) = X_p$. 

A time-dependent vector field might not generate flow, because two integral curves starting at the same point but different times might flow different paths, whereas all integral curves of a flow through a given point have the same image. 

**Fundamental Theorem on Time-Dependent Flows:** Let $M$ be a smooth manifold, let $J\subseteq \Bbb R$ be an open interval, and let $V: J \times M \to TM$ be a smooth time-dependent vector field on $M$. There exists an open subset ${\cal E} \subseteq J \times J \times M$ and a smooth map $\psi: {\cal E} \to M$ called the *time-dependent flow of $V$*, with the following properties:
- For each $t_0\in J$ and $p\in M$ the set ${\cal E}^{(t_0, p)} = \{t\in J \mid (t, t_0, p)\in {\cal E}\}$ is an open interval containing $t_0$, and the smooth curve $\psi^{(t_0, p)}: {\cal E}^{(t_0, p)} \to M$ defined by $\psi^{(t_0, p)} (t) := \psi(t, t_0, p)$ is the unique maximal integral curve of $V$ with initial condition $\psi^{(t_0, p)}(t_0) = p$. 
- If $t_1 \in {\cal E}^{(t_0, p)}$ and $q = \psi^{(t_0, p)} (t_1)$, then ${\cal E}^{(t_1, q)} = {\cal E}^{(t_0, p)}$ and $\psi^{(t_1, q)} = \psi^{(t_0, p)}$. 
- For each $(t_1, t_0)\in J \times J$, the set $M_{t_1, t_0} := \{p\in M \mid (t_1,t_0, p)\in {\cal E}\}$ is an open set in $M$, and the map $\psi_{t_1, t_0}: M_{t_1, t_0} \to M$ defined by $\psi_{t_1, t_0}(p) := \psi(t_1, t_0, p)$ is a diffeomorphism from $M_{t_1, t_0}$ onto  $M_{t_0, t_1}$ with inverse $\psi_{t_0, t_1}$.
- If $p\in M_{t_1, t_0}$ and $\psi_{t_1, t_0}(p) \in M_{t_2, t_1}$, then $p\in M_{t_2, t_0}$ and $$(\psi_{t_2, t_1}\circ \psi_{t_1, t_0}) (p) = \psi_{t_2, t_0} (p). $$
**Prop:** $M$ is a compact smooth manifold and $V: J \times M \to TM$ is a smooth time-dependent vector field on $M$. Then the domain of the time-dependent flow of $V$ is all of $J\times J \times M$. 

This came to me as the analogous idea of a [[Integral Curves, Flows and Flowouts on Smooth Manifolds#Complete Vector Fields|complete vector field]], like the flow is as global as it can be. 

**Def:** Let $M$ be a smooth manifold. A *smooth isotopy of $M$* is a smooth map $H: M\times J \to M$, where $J\subseteq \Bbb R$ is an interval, such that for each $t\in J$, the map $H_t: M \to M$ defined by $H_t(p) = H(p, t)$ is diffeomorphism. In particular if $J$ is the unit interval, then $H$ is a homotopy from $H_0$ to $H_1$ through diffeomorphism. 

**Prop:** Suppose $J\subseteq \Bbb R$ is an open interval and $H: M \times J \to M$ is a smooth isotopy. Then the map $V: J \times M \to TM$ defined by$$V(t,  p) :=\frac{\partial}{\partial t} H(H_t^{-1}(p), t) $$is a smooth time-dependent vector field on $M$, whose time dependent flow is given by $\psi(t, t_0, p) = (H_t \circ H_{t_0}^{-1})(p)$ with domain $J\times J \times M$. 

**Prop:** Suppose $J$ is an open interval and $V: J \times M \to M$ is a smooth time-dependent vector field on $M$ whose time-dependent flow is defined on $J \times J \times M$. For any $t_0\in J$, the map $H: M\times J \to M$ defined $H(t, p) := \psi(t,t_0, p)$ is smooth isotopy of $M$, 

This again feels like the analogous [[Integral Curves, Flows and Flowouts on Smooth Manifolds#^b2db44|theorem for global flows]]. 

**Prop:** Let $M$ be a smooth manifold. Suppose $V: J \times M \to TM$ is a smooth time-dependent vector field and $\psi: {\cal E} \to M$ is its time dependent flow. For any smooth covariant tensor field $A\in \mathcal T^k(M)$ and any $(t_1, t_0, p)\in \cal E$, $$\left.\frac{d}{dt}\right\rvert_{t = t_1}(\psi^*_{t, t_0} A)_p = (\psi^*_{t_1, t_0}(\mathcal L_{V_{t_1}} A))_p.$$
**Def:** A *smooth time-dependent tensor flow* on a smooth manifold $M$ is a smooth map $A: J \to M \to T^kT^* M$, where $J\subseteq \Bbb R$ is an interval, satisfying $A(t, p)\in T^k(T^*_p M)$ for each $(t, p)\in J \times M$. 

**Prop:** Let $M$ be a smooth manifold and $J\subseteq \Bbb R$ be an open interval. Suppose $V: J \times M\to TM$ is a smooth time-dependent vector field on $M$, $\psi: \mathcal E\to M$ is its time-dependent flow, and $A: J\times M \to T^kT^* M$ is a smooth time-dependent tensor field on $M$. Then for any $(t_1, t_0, p) \in \cal E$, $$\left.\frac{d}{dt}\right\rvert_{t =t_1} \left(\psi^*_{t, t_0} A_t\right)_p = \left(\psi^*_{t_1, t_0}\left(\mathcal L_{V_{t_1}} A_{t_1} + \left.\frac{d}{dt}\right\rvert_{t = t_1} A_t\right)\right)_p.$$