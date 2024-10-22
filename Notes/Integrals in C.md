---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Continuous Functions in C]]

# Integrals in $\Bbb C$

**Prop:** Let $\gamma:I\subseteq \Bbb R \to \Bbb C$ and $f:\Omega\subseteq \Bbb C \to \Bbb C$ . If $\gamma$ is differentiable at $t_0 \in I$ and $f$ is differentiable at $\gamma(t_0) =z_0 \in A$, then $f \circ \gamma$ is differentiable at $t_0$ and

$$ (f \circ \gamma)'(t_0) = f'(\gamma(t_0))\gamma'(t_0) $$

**********Def:********** Let $\gamma:I_1 \subseteq\Bbb R\to \Bbb C$ and $\sigma: I_2 \subseteq\Bbb R \to \Bbb C$ differentiable at $t_0 \in I_1$ and $u_0 \in I_2$, respectively such that $\gamma(t_0) = \sigma(u_0) = z_0$. If $\gamma'(t_0) \ne 0$ and $\sigma(u_0) \ne 0$, we say that the angle formed by $\gamma$ and $\sigma$ at $z_0$ is given by

$$ \arg\left(\frac{\gamma'(t_0)}{\sigma(u_0)}\right) \in [-\pi , \pi) $$

**********Def:********** Let $h = h_1 +ih_2 : I \subseteq \Bbb R \to \Bbb C$ continuous on $I$. If $[a,b] \subseteq I$, we define the integral of $h$ over $[a,b]$, denoted as $\int_a^b h$, is defined as

$$ \int_a^b h(t) \, dt = \int_a^b h_1(t) \, dt +i\int_a^b h_2(t) \, dt $$

************Prop:************ Let $h, g: I \subseteq \Bbb R \to \Bbb C$ continuous on $I$ and $[a,b] \subseteq I$. Then the following properties are satisfied:

$$ \Re\left(\int_a^b h(t) \, dt\right) = \int_a^b \Re(h(t)) \, dt $$

$$ \Im\left(\int_a^b h(t) \, dt\right) = \int_a^b \Im(h(t)) \, dt $$

If $\alpha, \beta \in \Bbb C$, then

$$ \int_a^b \alpha h(t)+ \beta g(t) \, dt = \alpha \int_a^b h(t) \, dt + \beta \int_a^b g(t) \, dt $$

$$ \left|\int_a^b h(t) \, dt\right| \le \int_a^b |h(t)| \, dt $$