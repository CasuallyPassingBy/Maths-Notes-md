---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Rectifiable Curves in Rn]], [[Continuity on Metric Spaces]]

A path in $X$ is a continuous function $\sigma :[a,b] \to X$. The length of $\sigma$ is defined as

$$ {\frak L}(\sigma) = \sup\left\{\left.\sum_{k = 1}^m d_X(\sigma(t_{k-1}), \sigma(t_k)) \right| a= t_0\le t_1 \le \dots \le t_m= b, m \in \Bbb N\right\} $$
or it can be denoted as, meaning the same thing
$$
L(\sigma ) = \Lambda(\sigma) = {\frak L}(\sigma)
$$
 we get that 
 $$
 \Lambda(\sigma) <\infty
 $$
 We call it rectifiable.

We see that ${\frak L}: {\cal C}^0([a,b],X) \to \Bbb R\cup\{\infty\}$ is [[Semicontinuity|lower semicontinuous]], but it is not continuous.

Let $\rho:[\alpha , \beta] \to [a,b]$ be a continuous, nondecreasing surjective function and $\sigma \in {\cal C}^0([a, b], X)$ be a path from $x$ to $y$ in $X$, then the new path $\sigma \circ \rho \in {\cal C}^0([\alpha, \beta], X)$ is also a path from $x$ to $y$ in $X$. It is called a ********************_reparemetrization of $\sigma$_.

If $\sigma \circ \rho$ is a reparamitraztion of $\sigma$ , then ${\frak L}(\sigma) = {\frak L}(\sigma \circ \rho)$

Let’s conside the subspsace of the paths from $x$ to $y$ meaning

$$ {\cal T}_{x, y}(X) := \{ \sigma \in {\cal C}^0([0,1], X) \mid \sigma(0) =x, \sigma(1) =y\} $$

with the uniform metric

$$ d_\infty (\sigma, \tau ) = \max_{t\in[0,1]}d(\sigma(t), \tau(t)) $$

Let $x, y \in X$, such that $x\ne y$, and $c \in \Bbb R$. Then if

$$ {\frak L}^{\le c} := \{ \sigma \in {\cal T}_{x, y}(X) \mid {\frak L}(\sigma ) \le c\} \ne \varnothing $$

then ${\frak L}^{\le c}$ is not compact

We say that a rectifiable path $\sigma \in {\cal C}^0([0,1], X)$ is ******************parametrized proportionally by arc length****************** if

$$ {\frak L}(\sigma|_{[0, t]}) = {\frak L}(\sigma) t $$

Given a rectifiable path $\sigma \in {\cal C}^0([0,1], X)$, we define the function $\lambda:[0,1] \to [0, {\frak L}(\sigma)]$ as

$$ \lambda(t) := {\frak L}(\sigma|_{[0,t]}) $$

is a function that is continuous, non decreasing and surjective

We will denote the space of special paths from $x$ to $y$ in $X$, that are parametrized proportionally by arc length as

$$ \hat {\cal T}_{x, y}(X) := \{ \sigma \in {\cal T}_{x, y}(X) \mid {\frak L}(\sigma) < \infty , \forall t \in [0,1]({\frak L}(\sigma|_{[0,t]}) = {\frak L}(\sigma) t )\} $$

For each rectifiable $\sigma \in {\cal T}_{x, y}(X)$ then there exists $\hat \sigma\in \hat {\cal T}_{x, y}(X)$ such that ${\frak L}(\sigma) ={\frak L}(\hat\sigma)$

### Existence of Geodesic Paths (Minimum Length Paths)

Let $X$ be a compact metric space and $x, y \in X$. If there exists a path from $x$ to $y$ in $X$, then there exists a path with minimum lenght path from $x$ to $y$ in $X$