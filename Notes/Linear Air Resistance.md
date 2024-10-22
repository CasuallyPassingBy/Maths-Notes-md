---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Air Resistance]]

We neglect the quadratic term and get the differential equation

$$ m \ddot{\bf r} = m{\bf g}- b\bf v $$

We see that the differential equation only depends on the derivatives of $\bf r$, then we simplify as

$$ m \dot{\bf v} = m {\bf g}-b \bf v $$

unpacking this differential equation we see that

$$ \begin{align*} m\dot v_x &= -bv_x \\ m \dot v _y &= mg-bv_y \end{align*} $$

This is an uncoupled system of differential equations. Which is really easy to solve

## Horizontal Motion with Linear Drag

We solve the differential equation

$$ m\dot v_x = -bv_x $$

We will define a convinient parameter

$$ \tau = \frac{m}{b} $$

When we solve the differenatial equation on $v_x$, with $v_x(0) = v_{x0}$, we get that

$$ v_x (t) = v_{x0}e^{-t/\tau} $$

We can calculate $x(t)$, as the antiderivative of $v_x$, and we can calculate $\lim\limits_{t \to \infty} x(t) = x_{\infty} = \tau v_{x0}$, then we can, get a formula as

$$ x(t) = x_\infty (1-e^{-t/\tau}) $$

## Vertical Motion with Linear Drag

We solve the differential equation

$$ m\dot v_y = mg -bv_y $$

If we consider when $\dot v_y = 0$, then we can calculate the terminal velocity, as

$$ v_\text{ter} = \frac{mg}{b} = \frac{1}{18} D^2g\frac{\rho_\text{sph}}{\eta_\text{air}}\qquad \text{[for linear drag]} $$

with this we can substitute it back into the equation getting

$$ m\dot v_y = -b(v_y -v_\text{ter}) $$

and solving

$$ v_y- v_\text{ter} = A e^{-t/\tau} $$

If we add the initial condition of $v_y(0) = v_{y0}$, then

$$ v_y(t) =v_{y0} e^{-t/\tau} + v_\text{ter} (1-e^{-t/\tau}) $$

we see that $\lim\limits_{t\to \infty } v_y (t) = v_\text{ter}$, wich makes a lot of sense.

Finally we solve with the initial condition, with $y(0) = 0$

$$ y(t) = v_\text{ter} t+(v_{y0} - v_\text{ter})\tau (1-e^{-t/\tau}) $$
# Trajectory and Range in Linear Medium

We have the parametric solutions solutions of the projectile motion in a linear medium, and we reverse the direction of $v_\text{ter}$, since we will make the $y$ axis point _upward_, leaving us with

$$ \begin{align*} x(t) &= v_{x0} \tau (1-e^{-t/\tau}) \\ y(t) &= (v_{y0}+v_\text{ter})\tau(1-e^{-t/\tau} ) - v_\text{ter}t \end{align*} $$

If we eliminate the dependency on $t$, we get that

$$ y(x) = \frac{v_{y_0}+ v_\text{ter}}{v_{x_0}} x + v_\text{ter} \tau \ln\left(1-\frac{x}{v_{x_0}\tau}\right) $$

## Horizontal Range

The range of the projectile in a vacuum, is

$$ R_\text{vac} = \frac{2v_{x0}v_{y0}}{g} \qquad \text{[no air resitance]} $$

The range $R$ is the value $x$ when $y(x) =0$. Thus $R$ is the solution to the equation

$$

\frac{v_{y0}+ v_\text{ter}}{v_{x0}} R + v_\text{ter} \tau \ln\left(1-\frac{R}{v_{x0}\tau}\right) =0

$$

This is a transcendental equation, meaning no analytic solution exists, and we have to find $R$ numerically. We can approximate it using a Taylor series, up to the third power term, assuming all other terms can be neglected,when air resistance is small