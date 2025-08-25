---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]]
Links: [[Vector Bundles on Smooth Manifolds]], [[Tensor Product of Linear Functions]], [[The Tangent Bundle]], [[The Cotangent Bundle]]

On a manifold $M$, we can perform the same linear algebraic constructions on each tangent space $T_p M$ that we can perform on any vector space, yielding tensors at $p$. For example a $(k, q)$-tensor at $p\in M$ is just an element of $\mathcal T^k_q(T_p M)$. We define the *bundle of $(k,q)$-tensors* on $M$ as $$ T^k_q M := \coprod_{p \in M} \mathcal T^k_q(T_p M).$$
To see that each of these tensor bundles is a vector bundle, we define the projection $\pi: T^k_q M \to M$. If $(x^i)$ are the local coordinates on $U \subseteq M$, and $p \in U$, the coordinate vectors $\left\{\dfrac{\partial}{\partial x^i}\right\}$ for a basis for $T_p M$ whose dual basis is $\{dx^i\}$. Any tensor $F \in \mathcal T^k_q(T_p M)$ can be expressed in terms of this basis as $$F = F^{\nu_1, \dots, \nu_k}_{\mu_1,\dots, \mu_q} \frac{\partial}{\partial x^{\nu_1}} \otimes \dots\otimes  \frac{\partial}{\partial x^{\nu_k}}\otimes dx^{\mu_1}\otimes \dots \otimes dx^{\mu_q}. $$
