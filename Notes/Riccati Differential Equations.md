---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[First Order Differential Equations]], [[Second Order Linear Differential Equations]]
The Riccati equation in the narrowest sense is any first-order ODE that is quadratic in the unknown function.

$$ y' = q_0(x)+q_1(x) y+q_2(x) y^2 $$

where $q_0, q_2 \ne 0$

### Method

We make the subsittution of $v = q_2 y$, then we have the following equation

$$ v' = v^2 +R(x) v+S(x) $$

with $S = q_0 q_2$ and $R = q_1 + \dfrac{q_2'}{q_2}$

From this we make the substitution $v = -\dfrac{u'}{u}$, then we have a simplification

$$ u''-Ru '+Su =0 $$

Which is a second order linear ODE