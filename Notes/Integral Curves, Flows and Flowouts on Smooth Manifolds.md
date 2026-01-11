---
tags:
  - DifferentialGeometry
  - OrdinaryDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Ordinary Differential Equations]]
Links: [[Vector Fields on Smooth Manifolds]], [[Existence and Uniqueness of Solutions to Systems of Differential Equations]], [[Tangent Space for Manifolds]]

**Def:** If $V$ is a vector field on $M$, an *integral curve of $V$* is differentiable curve $\gamma: J \to M$ whose velocity at each point is equal to the value of $V$ at each point: $$ \gamma'(t) = V_{\gamma(t)} \qquad \text{for all }t\in J.$$If $0\in J$, the point $\gamma(0)$ is called the *starting point of $\gamma$*. 

Finding integral curves boils down to solving a system of ordinary differential equation on a smooth chart. Suppose $V$ is a smooth vector field on $M$ and $\gamma: J \to M$ is a smooth curve. On a smooth coordinate domain $U \subseteq M$, we can write $\gamma$ in local coordinates as $\gamma = (\gamma^1(t), \dots, \gamma^n(t))$. Then the condition $\gamma'(t) = V_{\gamma(t)}$ for $\gamma$ to be an integral curve on $V$ can be written as $$\dot \gamma^i(t) \left.\frac{\partial}{\partial x^i}\right\rvert_{\gamma(t)} = V^i(\gamma(t)) \left.\frac{\partial}{\partial x^i}\right\rvert_{\gamma(t)}, $$which reduced to the following autonomous system of ordinary differential equations: $$\begin{align*}\dot\gamma^1 (t) &= V^1(\gamma^1(t),\dots, \gamma^n(t)) \\ \vdots & \\ \dot\gamma^n (t) &= V^n(\gamma^1(t),\dots, \gamma^n(t)). \end{align*}$$
We use a dot denote the ordinary derivative with respect to $t$ when there are such superscripts that would make primes hard to read. The important fact about such system is the existence, uniqueness, and smoothness theorem. This is the reason for the name *integral curves*, because solving a system of ODEs is often referred as 'integrating' the system.

**Prop:** Let $V$ be a smooth vector field on a smooth manifold $M$. For each point $p\in M$, there exists $\varepsilon > 0$ and a smooth curve $\gamma: (-\varepsilon, \varepsilon) \to M$ that is an integral curve of $V$ starting at $p$. 

**Rescaling Lemma:** Let $V$ be a smooth vector field on a smooth manifold $M$, let $J \subseteq \Bbb R$ be an interval and $\gamma: J \to M$ be an integral curve of $V$. For any $a\in \Bbb R$, the curve $\tilde \gamma: \tilde J\to M$ defined by $\tilde \gamma(t) := \gamma(at)$ is an integral curve of the vector field $aV$, where $\tilde J := \{t \mid at \in J\}$. 

**Translation Lemma:** Let $V$, $M$, $J$, and $\gamma$ be as in the preceding lemma. For any $b\in \Bbb R$, the curve $\hat \gamma: \hat J \to M$ defined by $\hat \gamma(t) := \gamma(t+b)$ is also an integral curve of $V$, where $\hat J:= \{t\mid t+b\in J\}$. 

**Naturality of Integral Curves:** Suppose $M$ and $N$ are smooth manifolds and $F: M \to N$ is a smooth map. The $X\in {\frak X}(M)$ and $Y\in {\frak X}(N)$ are $F$-related iff $F$ takes integral curves of $X$ to integral curves of $Y$, meaning that for each integral curve $\gamma$ of $X$, $F \circ \gamma$ is an integral curve of $Y$.

# Flows

**Def:** We define a *global flow* on $M$, also called a *one-parameter group action*, to be a continuous left $\Bbb R$-action on $M$; that is a continuous map $\theta: \Bbb R\times M\to M$ satistfying the following properteis for all $s, t\in \Bbb R$ and $p\in M$:$$\theta(t, \theta(s, p)) = \theta(t+s, p), \qquad \theta(0, p) = p.$$Given a global flow $\theta$ on $M$, we define two collections of maps:
- For each $t\in \Bbb R$, we define $\theta_t: M \to M$ by $$\theta_t(p) = \theta(t, p).$$We see that that $\theta_t\circ \theta_s = \theta_{t+s}$ and $\theta_0 = \text{id}_M$. As in the case for continuous group actions, each $\theta_t : M\to M$ is a homeomorphism, and if the flow is smooth, $\theta_t$ is a diffeomorphism. 
- For each $p\in M$, we define a curve $\theta^{(p)}: \Bbb R\to M$ by $$\theta^{(p)}(t) := \theta(t, p).$$The image of this curve is the orbit of $p$ under the group action.  

If $\theta: \Bbb R \times M \to M$ is a smooth global flow, for each $p\in M$ we define a tangent vector $V_p\in T_p M$ by $$V_p := {\theta^{(p)}}'(0).$$The assingment $p\mapsto V_p$ is a (rough) vector field on $M$, which is called the *infinitesimal generator of $\theta$*.

**Prop:** Let $\theta: \Bbb R \times M\to M$ be a smooth global flow on a smooth manifold $M$. The infinitesimal generator $V$ of $\theta$ is a smooth vector field on $M$, and each curve $\theta^{(p)}$ is an integral curve of $V$. 

We have that every smooth global flow gives rise to a smooth vector field whose integral curves are precisely the curves defined by the flow. We would like to be able to say that every smooth vector field is an infinitesimal generator of a smooth global flow. However, we can see that this cannot be the case, because there are smooth vector fields whose integral curves are not defined for all $t\in \Bbb R$. 

With this in mind, we need a generalisation of the idea of a global flow. 

**Def:** If $M$ is a manifold a *flow domain* for $M$ is an open subset $\mathcal D \subseteq \Bbb R\times M$ with the property that for each $p\in M$ the set $\mathcal D^{(p)} := \{t\in \Bbb R\mid (t, p) \in \mathcal D\}$ is an open interval containing $0$. A *flow* on $M$ is a continuous map $\theta: \mathcal D \to M$, where $\mathcal D \subseteq \Bbb R \times M$ is a flow domain that satisfies the following group laws: for all $p\in M$,$$\theta(0, p) = p,$$and for all $s\in \mathcal D^{(p)}$ and $t\in \mathcal D^{(\theta(s, p))}$ such that $s+t\in \mathcal D^{(p)}$, $$\theta(t, \theta(s, p)) = \theta(t+s, p).$$
We sometimes call $\theta$ a *local flow* to distinguish it from a global flow. The unwieldy term *local one-parameter group action* is also used.

If $\theta$ is a flow, we define $\theta_t(p) = \theta^{(p)} (t) = \theta(t, p)$ whenever $(t, p)\in\cal D$, just as for the global flow. For each $t\in \Bbb R$, we also define $$M_t = \{p\in M \mid (t, p)\in \mathcal D\},$$so that $$p\in M_t \iff t\in\mathcal D^{(p)} \iff (t, p) \in \cal D.$$If $\theta$ is smooth, the *infinitesimal generator of $\theta$* is defined by $V_p = {\theta^{(p)}}' (0)$. 

**Prop:** If $\theta: \mathcal D \to M$ is a smooth flow, then the infinitesimal generator of $\theta$ is a smooth vector field, and each curve $\theta^{(p)}$ is an integral curve of $V$. 

**Def:** A *maximal integral curve* is one that cannot be extended to an integral curve on any larger open interval, and a *maximal flow* is a flow that admits no extension to a flow on a larger flow domain. 

**Fundamental Theorem on Flows:** Let $V$ be a smooth vector field on a smooth manifold $M.$ There is a unique smooth maximal flow $\theta: {\cal D}\to M$ whose infinitesimal generator is $V.$ This flow has the following properties:
- For each $p\in M$, the curve $\theta^{(p)}: {\cal D}^{(p)} \to M$ is the unique maximal integral curve of $V$ starting at $p$.
- If $s\in \mathcal D^{(p)}$, then $\mathcal D^{(\theta(s, p))}$ is the interval $\mathcal D^{(p)}-s$. 
- For each $t\in\Bbb R$, the set $M_t$ is open in $M$, and $\theta_t: M_t \to M_{-t}$ is diffeomorphism with inverse $\theta_{-t}$. 

### Complete Vector Fields

**Def:** The flow whose existence and uniqueness are asserted in the fundamental theorem is called the *flow generated by $V$*, or just the *flow of $V$*. 

**Naturality of Flows:** Suppose $M$ and $N$ are smooth manifolds, $F: M \to N$ is a smooth map $X\in {\frak X}(M)$, and $Y\in {\frak X}(N)$. Let $\theta$ be the flow of $X$ and $\eta$ be the flow of $Y$. If $X$ and $Y$ are $F$-related, then for each $t\in \Bbb R$, $F[M_t] \subseteq N_t$ and $\eta_t \circ F = F \circ \theta_t$ on $M_t$: 
```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
M_t \arrow[r,"F"] \arrow[d, "\theta_t"'] & N_t \arrow[d, "\eta_t"] \\ M_{-t} \arrow[r, "F"'] & N_{-t}
\end{tikzcd}
\end{document}
```

**Diffeomorphism Invariance of Flows:** Let $F: M \to N$ be a diffeomorphism. If $X\in {\frak X}(M)$ and $\theta$ is the flow of $X$, then the flow of $F_*X$ is $\eta_t = F \circ \theta_t \circ F^{-1}$, with domina $N_t = F[M_t]$ for each $t\in \Bbb R$.

**Def:** We say that a smooth vector field is complete if it generates a global flows, or equivalently if each of its maximal integral curves is defined for all $t\in\Bbb R$. 

**Uniform Time Lemma:** Let $V$ be a smooth vector field on a smooth manifold $M$, and let $\theta$ be its flow. Suppose there is a positive number $\varepsilon$ such that for every $p\in M$, the domain $\theta^{(p)}$ contained $(-\varepsilon, \varepsilon)$. Then $V$ is complete.

**Th:** Every compactly supported smooth vector field on a smooth manifold is complete.

**Cor:** On a compact smooth manifold, every smooth vector field is complete.

**Th:** Every left-invariant vector field on a Lie group is complete.

**Escape Lemma:** Suppose $M$ is a smooth manifold and $V\in {\frak X}(M)$. If $\gamma: J \to M$ is a maximal integral curve of $V$ whose domain $J$ has a finite supremum $b$, then for any $t\in J$, $\gamma[[t_0, b)]$ is not contained in any compact subset of $M$. 

**Prop:** Every non-compact manifold admits and incomplete vector field.

**Cor:** A smooth manifold is compact iff every vector field is complete.

### Flowout

**Flowout Theorem:** Suppose $M$ is a smooth manifold, $S\subseteq M$ is an embedded $k$-dimensional submanifold, and $V\in {\frak X}(M)$ is a smooth vector field that is nowhere tangent to $S$. Let $\theta: {\cal D}\to M$ be the flow of $V$, and let ${\cal O} := (\Bbb R \times S) \cap \cal D$ and let $\Phi = \theta|_\cal O$.
- $\Phi: {\cal O}\to M$ is an immersion.
- $\dfrac{\partial}{\partial t}\in {\frak X}({\cal O})$ is $\Phi$-related to $V$.
- There is a smooth positive function $\delta: S \to \Bbb R$ such that the restriction of $\Phi$ to ${\cal O}_\delta$ is injective, where $\cal O_\delta \subseteq O$ is the flow domain, $${\cal O}_\delta := \{(t,p) \in |t| < \delta(p)\}. $$Thus, $\Phi[{\cal O}_\delta]$ is an immersed submanifold of $M$ containing $S$, and $V$ is tangent to this manifold.
- If $S$ has codimension $1$, then $\Phi|_{{\cal O}_\delta}$ is a diffeomorphism onto an open submanifold of $M$. 

**Def:** The submanifold $\Phi[{\cal O}_\delta]\subseteq M$ is called the *flowout from $S$ along $V$*. 

### Regular and Singular Points

**Def:** If $V$ is a vector field on $M$, a point $p\in M$ is said to be a *singular point of $V$* if $V_p = 0$, and a *regular point* otherwise. 

**Prop:** Let $V$ be a smooth vector field on a smooth manifold $M$, and let $\theta: \mathcal D \to M$ be the flow generate by $V$. If $p\in M$ is a singular point of $V$, then $\mathcal D^{(p)} = \Bbb R$ and $\theta^{(p)}$ is the constant curve $\theta^{(p)}(t) = p$ for all $t\in \Bbb R$. If $p$ is a regular point, then $\mathcal D^{(p)}\to M$ is a smooth immersion. 

**Def:** If $\theta: \mathcal D \to M$ is a flow, a point $p\in M$ is called an *equilibrium point of $\theta$* if $\theta(t, p) = p$ for all $t\in {\cal D}^{(p)}$. We see that equilibrium points of a smooth flow are precisely the singular points of its infinitesimal generator.

**Canonical Form Near a Regular Point:** Let $V$ be a smooth vector field on a smooth manifold $M$, and let $p\in M$ be a regular point of $V$. There exists smooth coordinates $(s^i)$ on some neighbourhood of $p$ in which $V$ has the coordinate representation $\dfrac{\partial}{\partial s^1}$. If $S\subseteq M$ is any embedded hypersurface with $p\in S$ and $V_p \notin T_pS$, then the coordinates can be also chosen so that $s^1$ is a local defining function for $S$. 