---
tags:
  - OrdinaryDifferentialEquations
---
Subjects: [[Ordinary Differential Equations]]
Links: [[Series Solutions of Linear Equations around Ordinary Points]], [[nth Order Linear Differential Equations]], 

We are going to investigate linear equations with variable coefficients

$$ \sum_{k = 0}^n a_k(x) y^{(k)} = 0 $$

we want to examine what happens when $a_k$ are analytic functions, and the point $x_0$ such that $a_n(x_0)= 0$, this is called a _singular point_ of the equation. It is dificult to determine the nature of the solutions in the vecinity of such singular points.

We are going to examamine a class of equations for which the singularity is “weak”, in the sense that modifying the method above will yeild solutions near singularities. We say that $x_0$ is a ********regular singular point******** if the equation above can be written in the form:

$$ \sum_{k = 0}^n b_k(x)(x-x_0)^k y^{(k)} = 0 $$

near $x_0$, with $b_n = 1$, and the functions $b_0, \dots, b_{n-1}$ are analytic at $x_0$. If the functions can be written in the form

$$ b_k = (x-x_0)^{n-k}\beta_k(x) \qquad \text{for }k =0, 1, \dots, n-1 $$

where $\beta_0, \dots, \beta_{n-1}$ are analytic at $x_0$, we see that the equation becomes

$$ \sum_{k = 0}^n \beta_k(x) y^{(k)} = 0 $$

after diving out $(x-x_0)^n$. Thus a generaliztion of the equation with analytic coefficients can be of the form

$$ \sum_{k = 0}^n c_k(x)(x-x_0)^k y^{(k)} =0 $$

has a regular singular point at $x_0$ if $c_0, c_1, \dots, c_n$ are analytic at $x_0$ and $c_n(x_0) \ne 0$, we can divide $c_n(x)$, for $x$ near $x_0$, to obtain that $b_k (x) = c_k(x)/c_n(x)$, and all the $b_k$ are analytic at $x_0$.