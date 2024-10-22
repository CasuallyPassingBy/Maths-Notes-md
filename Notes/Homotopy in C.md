---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Contour Integrals in C]]

**Def:** Suppose $\gamma_0, \gamma_1:[0,1] \to G$ are two continuous curves from $z_0$ and $z_1$ in a set $G$. We say that $\gamma_0$ is **homotopic** with fixed endpoints to $\gamma_1$ in $G$ if there’s a continuous function ${H:[0,1]\times [0,1] \to G}$ from the unit square $[0,1]\times [0,1]$ into $G$ such that:
- $H(0, t) = \gamma_0(t)$ for $t \in [0,1]$
- $H(1, t) = \gamma_1(t)$ for $t \in [0,1]$
- $H(s, 0)= z_0$ for $s \in [0,1]$
- $H(s, 1)= z_1$ for $s \in [0,1]$

this can be expressed as $\gamma_0 \simeq \gamma_1 \pmod G$ or, $\gamma_0 \simeq_H \gamma_1 \pmod G$ if we want to specify the .

This forms an equivalence relations is over the set of continuous curves in $G$ with fixed enpoints $z_0$ and $z_1$.

**Def:** Suppose $\gamma_0, \gamma_1:[0,1] \to G$ are two continuous closed curves in a set $G$, sometimes called a **loop**. We say that $\gamma_0$ and $\gamma_1$ are homotopic as closed curves in $G$ if there’s a continuous function ${H:[0,1]\times [0,1] \to G}$ from the unit square $[0,1]\times [0,1]$ into $G$ such that:
- $H(0, t) = \gamma_0(t)$ for $t \in [0,1]$
- $H(1, t) = \gamma_1(t)$ for $t \in [0,1]$
- $H(s, 0)= H(s, 1)$ for $s \in [0,1]$

this can be expressed as $\gamma_0 \simeq \gamma_1 \pmod G$, and this form an equivalence relation of loops in $G$.

Given $U \subseteq \Bbb C$, the set $X(U) = \{\gamma:[0, 1] \to U \mid \gamma \text{ is closed piecewise smooth} \}$, and the function $d:X(U) \times X(U) \to \Bbb R$ be defined as $$d(\gamma, \sigma) = \sup_{t\in[0,1]}|\gamma(t)-\sigma(t)|$$ 
this gives us that $(X(U), d)$ is a metric space. Let $\varphi:[0,1] \to X(U)$ be continuous, with the added constrains that $\varphi(0) = \gamma_0$ and $\varphi(1) = \gamma_1$, then we see that a homotopy, is just a path connecting both of the curves, in $X(U)$ space 

Let $U\subseteq \Bbb C$ region. Given $a, b \in U$ with $a\ne b$. If $\gamma_a \equiv a$ and $\gamma_b \equiv b$, then $\gamma_a \simeq \gamma_b \pmod U$. 

Given the two homotopic curves $\gamma \simeq \sigma \pmod U$, then it is not true that $\gamma - \sigma \simeq 0 \pmod U$, since we cannot even ensure that $\gamma - \sigma$ is a closed curve, using the difference for [[Homology in C|cycles]]

**Prop:** If $A$ is a convex region, then any two closed curves in $A$ are homotopic as closed curves in $A$, and any two curves with some endpoints are homotopic with fixed points.

**Cor:** A convex region is simply connected

If $U \subseteq \Bbb C$ is a star region, then every closed piecewise smooth curve $\gamma$, $\gamma \simeq 0 \pmod U$

If $\gamma \subseteq B_r(z)$, then $\gamma \simeq 0 \pmod {B_r(z)}$  

**Def:** A homotopy $H:[0,1]\times [0,1] \to G$ is called _**smooth**_ if the intermediate curves $\gamma_s(t)$ are piecewise smooth functions of $t$ for each $s$ and the cross curves $\lambda_t(s)$ are piecewise smooth functions of $s$ for each $t$

We have that in general, $\gamma \sim 0 \pmod U \centernot \implies \gamma \simeq 0 \pmod U$, so in a sense homology is weaker

### Smooth Deformation Theorem
Suppose $f$ is an holomorphic function on an open set $G$ and that $\gamma_0$ and $\gamma_1$ are piecewise smooth curves in $G$.

- If $\gamma_0$ and $\gamma_1$ are paths from $z_0$ to $z_1$ and are homotopic in $G$ with fixed endpoints with a smooth homotopy, then
    
    $$ \int_{\gamma_0} f = \int_{\gamma_1} f $$
    
- If $\gamma_0$ and $\gamma_1$ are closed curves which are homotopic as closed curves in $G$ with a smooth homotopy, then
    $$ \oint_{\gamma_0} f = \oint_{\gamma_1} f $$
