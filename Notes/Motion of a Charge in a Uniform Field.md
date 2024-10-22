---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Trayectories in Physics]], [[Newton's Laws]]
### The Lorentz Force on a Charged Particle

$$ {\bf F} = q (\mathbf{E+v \times B} ) $$

Let’s consider a charged particle $q$, moving in a uniform magnetic field $\bf B$ that points in the $z$ direction. The net force on the particle is just the magnetic force

$$ {\bf F} = q \bf{v \times B} $$

so the equation of motion is

$$ m \dot {\bf v} = q \bf{v \times B} $$

we can calculate the components of $\bf v \times B$, and we are getting, with ${\bf B }=(0,0,B)$,

$$ \begin{align*} m \dot v_x &=qBv_y \\ m \dot v_y &=-qBv_x \\ m \dot v_z &= 0 \\

\end{align*} $$

meaning $v_z = \text{constant}$, and we only need to deal with the remaining equations, we need a convinient parameter

$$ \omega = \frac{qB}{m} $$

which has dimensions of inverse time and is called the _cyclotron frequency_. with this notation we get the system of equations

$$ \begin{align*} \dot v_x &=\omega v_y \\ \dot v_y &=-\omega v_x \\

\end{align*} $$

We can solve it using the matrix rearranging as can get this system as

$$ \eta = v_x + i v_y $$

then

$$ \dot \eta = -i \omega \eta $$

we get the solution

$$ \eta = A \exp(-i\omega t) $$

integrating we get that

$$ x+iy = \frac{i A}{\omega} \exp(-i \omega t) +x_0 +i y_0 $$