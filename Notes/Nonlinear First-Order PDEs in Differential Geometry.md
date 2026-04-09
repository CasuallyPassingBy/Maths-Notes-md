---
tags:
  - PartialDifferentialEquations
  - DifferentialGeometry
---
Subjects: [[Differential Geometry]], [[Partial Differential Equations]]
Links: [[Symplectic Forms on Smooth Manifolds]], [[Contact Structures on Smooth Manifolds]], [[Solution of Linear and Quasilinear First Order PDEs using Vector Flows]], [[Hamiltonian Vector Fields]], [[Jet Bundles on Smooth Manifolds]]

# Hamilton-Jacobi Equations

We begin with a somewhat special case. A first-order PDE that involves only the first derivatives of the unknown function but not the values of the function itself is called (in this note) a *Hamilton-Jacobi equation*. Such an equation for an unknown function $u(x^1,\dots, x^n)$ can be written in the form $$F\left(x^1,\dots, x^n, \frac{\partial u}{\partial x^1}, \dots, \frac{\partial u}{\partial x^n}\right) = 0. $$
More generally, if $M$ is a smooth manifold, a Hamilton-Jacobi equation on $M$ is given by a smooth real-valued function $F$ defined on an open subset $W\subseteq T^* M$, and a solution to the equation is a real-valued function $u$ defined on an open subset $U\subseteq M$ such that the image of $du$ lies in the zero set of $F$: $$F(x, du(x)) = 0 \qquad \text{for all }x\in U. $$
We are interested in solving a Cauchy problem for the equation above, given an embedded hypersurface $S\subseteq M$ and a smooth function $\varphi: S\to\Bbb R$, we wish to find a smooth function $u$ defined on a neighbourhood of $S$ in $M$ and satisfying the equation above together with the initial condition $$u|_S = \varphi.$$
We look for a closed $1$-form $\alpha$ satisfying $F(x, \alpha(x)) = 0$; then the Poincaré lemma guarantees that locally $\alpha = du$ for some function $u$. It suffices to construct function $u$. It suffices to construct a Langrangian submanifold of $T^*M$ that is the image of a $1$-form and is contained in $F^{-1}\{0\}$. The key to finding such a submanifold is the [[Hamiltonian Vector Fields#Hamiltonian Integral Curves, Flows and Flowouts on Smooth Manifolds Flowouts|Hamiltonian flowout theorem]]; after identifying are appropriate isotropic embedded initial submanifold $\Gamma \subseteq T^*M$.

The first challenge is to construct the initial submanifold $\Gamma \subseteq T^*  M$. We must look for an appropriate section of the restricted bundle $T^*M|_S$, that is, a smooth map $\sigma: S \to T^*M$ such that $\sigma(x) \in T_x M$ for each $x\in S$. This will be the value of $du$ along $S$ for our eventual solution $u$. Thus, we should expect that if it matches $d\varphi$ when restricted to vectors tangent to $S$, and that it satisfies the PDE at points of $S$. We requiere $\sigma$ to satisfy the following conditions: $$\begin{align*}
\sigma(x)|_{T_xS} &= d\varphi(x) \qquad \forall x\in S, \\
F(x, \sigma(x)) &= 0  \qquad\qquad \forall x\in S.
\end{align*}$$
To find a $\sigma$, at least locally, begin by extending $\varphi$ to a smooth function $\tilde\varphi$ in a neighbourhood of $S$ and choosing a smooth local defining function $\psi$ for $S$. Since $\sigma$ must agree with $d\varphi$ when restricted to $TS$, and the annihilator of $TS$ at each point is spanned by $d\psi$, the only possibility for $\sigma$ is a section of the form $\sigma = d \tilde\varphi + fd\psi$ for some unknown real-valued function $f$ defined in a neighbourhood of $S$. We can then inserte this into the equation $F(x, \sigma(x)) = 0$, and attempt to solve for the values of $f$ along $S$.

**Def:** The Cauchy problem$$\begin{align*}
F(x, du(x)) &= 0 \qquad \text{for all }x\in U, \\
u|_S &= \varphi
\end{align*} $$is said to be *noncharacterstic* if there exists a smooth section $\sigma \in \Gamma(T^*M|_S)$ that satisfies $$\begin{align*}
\sigma(x)|_{T_xS} &= d\varphi(x) \qquad \forall x\in S, \\
F(x, \sigma(x)) &= 0  \qquad\qquad \forall x\in S,
\end{align*}$$with the additional property if $(x^i)$ are any local coordinates on $M$ and $(x^1,\dots, x^n, \xi_1,\dots, \xi_n)$ are the corresponding natural coordinates on $T^*M$, the following vector field along $S$ is nowhere tangent to $S$: $$A^\sigma|_x = \frac{\partial F}{\partial\xi_1}(x, \sigma(x)) \frac{\partial}{\partial x^1} +\cdots +  \frac{\partial F}{\partial\xi_n}(x, \sigma(x)) \frac{\partial}{\partial x^n}.$$
This last condition is specifically considered to make that $\Gamma$ nowhere tangent to $X_F$, and we could use the Hamilton Flowout Theorem. 

**The Cauchy Problem for a Hamiltonian-Jacobi Equation:** Suppose $M$ is a smooth manifold, $W\subseteq T^* M$ is an open subset, $F: W \to \Bbb R$ is a smooth function, $S\subseteq M$ is an embedded hypersurface, and $\varphi: S \to \Bbb R$ is a smooth function. If the Cauchy problem $$\begin{align*}
\sigma(x)|_{T_xS} &= d\varphi(x) \qquad \forall x\in S, \\
F(x, \sigma(x)) &= 0  \qquad\qquad \forall x\in S
\end{align*}$$is noncharacteristic, then for each $p\in S$ there is a smooth solution defined on some neighbourhood of $p$ in $M$.

**Prop:** Suppose $$u|_S = \varphi $$is a noncharacteristic initial condition for a Hamilton-Jacobi equation $$F(x, du(x)) = 0 \qquad \text{for all }x\in U.$$For any choice of $\sigma S \to T^*\Bbb R^n$ satisfying $$\begin{align*}
\sigma(x)|_{T_xS} &= d\varphi(x)  \\
F(x, \sigma(x)) &= 0   \\
A^\sigma|_x &= \frac{\partial F}{\partial\xi_1}(x, \sigma(x)) \frac{\partial}{\partial x^1} +\cdots +  \frac{\partial F}{\partial\xi_n}(x, \sigma(x)) \frac{\partial}{\partial x^n}
\end{align*} $$for any $x\in $S$. Then there is a neighbourhood $U$ of $p$ on wich there is a *unique* solution to the Cauchy problem $$\begin{align*}
\sigma(x)|_{T_xS} &= d\varphi(x) \qquad \forall x\in S, \\
F(x, \sigma(x)) &= 0  \qquad\qquad \forall x\in S
\end{align*}$$satisfying $du(x) = \sigma(x)$ for all $x\in S$.

The proof gives us a way how to solve the this type of PDEs.

**Example:** 

**Def:** The classical *eikonal equation* for a real-valued function $u$ on an open subset $U\subseteq \Bbb R^b$ is $$\sum_{i = 1}^n\left(\frac{\partial u}{\partial x^i}\right)^2 = f(x), $$where $f(x)$ is a given smooth real-valued function on $u$. It plays an important role in the theory of optics. 

**Example:** We can consider the case of the eikonal equation where $f(x) = 1$ on an open subset of $\Bbb R^n$ with $u = 0$ on the unit sphere. We can use the spherical symmetry and note that the eikonal equation is really $$\|\nabla u\| ^2 = 1,$$and the sphere is a level set of $u$. Then we can use [[Change of Variable Theorem in Rn#Sphere in $n$ dimensions|spherical coordinates]], and get that  $$\left(\frac{\partial u}{\partial r}\right)^2 = \|\nabla u \|^2 = 1. $$Then we get that $$\frac{\partial u}{\partial r} = \pm 1.  $$We get the defining function of the sphere $\psi(r) = r- 1$. Then we can get that solutions to be $$u(x) = \pm (\|x\| -1 ).$$

**Example:** Consider the following problem in the plane: $$\frac{\partial u}{\partial x}- \left(\frac{\partial u}{\partial y}\right)^2 = 0, \qquad u(0, y) = y^2. $$The corresponding function on $T^*\Bbb R^2$ is $F(x, y, \xi, \eta) = \xi-\eta^2$, where we use $(x, y, \xi,\eta)$ to denote the natural coordinates on $T^*\Bbb R^2$ associated with $(x, y)$.

The initial manifold $S = \{(x, y) \mid x =0\}$ has $x$ as its defining function. Then we can look for the suitable $1$-form $\sigma$ we know it is of the form $$\sigma = d(y^2) + f(y)\,dx = 2y\, dy+  f(y)\, dx.$$If we solve the equation $F(0, y, f(y), 2y) = 0$, then we get that $f(y) =4y^2$, and set $\sigma(y) = 2y\, dy + 4y^2\, dx$. The vector field $A^\sigma$ is given by  $$A^\sigma|_{(x, y)} = \frac{\partial }{\partial x}-4y \frac{\partial}{\partial y}, $$which is never tangent to $S$.

The initial curve $S$ can be parametrised by $X(s) = (0, s)$, and therefore the initial curve $\Gamma\subseteq T^*\Bbb R^2$ can be parametrised by $\widetilde X(s) := \sigma(X(s)) = (0, s, 4s^2, 2s)$. The Hamiltonian field of $F$ is  $$X_F|_{(x, y, \xi, \eta)} = \frac{\partial}{\partial x} - 2\eta \frac{\partial}{\partial y}, $$and it is easy to solve the corresponding system of ODEs with initial condition $(x, y, \xi, \eta) = (0, s, 4s^2, 2s)$ to obtain the following parametrisation of $\cal S$: $$\Psi(t, s) = (t, s-4st, 4s^2, 2s). $$solving $(x, y) = (t, s(1-4t))$ for $(t, s)$ and inserting the formulas for $(\xi, \eta)$ we see that $\cal S$ is the image of the following $1$-form: $$\alpha =\frac{4y^2}{(1-4x)^2}\, dx+\frac{2y}{1-4x}\, dy. $$We can find the $\alpha = du$ on the set $\{(x, y) \mid x< 1/4\}$, where  $$u(x, y) = \frac{y^2}{1-4x}. $$
# General Nonlinear Equations

**Def:** If $M$ is a smooth manifold, the $1$-jet bundle of $M$ is a smooth vector bundle $J^1M := \Bbb R \times T^*M \to M$, whose fibre at $x\in M$ is $\Bbb R\times T_x^*M$. We can think of it as the Whitney sum of a trivial $\Bbb R$-bundle, with $T^*M$. If $u: M \to \Bbb R$ is a smooth function, the $1$-jet of $u$ is the section $j^1u: M \to J^1M$ defined by $$j^1u(x) = (u(x), du(x)).$$A point in the fibre $J^1M$ over $x\in M$ can be viewed as the first order Taylor polynomials at $x$ of a smooth function on $M$, represented invariantly as the values of the function and its differential at $x$.

**Def:** The *canonical contact form* on $J^1M$ is the $1$-form $\theta := dz-\tau$ defined, where $z$ is the standard coordiante on $\Bbb R$ and $\tau$ is the tautological $1$-form on $T^*M$. In terms of natural coordinates $(x^i, \xi_i)$ for $T^*M$, then form $\theta$ has the coordinate representation $$\theta = dz - \sum_{i = 1}^n \xi_i \, dx^i. $$A smooth, local or global, section $\eta:M \to J^1M$ is said to be *Legendrian* if its image is a Legendrian submanifold of $J^1M$, or equivalently if $\eta^*\theta = 0$.

**Prop:** Let $M$ be a smooth manifold. A smooth local section of $J^1M$ is the $1$-jet of smooth function iff it is Legendrian.

The $1$-jet bundle provides the most general setting in which to consider first-order partial differential equations. If $M$ is a smooth manifold, a first-order PDE for a function $u: M \to \Bbb R$ can be viewed as a real-valued function $F$ on the $1$-jet bundle of $M$, and a solution is a function whose $1$-jet takes its vales in the zero set of $F$.

Let $M$ be a smooth manifold, and suppose we are given a function $F\in\mathcal C^\infty(w)$ on some open subset $W\subseteq J^1M$, a smooth hypersurface $S\subseteq M$, and a smooth function $\varphi: S \to \Bbb R$. We wish to solve the following Cauchy problem for $u$, $$\begin{align*}
F(x,u(x), du(x)) &= 0  \\
u|_S &= \varphi.
\end{align*} $$This problem is said to be *noncharacterisitc* if there exists a smooth section $\sigma \in \Gamma(T^*M|_S)$ taking its values in $W$ and satisfying  $$ \begin{align*}
\sigma(x)|_{T_xS} &= d\varphi(x) \qquad \forall x\in S, \\
F(x, \varphi(x), \sigma(x)) &= 0  \qquad\qquad \forall x\in S,
\end{align*}$$and such that the following vector field along $S$ is nowhere tangent to $S$: $$A^{\varphi, \sigma}|_x =  \frac{\partial F}{\partial\xi_1}(x,\varphi(x),  \sigma(x)) \frac{\partial}{\partial x^1} +\cdots +  \frac{\partial F}{\partial\xi_n}(x, \varphi(x), \sigma(x)) \frac{\partial}{\partial x^n}.$$
**The General First-Order Cauchy Problem:** Suppose $M$ is a smooth manifold, $W\subseteq J^1M$ is an open subset, $F: W \to \Bbb R$ is a smooth function, $S\subseteq M$ is an embedded hypersurface, and $\varphi: S \to \Bbb R$ is a smooth function. If the Cauchy problem $$\begin{align*}
F(x,u(x), du(x)) &= 0  \\
u|_S &= \varphi
\end{align*} $$is noncharacterisitc, then for each $p\in S$ there is a smooth solution on some neighbourhood of $p$ in $M$. 