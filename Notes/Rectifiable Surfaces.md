---
tags:
  - VectorAnalysis
  - DifferentialGeometry
---
Subjects: [[Vector Analysis]], [[Differential Geometry]]
Links: [[Intro to Surfaces]], [[Rectifiable Curves in Rn]] 

********Def:******** Let $f:R =[a, b]\times [c,d] \to \Bbb R^n$, with $n \ge 3$. Let $\cal P$ be a partition of $R$, then we will define polyhedral approximation of the surface area as

$$ \text{A}(f, \mathcal P) = \sum_{i = 1}^k\sum_{j = 1}^m\|(f(x_i, y_{j-1}) - f(x_{i-1}, y_{j-1}) ) \wedge (f(x_{i-1}, y_j) -f(x_{i-1}, y_{j-1}) )\| $$

then the area of $f$ is

$$ \text{A} (f) = \sup_{\mathcal P \in \wp} A (f, \cal P) $$

If $A(f) < \infty$ then we say that $f$ is rectifiable
Conjecture:************ Let $f:R =[a, b]\times [c,d] \to \Bbb R^n$, with $n \ge 3$, and $f$ be $\cal C^1$. Then $f$ is rectifiable and

$$ \text{A}(f) = \int_R \left\|\frac{\partial f}{\partial x} \wedge \frac{\partial f}{\partial y}\right\| $$

Attempt:

Let $f \in \mathcal C^1(R)$, then $\partial_xf$ and $\partial_y f$ are uniformly continuous. and let $\cal P \in \wp$, then

$$ \text{A}(f, \mathcal P) = \sum_{i = 1}^k\sum_{j = 1}^m\|(f(x_i, y_{j-1}) - f(x_{i-1}, y_{j-1}) ) \wedge (f(x_{i-1}, y_j) -f(x_{i-1}, y_{j-1}) )\|

$$

by the mean value theorem for partials we can simplify it to

$$ \text{A}(f, \mathcal P) = \sum_{i = 1}^k\sum_{j = 1}^m\|\partial_x f(x_i^*, y_{i-1}) \wedge \partial_yf(x_{i-1}, y_i^*)\|m(R_{ij}) $$

which certainly looks like close to a Riemann sum, and could try to use continuity of $\partial_x f$ and $\partial _y f$ to maybe simplify as we can use that the $\operatorname{diam}(R_{ij}) < \delta$ for some $\delta >0$,

$$ \sum_{i = 1}^k\sum_{j = 1}^m\|\partial_x f(\eta_{ij}) \wedge \partial_yf(\eta_{ij})\|m(R_{ij}) $$

for some $\eta_{ij}$ that is close enough such that the sum is approximately. Then we can think of it as Riemann sum of the function $\|\partial_x f \wedge \partial _y f\|$ which I think is continuous, which is integrable. Thus $f$ is rectifiable, and

$$ A(f) = \int_R \left\|\frac{\partial f}{\partial x} \wedge \frac{\partial f}{\partial y}\right\| $$