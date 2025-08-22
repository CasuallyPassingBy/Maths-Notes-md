---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Vibrations]], [[Energy for One Dimensional Systems in Classical Mechanics]], [[Linear System of Ordinary Differential Equations]]

# Hooke's Law

Let us remember that Hooke's law asserts that the force exerted by spring has the form $$F_x (x) = -k x,$$where $x$ is the displacement of the spring from its equilibrium length and $k> 0$  called the force constant. That $k$ is positive means that the equilibrium at $x = 0$ is stable. The force is a *restoring force*, and the equilibrium is stable. An exactly equivalent way to state Hooke's law is that the potential energy is $$U(x) = \frac12 kx^2.$$

Let us consider conservative one-dimensional system which is specified by a coordinate $x$ and has potential energy $U(x)$. Suppose that the system has a stable equilibrium position $x=x_0$, which we may as well as well take to be the origin $(x_0 = 0)$. Now consider the behaviour of $U(x)$ in the vicinity of the equilibrium position. Since any reasonable function in physics can be expanded in a Taylor series, $$U(x) = \sum_{n =0}^\infty \frac{x^n}{n!}U^{(n)}(x). $$
As long as $x$ remains small, the first three terms in the series should be good approximation. The term in constant, we can just ignore it. Because $x = 0$ is an equilibrium point, $U'(x) = 0$ and the second term in the series is automatically zero. Since the equilibrium is stable, $U''(0) = k > 0$. For sufficiently small displacements we get the approximation $$U(x) = \frac12 kx^2.$$
Thus, we get that Hooke's law is always valid around a small neighbourhood around $x_0$. 

# Simple Harmonic Motion

We can now examine the equation of motion for a mass $m$ that is displaced from a position of stable equilibrium. To be definite, let us consider a frictionless track attached to a fixed spring. We have see that we can approximate the potential energy $U(x) = kx^2/2$, or equivalently, the force $F_x = -kx$. The equation of motion is $m \ddot x = -kx$, or $$\ddot x = -\frac kmx = -\omega^2x,$$where $\omega = \sqrt{k/m}$. 

If we solve the ODE, we get a couple of ways to write the solution. For example in terms of exponentials $$x(t) = C_1e^{i\omega t} + C_2e^{-i\omega t}.$$We could also write it in terms of $\sin$ and $\cos$: $$x(t) = B_1 \cos(\omega t)+B_2\sin(\omega t).$$This form can be taken as the definition of *simple harmonic motion*: any motion that is a combination of a sine and cosine of this form is called *simple harmonic*. Naturally, we can calculate the period of motion of the cart: $$\tau = \frac{2\pi}{\omega} = 2\pi \sqrt{\frac{m}{k}}.$$

One benefit of the simple harmonic form is that the coefficients $B_1$ and $B_2$ are easily identifiable with the initial conditions. $B_1 = x(0) = x_0$, and $x'(0) = \omega B_2$. 

There's another way we can write the solutions as *phase shifted cosine*. We first define a new constant $$ A = \sqrt{B_1^2 + B_2^2}.$$From this we can write $$
\begin{align*}
x(t) &= B_1 \cos(\omega t) + B_2 \sin(\omega t) \\
&= A\left[\frac{B_1}{A}\cos(\omega t) + \frac{B_2}{A} \sin(\omega t)\right] \\
&= A [\cos \delta \cos(\omega t) + \sin\delta \sin(\omega t)]\\
&= A \cos(\omega t -\delta).
\end{align*}
$$
From this it is clear that the cart is oscillating with amplitude $A$, but instead of being a simple cosine, it is a cosine which is shifted in phase. We call $\delta$ the *phase shift*. We can also get this form from the exponentials.

## Energy considerations

We are going to consider the energy of the oscillator as it moves back and forth. Since $x(t) = A\cos(\omega t -\delta)$, the potential energy is just $$U(x) = \frac12k A^2\cos^2(\omega t- \delta).$$If we now calculate its kinetic energy we get that $$T(x) = \frac12 m \dot x^2 = \frac12 m \omega^2 A^2\sin^2(\omega t-\delta) = \frac12 k A^2\sin^2(\omega t-\delta).$$
Then we get that the total energy is constant, and $$E = T+U = \frac12 k A^2,$$as it has to be for any conservative force.

# Two-Dimensional Oscillators

In more dimensions, the possibilities for oscinalltion are considerably richer. the simples possibility is the so called *isotropic harmonic oscillator*, for which the restoring force is proportionals to the dislacement from equilibrium, with the same constant proportionality in all directions: $$\mathbf F = -k \mathbf r.$$
We get the equation of motion $\ddot{\mathbf r} = -k/m \mathbf r$. Then we get two independent equations: $$\begin{align*}
\ddot x = -\omega^2 x \\
\ddot y = -\omega^2 y \\
\end{align*}$$We solve them as usual, and get $$\begin{align*}
x(t) &= A_x \cos(\omega t- \delta_x) \\
y(t) &= A_y \sin(\omega t- \delta_y)
\end{align*}$$where the four constants are $A_x, A_y, \delta_x$ and $\delta_y$ are determined by the initial conditions of the problem. By redefining the origin of time, we can dispose of the phase shift $\delta_x$, but, in general we cannot also dispose of the corresponding phase in the $y$ solution. Thus the simplest form for the general solution is $$\begin{align*}
x(t) &= A_x \cos(\omega t) \\
y(t) &= A_y \sin(\omega t- \delta)
\end{align*}$$where $\delta := \delta_y-\delta_x$ is the *relative* phase of the $y$ and $x$ oscillations. 

The behaviour of the solution above depends on the values $A_x, A_y$ and $\delta$. If either $A_x = 0$ or $A_y =0$, we get simple harmonic motion in the other direction. If $A_x A_y \neq 0$, then the motion depends critically on the relative phase $\delta$. If $\delta = 0$, then $x(t)$ and $y(t)$ rise and fall in step, and the point $(x, y)$ moves back and forth slanting line that joins $(A_x, A_y)$ to $(-A_x, -A_y)$. If $\pi/2$, then $x$ and $y$ oscillate out of step, with $x$ at an extreme when $y = 0$, and vice versa; for the other values of $\delta$, the point $(x, y)$ moves around an slanting ellipse. 

In an *anisotropic oscillator*, the components of the restoring force are proportional to the components of the displacement, but with different constants of proportionality: $$F_x = -k_x x, \quad F_y = -k_yy, \quad F_z = -k_z z.$$
We get that $$\begin{align*}
\ddot x = -\omega^2_x x \\
\ddot y = -\omega^2_y y \\
\end{align*}$$
We get the solution $$\begin{align*}
x(t) &= A_x \cos(\omega_x t) \\
y(t) &= A_y \sin(\omega_y t- \delta)
\end{align*}$$where $\delta$ is the relative phase between $y$ and $x$. If $\omega_x/\omega_y = p/q$ with $(p,q) = 1$, then period is $2\pi p/\omega_x = 2\pi q/\omega_y$. Additionally, if the motion is periodic, then that means that $\omega_x/\omega_y$ is rational, i.e., the motion is periodic iff $\omega_x/\omega_y$ is rational. If $\omega_x/\omega_y$ is  irrational. then the motion is *quasiperiodic*: the motion of the separate coordinates $x$ and $y$ is periodic but because the two periods are incompatible, the motion $(x, y)$ is not. 