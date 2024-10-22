---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]]

## Cauchy-Riemann Equations

A function $f:A\subseteq \Bbb C \to \Bbb C$ can be thought of $f(z)$ where $z$ is a single complex value or $f(x+iy)$ where it depends on two real values, and $f(x+iy) = u(x,y) +iv(x,y)$. This decomposition has many merits. In particular we have that if $z_0 = x_0 +y_0 i$

$$ \lim_{z\to z_0}f(z) = \lim_{(x, y) \to (x_0, y_0)} u(x,y) + i \lim_{(x, y) \to (x_0, y_0)} v(x,y) $$

the limit on the left exists iff the limits on the right exists. From this it is easy see that $f$ is continuous iff $u$ and $v$ are continuous.

********Def:******** Suppose $A$ is an open set in $\Bbb C$ and $f=u+iv:A \to \Bbb C$ is a given function. Then we say that $f$ differentiable in the real variable sense at $z_0 = x_0 +y_0i$, if the function $(u,v):\varphi[A] \to \Bbb R^2$ is differentiable at $(x_0, y_0)$, where $\varphi(x+yi) =(x,y)$. In other words, if the differential of $(u,v)$ exists at $(x_0, y_0)$. We can define the Jacobian matrix of $f$ as the Jacobian matrix of $(u,v)$

$$ J_f(z_0) = \begin{pmatrix} \partial_x u & \partial_y u \\ \partial_x v & \partial_y v \end{pmatrix}(x_0, y_0) $$

### Cauchy-Riemann Theorem

Suppose $A$ is an open set in $\Bbb C$ and $f=u+iv:A \to \Bbb C$ is a given function. Then $f'(z_0)$ exists iff $f$ is differentiable in the real variable sense and $x_0 +y_0i = z_0$, the function $u, v$ are $\cal C^1$ functions on $A$ and satisfy

$$ \frac{\partial u}{\partial x} = \frac{\partial v}{\partial y} \quad \text{ and } \quad \frac{\partial u}{\partial y} = -\frac{\partial v}{\partial x} $$

(called the _******Cauchy-Riemann Equations******_)

Thus, if $\partial_x u,\partial_y u, \partial_x v$ and $\partial_y v$ exists, and are continuous on $A$, and satisfy the Cauchy-Riemann equations, then $f$ is holomorphic on $A$.

If $f'(z_0)$ does exist, then

$$ \begin{align*} f'(z_0) &= \frac{\partial u}{\partial x}(x_0, y_0)+i \frac{\partial v}{\partial x}(x_0, y_0) = \frac{\partial f}{\partial x}(z_0) \\ \\ &= \frac{\partial v}{\partial y}(x_0, y_0) -i \frac{\partial u}{\partial y}(x_0, y_0) = \frac{1}{i}\frac{\partial f} {\partial y}(z_0) \end{align*} $$

This theorem can be proven directly, with a bit of work. Another way to prove it is by using the following lemma.

**************Lemma:************** A matrix

$$ \begin{pmatrix} a & b\\ c & d \end{pmatrix} $$

represents, under matrix multiplication, multiplication by a complex number iff $a=d$ and ${b=-c}$. The complex number in question is $a+ic = d-ib$.

By using this lemma and checking the Jacobian of $f$, then we get the Cauchy-Riemann equations.

### Polar Cauchy-Riemann Equations

Let $T:(-\pi,\pi)\times \Bbb R^+ \to \Bbb R^2$, given by $T(\theta, r) = r(\cos \theta, \sin\theta)$. ${\operatorname{Im}(T) = \Bbb R^2\{(x,0) \mid x \le 0\}}$. Let $f=u+iv :A\to \Bbb C$, where $A$ is an open set in $\Bbb C$. Then we can define

$$ \tilde u = u \circ T \quad \tilde v = v \circ T $$

Since $T$ is continuously differentiable, and has a continuously differentiable inverse, then we have the following equivalence:

$f$ is holomorphic on $A\setminus \{x+iy \mid y= 0, x \le 0\}$ iff $(\tilde u, \tilde v) :T^{-1}[A] \to \Bbb R^2$ is differentiable and

$$ \frac{\partial \tilde u}{\partial r} = \frac{1}{r} \frac{\partial \tilde v}{\partial \theta} \quad \text{ and }\quad \frac{\partial \tilde v}{\partial r} = \frac{-1}{r} \frac{\partial \tilde u}{\partial \theta} $$

on $T^{-1}[A]$.

******Prop:****** From this we can derive the Laplacian in spherical coordiates, let $f \in \cal C^2$

$$ \nabla^2 f =\frac{\partial^2f}{\partial r^2} + \frac{1}{r}\frac{\partial f}{\partial r} + \frac{1}{r^2} \frac{\partial^2 f}{\partial \theta^2} $$

**************Lemma:************** If $f:A\subseteq \Bbb C \to \Bbb C$ is holomorphic then

$$ \det J_f = |f'(z)|^2 $$
### Inverse Function Theorem

Let $f:A\to \Bbb C$ holomorphic and assume that $f'(z_0) \ne0$. Then there exists a neighborhood $U$ of $z_0$ and a neighborhood $V$ of $f(z_0)$ such that $f:U\to V$ is a bijection and its inverse $f^{-1}$ is holomorphic with derivative given by

$$ (f^{-1})'(f(z)) = \frac{1}{f'(z)} $$

This is proved using the [[Inverse Function Theorem in Rn]]

**********Prop:********** If $f:A\to \Bbb C$ is holomorphic and $f'(z) \ne0$ for all $z \in A$, then $f$ maps open sets in $A$ to open sets.