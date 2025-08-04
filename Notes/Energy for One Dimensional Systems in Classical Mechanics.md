---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Potential Energy and Conservative Forces in Classical Mechanics]], [[Kinetic Energy and Work in Classical Mechanics]]

To begin, let us consider an object contrained to move along a perfectly straight track, which we take to be the $x$ axis. The only component of any force $\bf F$ that can work is the $x$ component, and we can simply ignore the other two components. Therefore, the work done by $\bf F$ is the one dimensional integral: $$W(x_1 \to x_2) = \int_{x_1}^{x_2} F_x(x)\, dx.$$If the force is to be conservative, $F_x$ must satisfy two conditions:
- It must only depend on the position $x$
- The work must path independent.
Fortunately, on one-dimensional systems the first condition implies the second one. This is because of a property of integrals.

### Graphs of the Potential Energy

A second useful feature of one-dimensional systems is that with only one independent variable we can plot the potential energy $U(x)$, this makes it easy to visualise the behaviour of the system. Assuming all the forces on the object are conservative, we define the potential energy as $$U(x) = - \int_{x_0}^x F_x(x')\, dx',$$where $F_x$ is the $x$ component of the net force on the particle. Corresponding to the three-dimensional result ${\bf F} = -\nabla U$, we have the simpler result in one dimension $$F = -\frac{dU}{dx}.$$

If we plot the potential energy against $x$, we can easily qualitatively how the object has to behave. The direction of the net force is given by the equation above as downhill on the graph $U(x)$. For any one-dimensional system, we can always *think* about the graph $U(x)$ as a picture of a roller coaster, and common sense will generally tell us the kind of motion that is possible at different places. 

At points where $dU/dx = 0$, the net force is $0$, and the object can remain in equilibrium. That is, the condition $dU/dx =0$ characterises points of equilibrium. If $\frac{d^2U}{dx^2} > 0$, and $\frac{dU}{dx} = 0$, the points are stable, i.e., a small displacement from equilibrium causes a foce which pushes the object back to equilibrium. At equilibrium points where $\frac{d^2U}{dx^2} < 0$ and $\frac{dU}{dx} = 0$, a small displacements leads to a force *away* from equilibrium, and the equilibrium is unstable. 

# Complete Solution of Motion

A third feature of one-dimensioanl conservative systems is that we can —at least in principle— use the conservation of energy to obtain a complete solution of the motion. Since $E = T+ U(x)$ is conserved, with $U(x)$ a known function, and $E$ determined by the initial conditions, we can solve for $T = \frac12 m \dot x^2 = E-U(x)$ and hence for the velocity $\dot x$ as a function of $x$ $$\dot x (x) = \pm \sqrt{\frac2m} \sqrt{E- U(x)}. $$We need to consider the sign since energy cannot determine the *direction* of the velocity. For this reason this method doesn't work in a truly three dimensional problem. 

Knowing the velocity as a function of $x$, we can now find $x$ as a function of $t$, using separation of variables, as follows: $$dt = \frac{dx}{\dot x}.$$Next, we can integrate between any initial and final points to give $$t_f -t_i = \int_{x_i}^{x_f} \frac{dx}{\dot x}.$$This gives the time for travel between any initial and final positions of interests. If we substitute for $\dot x$ in our ODE above and assume that $\dot x$ is positive, then the time to go from initial $x_0$ at time $0$ to an arbitrary $x$ at time $t$ is $$t = \int_{x_0}^x\frac{dx'}{\dot x(x')} = \sqrt{\frac m2}\int_{x_0}^x \frac{dx'}{\sqrt{E- U(x')}}.$$
## Curvilinear One-Dimensional Systems

So far the only dimensional system we have considered is an object contrained to move along a linear path, with position specified by the coordinate $x$. There are other, more general, systems that can equally be said to be one-dimensional, inasmuch as their position is bead threaded on curved rigid wire. The position of the bead can be specified by a simple parameter, which we can choose as their distance $s$, measured along the wire, from a chosen origin $O$. 

The coordinate $s$ of out bead corresponds, of course, to $x$ for a cart on a straight track. The speed of the bead is easily seen to be $\dot s$, and the kinetic energy is therefore just $$T= \frac12 m\dot s^2.$$The force is a little bit more complicated. As out bed moves on the curved wire the net normal force is not zero. The normal force is what constraints the bead to follow its assigned curving path, for this reason the normal force is called the *force of restraint*. On the other hand, the normal force does not work, and it is the *tangential* component $F_\text{tang}$of the net force that is out concern. We can actually prove that $$m \ddot s = F_\text{tang}. $$Furhter, if all the forces on the bead that have a tangential component are conservative, we define a corresponding potential energy $U(s)$ such that $$F_\text{tang} = \frac{dU}{ds},$$and the total mechanical energy $E = T+ U(s)$ is constant. 