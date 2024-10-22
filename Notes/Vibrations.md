---
tags:
  - OrdinaryDifferentialEquations
  - ClassicalMechanics
---
Subjects: [[Ordinary Differential Equations]], [[Classical Mechanics]]
Links: [[Second Order Linear Differential Equations]]
### Undamped Free Vibration

If we have a simple harmonic oscilator with the differential equation

$$ m u'' -k u=0 $$

we can define the natural frequency $\omega_0 ^2 = k/m$. Then the solutions are of the form

$$ u = A\cos \omega_0 t + B\sin\omega_0 t $$

We can rewrite this as

$$ u = R\cos(\omega_0 t -\delta) $$

The way we can change between these representations by

$$ \begin{align*} A = R\cos \delta& \qquad B = R\sin \delta \\ R= \sqrt{A^2+B^2}& \qquad \tan\delta = B/A \end{align*} $$

The period of the motion is

$$ T = \frac{2\pi}{\omega_0} $$

$R$ is called the _**amplitud**_ of the motion, and $\delta$ is called the **phase**.

### Damped Free Vibrations

If we include the damping effect, on the differential equation we get that, with $m, \gamma, k > 0$

$$ mu''+\gamma u'+ku =0 $$

Solving the characteristic polinomial we get that the roots are

$$ r_1, r_2 = \frac{\gamma}{2m}\left(-1\pm \sqrt{1-\frac{4km}{\gamma^2}}\right) $$

There are various cases,

- $\gamma^2-4km >0$, then $u = Ae^{r_1t}+Be^{r_2 t}$, this is called **********overdamped**********
- $\gamma^2-4km =0$, then $u = (A+Bt) e^{-\gamma t/2m}$, this is called **********critically damped**********
- $\gamma^2 -4km <0$, then $\mu =\dfrac{\sqrt{4km-\gamma^2}}{2m} >0$, and $u = e^{-\gamma t/2m}(A \cos\mu t+B\sin \mu t)$, this is called **********underdamped**********

In this last case, the motion isn’t periodic but it oscilates back and forth, $\mu$ is called the ****************quasi frecuency****************. By comparing $\mu$ to the frequency $\omega_0$ of an undamped motion we get that

$$ \frac{\mu}{\omega_0} = \left(1-\frac{\gamma^2}{4km}\right)^{1/2} \approx 1-\frac{\gamma^2}{8km} $$

if $\gamma^2/4km$ is small. By annalogy, the quatity $T_d = 2\pi/\mu$ is called the _**quasi period**_. If we compare $T_d$ and $T$ we get that

$$ \frac{T_d}{T} =\frac{\mu}{\omega_0} = \left(1-\frac{\gamma^2}{4km}\right)^{1/2} \approx 1-\frac{\gamma^2}{8km} $$

The time between succsive maxima is $T_d$, and it behaves more like a period.

The ratio of the displacements at two succesive maxima is given by $\exp(\gamma T_d/2m)$. No matter the maxima chosen. The natural logarthm of this ratio is called the ******************logarithmic decremet****************** and is denoted as $\Delta$. Thus $\Delta = \pi\gamma/m\mu$.

# Forced Vibrations

## Forced Vibrations with Damping

The equation of a general spring mass system subject to an external force $F(t)$ is

$$ mu''+\gamma u'+ku = F(t) $$

We will make the external force to be given by $F_0 \cos \omega t$, where $F_0$ and $\omega$ are positive constants. Then the solutions are of the form

$$ u = c_1 u_1+c_2u_2 +A\cos\omega t+B\sin\omega t = u_c+ U $$

### Intuitive Way

A way I found to do it is to non-dimensionalize, to make the equation easier to understand. We divide with respect to $m$, we get the equation

$$ u'' + \frac{\gamma}{m}u' + \frac{k}{m}u =\frac{F_0}{m} \cos(\omega t) $$

We take advantage and define $\omega_0$ to be the natural frequency, defined as

$$ \omega_0^2 = \frac{k}{m} $$

The equation now looks like

$$ u'' + \frac{\gamma}{m}u' + \omega_0^2u =\frac{F_0}{m} \cos(\omega t) $$

Finally we make a weird step, and take that $\tau = \omega_0 t$. Then the next step, is to look at how the differential equation changes given that

$$ \frac{d u}{dt} = \frac{du}{d\tau} \frac{d\tau}{dt}, \qquad \frac{d^2 u}{dt^2} = \frac{d^2u}{d\tau^2}\left( \frac{d\tau}{dt}\right)^2 +\frac{du}{d\tau}\frac{d^2\tau}{dt^2} $$

We get that is now:

$$ \omega_0^2\frac{d^2u}{d\tau^2}+ \frac{\gamma \omega_0}{m} \frac{du}{d\tau} + \omega_0^2 u = \frac{F_0}{m}\cos\left(\frac{\omega}{\omega_0}\tau\right) $$

We define $\beta = \omega/\omega_0$, and $\alpha = \gamma /m\omega_0>0$, getting the equation and diving by $\omega_0^2$

$$ u'' + \alpha u' + u = \frac{F_0}{m \omega_0^2}\cos(\beta \tau) $$

Finally, we make one last subsitution $x = \frac{u }{{F_0}/{m \omega_{0}^2}}$, meaning we can divide the whole experesion by $F_0/m\omega^2_0$, then we get

$$ x'' + \alpha x' + x = \cos(\beta \tau) $$

This is much easier to analize. We can examine the homogeneous solutions. We get that if ${u = e^{rt}}$, then

$$ r = \frac{-\alpha \pm \sqrt{\alpha^2-4}}{2} $$

We can examine it, but no matter the $\alpha$, we get that $\Re(r) <0$, then the particular solutions must vanish. If $\alpha\ne 2$, then $x _h(t) = Ae^{r_1 t}+ Be^{r_2 t}$, then since $\Re(r_1), \Re(r_2) <0$. then $x_h \to 0$ as $t\to \infty$. If $\alpha = 2$, then $x_h(t) = e^{-t}(A+ Bt)$, which also $x_h \to 0$ as $t\to \infty$. This solutions are called **********transient solutions********** since vanish when $t\to \infty$.

The solutions that don’t vanish are called the _****steady-state solutions****_. Then for the particular solution we get that if we define $z$ such that $\Re(z) = x$, then we can solve the differential equation with $z(t) = Ae^{i\beta \tau}$, getting for the value of $A$

$$ A = \frac{1}{1-\beta^2 +i\alpha \beta} $$

Doing some algebra we get

$$ x(\tau) = \frac{1}{(1-\beta^2)^2 +(\alpha\beta)^2}[(1-\beta^2)\cos(\beta \tau) + \alpha\beta\sin(\beta\tau)] $$

We can make it a little less ugly, using the [[Harmonic Addition Theorem|harmonic addition theorem]], getting

$$ x(\tau) = \frac{1}{\sqrt{(1-\beta^2)^2 +(\alpha\beta)^2}}\sin\left(\beta \tau + \arctan\left(\frac{1-\beta^2}{\alpha\beta}\right)\right) $$

Resonance happens when $\omega = \omega_0$, then $\beta = 1$. If resonance happens then

$$ x(\tau ) = \frac{\sin( \tau)}{\alpha} $$

If we try to translate back to $u$, we get the following

### Weird Way
Since $m, \gamma, k>0$, then $r_1$ and $r_2$ have that $\Re(r_1), \Re(r_2) <0$. Then we know that as $t \to \infty$, then $u_1$ and $u_2$ tend to $0$. Since $u_c$ dies out as $t$ increases, it is called the ********************transient solution.********************

The remaining terms $U(t)$ do not die out as $t\to \infty$, but persists indefinetely, as long as the force is applied. They represent a steady oscillation with the same frequency as the external force and are called the _********steady state solution********_ or the _**************forced response**************_ or the _**forced response**_.

It is convinient to write $U(t)$ to write it as a single trignometric expresion

$$ U (t) = R\cos(\omega t-\delta) $$

We need a couple of useful terms before getting the expression, with $\omega_0$ being the natural frequency of the system.

$$ \omega_0^2 =\frac{k}{m} \quad \Delta = \sqrt{m^2(\omega_0^2-\omega^2}+\gamma^2\omega^2 $$

Then

$$ R= \frac{F_0}{\Delta} \quad \cos \delta = \frac{m(\omega_0^2-\omega^2)}{\Delta}\quad \sin \delta= \frac{\gamma \omega}{\Delta} $$

If we try to look how $R$ of the steady state oscillation depends on $\omega$ we get that

$$ \frac{Rk}{F_0} = \left[\left(1-\frac{\omega^2}{\omega_0^2}\right)^2+ \Gamma\frac{\omega^2}{\omega_0^2}\right]^{-1/2} $$

where $\Gamma = \gamma^2/mk$. If we try to maximize $R$, we need to differentiate with respct to $\omega$ and set it to $0$. Then we get the expresion

$$ \omega_{\max}^2 = \omega_0^2 - \frac{\gamma^2}{2m^2}= \omega_0^2\left(1-\frac{\gamma^2}{2mk}\right) $$

We can see that $\omega_{\max} < \omega$, and it is close when $\gamma$ is small. Then

$$ R_{\max }= \frac{F_0}{\gamma\omega_0\sqrt{1-\gamma^2/4mk}} \approx \frac{F_0}{\gamma \omega_0}\left(1+\frac{\gamma^2}{8mk}\right) $$

The last expression is true for small $\gamma$. If $\Gamma >2$, then $\omega_{\max}$ is imaginary and in this case $R_{\max}$ is given by $\omega=0$. The critical damping is equivalent of $\Gamma = 4$.

For small $\gamma$, we have that $R_{\max} \approx F_0/\gamma\omega_0$. Thus for lightly damped systems, the amplitud $R$ of the forced response when $\omega$ is near $\omega_0$ is quite large even for small relatively small external forces, and the smaller $\gamma$, the more pronounced effect. This is called ********resonance********.

## Forced Vibrations without Damping

We will assume that $\gamma =0$, now we have the differential equation

$$ mu''+ku= F_0\cos \omega t $$

### Without Resonance

The form of the solution of depends on the value of $\omega$, with $\omega_0 = \sqrt{k/m}$, in case of $\omega \ne \omega_0$, then the solution is of the form

$$ u=c_1 \cos \omega_0 t+ c_2\sin\omega_0 t + \frac{F_0}{m(\omega_0^2-\omega^2)}\cos\omega t $$

The constants $c_1$ and $c_2$ are constants determined by initial conditions. If look at the particular case where $u(0) =0$ and $u'(0) =0$, meaning all the energy of the system comes from the external force we get that

$$ c_1 = -\frac{F_0}{m(\omega_0^2-\omega^2)}\qquad c_2 = 0 $$

Meaning we have

$$ u = \frac{F_0}{m(\omega_0^2-\omega^2)}(\cos\omega t- \cos \omega_0 t) $$

using trigonometric identities we get that

$$ u = \left(\frac{2F_0}{m(\omega_0^2-\omega^2)}\right)\left(\sin \frac{(\omega_0 -\omega)}{2}t\right)\left(\sin\frac{(\omega_0 +\omega)}{2}t\right) $$

If $|\omega_0-\omega|$ is small, then $\omega_0+\omega$ is much greater than $|\omega_0 - \omega|$. Consquently, ${\sin(\omega_0+\omega)t/2}$ is rapidly oscilating compared to ${\sin(\omega_0-\omega)t/2}$. Thus the motion is rapidly oscilation with a frequncy of ${(\omega_0+\omega)/2}$, but slowly varying amplitud of

$$ \left(\frac{2F_0}{m|\omega_0^2-\omega^2|}\right)\left|\sin \frac{(\omega_0 -\omega)}{2}t\right| $$

This type of motion exhibits what is called a ****beat****. In electronics, the variation of amplitud with time is called ********amplitud modulation********.

### With Resonance

In the case that $\omega = \omega_0$ we get that the solution to the differential equation

$$ mu'' +ku = F_0\cos \omega t $$

is of the form

$$ u = c_1\cos\omega_0 t+c_0\sin\omega_0t + \frac{F_0}{2m\omega_0} t\sin \omega_0 t $$

and will become unbounded.