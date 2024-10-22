---
tags:
  - VectorAnalysis
  - DifferentialGeometry
---
Subjects: [[Vector Analysis]], [[Differential Geometry]]

Let $f:D\subseteq \Bbb R\to \Bbb R^n$, we can define coordinates of $f_i :D\subseteq \Bbb R\to \Bbb R^n$ such that:

$$ \begin{align*} f(t) &= \begin{pmatrix} f_{1}(t) \\ f_{2}(t) \\ \vdots \\ f_{n}(t) \end{pmatrix} \end{align*} $$

We can also define them as $f_i = \pi_i \circ f$, where $\pi_i$ is the $i$th projection of $\Bbb R^n$.

The image of the function $f:D\subseteq \Bbb R\to \Bbb R^n$, is just $\{f(t)\mid t \in D\} \subseteq \Bbb R^n$. The expressions for any $1\le i \le n$ of $x_i = f_i(t)$ is said to be a parametrization of the image of $f$ with parameter $t$.

While the graph of the function is the set ${\{(t, f_1(t), \dots, f_n(t)\mid t \in D\} =\{(t, f(t))\mid t\in D\}\subseteq \Bbb R^{n+1}}$

The graph of a function $f:D\subseteq \Bbb R\to \Bbb R^n$, can be considered as the image of a function ${f:D\subseteq \Bbb R\to \Bbb R^{n+1}}$, such that $f^*(t) =(t, f(t))$