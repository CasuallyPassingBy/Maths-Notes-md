---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Oscillations and Hooke's Law]], [[Vibrations]], [[Second Order Linear Differential Equations]], [[Main definitions for Fourier Analysis]]

There are several possibilities for the resistive force. Ordinary sliding friction is approximately constant in magnitud, but always directed opposite to the velocity. As we have seen when studying [[Air Resistance]], it is a reasonable assumption that the resistive force is proportional to $v$ or $v^2$. 

If we consider an object that is subject to a Hooke's law force $-kx$ and a resistive force $-b\dot x$. The net force on the object is $-b\dot x -kx$, and Newton's second law reads $$m\ddot x +b\dot x +kx=0.$$
We are going to consider two constants $$2\beta = \frac{b}{m}, \qquad \omega_0 = \sqrt{\frac km}.$$
We call $\omega_0$ the system's **natural frequency**, the *frequency at which it would oscillate if there were no resistive force present*. The equation of motion for the damped oscillator becomes $$\ddot x + 2\beta\dot x + \omega_0^2x = 0.$$
If $x(t) = e^{rt}$, we get the solutions of to be $r= -\beta \pm \sqrt{\beta^2-\omega_0^2}$, and we get the general solution as $$x(t) = e^{-\beta t}\left(C_1 e^{\sqrt{\beta^2-\omega_0^2}t}+ C_2 e^{-\sqrt{\beta^2-\omega_0^2}t}\right).$$
## Undamped Oscillation
If there is no damping, meaning that $\beta = 0$, then we get $$x(t) = C_1 e^{i\omega_0t}+ C_2 e^{-i\omega_0t}.$$
## Weak Damping 

Suppose that $\beta$ is small, we mean that $$\beta < \omega_0,$$a condition sometimes called *underdamping*. In this case we define another constant $$\omega_1 := \sqrt{\omega_0^2-\beta^2}.$$We see that $\omega_1$ is a frequency, which is less than the natural frequency $\omega_0$. In the important case of very weak damping $(\beta \ll \omega_0)$, $\omega_1$ is very close to $\omega_0$. With this in mind, we get the solution $$x(t) = e^{-\beta t}\left(C_1 e^{i\omega_1t}+ C_2 e^{-i\omega_1t}\right) = A e^{-\beta t} \cos(\omega_1 t-\delta).$$

We get that the decay parameter is $\beta$.
## Strong Damping

Suppose instead that $\beta$ is large. Specifically suppose that $$\beta > \omega_0,$$a condition sometimes called *overdamping*. In this case, $r$ is real, and our solution is $$x(t) = C_1 e^{\left(-\beta +\sqrt{\beta^2-\omega_0^2}\right)t}+ C_2 e^{\left(-\beta -\sqrt{\beta^2-\omega_0^2}\right)t}.$$
Here we have that the decay parameter is $-\beta +\sqrt{\beta^2-\omega_0^2}$, then we get that as $\beta \to \infty$, then $-\beta +\sqrt{\beta^2-\omega_0^2}\to 0$. 

## Critical Damping

The boundary between underdamping and overdamping is called *critical damping* and occurs when the damping constants equal to the natural frequency $$\beta = \omega_0.$$With this in mind, we get the solution $$x(t) = e^{-\beta t}(C_1 + C_2 t).$$
The decay parameter is $\beta$. 

| Damping          | $\beta$            | Decay Parameter                   |
| ---------------- | ------------------ | --------------------------------- |
| None             | $\beta = 0$        | $0$                               |
| Underdamping     | $\beta <\omega_0$  | $\beta$                           |
| Critical Damping | $\beta = \omega_0$ | $\beta$                           |
| Overdamping      | $\beta > \omega_0$ | $\beta-\sqrt{\beta^2-\omega_0^2}$ |

The decay parameter reaches its maximum, when $\beta = \omega_0$. 

# Driven Damped Oscillations

Any natural oscillator eventually comes to a rest, as the damping forces drain its energy. If we want the oscillations to continue we need an external *driving force*. If we denote the external driving force by $F(t)$, and if we assume as before the damping force is of the form $-bv$, then the net force on the oscillator is $-b\dot x- kx+ F(t)$, and the equation can be written as $$m \ddot x + b\dot x + kx = F(t).$$
Just as before we can consider $$f(t) = \frac{F(t)}{m},$$the force per unit mass. With this notation we get the equation $$\ddot x + 2\beta \dot x+ \omega_0^2 x = f(t).$$
We shall see the special case for the driving force $f(t)$ as a sinusoidal function on time, $$f(t) = f_0 \cos(\omega t),$$where $f_0$ denotes the amplitud of the driving force, and $\omega$ is the angular frequency of the driving force, also called the *driving frequency*. Then we get the following equation $$\ddot x + 2\beta\dot x+\omega_0^2 x= f_0 \cos(\omega t).$$
We can consider a similar equation $$\ddot y + 2\beta\dot y+\omega_0^2 y= f_0 \sin(\omega t),$$with these equations in mind, we can make a substitution. Let $z = x+iy$, then $$\ddot z + 2\beta\dot z+\omega_0^2 z= f_0 e^{i\omega t}.$$
If we look for the particular solution to this equation, we get that $$z = \frac{f_0}{(\omega_0^2-\omega^2) + 2i \beta\omega} e^{i\omega t}.$$This while correct needs a bit of tidying up. We get a polar form on the constant, then we see that $$ A = \frac{f_0}{\sqrt{(\omega_0^2-\omega^2)^2+4\beta^2\omega^2}}, \qquad \text{and}\qquad \delta = \arctan\left(\frac{2\beta\omega}{\omega_0^2-\omega^2}\right). $$Thus we get that $$z(t) = Ae^{i(\omega t -\delta)},$$and the solutions to the other differential equations $$x(t) = A \cos(\omega t -\delta), \qquad y(t) = A \sin(\omega t-\delta).$$
We get the general solution of $$x(t) = A \cos(\omega t-\delta) + C_1 e^{r_1 t} + C_2 e^{r_2 t}.$$
We see that if $\beta > 0$, then the terms in the general solution will decay exponentially, and just leave the motion of the particular solution *irrespective of the initial conditions*. For this reason, the motion $x(t) = A \cos(\omega t-\delta)$ is called an *attractor*.

Lastly, we get the solution of the underdamped version $$
\begin{align*}
x(t) &= A \cos(\omega t -\delta) + A_\text{tr} \cos(\omega_1 t-\delta_\text{tr})\\ &= A \cos(\omega t -\delta) +e^{-\beta t}(B_1\cos(\omega_1 t)+ B_2\sin(\omega_1 t)),
\end{align*} $$where we get that $A_\text{tr}$ and $\delta_\text{tr}$ are arbitrary constants, and have the subscript $\text{tr}$ because it is they are *transient terms.*

We can be even more explicit in this case, and let $x(0) = x_0$, and $\dot x(0) = v_0$, $$\begin{align*}
B_1 &= x_0-A\cos\delta\\
B_2 &= \frac{1}{\omega_1}(v_0-\omega A \sin\delta + \beta B_1)
\end{align*}$$


## Resonance

We We say that apart from transient motions that die out quickly, the system's response is to oscillate sinusoidally at the same frequency as the driving force $$x(t) = A \cos(\omega t-\delta),$$where the amplitude $A$ is given by $$ A^2 = \frac{f_0^2}{(\omega_0^2-\omega^2)^2+4\beta^2\omega^2}.$$We see that $A \propto f_0$. We also need to examine how does the $A$ depend on the $\omega_0$, $\omega$ and $\beta.$ The most interesting case is when $\beta$ is small, so the second term of the denominator is small. If $\omega_0$ and $\omega$ are very different, then the first term is large, and the amplitude of the driven oscillations are small. On the other hand, if $\omega_0$ and $\omega$ are really closes, then both terms are very small, and the amplitude $A$ is very large. 

This means that the oscillator would vibrate at its natural frequency $\omega_0$. If we try to force it to vibrate at a frequency $\omega$, then the for values of $\omega$ close to $\omega_0$ the oscillator responds very well, but if $\omega$ is far from $\omega_0$, it hardly responds at all. We call *resonance* as the phenomenon of the greater response of an oscillator when driven at the right frequency.

The amplitude $A$ is a maximum when the denominator $$(\omega_0^2-\omega^2)^2+4\beta^2\omega^2$$is minimum. If we vary $\omega_0$ with $\omega$ fixed, this minimum occurs when $\omega_0 = \omega$. On the other hand if we vary $\omega$ with $\omega_0$ fixed, then we see that the maximum occurs at $$\omega_2 := \sqrt{\omega_0^2-2\beta^2}.$$
However, when $\beta \ll \omega_0$, we see that $\omega_2$ is really close to $\omega_0$. As a recap of all the frequencies we have seen $$\begin{align*}
\omega_0 := \sqrt{\frac km} &\quad \text{natural frequency of undamped oscillator} \\
\omega_1 := \sqrt{\omega_0^2-\beta^2} &\quad \text{frequency of damped oscillator} \\
\omega &\quad \text{frequency of driving force} \\
\omega_2 := \sqrt{\omega_0^2-2\beta^2} &\quad \text{value of $\omega$ at which response is maximum} \\
\end{align*}
$$
If we make the driving force $\omega_2$, then we get that the amplitud is $$A = \frac{f_0}{2\beta\omega_1}\approx \frac{f_0}{2\beta\omega_0}.$$
### Width of the Resonance; the $Q$ factor

If we make the damping constant $\beta$ smaller, the resonance peak not only higher, but also gets narrower. We can make this idea more precises by defining *full width at half maximum* or *FWHM* as the interval between where $A^2$ is equal to its half maximum height. 

We see that the points of half maximum are $$\omega = \sqrt{\omega_2^2 \pm \sqrt{12}\beta\omega_1}\approx \omega_0 \pm \beta. $$Thus the gull width at half maximum is $$\text{FWHM} = \sqrt{\omega_2^2 + \sqrt{12}\beta\omega_1}- \sqrt{\omega_2^2 - \sqrt{12}\beta\omega_1} \approx 2\beta,$$
or, equivalently, the *half width at half maximum* is $$\text{HWHM} = \frac{\sqrt{\omega_2^2 + \sqrt{12}\beta\omega_1}- \sqrt{\omega_2^2 - \sqrt{12}\beta\omega_1} }{2} \approx \beta.$$
The sharpness of the resonance peak is indicated by the ratio of its width $2\beta$ to its position $\omega_2$. Sometimes we want a very sharp resonance, so it is common to practice to define a *quality factor* $Q$ as $$Q = \frac{\omega_0}{2\beta} = \pi \frac{1/\beta}{2\pi /\omega_0} = \pi \frac{\text{decay time}}{\text{period}}.$$
# Periodic Driving Force

Let $f$ be a periodic driving force, with period $\tau$. Then, we can define a $\omega := 1/\tau$. With this in mind, we can assume that $f$ is representable as Fourier series $$f(t) = \frac{a_0}{2} + \sum_{n = 1}^\infty a_n\cos(\omega n t) + b_n\sin(\omega n t),$$where $$a_n := \frac{2}{\tau}\int_{0}^\tau f(t)\cos(n\omega t)\, dt, \qquad b_n := \frac{2}{\tau}\int_{0}^\tau f(t)\sin(n\omega t)\, dt.$$
Fortunately, we can assume that $f$ is an even function since we only need to know what happens for $t> 0$, then $b_n = 0$ for all $n \in \Bbb N ^+$. Then we get that $$f(t) = \sum_{n = 0}^\infty f_n\cos(\omega n t).$$
We can get a solution for the differential equation $$\ddot x + 2\beta \dot x + \omega_0^2 x = f(t),$$as $$x(t) = \sum_{n = 0}^\infty A_n \cos(n\omega t - \delta_n)$$where $$A_n := \frac{f_n}{\sqrt{(\omega_0^2- n^2\omega^2)+ 4 \beta^2n^2 \omega^2}}, \qquad \delta_n := \arctan\left(\frac{2\beta n \omega}{\omega_0^2-n^2\omega^2}\right).$$
### The Root Mean Squared Displacement

