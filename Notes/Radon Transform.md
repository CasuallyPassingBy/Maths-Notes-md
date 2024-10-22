---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Fourier Transform in Rn]], [[Fourier Transform in R]]

If $\cal O$ is an object in $\Bbb R^n$ determines by a function $\rho$ which describes density and physical characteristics of this object, sending and $X$-ray beam through $\cal O$ determines the quantity $$\int_L \rho$$for every line in $\Bbb R^n$. 

If $\cal P$ is a hyperplane, we define the Radon transform $\mathcal R(f)$ by $$\mathcal R(f)(\mathcal P)=\int_\mathcal P f$$To simplify our presentation, we shall assume we are dealing with functions in class $\mathcal S(\Bbb R^n)$. 

The description we use for planes in $\Bbb R^3$ is the following: given unit vector $\gamma \in \Bbb S^{n-1}$ and a real number $t\in \Bbb R$, we define the plane $\mathcal P_{t, \gamma}$, by $$\mathcal P_{t, \gamma} = \{x\in \Bbb R^3 \mid x \cdot \gamma = t\}$$So we parametrize a plane by a unit vector $\gamma$ orthogonal to ir, and by its "distance" $t$ to the origin. We see that $\mathcal P_{t, \gamma} = \mathcal P_{-t, -\gamma}$, and allow $t$ to take negative values.

To make sense of the integral, we can consider $e_1, e_2, \dots, e_{n-1}$ such that $e_1, e_2, \dots, e_{n-1}, \gamma$ is an orthonormal basis for $\Bbb R^3$. Then $x \in P_{t, \gamma}$ can be written as $$x = t\gamma + u \qquad \text{where}\qquad u = u_1 e_1 + u_2 e_ 2+ \dots + u_{n-1}e_{n-1} \qquad u_1, u_2, \dots, u_{n-1} \in \Bbb R$$
If $f \in \mathcal S(\Bbb R^n)$, we define $$\int_{\mathcal P_{t, \gamma}} f = \int_{\Bbb R^{n-1}} f(t\gamma + u_1 e_1 + u_2 e_2+ \dots u_{n-1}e_{n-1})\, du_1 \, du_2 \dots \,du_{n-1} $$
**Prop:** If $f\in \mathcal S(\Bbb R^n)$, then for each $\gamma$ the definition of $\int_{\mathcal P_{t, \gamma}}f$  is independent of choice of $e_1, e_2, \dots, e_{n-1}$. Moreover $$\int_{-\infty}^\infty \left(\int_{\mathcal P_{t, \gamma}}f\right)\, dt = \int_{\Bbb R^n} f(x) \, dx$$
The *Radon transform* of a function $f\in \mathcal S(\Bbb R^3)$ is defined by $$\mathcal R(f)(t, \gamma) = \int_{\mathcal P_{t, \gamma}} f$$
We see that the Radon transform is a function on the set of planes in $\Bbb R^n$. From the parametrization given for a plane we may equivalently think of $\mathcal R(f)$ as a function on the product $\Bbb R \times \Bbb S^{n-1}$. 

The relevant class of functions on $\Bbb R \times \Bbb S^{n-1}$ consists of those that satisfy the Schwartz condition in $t$ uniformly in $\gamma$. In other words, we define $\mathcal S(\Bbb R\times \Bbb S^{n-1})$ to be the space of all continuous functions $F(t, \gamma)$ that are infinitely differentiable in $t$, and satisfy that $$\sup_{t\in \Bbb R, \gamma \in \Bbb S^2} |t|^k \left|\frac{\partial^n F}{\partial t^n}(t, \gamma) \right| < \infty \qquad \forall n, k \in \Bbb N$$
**Lemma:** If $\mathcal S(\Bbb R^3)$, then $\mathcal R(f)(t, \gamma) \in \mathcal S(\Bbb R)$ for each fixed $\gamma$. Moreover, $$\widehat {\mathcal R}(f)(s, \gamma) = \hat f(s\gamma)$$where $\widehat{\mathcal R}(f)$ is the one-dimensional Fourier transform of $t$, with $\gamma$ fixed, and $\hat f$ denotes the $n$-dimensional Fourier transform of $f$.

**Cor:** If $f, g \in \mathcal S(\Bbb R^n)$ and $\mathcal R(f) = \mathcal R(g)$, then $f= g$.

# Check After Measure Theory

Given a function $F$ on $\Bbb R\times \Bbb S^{n-1}$, we define its *dual Radon transform* by $$\mathcal R^*(F) (x) = \int_{\Bbb S^{n-1}} F(x \cdot \gamma, \gamma) \, d\sigma(\gamma)$$
Let $\mathcal R^* : \mathcal S(\Bbb R \times \Bbb S^2) \to \mathcal S(\Bbb R^3)$, and $\mathcal R:\mathcal S(\Bbb R^3) \to \mathcal S(\Bbb R\times \mathcal S^2)$. To see that is indeed the hermitian adjoint of the Radon transform, we need to define an inner product in $\mathcal S(\Bbb R\times \Bbb S^2)$. This being defined as $$(F, G)_2 = \int_{\Bbb R} \int_{\Bbb S^2} F(t, \gamma) \overline{G(t, \gamma)}\, d\sigma(\gamma)\, dt $$and we remember the inner product on $\mathcal S(\Bbb R^3)$, as $$ (f, g)_1= \int_{\Bbb R^3}f(x)\overline{g(x)}\, dx$$
We see that $$(\mathcal R f, F)_2 = (f, \mathcal R^* F)_1$$
letting us know that the dual Radon transform is the the adjoint of the Radon transform

**Th:** If $f \in \mathcal S(\Bbb R^3)$, then $$ \Delta(\mathcal{R^* R}(f)) = -8\pi^2f$$