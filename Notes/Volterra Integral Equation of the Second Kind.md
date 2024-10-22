---
tags:
  - Analysis
  - FredholmTheory
---
Subjects: [[Metric and Normed Spaces]], [[Fredholm Theory]]
Let ${\cal K}:[a,b]\times [a, b] \to \Bbb R$ and $g:[a,b]\to \Bbb R$ are continuous with $\lambda \in \Bbb R$. Then the integral equation

$$ \lambda f(x) - \int_a^x {\cal K}(x,y)f(y)\, dy = g(x) $$

is called a _**Volterra Integral equation.**_ We say that it is of the **********first kind********** if $\lambda=0$ and it is of the _******second kind******_ if $\lambda \ne 0$

We will simplify the notation, we define ${\frak V}f:[a, b] \to [a, b]$ as

$$ ({\frak V}f)(x) := \int_a^x {\cal K}(x,y)f(y)\, dy $$

then we get that the Volterra Integral equation is just

$$ \lambda f- {\frak V}f = g $$

Shuffling things around when $\lambda \ne0$, we get

$$ f = \frac{1}{\lambda}({\frak V}f-g) $$

We can prove that if $f\in {\cal C}^0[a,b]$ then is also ${\frak V}f \in {\cal C}^0[a, b]$. Meaning that ${{\frak V}:{\cal C}^0[a,b]\to {\cal C}^0[a,b]}$, and ${\frak V}$ is a [[Bounded Linear Operators]].

We define the function $\phi_\lambda:{\cal C}^0[a,b]\to {\cal C}^0[a,b]$ defined as

$$ \phi_\lambda(f) = \frac{1}{\lambda}({\frak V}f-g) $$

The function $\phi_\lambda$ satisfies that

$$ \|\phi_\lambda^k (f_1) -\phi_\lambda^k(f_2) \|_\infty \le |\lambda|^{-k}\|{\cal K}\|_\infty ^k \frac{(b-a)^k}{k!}\|f_1-f_2\|_\infty $$

If $\lambda\ne 0$, then for every $g \in {\cal C}^0[a,b]$, the Volterra equation $\lambda f- {\frak V}f = g$ has a unique solution. We know this using [[Banach's Fixed Point Theorem]]

Let ${\cal K}:[a,b] \times[a,b]\to \Bbb R$ be continuous. The Volterra operator ${\frak V}:{\cal C}^0[a,b]\to {\cal C}^0[a,b]$ given as

$$ ({\frak V}f)(x) := \int_{a}^x {\cal K}(x, y)f(y) \, dy $$

is a [[Compact Operators|compact operator]]. This can be proven using the [[Arzelà–Ascoli Theorem]]

From this result, we know that if we let $g = 0$, it is a eigenvalue problem getting

$$ \lambda f={\frak V}f $$

for the **********Volterra operator**********. By the result above we know that any $\lambda\ne0$ is not an eigenvalue of ${\frak V}$. The Volterra equation of the first kind ${\frak V}f = g$ is a lot more complicated and it is studied in Fredholm Theory

It is in fact related to the [[Fredholm Integral Equation of the Second Kind]]