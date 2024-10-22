---
tags:
  - ComplexAnalysis
  - "#PartialDifferentialEquations"
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[Harmonic Functions]]

We can think of the set of all harmonic functions on $U$, denoted as $a(U)$, maybe $h(U)$, then $u\in a(U)$ is the same as, $u: U \subseteq \Bbb C \to \Bbb R$ is harmonic

**Prop:** If $f=u+iv:A\to \Bbb C$ is holomorphic on $A$, and $A$ is an open set of $\Bbb C$, then $u$ and $v$ are harmonic on $A$.

**Def:** Let $u$ and $v$ be real valued functions defined on an open subset $A$ of $\Bbb R^2$, then we call $v$ the **harmonic conjugate of $u$**, if the function $f =u+iv$ is holomorphic on $A$.

**Prop:** Let $u$ and $v$ be harmonic conjugates on a region $A$. Suppose that the equations

$$ u(x,y) =c_1 \quad\text{ and }\quad v(x, y) =c_2 $$

define smooth curves. Then these curves intersect orthogonally.

## Harmonic Functions and Harmonic Conjugates

Let $A$ be a region in $\Bbb C$ and let $u$ be twice differentiable harmonic function on $A$. Then $u$ is $\cal C^\infty$, and in a neighbourhood of each $z_0 \in A$, $u$ is the real part of some holomorphic function. We can calculate the harmonic conjugate, when the region is a ball, around $z_0$ or it is all of $\Bbb C$. We get that $v$ is of the form:
$$
v = \int_{y_0}^y \frac{\partial u}{\partial x} (x, t)\, dt - \int_{x_0}^x \frac{\partial u}{\partial y}(t, y)\, dt
$$

this means, that locally every harmonic function has a conjugate

If $A$ is a simply connected, there is an holomorphic function $f$ on $A$ such that $\Re (f) = u$

Let $u \in a(U)$, and $f:W\subseteq \Bbb C \to \Bbb C$ analytic on $W$, with $f[W] \subseteq U$, then $u \circ f \in a(W)$. 

This gives us the corollary that the linear combination of harmonic functions is harmonic. Thus $a(U)$ is a vector space. 

Let $u\in a(U)$. If $\text{int}(Z(u)) \ne \varnothing$, then $u \equiv 0$. Where $Z(u) := \{z \in U \mid u(z) = 0\}$  

Let $u, v \in a(U)$, and $D = \{z \in  U \mid u(z) = v(z)\}$. If $\text{int}(D) \ne \varnothing$, then $u = v$

### Mean Value Property

Let $u: U \subseteq \Bbb C \to \Bbb C$  continuous, we say that $u$ has the mean value property on $U$ if for any $a \in U$, and any $r>0$ such that $\overline{B_r(a)} \subseteq U$, it follows that
$$
u(a) = \frac{1}{2\pi} \int_0^{2\pi} u(a+re^{it})\, dt
$$
Let $u$ be harmonic on a region then $u$ has the mean value property

Let $u : U \subseteq \Bbb C \to \Bbb R$ with the mean value property if there's $a\in U$ such that for all $z \in U$ we have that $u(z) \le u(a)$, then $u$ is constant. 

Let $u : U \subseteq \Bbb C \to \Bbb R$ with the mean value property if there's $a\in U$ such that for all $z \in U$ we have that $u(z) \ge u(a)$, then $u$ is constant. 

Let $U\subseteq \Bbb C$ a bounded region and $u:\overline U\subseteq \Bbb C$ be continuous with the mean value property on $U$, such that $u|_{\partial U} \equiv 0$, then $u \equiv 0$
### Local Maximum Principle
Let $u$ be harmonic on a region $A$. Suppose that $u$ has a relative maximum on $z_0 \in A$ (that is, ${u(z) \le u(z_0)}$ for $z$ near $z_0$). Then $u$ is constant in a neighborhood of $z_0$. 

### Global Maximum Principle
Suppose $A \subseteq \Bbb C$ is an open, connected and bounded set. Let $u: \operatorname{cl}(A) \to \Bbb R$ be continuous and harmonic on $A$ and let $M$ be the maximum of $u$ on $\partial A$. Then

- $u(x, y) \le M$ for all $(x, y) \in A$
- If $u(x,y) = M$ for some $(x,y) \in A$, then $u$ is constant on $A$

We can also deduce the Minimum Principle, getting that if $m$ is a minimum of $u$ on $\partial A$. Then

- $u(x, y) \ge m$ for $(x,y) \in A$
- If $u(x,y) = m$ for some $(x,y) \in A$, then $u$ is constant on $A$

********Def:******** Let $A$ be an open bounded region and let $u_0$ be given continuous function on $\partial A$. Finding the real-valued function $u$ on $\operatorname{cl}(A)$ that is continuous on $\operatorname{cl}(A)$ and harmonic on $A$ and that equals $u_0$ on $\partial A$. This is called ***Dirichlet Problem****.

To find a solution to the Dirichlet Problem on a disk we use:

### Poisson’s Formula
Let $u:\overline{B_r(0)}\subseteq \Bbb C \to \Bbb R$ continuous, and $u \in a(B_r(0))$, then for all $a \in B_r(z)$ it satisfies
$$
u(a) = \frac{1}{2\pi i}\oint_{|z| =r} \frac{r^2-|a|^2}{|z-a|^2}\frac{u(z)}{z}\, dz = \frac{1}{2\pi i} \oint_{|z| = r} \Re\left(\frac{z+a}{z-a}\right) \frac{u(z)}{z}\, dz
$$

This is called Poisson's Formula 

Assume that $u$ is defined and continuous on the closed disk $\{ z \mid |z|\le r\}$ and is harmonic on the open disk $B_r(0)$. Then for $\rho < r$, we have that the **real form of Poisson’s Formula**

$$ u (\rho e^{i\phi})= \frac{r^2-\rho^2}{2\pi} \int_0^{2\pi} \frac{u (re^{i \theta})}{r^2-2r\rho \cos(\theta+\phi)+\rho^2}\, d\theta $$

which is equivalent to the **complex form of Poisson’s Formula**

$$ u (z) = \frac{1}{2\pi} \int_0^{2\pi} u(re^{i\theta})\frac{r^2-|z|^2}{|re^{i\theta}-z|^2}\, d\theta $$

in the special case that $r =1$, then $$u (\rho e^{i\phi})= \frac{1-\rho^2}{2\pi} \int_0^{2\pi} \frac{u (re^{i \theta})}{1-2\rho \cos(\theta-\phi)+\rho^2}\, d\theta $$
This exactly the same result as when we examine the problem using [[Laplace's Equation on the disk|Fourier Analysis]]

# Dirichlet Problem
The Dirichlet problem is a boundary problem for the partial differential equation, $U$ be a region, and $\varphi:\partial U \to \Bbb R$ be continuous, then the problem is to find $u: \overline U \to \Bbb R$  be continuous and $\nabla^2 u =0$ on $U$, and $u|_{\partial U} = \varphi$. This is really difficult to solve in general, but we can solve it for balls.

Let  $D= B_1(0)$, if $\varphi:\partial D \to \Bbb R$ be continuous on $\partial D$, then $f:D \to \Bbb C$ defined as
$$
f(z) = \frac{1}{2\pi i}\oint_{|w| =1}\frac{w+z}{w-z}\frac{\varphi(w)}{w}\, dw
$$
$f$ is analytic on $D$ and $P_\varphi(z) := \Re(f(z))$ is called the Poisson Integral of $\varphi$.
$$
\Re(f(z)) =  \frac{1}{2\pi i}\oint_{|w| =1}\Re\left(\frac{w+z}{w-z}\right)\frac{\varphi(w)}{w}\, dw
$$
### Schwarz Theorem
Let $D= B_1(0)$, $\varphi:\partial D \to \Bbb R$ is continuous on $\partial D$. Then there exists a unique function $u:\overline D \to \Bbb R$ continuous on $\overline D$ and 
- $u|_{\partial D} = \varphi$
- $u \in a(D)$
This $u$ is given by:
$$
u(z) = \begin{cases}
\varphi(z) & z \in \partial D\\
P_\varphi (z) & z\in D
\end{cases}
$$
Let $U = B_r(a)$ , if $\varphi:\partial U\to \Bbb R$ continuous. Then there exists a unique function $u:\overline D \to \Bbb R$ continuous on $\overline D$ and 
- $u|_{\partial U} = \varphi$
- $u \in a(U)$

Let $u:U\subseteq\Bbb C\to \Bbb R$ continuous with the mean value property. Then $u\in a(U)$. 

### Harnack's Inequality
Let $u: \overline{B_R}(a)\subseteq \Bbb C \to \Bbb R$  continuous and $u \in a(U)$ , with $u \ge 0$. if $0\le r < R$ and $\theta \in [0, 2\pi]$ , then 
$$
\frac{R-r}{R+r} u(a) \le u(a+re^{i\theta}) \le \frac{R+r}{R-r}u(a)
$$
## Dirichlet Problem for the Upper Half plane
Let $U(t)$ be a function defined for all $t\in \Bbb R$, piecewise continuous and bounded. Then the function 
$$
P_U(x+iy) = \frac{1}{\pi} \int_{-\infty}^\infty \frac{y}{(x-t)^2+y^2}U(t)\, dt
$$
represents a bounded harmonic function on the upper half plane, such that if $t_0 \in \Bbb R$ is a point of continuity of $U$, then 
$$
\lim_{z\to t_0} P_U(z) = U(t_0)
$$
Then we have two bounded continuous functions on the closed upper half plane, and harmonic on the upper half plane, and the have the same values on the real line, then they are equal.

An unbounded harmonic function on the upper half plane is $u(x, y) =y$, that also is equal to $0$ at the real line.