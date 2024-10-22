---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Second Order Linear Differential Equations]], [[Second Order Linear Exact Differential Equations]]
A differential equation of the form

$$ P(t) y''+Q(t) y'+R(t) y =0 $$

is not exact, we can make it exact by multiplying an integrating factor $\mu$. Thus we get ${\mu(t)P(t) y''+\mu(t)Q(t) y'+\mu(t)R(t) y =0}$, can be written of the form ${[\mu(t)P(t) y']'+[f(t)y]' =0}$. To find the integration factor we need to solve the differential equation

$$ P \mu''+(2P'-Q)\mu' +(P''-Q+R)\mu =0 $$

This equation on $\mu$, is called _******the adjoint******_ of the original equation. In general, the problem of solving the adjoint differential equation is as difficult as that of solving the original.

The adjoint of the adjoint equation is the original equation.

An equation is called _self-adjoint_ if the adjoint equation is the same as the original equation. An equation is self adjoint iff $P' = Q$.