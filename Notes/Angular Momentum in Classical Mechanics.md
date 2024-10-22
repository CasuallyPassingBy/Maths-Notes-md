---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Linear Momentum in Classical Mechanics]], [[Newton's Laws]], [[Centre of Mass]]

# Single Particle
The **angular momentum** $\ell$ of a single particle is defined as the vector 
$$
\ell = \bf{r \times p}
$$
Here $\mathbf r$ is the position vector relative to an origin $O$, and its momentum $\bf p$. Since $\bf r$ depends on $O$, so does $\ell$. The angular momentum $\ell$ depends on the choice of origin, and we should, strictly speaking, refer to $\ell$ as the angular momentum *relative to $O$*. We can get the rate of change as
$$
\dot \ell  = \frac{d}{dt}\bf{r\times p} = (\dot r \times p) +(r\times \dot p)
$$
since $\mathbf p = m \bf \dot r$, then the first part cancels out by properties of the cross product. Then we can replace $\bf \dot p$ by the net force $\bf F$ on the particle, and we get
$$
\dot \ell = \mathbf {r \times F} = \Gamma
$$
Here $\Gamma$ denoted the net *torque* about $O$ on the particle defined as $\bf r\times F$, other popular symbols for torque are $\bf \tau$ and $\bf N$ 
$$
\dot \ell  = \Gamma
$$
is the rotational equivalent to Newton's second law

In many one-particle we can choose the origin $O$ so that the net torque $\Gamma$ is zero, meaning constant angular momentum. In the case of a single planet orbiting the sun. The only force on the planet is gravitational $GmM/r^2$ of the sun, and this means that the force is parallel to $\bf r$, meaning $\bf r \times F = 0$. Thus if we choose our origin at the sun, the planet's angular momentum about $O$ is constant. Because $\bf r \times p$ is constant, then $\bf r$ and $\bf p$ must remain in a fixed plane; meaning, the planet's orbit is confined to a single plane containing the sun, and the problem is reduced to two dimensions.
### Kepler's Second Law
As each planet moves around the sun, a line drawn from the planet to the sun sweeps out equal areas in equal times.

If we consider the area function $A$, this is equivalent to saying that $\dot A$ is constant. To prove this, we need to consider that for smol times $dt$, we can approximate the area as
$$
dA = \frac{1}{2}\|\mathbf{r \times v} \|dt
$$
Then we can convert $\mathbf{v} = \mathbf p/m$ getting that
$$
\frac{dA}{dt} = \frac{1}{2m}\|\mathbf{r\times p}\| = \frac{1}{2m}\|\ell\|
$$
since $\ell$ is constant by our choice of coordinates, then $\dot A$ is constant. 

# Multiple Particles

A system of $N$ particles, $\alpha = 1, \dots, N$ each with its angular momentum $\ell_\alpha = \bf r_\alpha \times p_\alpha$, with all $\bf r_\alpha$ measured from the same origin $O$. We define the **total angular momentum** $\bf L$ as
$$
\mathbf L= \sum_{\alpha = 1}^N \ell_\alpha = \sum_{\alpha = 1}^N \mathbf{r_\alpha \times p_\alpha}
$$
differentiating with respect to $t$ we get that
$$
\mathbf{\dot L} = \sum_\alpha \dot \ell_\alpha = \sum_\alpha \bf r_\alpha \times F_\alpha
$$
Then we can expand the forces to, as we did for the linear momentum, getting that
$$
\mathbf{\dot L} = \sum_{\alpha } \sum_{\beta\ne \alpha} \mathbf{r_\alpha} \times \mathbf{F}_{\alpha \beta} + \sum_{\alpha} \mathbf{r_\alpha \times F_\alpha ^\text{ext}}
$$
doing some algebra we get the first part is
$$
\sum_\alpha \sum_{\beta\ne \alpha} \mathbf{r_\alpha\times F_{\alpha \beta}} = \sum_\alpha \sum_{\beta > \alpha} (\mathbf{r_\alpha -r_\beta})\times\mathbf { F_{\alpha \beta}}
$$
Since $\bf r_\alpha - r_\beta$ is the vector from $\bf r_\beta$ to $\bf r_\alpha$, and the force $\bf F_{\alpha \beta}$ is in this direction, since the forces are central, then the we get that $(\mathbf{r_\alpha - r_\beta} )\times \bf F_{\alpha \beta} =0$. The remaining sum  single sum is just the net external torque, and we conclude that 
$$
\mathbf {\dot L} = \Gamma^\text{ext}
$$
### Principle of Conservation of Angular
If the net external force of an $N$-particle system is zero, the system's total angular momentum $\bf L = \sum r_\alpha \times p_\alpha$ is constant.

The validity of this principle depends on our two assumptions that all internal forces $\bf F_{\alpha \beta}$ are central and satisfy the third law. 
## Angular Momentum about CM

The conservation of angular momentum and the more general result $\mathbf{\dot L} =\Gamma^\text{ext}$ were derived on the assumption that all quantities were measured in inertial frame, so that Newton's Second Law could be invoked. This required that both $\bf L$ and $\Gamma^\text{ext}$ be measured about an origin $O$ fixed in some inertial frame. 

The weird thing, is that we can get the same results also hold if $\bf L$ and $\Gamma^\text{ext}$ are measured about the centre of mass - even if $\text{CM}$ is being accelerated and so is not fixed in an inertial frame. That is
$$
\frac{d}{dt} \mathbf L (\text{about CM}) = \Gamma^\text{ext} (\text{about CM})
$$

