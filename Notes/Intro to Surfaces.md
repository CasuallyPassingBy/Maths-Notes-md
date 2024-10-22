---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]], [[Differential Geometry]]

**Def:** Let $S \subseteq \Bbb R^n$ is a surface if there’s $\sigma =(\sigma_k)_{k = 1}^n : U \subseteq\Bbb R^2\to \Bbb R^n$ of class $\cal C^1$ on $U$ (open) and $A \subseteq U$ a region of type $1$ or type $2$, such that $S = \sigma [A]$. In this case we call $\sigma$ a parametrization of $S$.

**Def:** Let $S \subseteq \Bbb R^3$ is a surface be parametrization $\sigma : U \subseteq\Bbb R^2\to \Bbb R^3$, then let $A\subseteq U$ and ${\sigma[A] = S}$, let $x_0 \in A$, and $y_0 = \sigma (x_0)$ such that

$$ \frac{\partial\sigma}{\partial x}(x_0) \times \frac{\partial \sigma }{\partial y}(x_0) \ne \mathbf 0 $$

then we say that $S$ is _smooth at_ $y_0$. Similarly if for all $y _0 \in S$, $S$ is smooth at $y_0$, then we say that $S$ is _smooth_.

Def: Let $S \subseteq \Bbb R^3$ is a surface be parametrization $\sigma : U \subseteq\Bbb R^2\to \Bbb R^3$, then let $A\subseteq U$ and ${\sigma[A] = S}$, we will define the boundary of $S$ induced by $\sigma$, denoted as $\partial_\sigma S$, as

$$ \partial_\sigma S= \sigma[\partial A] $$

**Def:** Let $S \subseteq\Bbb R^3$ be a surface. We say $S$ is oriented if there’s a $F:S\to \Bbb R^3$ continuous, $F(x)$ is normal to $x\in S$ and $\|F(x)\| = 1$, for all $x \in S$.

**Def:** Let $\sigma :A\subseteq \Bbb R^2 \to \Bbb R^3$ a parametrization of the curve $S$ and $\alpha :B\subseteq\Bbb R^2\to \Bbb R^2$ is a $\cal C^1$ function injective on $B$, and $\det (d\alpha_x) \ne 0$ (except in a set of $0$ Jordan-measure, for both conditions) such that $\sigma[B] = A$ . We say that the function $\tilde \sigma = \sigma \circ \alpha:A\subseteq\Bbb R^2\to \Bbb R^3$ is a reparameterization of $S$. If $\det (d\alpha_{(u,v)}) \ge 0$, for all $(u,v) \in B$, then we say that $\tilde \sigma$ preserves “orientation”, but if $\det (d\alpha_{(u,v)}) \ge 0$, for all $(u,v) \in B$, then we say that $\tilde \sigma$ reverses “orientation”.

**Def:** We say that $S\subseteq \Bbb R^n$ is piecewise surface if there are $S_1, \dots, S_k \subseteq \Bbb R^n$ surfaces that ${S= \bigcup_{i = 1}^k S_i}$. If $\sigma_i$ is a parametrization of $S_i$ for all $1 \le i \le k$, we write $\sigma = \sigma_1 * \cdots * \sigma_k$

### Surface Area
Def:****************** Let $S\subseteq \Bbb R^3$ be a surface parameterised by the function $\sigma :A\subseteq \Bbb R^2\to \Bbb R^3$. If $\sigma$ is simple parametrization, we define the area of $S$ as, denoted as $A(S)$

$$ A(S) = \int_A \left\|\frac{\partial \sigma}{\partial x} \times \frac{\partial \sigma}{\partial y}\right\| $$