---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Air Resistance]]

In this case we are going to solve the equation

$$ m \dot{\bf v} = m\bf g +f $$

but ${\bf f} = -cv \bf v$, and this can couple the equations

## Horizontal Motion and Quadratic Drag

We have the equation

$$ m \dot v = -cv^2 $$

this is easily for $v(0)= v_0$, and we get

$$ v(t) = \frac{v_0}{1+cv_0t/m} $$

As we did in the linear case we are going to define an abbreviation of constants

$$ \tau = \frac{m}{cv_0} \qquad\text{[for quadratic drag]} $$

Simplifying, the function

$$ v(t) = \frac{v_0}{1+t/\tau} $$

We can solve for $x(0)= x_0$, then we have that

$$ x(t) = x_0 +v_0\tau \ln\left(1+\frac{t}{\tau}\right) $$

meaning if we add that $x(0) =0$, we get that

$$ x(t) = v_0\tau \ln(1+t/\tau) $$

This means that $\lim\limits_{t\to \infty} x(t) = \infty$

## Vertical Motion with Quadratic Drag

We get the equation

$$ m \dot v = mg-cv^2 $$

to find the $v_\text{ter}$, we make $\dot v =0$, and we get that

$$ v_\text{ter} = \sqrt{\frac{mg}{c}} = \sqrt{\frac{8}{3}Dg\frac{\rho_\text{sph}}{\rho_\text{air}}} $$

Meaning denser objects fall faster given same diameter, and if same density, the one with bigger diameter falls faster

We get the equation, as

$$ \dot v = g\left(1-\frac{v^2}{v_\text{ter}^2}\right) $$

Solving the differenatial equation with $v(0) =0$, we get that

$$ v(t) = v_\text{ter}\tanh\left(\frac{gt}{v_\text{ter}}\right) $$

We integrate and add the fact that $y(0) =0$, then

$$ y(t) = \frac{(v_\text{ter})^2}{g}\ln \left[\cosh\left(\frac{gt}{v_\text{ter}}\right)\right] $$

## Quadratic Drag with Horizontal and Vertical Motion

We need to solve the differential equation

$$ \begin{align*} m \ddot {\bf r} &= m {\bf g} -cv^2 \hat{\bf v} \\ & = m{\bf g} - cv{\bf v} \end{align*} $$

If we unpack this equation into horizontal and vertical components
$$ mv_x =-c\sqrt{v_x^2+v_y^2}\ v_x $$$$ mv_y = mg-c\sqrt{v_x^2+v_y^2}\ v_y $$
This system of equations cannot be solved analytically just numerically. Meaning we will not be able to cannot find a general soltution, just estimate it using initial conditions.

We know that as $t \to \infty$ , then $v_x \to 0$, and $v_y \to -v_\text{ter}$, then we can estimate that

$$ \dot v_x \approx -\frac{c v_\text{ter}}{m} v_x = -kv_x $$

We get that $v_x = Ae^{-kt}$, and we get that $v_x \to 0$ rapidly, then $x(t)$ , as $t\to \infty$, approaches a finite limit, and thus the trajectory has finite vertical asymptote.