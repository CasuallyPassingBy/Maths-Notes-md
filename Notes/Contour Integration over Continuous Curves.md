---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Contour Integrals in C]]
# Shabat's Technique

********Def:******** Let a function $f$ be defined in a domain $D$ and let $\gamma:[a,b] \to D$ be an arbitrary continuous path. A function $\Phi :[a,b] \to \Bbb C$ is an antiderivative of $f$ along the path $\gamma$ if:
- $\Phi$ is continuous on $I$
    
- for any $t_0 \in I$ there exists an open neighborhood $U \subseteq D$ of the point $z_0 = \gamma(t_0)$ so that $f$ has an antiderivative $F_U$ in $U$ such that  $$ F_U(\gamma(t)) = \Phi(t) $$
    for all $t$ in a neighborhood $U_{t_0} \subseteq I$
    
**Def:** Let $\gamma:[a, b] \to D$ a continuous curve and let $f: D \to \Bbb C$ be an anaylitic function on $D$, with antiderivative $\Phi$ along $\gamma$, we define the integral over $\gamma$ of $f$ as

$$ \int_\gamma f(z) \, dz := \Phi(b) - \Phi(a) $$

********Th:******** Let $f:D \to \Bbb C$ be holomorphic on $D$, and let $\gamma:I \to D$ be a continuous path. Then an antidervative of $f$ along $\gamma$ exists and is defined up to a constant.

**Th:** Let $\gamma:[a,b] \to \Bbb C$ be a piecewise smooth path and let $f$ be a continuous on $\gamma$ and have an antiderivative of $\Phi$ along $\gamma$, then
$$ \int_\gamma f(z) \, dz = \Phi(b) - \Phi(a) $$

# Paper's Techinque

in this section all parametrizations of curves are from the interval $[0,1]$

**Def:** Let $\gamma, \lambda:[0,1] \to \Bbb C$ be parameterized curves in $\Bbb C$, let

$$ d(\lambda, \gamma) := \sup_{t\in [0,1]} |\lambda(t)-\gamma(t)| $$

**Def:** Let $f$ be analytic on an open set $G$, that contains the curve $C$ given by a parametrization $\gamma$, we define

$$ \rho(C, f) := d(\partial G, C) $$

If $\rho(C, f)>\delta$ then $f(z)$ is analytic at $B(\gamma(t); \delta)$ for $t \in [0,1]$, and we call $\rho(C, f)$ _the radius of regularity_ for $f$ on $C$.

**Def:** If $C$ is a curve with parametrization $\gamma$, _**************the modulus of continuity**************_ of $C$ (or of $\gamma)$ satisfies

$$ \omega(\eta) := \sup_{|t_0-t_1|< \eta}|\gamma(t_0) -\gamma(t_1)| $$

Similarly we can define the modulus of continuity of $F(s,t)$ as

$$ \omega(\eta) := \sup\{|F(s_0, t_0)-F(s_1, t_1)| \mid |s_0-s_1| +|t_0-t_1| <\eta\} $$

**Prop:** If $C_p$ and $C_q$ are given by the parametization $\gamma_p(t) =F(p, t)$ and $\gamma_q(t)=F(q, t)$ with $t$ being free, then

$$ d(\gamma_p,\gamma_q) \le \omega_F(p-q) $$
### Integration on nonrectifiable paths

**Lemma:** Let $\gamma:[0,1] \to \Bbb C$ be piecewise smooth and $\zeta_p, \zeta_q :[0,1] \to \Bbb C$ such that ${\gamma(0) = \zeta_p(0) = \zeta_q(0)}$, ${\gamma(1) = \zeta_p(1) = \zeta_q(1)}$ and

$$ d(\zeta_p, \gamma), d(\zeta_q, \gamma) < \rho(C, f) $$

then

$$ \int_{\zeta_p} f = \int_{\zeta_q} f $$

Note that we didn’t specify that $\zeta_p, \zeta_q$ be rectfiable.

**Def:** Let $f$ be analytic at every point of $\gamma$, being piecewise smooth, and $\lambda$ is a parametrization of a curve such that $d(\lambda, \gamma) < \rho(C, f)$, then we define the integral of $\lambda$ as

$$ \int_\lambda f = \int_\gamma f $$

**************Lemma:************** Let $f$ be analytic on the curves $C_p$ and $C_q$ with parametrizations $\gamma_p$ and $\gamma_q$ respectively, suppose the correspoonding radii of regularity satisfy

$$ \rho(C_p, f) >d(\gamma_p, \gamma_q) \quad \text{ or } \quad \rho(C_q, f) >d(\gamma_p, \gamma_q) $$

then

$$ |\rho(C_p, f) -\rho(C_q, f)| \le d(\gamma_p, \gamma_q) \quad \text{and }\quad \int_{\gamma_p}f =\int_{\gamma_q}f $$