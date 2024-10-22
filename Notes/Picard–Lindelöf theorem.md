---
tags:
  - OrdinaryDifferentialEquations
  - Analysis
---
Subjects: [[Metric and Normed Spaces]], [[Ordinary Differential Equations]]
Links: [[Space of Continuous Functions From Rn to Rm]], [[First Order Differential Equations]], [[Complete Metric Spaces]]
### Contraction Mapping Theorem in $\mathcal C_b(A, \Bbb{R}^n)$

Let $T: \mathcal C_b(A, \Bbb{R}^n) \to \mathcal C_b(A, \Bbb{R}^n)$ be given a mapping such that there is a constant $\lambda$ , ${0 \le \lambda < 1}$ with

$$ \| T(f) - T(g) \| \le \lambda \|f-g\| $$

for all $f,g \in \mathcal C_b(A, \Bbb{R}^n)$. Then $T$ (is continuous and) has a unique fixed point; that is there is a unique point $f_0 \in \mathcal C_b(A, \Bbb{R}^n)$ such that $T(f_0) = f_0$. This is a special case of [[Banach's Fixed Point Theorem]]

### Integral Equation

********Th:******** If $\sup_{x \in [0, r]} \int_0^x |k(x,y)|\,dy = \lambda <1$ then the following equation

$$ f(x) = a +\int_0^xk(x,y)f(y) \, dy $$

has a unique solution on $[0, r]$. This looks similar to a [[Volterra Integral Equation of the Second Kind]]


We need that $\Omega$ is an open set in $\Bbb R^n$, 
A **************solution to the Cauchy problem***************

$$ \begin{cases} u' = \chi(t, u), \\ u(t_0) = x_0 \end{cases} $$

is a continuously differentiable function $u:J \to \Omega$, defined on the sub interval of $(a,b)$ that contains $t_0$, and that satisfies

$$ u '(t) = \chi(t, u(t))\quad \forall t\in J, \qquad u(t_0) = x_0 $$

and the point $(t_0, x_0)$ is called the ********initial condition******** of the problem. We are going to use component wise integration as in the integrals of vector valued function of R

We need lemma: Let $u:[t_0-\delta, t_0+\delta]\to \Omega$ is a solution to the Cauchy problem above iff $u$ satisfies

$$ u(t) =\int_{t_0}^t\chi(s, u(s))\, ds+x_0 $$

We say that $\chi:(a,b) \times \Omega \to \Bbb R^n$ is ******************************locally Lipschitz continuous on the second variable****************************** if for each $t_0 \in (a, b)$ and $x_0 \in \Omega$, there exist $\delta>0$ and $C>0$ (dependent on $t_0$ and $x_0$) such that ${[t_0-\delta, t_0+\delta]\subseteq (a,b)}$, $\overline B(x_0, \delta) \subseteq \Omega$ and

$$ \|\chi(t, x_1) - \chi(t, x_0)\| \le C \|x_1 -x_2\| \quad \text{if }|t-t_0|\le \delta \text{ and }x_1, x_2 \in \overline B(x_0, \delta) $$

We will supose that $\chi$ is locally Lipschitz continuous on the second variable, for the rest of this section. For the initial condition $(t_0, x_0)$ we choose $\delta_0>0$ and $C >0$, and we will choose ${M\ge 1}$ such that

$$ \|\chi(t, x)\| \le M \qquad \forall (t, x)\in [t_0-\delta_0, t_0+\delta_0]\times \overline B(x_0, \delta_0) $$

We will choose $0<\delta < \min\{\frac{1}{C}, \frac{\delta_0}{M}\}$

We will we define the set

$$ X:= \{ u\in {\cal C}^0([t_0 -\delta, t_0 + \delta], \Bbb R^n)\mid \|u-x_0\|_\infty \le \delta M\} $$

where $x_0$ represents the constant function with value $x_0$, and

$$ \|u\|_\infty = \max_{t \in [t_0-\delta, t_0+\delta]}\|u(t)\| $$

since ${\cal C}^0([t_0 -\delta, t_0 + \delta], \Bbb R^n)$ is a Banach space, with the uniform norm. Then we have that

- $X$ is a complete metric space
- If $u \in X$, then $u(t)\in \Omega$ for all $t \in [t_0 -\delta, t_0+\delta]$

Let $u \in X$, then we will define $\phi(u) : [t_0-\delta, t_0+\delta] \to \Bbb R^n$ as

$$ \phi(u)(t) := \int_{t_0}^t \chi(s, u(s))\, ds + x_0 $$

We get that if $u \in X$, then is also $\phi(u)\in X$

## Picard-Lindelöf Theorem

Let $\chi:(a,b)\times \Omega\to \Bbb R^n$ be a function that is locally Lipschitz in the second variable. Then given $t_0\in (a,b)$ and $x_0\in \Omega$, there’s $\delta>0$ such that the Cauchy Problem

$$ \begin{cases} u' = \chi(t, u), \\ u(t_0) = x_0 \end{cases} $$

has a unique solution on the interval $[t_0-\delta, t_0+\delta]$.

The proof, involves showing that $\phi:X\to X$ is a contraction, and by completeness we have that there’s a unique fixed point. Given one of the lemmas a above, the solution to the problem is the fixed point of $\phi$.

### Picard Iterative Method
Since the proof relies on the [[Banach's Fixed Point Theorem]], we can use the a sequence to approximate a solution to the differential equation defined recursively:

$$ \begin{dcases} x_1(t) = x_0 &\text{(Initial Conditions)} \\ x_{n+1} (t) = x_0 + \int_{t_0}^t f(s, x_{n}(s))\, ds \end{dcases} $$

A weaker version that only says if a Cauchy problem has at least one solution is [[Peano Existence Theorem]], with slightly less strong hypotheses.