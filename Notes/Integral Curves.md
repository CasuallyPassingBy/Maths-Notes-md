---
tags:
  - DifferentialGeometry
  - OrdinaryDifferentialEquations
---
Subjects: [[Differential Geometry]], [[Ordinary Differential Equations]]
Links: [[Vector Fields on Smooth Manifolds]]

**Def:** If $V$ is a vector field on $M$, an *integral curve of $V$* is differentiable curve $\gamma: J \to M$ whose velocity at each point is equal to the value of $V$ at each point: $$ \gamma'(t) = V_{\gamma(t)} \qquad \text{for all }t\in J.$$If $0\in J$, the point $\gamma(0)$ is called the *starting point of $\gamma$*. 

Finding integral curves boils down to solving a system of ordinary differential equation on a smooth chart. Suppose $V$ is a smooth vector field on $M$ and $\gamma: J \to M$ is a smooth curve. On a smooth coordinate domain $U \subseteq M$, we can write $\gamma$ in local coordinates as $\gamma = (\gamma^1(t), \dots, \gamma^n(t))$. Then the condition $\gamma'(t) = V_{\gamma(t)}$ for $\gamma$ to be an integral curve on $V$ can be written as $$\dot \gamma^i(t) \left.\frac{\partial}{\partial x^i}\right\rvert_{\gamma(t)} = V^i(\gamma(t)) \left.\frac{\partial}{\partial x^i}\right\rvert_{\gamma(t)}, $$which reduced to the following autonomous system of ordinary differential equations: $$\begin{align*}\dot\gamma^1 (t) &= V^1(\gamma^1(t),\dots, \gamma^n(t)) \\ \vdots & \\ \dot\gamma^n (t) &= V^n(\gamma^1(t),\dots, \gamma^n(t)). \end{align*}$$
We use a dot denote the ordinary derivative with respect to $t$ when there are such superscripts that would make primes hard to read. 