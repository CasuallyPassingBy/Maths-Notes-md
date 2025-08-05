---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]

If $\bf r$ represents a trajectory through space, we have that, we can derive it differently since the basis vectors are non-constant in different coordinante systems. 

We add notation where $\hat{\bf{ r}}$ represents the normalised version of $\bf r$ and represents the direction, and $\hat{\pmb{\phi}}$ or $\hat{\boldsymbol{\phi}}$ represents the unit vector in the $\phi$ direction

We have that

$$ \frac{d \hat{\bf r}}{dt } = \dot\phi \hat{\boldsymbol{ \phi}} \qquad \frac{d\hat{\boldsymbol{\phi}}}{dt} = -\dot \phi \hat{\bf r } $$

### Velocity
Cartesian:
$\dot{ \bf r}=\mathbf{v}= \dot x e_1 + \dot y e_2$

Polar
$\dot{\bf r} =\mathbf v = \dot r \hat{\bf r}+r \dot\phi \hat{\boldsymbol\phi}$

Spherical:
$\dot{\bf r} =\mathbf v = \dot r \hat{\bf r}+r \dot\theta \hat{\boldsymbol\theta} + r \sin \theta \dot \phi \hat{\boldsymbol\phi}$

### Accelartion

Cartesian
$\ddot{\bf r} = {\bf a} = \ddot x e_1 + \ddot y e_2$

Polar
$\ddot{\bf r} = {\bf a} = (\ddot r-r\dot\phi^2)\hat{\bf r} +(r\ddot \phi+ 2\dot r\dot \phi)\hat{\boldsymbol \phi}$