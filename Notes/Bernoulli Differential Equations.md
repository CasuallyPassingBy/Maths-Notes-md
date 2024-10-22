---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[First Order Linear Differential Equations]], [[First Order Differential Equations]]
********Def:******** Some differential equations of the form:

$$ y'+p(t)y= q(t) y^n $$

are called ********Bernulli equations.********

### Method

If $n = 0, 1$, then it simplifies into a first order differential equation that we know how to solve.

If $n \ne 0,1$ then we multiply by $y^{-n}$ in both sides getting

$$ y^{-n} y' +p(t)y^{1-n} = q(t) $$

if we make a substitution of the form $v = y^{1-n}$, then we get the following equation

$$ \frac{1}{1-n} v' +p(t) v = q(t) $$

which is a first order linear differential equation which we know how to solve. Lastly we just make the substitution back, getting $y = \sqrt[1-n]{v}$, getting the solution to the equation.