---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Linear Momentum in Classical Mechanics]]

One of the most basic types of energy, is the **kinetic energy** ($\text{KE}$), which for a single particle of mass $m$ travelling with speed $v$ is defined as
$$
T = \frac{1}{2}m v^2
$$
If we calculate the time derivative of $T$, keeping in mind that $v = \bf{v \cdot v}$, then
$$
\frac{dT}{dt} = m \mathbf{ \dot v \cdot v}
$$
since the mass is not changing we can translate it as
$$
\frac{dT}{dt} = \mathbf {F \cdot v} = \mathbf{ F} \cdot \frac{d\mathbf r}{dt}
$$
using the physicists, convention we get that
$$
dT = \mathbf F \cdot d\mathbf r
$$
The expression on the right, $F \cdot d\mathbf r$, is defined to be the **work done by the force** $\bf F$ in the displacement $d\bf r$. This is the **Work-KE theorem**. The change in a particles kinetic energy between two neighbouring points on it path is equal to the work done by the net force as it moves between the two points. 

We can extend this notion using integrals, getting that
$$
\Delta T \equiv T_2 - T_1 = \int_1^2 \mathbf F \cdot d\mathbf r \equiv W(1\to 2)
$$
This served as inspiration to formulate mathematically the [[Line Integral over a Vector Field]]

This it the **Work-KE theorem** for arbitrary displacements, and since the line integral is linear, we can decompose $\bf F$ into different forces, getting that $\mathbf{ F = \sum F}_i$, and getting that
$$
\Delta T \equiv T_2-T_1 = \int_1^2 \mathbf F \cdot d\mathbf r = \sum_i \int_1^2 \mathbf F_i \cdot d\mathbf r = \sum_i W_i(1\to 2)
$$
which is the useful version of the theorem
