---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Continuity on Metric Spaces]], [[Functional Limits in R]], [[Limits and Continuity of real valued functions of Rm]], [[Limits and Continuity of Vector valued functions of Rn]]

Let $X$, $Y$ be metric spaces, and $A$ be a subset of $X$, $f:A \to Y$ be a function, $x_0 \in \overline A$ and $y_0 \in Y$, we say that 
$$
\lim_{x \to x_0} f(x) = y_0
$$
if for any $\varepsilon >0$, there's $\delta>0$ such that
$$
\forall x \in A[0<d_X(x, x_0) < \delta \implies d_Y(f(x), y_0)]
$$
This actually connects to a lot, to the limits in $\Bbb R^n$ to $\Bbb R^m$. 

We get that $\lim\limits_{x \to x_0}f(x) = f(x_0)$, then $f$ is continuous at $x_0$. 