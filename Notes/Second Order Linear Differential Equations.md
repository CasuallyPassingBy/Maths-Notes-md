---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]

**Def:** A second order ordinary differential equation has the form

$$ y'' = f(t, y, y') $$

If $f$ has the form

$$ f(t,y, y') = g(t)-p(t)y'-q(t)y $$

We can rewrite it as

$$ P(t)y'' +Q(t)y'+R(t) y= G(t) $$

with $P \ne 0$

*********Def:********* We say that the differential equation is **homogeneous** if $G = 0$, if it isn’t is called ********nonhomogeneous.********

Additionally, an initial value problem consists of a differential equation and a pair of initial conditions:

$$ y(t_0) = y_0 \quad y'(t_0) = y'_0 $$
# Constant Coefficients

********Def:******** We say that a second order linear homogeneous ordinary differential equation has constant coefficients if $P, Q, R$ are constants, in other words we have

$$ ay'' +by'+cy = 0 $$

### Method

Let $y = e^{rt}$, then $y' = re^{rt}$ and $y'' = r^2 e^{rt}$, subsitituing on the equation we get

$$ e^{rt}(ar^2+br+c)= 0 $$

Then since $e^{rt} \ne 0$, we have that

$$ ar^2+br+c=0 $$

This is the ************characteristic polinomial for the differential equation.************ The roots of this polinimial correspond to the exponents that help us solve the differential equation. Let $r_1$ and $r_2$ be roots of the characteristic polinomial, there are two cases:

- If $r_1 \ne r_2$, then the solution to the differential equation is of the form $y = Ae^{r_1t}+ Be^{r_2 t}$
- If $r_1 = r_2$, then the solution to the differential equation is of the form $y = e^{r_1t}(A+Bt)$

With $A, B \in \Bbb R$, that helps us satisfy the initial conditions