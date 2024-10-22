---
tags:
  - Analysis
  - OrdinaryDifferentialEquations
---
Subjects: [[Metric and Normed Spaces]], [[Ordinary Differential Equations]]
Links: [[Picard–Lindelöf theorem]], [[Existence of Solutions of First Order Differential Equations]]
Let $\Omega$ be an open set in $\Bbb R^n$, $\chi:(a,b) \times \Omega \to \Bbb R^n$ be a continuous function, $t_0 \in(a, b)$ and $x_0 \in \Omega$. The Cauchy problem

$$ \begin{cases} u'= \chi(t, u) \\ u(t_0) =x_0 \end{cases} $$

If we fix a $r>0$, such that

$$ [t_0-r, t_0+r]\subseteq (a,b) \quad \text{ and } \quad \overline B(x_0, r) \subseteq \Omega $$

Let’s consider

$$ K:= \{(t, x) \in \Bbb R\times \Bbb R^n\mid |t-t_0|\le r, \|x-x_0\|\le r\} $$

Let $M>0$, such that

$$ M>\max _{(t,x)\in K}\|\chi(t, x)\| $$

Let

$$ \delta:=\min\left\{r, \frac{r}{M}\right\} $$

The following lemma is important:

Given $\varepsilon>0$, there’s $u_\varepsilon\in {\cal C}^0([t_0-\delta, t_0+\delta], \Bbb R^n)$ with the following properties:

- $u_\varepsilon(t_0) = x_0$
- $\|u_\varepsilon(t) -x_0\|\le r$ for all $t \in[t_0-\delta, t_0+\delta]$
- $\|u_\varepsilon(t)-u_\varepsilon(s)\|\le M|t-s|$ if $s, t \in[t_0-\delta, t_0+\delta]$
- There’s a finite subset $F_\varepsilon$ of $(t_0-\delta, t_0+\delta)$ such that $u_\varepsilon$ is continuously differentiable on $(t_0-\delta, t_0+\delta) \setminus F_\varepsilon$ and

$$ \|u_\varepsilon'(t) -\chi(t, u_\varepsilon(t))\|<\varepsilon \qquad \forall t\in (t_0-\delta, t_0+\delta) \setminus F_\varepsilon $$

## Peano Existence Theorem
Let $\Omega$ be an open set of $\Bbb R^n$ and $\chi:(a,b)\times \Omega \to \Bbb R^n$ be a continuous function. Then, for every $(t_0, x_0) \in (a, b)\times \Omega$, there’s a $\delta>0$ such that the Cauchy problem

$$ \begin{cases} u'= \chi(t, u) \\ u(t_0) =x_0 \end{cases} $$

has at least one solution on the interval $[t_0-\delta, t_0+\delta]$

This proof relies on the [[Arzelà–Ascoli Theorem]]

This theorem is really important theorem that guarantees the solution to certain Cauchy problems, while having weaker hypothesis than the Picard-Lindelöf Theorem.

There’s a theorem that functions as a generalisation to this one being that shows the existence of solutions with even weaker conditions, that being the [[Carathéodory's Existence Theorem]]