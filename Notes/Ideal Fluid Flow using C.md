---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Solenoidal Fields]], [[Conservative Fields]], [[Analytic Functions]]

Some characteristics to fluid ideal fluid flow are two constraints, where $v$ represents the velocity field:

- incompressibility
    
    $$ \operatorname{div}(v) =0 $$
    
- irrotationality
    
    $$ \operatorname{curl}(v) =0 $$
    

If we make the following substitution we get that

$$ v_1 = \frac{\partial \phi}{\partial x} = \frac{\partial \psi}{\partial y} \quad \text{and }\quad v_2 = \frac{\partial \phi}{\partial y} = -\frac{\partial \psi}{\partial x} $$

then $v = \nabla \phi$. We call $\phi$ the _********velocity potential,********_ and $\psi$ the ****************stream function,**************** notice that $\phi$ and $\psi$ satisfy the Cauchy-Riemann Equations, and we have, an associeted _**************************complex velocity potential:**************************_

$$ \Omega(z) := \phi(x, y) +i\psi(x,y) $$

The derivative of $\Omega(z)$ is usually called the complex velocity

$$ \Omega'(z) = \frac{\partial \phi}{\partial x} +i\frac{\partial \psi}{\partial x} = \frac{\partial \phi}{\partial x}-i \frac{\partial \phi}{\partial y} = v_1 - iv_2 $$

thus $\overline{\Omega'(z)} = v_1+iv_2$ is analogous to the usual velocity vector.

There are associeted boundary conditions

- The normal derivative of $\phi$ along must vanish on a rigid boundary of an ideal fluid.