---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Kinetic Energy and Work in Classical Mechanics]], [[Energy for One Dimensional Systems in Classical Mechanics]], [[Potential Energy and Conservative Forces in Classical Mechanics]]

A three-dimensional situation that has some of the simplicity of one-dimensional problems is a particle that is subject to a *central force*. If we take the force centre to be the origin, a central force has the form $$ \mathbf F(\mathbf r) = f(\mathbf r) \hat{ \mathbf r},$$where the function $f(\mathbf r)$ gives the magnitud if the force. 

We say that a function is spherically symmetric, with $\mathbf r$ expressed in polar coordinates, $f$ is independent of $\theta$ and $\phi$. To test of spherical symmetry we simply that the two partial derivatives $\frac{\partial f}{\partial \theta} = \frac{\partial f}{\partial \phi} = 0$. 

### The Gradient in Spherical Coordinates

We are going to consider the gradient in Cartesian coordinates. Let $f$ a continuously differentiable function, then $$\nabla f = \frac{\partial f}{\partial x}\hat{\mathbf x} + \frac{\partial f}{\partial y}\hat{\mathbf y} + \frac{\partial f}{\partial z}\hat{\mathbf z}.$$We would like to calculate the same vector in spherical coordinates. To find it, we consider a small displacement and recall that $$df = \nabla f \cdot d\mathbf r.$$This expression can be thought of the canonical way to represent the gradient, since $df$ can be expressed without any difference in coordinates since it represents the exterior derivative. We also need to know that actually means $d\mathbf r$, If we do that we get that $$d \mathbf r = dr \hat{\mathbf r} + r d\theta \hat{\boldsymbol \theta}+ r\sin\theta  d\phi \hat {\boldsymbol \phi}.$$
Since, in the physics convention $\hat{\mathbf r}, \hat{\boldsymbol \theta}, \hat{\boldsymbol \phi}$ are orthonormal vectors, then we get that: $$df = (\nabla f)_r \, dr + r(\nabla f)_\theta\, d\theta + r\sin\theta(\nabla f)_\phi\, d\phi,$$and we know that $$df = \frac{\partial f}{\partial r}\, dr + \frac{\partial f}{\partial \theta}\, d\theta + \frac{\partial f}{\partial \phi}\, d\phi.$$Thus, we get that $$\nabla f = \frac{\partial f}{\partial r} \hat{\mathbf r} + \frac1{r}\frac{\partial f}{\partial \theta} \hat{\boldsymbol \theta} +\frac1{r\sin \theta}\frac{\partial f}{\partial \phi} \hat{\boldsymbol \phi}.$$
This is neat enough, and we can see the dual nature of $df$ and $\nabla f$. In terms of correlations, we get that $\sharp (df) = \nabla f$. This nicely illustrates the duality: the gradient vector $\nabla f$ is the image of the $1$-form $df$ under the sharp isomorphism induced by the Riemannian metric, and viceversa. 

## Conservative and Spherically Symmetric

Let us assume that the central force $\mathbf F(\mathbf  r)$ is conservative. Since it is conservative, it can be expressed in the form $-\nabla U$, which the formula above we get that $$\mathbf F(\mathbf r) = - \nabla U = -\frac{\partial U}{\partial r} \hat{\mathbf r} - \frac1{r}\frac{\partial U}{\partial \theta} \hat{\boldsymbol \theta} - \frac1{r\sin \theta}\frac{\partial U}{\partial \phi} \hat{\boldsymbol \phi}.$$Since $\mathbf F$ is central, then only its radial component can be nonzero, and the last two terms must be zero, and thus, $U(\mathbf r)$ is spherically symmetric, and the equation reduces to $$\mathbf F(\mathbf r) = - \frac{\partial U}{\partial r} \hat{\mathbf r}.$$Since $U$ is spherically, the same is true of $\frac{\partial U}{\partial r}$, and we see that the central force $\mathbf F$ is indeed spherically symmetric. 

On the other hand if $\mathbf F(\mathbf r)$ is a central and spherically symmetric force, then $\mathbf F$ is conservative. 

**Virial Theorem:** A mass $m$ moves in a circular orbit centred at the origin in the field of an attractive central force with potential energy $U= kr^n$, then $T= \frac12 mv^2 = n U/2$. 