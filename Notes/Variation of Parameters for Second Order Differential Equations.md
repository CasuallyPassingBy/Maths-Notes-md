---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Solution to Nonhomogeneous Second Order Linear Differential Equations]], [[Second Order Linear Differential Equations]]
The idea of variation of parameters is that if we have the nonhomogeneous differential equation

$$ y'' +py'+qy = g $$

and find the homogeneous solutions $y_1$ and $y_2$ that form a fundamental set of solutions. Then we can find the particular solution if we look at the functions generated

$$ y = u_1(t) y_1 + u_2(t)y_2 $$

with $u_1$ and $u_2$ functions. Now we need to determine the functions $u_1$and $u_2$.

We add the restriction that

$$ u_1' y_1 +u_2' y_2 = 0 $$

and substitute on the equation we get that

$$ u_1'y_1'+u_2'y_2' = g $$

Solving the system of equations we get that

$$ u_1' = -\frac{y_2 g}{W(y_1, y_2)} \qquad u_2' =\frac{y_1 g}{W(y_1, y_2)} $$

**************Th:************** If $p, q$ and $g$ are continuous on an open interval $I$, and if the functions $y_1$ and $y_2$ are a fundamental set of solutions of the homogeneous equation $y'' +py'+qy = 0$, then the particular solution of

$$ y''+py'+qy= g $$

is of the form

$$ \begin{align*}Y(t) &=-y_1(t) \int_{t_0}^t \frac{y_2(s) g(s)}{W(y_1, y_2)(s)}\, ds+ y_2 \int_{t_0}^t \frac{y_1(s) g(s)}{W(y_1, y_2)(s)}\, ds \\ &=\int_{t_0}^t \frac{y_1(s) y_2(t)-y_1(t)y_2(s)}{W(y_1, y_2)(s)} \, ds \end{align*} $$

where $t_0$ is any convinently chosen point in $I$. The general solution is

$$ y =c_1 y_1+c_2y_2 +Y $$

Where $Y$ has the properties of $Y(t_0) =0$ and $Y'(t_0) =0$.