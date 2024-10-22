---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Normed Spaces]], [[Metric Spaces]]

A function $f:S \to X$ is ********bounded******** if there are $c \in \Bbb R$ and $x_0 \in X$ such that, for any $z \in S$

$$ d(f(z), x_0)\le c $$

We denote

$$ \mathcal B(S, X) := \{ f:S \to X\mid f\text{ is bounded} \} $$

and we define

$$ d_\infty(f,g) = \sup_{z \in S}d(f(z), g(z)) $$

$d_\infty$ is a metric on $\mathcal B(S,X)$. This metric is called the ****uniform metric.****

If $V$ is a vector space, the set of all function from $S$ to $V$ is a vector space with the operations

$$ (f+g)(z) := f(z)+g(z) \qquad (\lambda f)(z) := \lambda f(z) $$

If $V$ is a normed space with norm $\|\cdot\|$, then $\mathcal B(S, V)$ is a vector space and

$$ \|f\|_\infty := \sup_{z \in S}\|f(z)\| $$

is a norm in $\mathcal B(S , V)$. This norm is called the _*********uniform norm.************_