---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Kinetic Energy and Work in Classical Mechanics]]

A force $\bf F$ acting on a particle is **conservative** iff it satisfies two conditions
- $\bf F$ depends only on the particle position $\bf r$ (and not the velocity $\bf v$, or the time $t$, or any other variables); that is $\mathbf{F} = \mathbf{F}(\mathbf r)$
- For any two points $1$ and $2$, the work $W(1\to 2)$ done by $\bf F$ is the same for all paths between $1$ and $2$

This is closely related to [[Conservative Fields]]

The reason, it is called *"conservative"*, and why it is important: if all forces on an object are conservative, we can define a quatity called potential energy (or just $\text{PE}$), denoted as $U(\mathbf r)$, a function only of position, with the property that the total mechanical energy

$$
E =\text{KE}+\text{TE} = T+U(\mathbf r)
$$

is constant; that is, $E$ *conserved*.

Similarly, as we [[Conservative Fields#^13cae7|proved the equivalence of conservative fields in maths]], we can construct a potential for a conservative field. We first choose a reference point $\mathbf r_0$ at which $U$ is defined to be zero. We then define $U(\mathbf r)$, the **potential energy** at an arbitrary point $\bf r$, to be

$$
U(\mathbf r) = -W(\mathbf r_0 \to \mathbf r) =-\int_{\mathbf r_0}^\mathbf r \mathbf F(\mathbf r') \cdot d\mathbf r'
$$
The minus sign is a thing that makes it different from the mathematical idea of a potential or gradient, and we fully exploit that $\bf F$ is a conservative force, since it is this fact that makes $U$ a function. 

The reason for the minus sign is really simple, since we want that the energy is conserved. Let's consider the work from $\mathbf r_1$ to $\mathbf r_2$. We get that
$$
W(\mathbf r_1 \to \mathbf r_2) = -[U(\mathbf r_2)- U(\mathbf r_1)]  = -\Delta U
$$
and similarly
$$
W(\mathbf r_1 \to \mathbf r_2) = \Delta T
$$
by the Work-KE Theorem. We get the following equation
$$
\Delta T = - \Delta U \iff \Delta(T+U) =0
$$
That is **mechanical energy**
$$
E = T+U
$$
### Principle of Conservation of Energy for One Particle

If all of the $n$ forces $\mathbf F_i$ ($i = 1,\dots, n$) acting on a particle on are conservative, each with its corresponding potential energy $U_i(\mathbf r)$, the **total mechanical energy**, defined as
$$
E = T+ U = T+ \sum_{i =1}^n U_i(\mathbf {r})
$$

is constant in time. 

## Non-conservative Forces

If some of the forces on our particle are non-conservative, then we can split the forces into conservative and non-conservative. Then, we have that $\mathbf F_\text{cons}$ (the conservative forces) has its associated potential $U$, and $\mathbf F_\text{nc}$ is the non-conservative part. By the Work-KE theorem, the change in kinetic energy between two times is
$$
\Delta T = W = W_\text{cons} + W_\text{nc}
$$
The first term on the right is just $-\Delta U$ can be moved to the left side to give $\Delta(T+U) = W_\text{nc}$. If we define the mechanical energy as $E=T+U$, then we see that
$$
\Delta E = \Delta(T+U) = W_\text{nc}
$$
Mechanical energy is no longer conserved, but we have the next best thing, how much the mechanical energy changes.

## Force as a Gradient of Potential Energy

We can see what happens when we make work on an infinitesimal path getting
$$
\begin{align*}
W(\mathbf{r} \to \mathbf{r}+d\mathbf{r}) &= \mathbf{F}\cdot d \mathbf{r}
\\
&= F_x \, dx +F_y \, dy+F_z \, dz
\end{align*}
$$
On the other hand we get that by conservation of energy
$$
W(\mathbf{r}\to \mathbf{r}+ d\mathbf{r}) = -[U(\mathbf{r}+d\mathbf{r})-U(\mathbf{r})] = -dU
$$

We can use some kind of weird notation, and get that
$$
dU = \frac{\partial U}{\partial x}\, dx + \frac{\partial U}{\partial y}\, dy + \frac{\partial U}{\partial z}\, dz
$$
Then we see that
$$
F_x = -\frac{\partial U}{\partial x} \qquad F_y =-\frac{\partial U}{\partial y} \qquad F_z = -\frac{\partial U}{\partial z}
$$
Thus 
$$
\mathbf F = -\nabla U
$$
Meaning that the force $\mathbf F$ can be obtained as from the potential energy. This is one of the equivalences to a [[Conservative Fields#^ddeab3|conservative field]] 

Similarly as we did when we wrote $dU$, we can give it a more mathematical expression, let $f$ be a scalar field
$$
df = \nabla f \cdot d\mathbf r
$$
## Second Condition That $\bf F$ be Conservative

Since we are supposing that the force is has a *nice domain* we can simply suppose that it is simply connected. Then we get a simple test for if a force is conservative

$$
\nabla \times F = 0
$$

With a little bit of work we know that this equality is equivalent to being conservative.

## Time dependent Potential Energy

We can sometimes study a force $\mathbf{F}(\mathbf r, t)$ that is irrotational $(\nabla \times \mathbf F =0)$, but doesn't satisfy being path independent, because it is *time-dependent*. We can still define a potential energy $U(\mathbf r, t)$ with the property $\mathbf F = -\nabla U$, but it is no longer the case that total mechanical energy $E = T+U$ is conserved. 

We now define the quantity $E= T+U$, but this quantity is no longer conserved. We can look at what happens at neighbouring moments in time, from $t$ to $t+dt$. Then we see that 
$$
dT = \frac{dT}{dt}\, dt = (m \mathbf{\dot v}\cdot \mathbf v) \, dt = \mathbf F\cdot d\mathbf r
$$
Meanwhile if we look at $U$, we get that
$$
dU = \frac{\partial U}{\partial x}\, dx+\frac{\partial U}{\partial y}\, dy +\frac{\partial U}{\partial z}\, dz+\frac{\partial U}{\partial t}\, dt
$$
The first three terms can be thought of $\nabla U \cdot d\mathbf r =-\mathbf F\cdot d\bf r$, getting the equality
$$
dU = -\mathbf F\cdot d\mathbf r +\frac{\partial U}{\partial t}\, dt
$$
Meaning that
$$
dE = d(T+U) = +\frac{\partial U}{\partial t}\, dt
$$
Finally getting that
$$
\frac{dE}{dt} = \frac{\partial U}{\partial t}
$$