---
tags:
  - FourierAnalysis
  - PartialDifferentialEquations
---
Subjects: [[Fourier Analysis]], [[Partial Differential Equations]]
Links: [[The Wave equation]], [[3D Wave Equation]]

We can use the solution of the wave equation in three dimensions leads to a solution of the wave equation in two dimensions

We define the corresponding mean: $$\widetilde M _t(F)(x) =\frac1{2\pi} \int_{\|y\| \le  1} F(x-ty) (1-\|y\|^2)^{-1/2}\, dy$$
This is not a spherical mean, but is related being a weighted ball average, since it has a weight function $(1-\|y\|^2)^{-1/2}$. 

Let $f, g\in \mathcal S(\Bbb R ^2)$, then we would like to solve the problem: $$\Delta u = \frac{\partial^2 u}{\partial t^2} \quad \text{subject to} \quad u(x, 0) = f(x) \quad \text{and}\quad \frac{\partial u}{\partial t} (x, 0)=g(x)$$
with this in mind we could just extend $f, g$ to $\Bbb R^3$ with a mute third variable. This is a good approach, the problem is that if it is constant with respect to the third variable, then those extensions aren't in $\mathcal S(\Bbb R^3)$

to solve this problem, let's fix $T>0$, and consider the function $\eta(x_3) \in \mathcal S(\Bbb R)$, being $\eta(x_3) = 1$, when $|x_3| \le 3T$. Now the functions: $$\tilde f^\flat(x_1, x_2, x_3) = f(x_1, x_2) \eta(x_3) \qquad\text{and}\qquad  \tilde g^\flat(x_1, x_2, x_3) = g(x_1, x_2) \eta(x_3)$$
We can see that if we have a function $H(x_1, x_2, x_3) = h(x_1, x_2)$, then we can get the neat identity $$M_t(H)(x_1, x_2, 0) = \widetilde M_t (h)(x_1, x_2)$$
We can solve the wave equation $$\Delta \tilde u^\flat = \frac{\partial^2 \tilde u^\flat}{\partial t^2} \quad \text{subject to} \quad \tilde u^\flat(x, 0) = \tilde f^\flat(x) \quad \text{and}\quad \frac{\partial u}{\partial t} (x, 0)=\tilde f^\flat(x)$$
Then what we can do know is define the function $u(x_1, x_2, t) = \tilde u^\flat(x_1, x_2, 0, t)$. We know how to calculate $\tilde u^\flat$ it is: $$\tilde u^\flat(x,t) = \frac{\partial}{\partial t}(t M_t(\tilde f^\flat)(x)) + t M_t(\tilde g^\flat)(x)$$
We can calculate how would $u$, the solution to the 2D wave equation by applying our identity, getting that $$u(x,t) = \frac{\partial}{\partial t}(t \widetilde M_t(f)(x))+t\widetilde M_t(g)(x)$$

We see that that in the case of $n = 3$, then  the solution at the point $(x,t)$ depends only on the data at the boundary of the base of the backward light cone will affect the solution. For the case where $n = 1, 2$, we don't see this behaviour, we actually see that the solution at $(x,t)$ depends on the whole base of the backward light cone. 

