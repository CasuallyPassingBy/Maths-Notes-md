---
tags:
  - ClassicalMechanics
---
Subjects: [[Classical Mechanics]]
Links: [[Newton's Laws]]

Let us consider a group of $N$ particles, $\alpha = 1, \dots, N$, with masses $m_\alpha$ and positions $\bf r_\alpha$  measured to an origin $O$. The **centre of mass** (or $\bf CM$) of the system is defined to to be the position (relative to the same origin $O$):
$$
\mathbf{R} = \frac{1}{M}\sum_{\alpha =1}^N m_\alpha \mathbf{r}_\alpha 
$$
Where $M$ denoted the total amount of mass of all particles $M = \sum m_\alpha$ 

We can write the total amount of momentum $\mathbf P$ of any $N$-particle system in terms of the $\bf CM$ as follows:
$$
\mathbf P = M \bf\dot R
$$
similarly we get that
$$
\frac{d}{dt}(M \mathbf{\dot R}) = \mathbf F^\text{ext}
$$
That is, the centre of mass $\bf R$ moves exactly as if it were a single particle with a mass $M$, subject to external force of the system. This result is the main reason we can treat extended bodies, such as baseballs and planets as point particles. Provided the a body is small compared to the scale of its trajectory, its $\bf CM$ position $\bf R$ is a good representative of overall location, and that implies that $\bf R$ moves just like a point particle


Let $A \subseteq \Bbb R^n$ be Jordan-measurable then and $\rho:A \to \Bbb R$ be integrable over $A$, be thought of a the density of $A$. Then the way we can find the centre of mass of $A$ with density $\rho$ is by extracting it coordinate by coordinate. Let $\overline x$ be the centre of mass , then
$$ \overline x_i = \dfrac{\int_A x_i\cdot \rho(x)}{\int_A \rho(x)} $$
Or we can put it as
$$
\mathbf R = \frac{1}{M} \int \mathbf r \, dm = \frac{1}{M}\int\rho \;\mathbf r\, dV
$$
