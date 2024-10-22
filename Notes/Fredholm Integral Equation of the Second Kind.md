---
tags:
  - Analysis
  - "#FredholmTheory"
---
Subjects: [[Metric and Normed Spaces]], [[Fredholm Theory]]
Links: [[Continuous Function Spaces]], [[Complete Metric Spaces]]
Let ${\cal K}:[a,b]\times [a, b] \to \Bbb R$ and $g:[a,b]\to \Bbb R$ are continuous with $\lambda \in \Bbb R$. Then the integral equation

$$ \lambda f(x) - \int_a^b {\cal K}(x,y)f(y)\, dy = g(x) $$

is called a _**Fredholm Integral equation.**_ We say that it is of the **********first kind********** if $\lambda=0$ and it is of the _******second kind******_ if $\lambda \ne 0$

We will simplify the notation with ${\frak F}f:[a, b] \to \Bbb R$ defined as

$$ ({\frak F}f)(x):=\int_a^b{\cal K}(x,y)f(y)\, dy $$

Meaning that the Fredholm integral equation can be rewritten as

$$ \lambda f -{\frak F}f = g $$

If $\lambda \ne 0$, then

$$ f=\frac{1}{\lambda}({\frak F}f+g) $$

A lemma we need is that if $f \in {\cal C}^0[a,b]$, then the function ${\frak F}f:[a,b]\to \Bbb R$ defined above is continuous, and that ${\frak F}:{\cal C}^0[a,b]\to {\cal C}^0[a,b]$. This operator is a [[Bounded Linear Operators]].

Meaning, that if we let the function $\phi_\lambda:{\cal C}^0[a,b]\to {\cal C}^0[a,b]$ with $\lambda \ne 0$ defined as

$$ \phi_\lambda(f)= \frac{1}{\lambda}({\frak F}f+g) $$

is well-defined.

If $|\lambda| >\|{\cal K}\|_\infty(b-a)$ then, for every $g\in {\cal C}^0[a,b]$, the Fredholm equation $\lambda f -{\frak F}f = g$, has a unique solution. This is because $\phi_\lambda$ becomes a contraction in ${\cal C}^0[a,b]$, and using the [[Banach's Fixed Point Theorem]]

Let ${\cal K}:[a,b] \times[a,b]\to \Bbb R$ be continuous. The Fredholm operator ${\frak F}:{\cal C}^0[a,b]\to {\cal C}^0[a,b]$

$$
({\frak F}f)(x) := \int_{a}^b {\cal K}(x, y)f(y) \, dy
$$

is a [[Compact Operators|compact operator]]. This can be proven using the [[Arzelà–Ascoli Theorem]]

We can see that ${\frak F}:{\cal C}^0[a,b] \to{\cal C}^0[a,b]$ is a linear and continuous function. If we examine $g = 0$, then we are looking at the equation

$$ {\frak F}f =\lambda f $$

meaning, we are looking for the eigenvalues of ${\frak F}$. Then we see that for any $\lambda$, $f=0$ satisfies the equation. If we have that $|\lambda|>\|{\cal K}\|_\infty(b-a)$, then $f=0$ is the only solution of the equation above. Meaning that the eigenvalues of $\frak F$ are contained in the closed interval${[-\|{\cal K}\|_\infty(b-a), \|{\cal K}\|_\infty(b-a)]}$. We have that a more through study of this types of equations are studied in Fredholm Theory

This are related to the [[Volterra Integral Equation of the Second Kind]]