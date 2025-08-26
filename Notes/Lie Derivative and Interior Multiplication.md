---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Fields on Smooth Manifolds]], [[Differential 1-forms on Smooth Manifolds]], [[Differential k-forms on Smooth Manifolds]], [[Integral Curves and Local Flows in Rn]]

# Families of Vector Fields and Differential Forms

**Def:** A collection $\{X_t \in \mathfrak X(M) \mid t \in I \}$ or $\{\omega_t \in \Omega^k(M)\mid t\in  I\}$ for some $I \subseteq \Bbb R$, where $M$ is a smooth manifold, is said to be a $1$-*parameter family*. Let $I$ be an open interval in $\Bbb R$. 

**Def:** Suppose $\{X_t \in \mathfrak X(M) \mid t \in I \}$ is a $1$-parameter family of vector fields on $M$ defined for all $t\in I$ except $t_0 \in I$. We say that the *limit* $\lim_{t \to t_0} X_t$ exists if every point $p \in M$ has a coordinate neighbourhood $(U, x^1, \dots, x^n)$ on which $X_t|_p = \sum a^i(t, p) \left.\dfrac{\partial}{\partial x^i}\right\rvert_p$ and $\lim_{t\to t_0} a^(t, p)$ exists for all $i$. In this case, we $$\lim_{t\to t_0} X_t|_p = \sum_{i = 1}^n \lim_{t \to t_0} a^i(t, p) \left.\dfrac{\partial}{\partial x^i}\right\rvert_p.$$
**Def:** A $1$-parameter family $\{X_t \in \mathfrak X(M) \mid t \in I \}$ of smooth vector fields on $M$ is said to *depend smoothly on $t$* if every point in $M$ has a coordinate neighbourhood $(U, x^1, \dots, x^n)$ on which $$(X_t)_p =  \sum_{i = 1}^n  a^i(t, p) \left.\dfrac{\partial}{\partial x^i}\right\rvert_p, \qquad (t, p) \in I \times U$$for some smooth function a^i on $I \times U$. In this case we also say that $\{X_t \in \mathfrak X(M) \mid t \in I \}$ is a *smooth family of vector fields* on $M$.

For a family of vector fields on $M$, one can define its derivative with respect to $t$ at $t = t_0$ by $$\left(\left.\frac{d}{dt}\right\rvert_{t = t_0}X_t \right)_p = \sum_{i = 1}^n \frac{\partial a^i}{\partial t}(t_0, p) \left.\frac{\partial}{\partial x^i}\right\rvert_p$$for $(t_0, p) \in I \times U$.

**Prop:** The derivative $\left.\dfrac{d}{dt}\right\rvert_{t = t_0} X_t$ is a smooth vector field on $M$.

Similarly, a $1$-parameter family $\{\omega_t \in \Omega^k(M)\mid t\in  I\}$ of smooth $k$-forms on $M$ is said to *depend smoothly* on $t$ if every point on $M$ has a coordinate neighbourhood $(U, x^1, \dots, x^n)$ on which $$(\omega_t)_p = \sum b_J(t, p) \left.dx^J\right\rvert_p, \qquad (t, p) \in I \times U,$$for some smooth functions $b_J$ on $I\times U$. We also call a family $\{\omega_t \in \Omega^k(M)\mid t\in  I\}$ a *smooth family of $k$-forms* on $M$ and define its derivative with respect to to $t$ to be $$\left(\left.\frac{d}{dt}\right\rvert_{t = t_0} \omega_t \right)_p = \sum \frac{\partial b^J}{\partial t}(t_0, p) \left.dx^J\right\rvert_p.$$ As for vector fields, this definition is independent of the chart and defines a smooth $k$-form $\left.\dfrac{d}{dt}\right\rvert_{t = t_0} \omega_t$ on $M$. 

**Prop:** if $\{\omega_t \in \Omega^k(M)\mid t\in  I\}$ and $\{\tau_t \in \Omega^k(M)\mid t\in  I\}$ are smooth families of $k$-forms and $\ell$-forms respectively on a manifold $M$, then $$\frac{d}{dt}(\omega_t \wedge \tau_t) = \left(\frac{d}{dt}\omega_t\right) \wedge\tau_t + \omega_t \wedge \left(\frac{d}{dt} \tau_t\right).$$
**Prop:** If $\{\omega_t \in \Omega^k(M)\mid t\in  I\}$ is a smooth family of differential forms on a manifold $M$, then $$\left. \frac{d}{dt}\right\rvert_{t =t_0} d\omega_t = d\left(\left.\frac{d}{dt}\right\rvert_{t = t_0} \omega_t\right).$$
# The Lie Derivative of Vector Fields

**Def:** For $X, Y \in \mathfrak X(M)$ and $p \in M$, let $\phi: (-\varepsilon, \varepsilon) \times U \to M$ be a loca flow of $X$ on a neighbourhood $U$ of $p$ and define the *Lie derivative* $\mathcal L_X Y$ of $Y$ with respect to $X$ at $p$ to be the vector: $$(\mathcal L_X Y)_p = \lim_{t \to 0} \frac{(\varphi_{-t *} Y)_p- Y_p}{t} = \left.\frac{d}{dt}\right\rvert_{t = 0} (\varphi_{-t *} Y)_p$$where $\varphi_{-t*}$ is the pushforward by $\varphi_{-t}$. 

**Th:** If $X$ and $Y$ are smooth vector fields on a manifold $M$, then the Lie derivative $\mathcal L_X Y$ coincides with the Lie bracket: $$ \mathcal L_X Y = [X, Y].$$
# The Lie Derivative of a Differential Form
