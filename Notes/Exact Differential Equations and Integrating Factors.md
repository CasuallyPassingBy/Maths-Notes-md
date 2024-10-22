---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Separable Differential Equations]], [[First Order Differential Equations]]

**********Def:********** Let $M, N:U\subseteq \Bbb R^2 \to \Bbb R$ that are $\cal C^1$, and $U$ is an open set then the differential equation

$$ M(x,y)+N(x,y)y' =0 $$

is called _**exact**_. We are looking for $\psi:U\subseteq \Bbb R^2 \to \Bbb R$ such that $\partial _x \psi = M$ and $\partial _y\psi = N$, and $y = \phi(x)$, such that

$$ \frac{d}{dx}\psi(x, \phi(x)) = M(x,y) +N(x,y)y' = 0 $$

the solutions are given implicitely with $c \in \Bbb R$ being an arbitrary constant

$$ \psi(x,y) = c $$

### Existence of Solution

Let $M, N:U\subseteq \Bbb R^2 \to \Bbb R$ that are $\cal C^1$, and $U$ is a simply connected set. Then the equation

$$ M(x,y)+N(x,y)y' =0 $$

is an exact differential equation on $U$ iff

$$ \frac{\partial \psi}{\partial x}=M(x, y) \quad \text{and} \quad \frac{\partial \psi}{\partial y} =N $$

That is, there exists a function $\psi:U \to \Bbb R$, such that iff

$$ \frac{\partial M}{\partial y} = \frac{\partial N}{\partial x} $$

### Method in a Rectangle

We want to construc $\psi$ that satisfies

$$ \frac{\partial \psi}{\partial x}=M(x, y) \quad \text{and} \quad \frac{\partial \psi}{\partial y} =N $$

The way we do it is by constructing is we set $\psi (x, y) = Q(x, y) +h(y)$, where $h(y)$ is similar to a constant of integration with respect to $x$, and $Q(x, y)$ is defined as

$$ Q(x, y) = \int M(x, y) \, dx $$

We defien $\psi$ in this way such that $\partial_x \psi = M(x, y)$. We need to check $\partial _y \psi$

$$ \frac{\partial \psi}{\partial y}(x,y )= \frac{\partial Q}{\partial y}(x,y) +h'(y) = N(x,y) $$

Then we solve for

$$ h'(y) = N(x,y) -\frac{\partial Q}{\partial y}(x,y) $$

Finally for determining the $c \in \Bbb R$, we just need to check the initial conditions since we get that $\psi(x, y) = c$, then we finally get $\psi(x, y) = \psi(x_0, y_0)$

## Integrating Factors

Sometimes we can transform a differential equation that isn’t exact into an exact one, by multiplying an integration factor $\mu = \mu(x, y)$, then get

$$ \mu M+\mu Ny' =0 $$

We must will assume that this equation is exact, meaning we assume this equality

$$ \frac{\partial}{\partial y} \mu M = \frac{\partial }{\partial x} \mu N $$

rearrenging we get the following partial differential equation

$$ M \frac{\partial \mu}{\partial y} -N \frac{\partial \mu}{\partial x} + \left(\frac{\partial M}{\partial y} - \frac{\partial N}{\partial x}\right)\mu =0 $$

This is a really complicated thing to solve, mainly because it can has more than one solution. There are couple of typical simplifications. The main one is assuming that $\mu$ is only dependent of one variable. There are two cases

If we assume that $\mu = \mu(x)$, then we only need to check that the function

$$ R=\frac{\partial_y M -\partial_x N}{N} $$

is only dependent of $x$. If it isn’t that integration factor doesn’t work. If it is then

If we assume that $\mu = \mu(y)$, then we only need to check that the function

$$ R = \frac{\partial_x N -\partial _y M}{M} $$

is only dependent of $y$. If it isn’t that integration factor doesn’t work. If it is then

A more general way to solve find the integration factor is by making $\mu = \mu (\omega)$, where $\omega$ is a function from $\Bbb R^2$ to $\Bbb R$, and omega being a function from $\Bbb R$ to $\Bbb R$. Then we need to check that

$$ R = \frac{\partial _y M -\partial_x N}{N \partial_x \omega -M \partial_y \omega} $$

and try to find $\omega$ such that $Q$ is only a function of $\omega$, but if we found it then

We only have the equation

$$ \mu' = R \mu $$

which is easy to solve.

Once we have found the integration factor we know it is an exact differential equation, and we solve it as such.