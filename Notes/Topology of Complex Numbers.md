---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[The Riemann Sphere]], [[Complex Numbers]], [[Rn]]

### Topology of $\Bbb C$

Since there’s an isomorphism between $\Bbb C$ and $\Bbb R^2$ that is of the form $x +iy \mapsto (x,y)$ and it also preserves lengths, (an isometry). Then it is also a homeomorphism, and thus $\Bbb C \cong \Bbb R^2$ topologically speaking.

### Topology of $\widehat{\Bbb C}$

The topological structure of $\Bbb C$ cannot be extended to $\widehat{\Bbb C}$, with the identification to the Riemann Sphere $S \subseteq \Bbb R^3$ and the euclidean distance in $\Bbb R^3$, we can define $d^*$ a metric on $\widehat{\Bbb C}$, defined as

$$ d^*(z, w) = \|E^{-1}(z) - E^{-1}(w)\| $$

then if $z, w \in \Bbb C$, then

$$ d^*(z ,w) = \frac{2|z-w|}{\sqrt{\left(|z|^2+1\right)\left(|w|^2+1\right)}} $$

if $z \in \Bbb C$

$$ d^*(z,\infty) = \frac{2}{\sqrt{|z|^2+1}} $$

**********Def:********** We can define open balls $\widehat{\Bbb C}$ as follows:

$$ \widehat{B_r}(z_0) := \{z \in \widehat{\Bbb C} \mid d^*(z,z_0) < r \} \subseteq \widehat{\Bbb C} $$

******************Prop:****************** If $U^* \subseteq \widehat{\Bbb C}$ is an open set iff there’s $U \subseteq {\Bbb C}$ (in the usual topology) such that ${U = U^* \cap{\Bbb C}}$.

********Def:******** Let $(a_n)_{n \in \Bbb N}$ be a sequence we say that the sequence converges to $a$ if

$$ \forall \varepsilon>0 \exists N\in \Bbb N\forall n\ge N[|a_n -a|< \varepsilon] $$

We know that a sequence $(a_n) _{n \in \Bbb N}$ is convergent iff it is Cauchy