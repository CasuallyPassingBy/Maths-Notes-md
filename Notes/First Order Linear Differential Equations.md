---
tags:
  - OrdinaryDifferentialEquations
links:
---
Subjects: [[Ordinary Differential Equations]]
Links: [[First Order Differential Equations]]

*********Def:********* A _first order linear differential equation_ is of the form

$$ y' +p(t)y= q(t) $$

where $p$ and $q$ are given functions of the independent variable $t$. This equation is linear in $y$, that is why is called _linear._

### Existence and Uniqueness

If the functions $p$ and $g$ are continuous on an open interval $I=(\alpha, \beta)$ containing the point $t = t_0$, then there exists a unique function $y = \phi(t)$ that satisfies the differential equation

$$ y' + p(t)y = g(t) $$

for each $t$ in $I$, and that also satisfies the initial condition

$$ y(t_0) = y_0, $$

where $y_0$ is an arbitrary prescribed initial value.

### Method

The most effective method to solve this kind of equation is by using an integrating factor. The main thing we want to see is left-hand side of the equation is of of the form of a product. We multiply by an unknown function $\mu(t)$ so we have the equation

$$ \mu(t) y' +\mu(t)p(t)y= \mu(t)q(t) $$

We make the left-hand side of the equation equal to the derivative of $\mu (t) y$, then we get that

$$ \frac{d}{dt}(\mu(t)y) = \mu(t)y' + \mu'(t) y =\mu(t) y' +\mu(t)p(t)y $$

If we simplify we get that

$$ \mu'(t) = \mu(t) p(t) $$

this is a special kind of differential equation solved by having $\mu(t) = c_1 \exp(\int p(t)\, dt)$ with $c_1 \ne 0$, where $\int p(t) \, dt$ represents the the anti derivative of $p(t)$. Plugging it back to the original equation we get that

$$ \frac{d}{dt}\left(\mu(t)y\right) =\mu(t)q(t) $$

Antiderivating we get that

$$ \mu(t) y = \int \mu(t) g(t) \, dt +C $$

if we solve for $y$ we get that

$$ y(t) = \frac{1}{\mu(t)} \int\mu(t) g(t)\, dt +\frac{C}{\mu(t)} $$

The value of $C$ is through the initial conditions, and this is final equation shows that the choice of $c_1$ doesn’t matter since it will get canceled as long as $c_1 \ne 0$.