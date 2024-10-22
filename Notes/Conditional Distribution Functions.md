---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Conditional Probability]], [[Random Vectors]], [[Probability Functions for Random Vectors]], [[Marginal Probability Functions]]
We have that the conditional probability, is that given two events $A$ and $B$, then 

$$
P(A\mid B) = \frac {P(A\cap B)}{P(B)}
$$
We are going to use similar reasoning to define the conditional probability distribution:

Let $(X, Y)$ be a discrete or continuous random vector with a mass or density function $f_{X, Y}(x, y)$. Let $y$ be a value of the $f_Y(y) \ne 0$. The function $f_{X\mid Y}(x\mid y)$, defined as follows is, it is called the conditional mass or density function of $X$ given $Y= y$.

$$
f_{X\mid Y}(x\mid y) = \frac{f_{X, Y}(x, y)}{f_Y(y)}
$$
Let $(X, Y)$ be a discrete or continuous random vector with a mass or density function $f_{X, Y}(x, y)$. Let $y$ be a value of the $f_Y(y) \ne 0$. The conditional distribution function of $X$, given $Y=y$, is the function 
$$
F_{X\mid Y}(x\mid y) = 
\begin{dcases}
\sum_{u \le x} f_{X\mid Y}(u\mid y) & \text{ in the discrete case} \\
\int_{-\infty}^x f_{X\mid Y}(u\mid y)\, du & \text{ in the continuous case}
\end{dcases}
$$