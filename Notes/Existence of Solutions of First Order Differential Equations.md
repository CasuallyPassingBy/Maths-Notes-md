---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Picard–Lindelöf theorem]], [[First Order Differential Equations]], [[First Order Linear Differential Equations]]
### Existence Theorem

Let $f$ be a continuous real valued function on the rectangle ${R= [x_0-a,x_0+a]\times[y_0-b, y_0+b]}$, and let $\|f\| \le M$. Let $f$ be Lipschitz continuous with a Lipschitz constant $K$ in $R$. Then the succesive approximations

$$ \phi_0 = y_0, \quad\phi_{k+1}(x) = y_0 + \int_{x_0}^xf(t, \phi_k(t))\, dt $$

converge on the interval $I= [x_0-\alpha, x+ \alpha]$, with $\alpha = \min\{a, b/M\}$ to a solution $\phi$ of the initial value problem

$$ y' = f(x, y) \quad y(x_0) =y_0 $$

on $I$.

****************Th:**************** The $k$th succesive approximation of the Picard iteratives $(\phi_k)$ to the solution $x$ of the initial value problem satisfies

$$ \|\phi-\phi_k\| \le \frac{M}{K}\frac{(K\alpha)^{k+1}}{(k+1)!}e^{K\alpha} $$

### Non-local Existence of Solutions

Let $S=[x_0-a, x_0+a] \times \Bbb R$, and $f:S \to \Bbb R$ be Lipschtiz continuous with constant ${K>0}$. The succesive approximations $(\phi_k)$ for the problem

$$ y' = f(x, y) \quad y(x_0) =y_0 $$

exists on the entire interval $[x_0-a, x_0+a]$, and converge there to solution $\phi$ of the initial value problem.

************Cor:************ Suppose $f:\Bbb R^2 \to \Bbb R$ be a continuous function on the plane which satisfies the Lipschitz condtion on the strip $S_a =[-a, a] \times \Bbb R$, where $a>0$. Then every initial value problem

$$ y' = f(x, y) \quad y(x_0) =y_0 $$

has a solution which exists for all $x$

### Approximations and uniqueness

Let $f, g$ be continuous functions on ${R= [x_0-a,x_0+a]\times[y_0-b, y_0+b]}$, and suppose $f$ satisfies the Lipschitz condition with a Lipschitz constant $K$. Let $\phi$ and $\psi$ be solutions of

$$ y' = f(x, y) \quad y(x_0) =y_1 \\ y' = g(x, y) \quad y(x_0) =y_2 $$

respectively on an interval $I$ containing $x_0$, with graphs contained in $R$. Additionally $\|f-g\| \le \varepsilon$ on $R$, and $|y_1-y_2| \le \delta$. Then

$$ |\phi(x)-\psi(x)| \le \delta e^{K|x-x_0|} + \frac{\varepsilon}{K}(e^{K|x-x_0|}-1) $$

for all $x$ in $I$.

**********Cor (Uniqueness Theorem):********** Let $f$ be continuous and satisfy a Lipschitz conditions on $R$. If $\phi$ and $\psi$ are solutions of

$$ y' = f(x, y) \quad y(x_0) =y_0 $$

on an interval $I$ containing $x_0$, then $\phi = \psi$ on $I$.

**********Cor: :********** Let $f$ be continuous and satisfy a Lipschitz conditions on $R$. Let $(g_k)$ be a sequence continuous functions on $R$, such that

$$ \|f-g_k \| \le \varepsilon_k $$

and $\psi_k$ be the solution to the initial value problem on the interval $I$ containing $x_0$

$$ y' = g_k(x, y) \quad y(x_0) =y_k $$

and $\phi$ be the solution to the initial value problem on the interval $I$ containing $x_0$

$$ y' = f(x, y) \quad y(x_0) =y_0 $$

and $|y_k -y_0| \le \delta_k$. If $\varepsilon_k , \delta_k \to 0$ as $k \to \infty$. Then $\psi \to \phi$ on $I$.

<aside> 💡 The Coddington Thereoms are true for complex value functions.

</aside>