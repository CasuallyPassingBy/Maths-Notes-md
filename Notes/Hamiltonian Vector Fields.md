---
tags:
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]], 
Links: [[Symplectic Forms on Smooth Manifolds]], [[The de Rham Cohomology Groups]], [[The Lie Derivative]]

**Obs:** Let $(M, \omega)$ be a symplectic manifold. Since $\omega$ is nondegenerate, there is a smooth bundle isomorphism $\widehat\omega : TM \to T^*M$ defined by $\widehat \omega(X) := X \;\lrcorner \;\omega$. 

**Def:** Suppose $(M, \omega)$ is a symplectic manifold. For any smooth function $f\in \mathcal C^\infty(M)$, we define the *Hamiltonian vector field of $f$* to be the smooth vector field $X_f$ defined by $$X_f := \widehat\omega^{-1}(df),$$where $\widehat\omega: TM \to T^*M$ is the bundle isomorphism determined by $\omega$. Equivalently, $$X_f \;\lrcorner\;\omega = df,$$ or for any vector field $Y$, $$\omega(X_f, Y) = df(Y) = Yf.$$
In Darboux coordinates, $X_f$ can be computed explicitly. Writing $$X_f = \sum_{i = 1}^n \left(a^i \frac{\partial}{\partial x^i}+ b^i\frac{\partial}{\partial y^i} \right)$$for some coefficients $(a^i, b^i)$ to be determined, we compute $$X_f \;\lrcorner\; \omega = \left(a^i \frac{\partial}{\partial x^i}+ b^i\frac{\partial}{\partial y^i} \right) \; \lrcorner  \sum_{i = 1}^n dx^i \wedge dy^i = \sum_{i = 1}^n(a^idy^i - b^i dx^i).$$On the other hand,  $$df = \sum_{i = 1}^n \left(\frac{\partial f}{\partial x^i} dx^i + \frac{\partial f}{\partial y^i} dy^i \right). $$Setting these two expression equal to each other, we find $a^i = \frac{\partial f}{\partial y^i}$ and $b^i = - \frac{\partial f}{\partial x^i}$, which yields the following formula for the Hamiltonian vector field of $f$ in Darboux coordinates: $$X_f = \sum_{i = 1}^n \left(\frac{\partial f}{\partial y^i}\frac{\partial}{\partial x^i}- \frac{\partial f}{\partial x^i}\frac{\partial }{\partial y^i} \right).$$This formula holds, in particular, on $\Bbb R^{2n}$ with its standard symplectic form.

**Properties of Hamiltonian Vector Fields:** Let $(M, \omega)$ be a symplectic manifold and let $f\in \mathcal C^\infty(M)$.
- $f$ is constant along each integral curve of $X_f$.
- At each regular point of $f$, the Hamiltonian vector field $X_f$ is tangent to the level set of $f$.

**Def:** A smooth vector field $X$ on $M$ is said to be *symplectic* if $\omega$ is invariant under the flow of $X$. It is said to be *Hamiltonian*, or *globally Hamiltonian*, if there exists a function $f\in \mathcal C^\infty(M)$ such that $X = X_f$, and *locally Hamiltonian* if each point $p$ has a neighbourhood on which $X$ is Hamiltonian.

**Hamiltonian and Symplectic Vector Fields:** Let $(M, \omega)$ be a symplectic manifold. A smooth vector field on $M$ is symplectic iff it is locally Hamiltonian. Every locally Hamiltonian vector field on $M$ is globally Hamiltonian iff $H_\text{dR}^1(M) = 0$. 

**Def:** A symplectic manifold $(M, \omega)$ together with a smooth function $H\in \mathcal C^\infty(M)$ is called a *Hamiltonian system*. The function $H$ is called the *Hamiltonian* of the system; the flow of the Hamiltonian vector field $X_H$ is called its *Hamiltonian flow*, and the integral curves of $X_H$ are called the *trajectories* or the *orbits* of the system. In Darboux coordinates, the formula of the Hamiltonian vector field implies that the orbits of those curves $\gamma(t) = (x^i(t), y^i(t))$ that satisfy  $$\begin{align*}
\dot x^i(t) &= \frac{\partial H}{\partial y^i}(x(t), y(t)), \\
\dot y^i(t) &=- \frac{\partial H}{\partial x^i}(x(t), y(t))
\end{align*} $$These are called *Hamilton's equations*. 

## Poisson Bracket

**Def:** Let $(M,\omega)$ be a symplectic manifold. Given $f,g\in \mathcal C^\infty(M)$, we define their *Poisson bracket* $\{f, g\}\in \mathcal C^\infty(M)$ by any of the following equivalent formulas: $$\{f, g\} := \omega(X_f, X_g) = df(X_g) = X_g f. $$Two function are said to *Poisson commute* if their Poisson bracket is zero.

We can readily compute the Poisson bracket of two function $f,g$ in Darboux coordinates $$\{f, g\} =\sum_{i = 1}^n \left(\frac{\partial f}{\partial x^i}\frac{\partial g}{\partial y^i}- \frac{\partial f}{\partial y^i}\frac{\partial g}{\partial x^i} \right).  $$
**Properties of the Poisson Bracket:** Suppose $(M, \omega)$ is symplectic manifold, and $f, g, h\in\mathcal C^\infty(M)$.
- *Bilinearity:* $\{f, g\}$ is linear over $\Bbb R$ in $f$ and in $g$.
- *Antisymmetry:* $\{f, g\} = -\{g, f\}$.
- *Jacobi Identity:* $\{\{f, g\}, h\} + \{\{g, h\}, f\} + \{\{h, f\}, g\} = 0$.
- $X_{\{f, g\}} = - [X_f, X_g]$.

**Cor:** If $(M, \omega)$ is a symplectic manifold, the vector space $\mathcal C^\infty(M)$ is a Lie algebra under the Poisson bracket.

**Def:** If $(M, \omega, H)$ is a Hamiltonian system, and function $f\in \mathcal C^\infty(M)$ that is constant on every integral curve of $X_H$ is called a *conserved quantity* of the system.

A smooth vector field $V$ on $M$ is called an *infinitesimal symmetry* of $(M, \omega, H)$ if both $\omega$ and $H$ are invariant under the flow of $V$.

**Prop:** Let $(M,\omega, H)$ be a Hamiltonian system.
- A function $f\in \mathcal C^\infty(M)$ is a conserved quantity iff $\{f, H\} = 0$. 
- The infinitesimal symmetries of $(M, \omega, H)$ are precisely the symplectic vector fields $V$ that satisfy $VH = 0$.
- If $\theta$ is the flow of an infinitesimal symmetry and $\gamma$ is a trajectory of the system then for $s\in \Bbb R$, $\theta_s\circ \gamma$ is also a trajectory on its domain of definition.

**Noether's Theorem:** Let $(M,\omega, H)$ be a Hamiltonian system. If $f$ is any conserved quantity, then its Hamiltonian vector field is an infinitesimal symmetry. Conversely, if $H_\text{dR}^1(M) = 0$, then each infinitesimal symmetry is the Hamiltonian vector field of a conserved quantity, which is unique up to the addition of a function that is constant on each component of $M$.

There is one conserved quantity that every Hamiltonian system possesses: the Hamiltonian $H$ itself. The infinitesimal symmetry corresponding to it generates the Hamiltonian flow of the system, which describes how the system evolves over time. Since $H$ is typically interpreted as the total energy of the system, one usually say that the symmetry corresponding to conservation of energy is "translation in the time variable". 

## Hamiltonian [[Integral Curves, Flows and Flowouts on Smooth Manifolds|Flowouts]]

Hamiltonian vector fields are powerful tools for constructing isotropic and Lagrangian submanifolds. Because Lagrangian submanifolds of $T^*M$ correspond to closed $1$-forms, which in turn correspond to differentials of functions, such constructions have numerous applications in PDE theory.

**Hamiltonian Flowout Theorem:** Suppose $(M, \omega)$ is a symplectic manifold, $H\in \mathcal C^\infty(M)$, $\Gamma$ is an embedded isotropic submanifold of $M$ that is contained in a single level set of $H$, and the Hamiltonian vector field $X_H$ is nowhere tangent to $\Gamma$. If $\cal S$ is a flowout from $\Gamma$ along $X_H$, then $\cal S$ is also an isotropic contained in the same level set of $H$.