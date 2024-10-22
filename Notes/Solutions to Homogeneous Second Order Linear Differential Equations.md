---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Link: [[Second Order Linear Differential Equations]], [[Solutions to Homogeneous nth Order Linear Differential Equations]]
**********Def:********** Let $p, q: I = (\alpha, \beta) \to \Bbb R$ be continuous functions. Then we can define the differential operator $L : \mathcal{C}^\infty(I, \Bbb R) \to \mathcal C^\infty(I, \Bbb R)$, defined as

$$ L[\phi] = \phi''+p\phi' +q\phi $$

We can write $L$ as $L = D^2 +pD+q$, where $D$ is the derivative operator. Then we can write the differential equation $y'' +py'+qy =0$, simply as $L[y] = 0$, with the corresponding initial conditions

$$ y(t_0) = y_0 \quad y'(t_0) = y'_0 $$

### Existence and Uniqueness Theorem

Consider the initial value problem

$$ y'' +py'+qy =g, \quad y(t_0) = y_0, \quad y'(t_0) = y_0' $$

where $p$, $q$ and $g$ are continuous functions on an open interval $I$ that contains the point $t_0$. Then theres exactly one solution $y = \phi(t)$ of this problem, and the solution exists throughout the interval $I$.

### Principal of Superposition

If $y_1$ and $y_2$ are two solutions of the differential equation

$$ L[y] =y'' +py'+qy = 0 $$

then the linear conmbination $c_1y_1+c_2y_2$ is also a solution for any values of the constants $c_1$ and $c_2$.

### Wronskian

Let $y_1$ and $y_2$ be differentiable functions, then we can define the _********Wronskian or Wronskian Determinant********_, of $y_1$ and $y_2$ as

$$ W(x)=\det \begin{pmatrix} y_1(x) &y_2(x) \\ y_1'(x) &y_2'(x) \end{pmatrix} = y_1y_2'-y_1'y_2 $$

Sometimes noted as $W(y_1, y_2)(x)$ or $W(x)$, and

$$ W'(x)=\det \begin{pmatrix} y_1(x) &y_2(x) \\ y_1''(x) &y_2''(x) \end{pmatrix} = y_1y_2''-y_1''y_2 $$

### Abel’s Theorem

If $y_1$ and $y_2$ are solutions of the differential equation

$$ L[y] = y''+py'+qy=0 $$

where $p$ and $q$ are continuous on an open interval $I$, then $W(y_1, y_2)$ is given by

$$ W(y_1, y_2)(x) = c\exp\left(-\int p(x) \, dx\right) = W(y_1, y_2)(t_0) \exp\left(-\int_{t_0}^t p(s)\, ds\right) $$

where $c$ is a certain constant that depends on $y_1$ and $y_2$, but not $x$. Further, $W(y_1, y_2)$ either is zero for all $x$ in $I$ (if $c = 0$) or else is never zero in $I$ (if $c\ne 0$)

**********Cor:********** Suppose $y_1$ and $y_2$ are two solutions to

$$ L[y] = y''+py'+qy=0 $$

and that the initial conditions

$$ y(t_0) =y_0 \quad y'(t_0) = y_0' $$

are assigned. Then it is always possible to choose the constants $c_1$ and $c_2$ so that

$$ y = c_1 y_1+c_2y_2 $$

satisfies the differential equation and the initial conditions iff $W(y_1, y_2)(t_0) \ne 0$.

**********Th:********** Suppose $y_1$ and $y_2$ are two solutions to

$$ L[y] = y''+py'+qy=0 $$

Then the family of solution $\operatorname{span}\{y_1, y_2\}$ over $\Bbb R$, includes every solution of $L[y] = 0$ iff there’s a point $t_0$ where $W(y_1, y_2)(t_0) \ne 0$.

This tells us that the [[Null Space and Range|null space]] of $L$ is two dimensional, and our equation is of second order, and $\{y_1, y\}$ are the basis for $N(L)$

**********Def:********** We say that the solutions $y_1$ and $y_2$ are said to form a _****fundamental set of solutions****_ iff their Wronskian is nonzero.

********Th:******** Consider the differential equation

$$ L[y] = y''+py'+qy=0 $$

where $p$, $q$ and $g$ are continuous functions on an open interval $I$ . Choose $t_0 \in I$. Let $y_1$ be the solution that satisfies the initial conditions

$$ y(t_0) = 1\qquad y'(t_0) =0 $$

and let $y_2$ be the solution that satisfies the initial conditions

$$ y(t_0) = 0\qquad y'(t_0) =1 $$

Then $y_1$ and $y_2$ form a fundamental set of solutions, which form a [[Bases and Dimension|basis]] of the space of solutions

An interesting theorem, we get that if $\phi$, be a non-trivial solution to the differential equation 

$$
y'' + \alpha (x) y =0
$$
on $a< x< b$, and let $\psi$ be  a non-trivial solution to the differential equation 

$$
y'' + \beta(x)y =0
$$
on $a < x < b$. Here $\alpha$, $\beta$ are real valued continuous functions. Suppose that 
$$
\beta(x) > \alpha (x) \qquad (a < x< b)
$$
If $x_1$ and $x_2$ are successive zeros of $\phi$ on $a < x< b$, then $\phi$ must vanish at some point $\xi$, $x_1 < \xi <x_2$.
