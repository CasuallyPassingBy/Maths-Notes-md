---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Second Order Linear Differential Equations]]

The procedure of for reduction of order of a second order linear differential equation, and suppose we know a solution $y_1$, not everywhere $0$ of

$$ L[y] = y''+py'+qy=0 $$

To find a second solution let

$$ y= v(t)y_1(t) $$

and substituing on the equation $y$, $y'$ and $y''$ we get

$$ y_1 v'' +(2y_1'+py_1)v' =0 $$

Which let’s us solve for $v'$ since it is a first order linear differential equation, and then get $v$.

### Nonhomogeneous Equations

We can also use reduction of order to solve nonhomogeneous equation.

$$ y'' +py'+qy = g $$

provided we know a solution for the homogeneous equation $y_1$. Let $y = v y_1$. then plugging it onto the equation above we get that

$$ y_1 v''+(2y_1'+py_1) v' = g(t) $$

which is again a first order linear differential equation on $v'$. Then we can get $y$.