---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Second Order Euler Equation]], [[nth Order Linear Differential Equations]]

The Cauchy-Euler equation is of a linear $n$th order differential equation of the form

$$L[y]=\sum_{k = 0}^n a_k x^k y^{(k)} = 0 $$

The way of solving it is by substituting $x = e^u$, then this will help reduce it to a $n$th order linear differential equation with constant coefficients. Alternatively, the trial solution $y = x^m$ may be used to directly solve for the basic solutions.

If we try the solution of the form $y = x^r$, then we get a polynomial $q (r)$, such that

$$ L[|x^r|] = q(r)|x^r| $$

If we try to solve who is $q(r)$, we get that

$$ q(r) = \sum_{k = 0}^n a_k (r)_n $$

with $(r)_n$ being the falling factorial. This polynimial is called the _******indical polynomial******_ of the Euler equation. Differentiating $k$ times with respect to $r$ we obtain that

$$ \frac{\partial ^k }{\partial r^k} L[|x^r|] = L\left[\frac{\partial ^k }{\partial r^k} |x^r|\right] = L[x^r\ln^k |x|] $$

This is equal to

$$ \frac{\partial ^k }{\partial r^k} [q(r)|x^r|]=\left[\sum_{m = 0}^k {k\choose m}q^{(m)}(r) \ln^{k-m}|x|\right] |x|^r $$

if $r_1$ is a root with multiplicity of $m_1$, then

$$ q^{(k)}(r_1) =0 \qquad \text{for }k =0, 1, \dots, m_1-1 $$

then we know that

$$ |x|^{r_1} \ln^k|x| \qquad \text{for }k =0, 1, \dots, m_1-1 $$

are solutions to $L[y] =0$. Repeating this process for each root in $q$ we obtain that

******Th:****** Let $r_1, \dots, r_s$ be distinct roots of the indical polynomial $q$ for an Euler-Cauchy equation, and suppose $r_i$ has multiplicity $m_i$. Then the functions

$$ |x|^{r_i} \ln^k|x| \qquad \text{for }k =0, 1, \dots, m_i-1 $$

for $i=1, \dots, s$

form a basis for the solutions of the $n$th order Euler-Cauchy equation on any interval not contaning $x = 0$