---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links:[[Vector Surface Integral]], [[Riemann Integral in Rn]], [[Divergence Theorem in R2]]

Prop:************ Let $F =(P,Q, R) :U\subseteq\Bbb R^3\to\Bbb R^3$ be $\cal C^1$on $U$, then we can define $\nabla \cdot F$ as follows:

$$ \nabla \cdot F = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z} $$

### Gauss’ Theorem

Let $F =(P,Q, R) :U\subseteq\Bbb R^3\to\Bbb R^3$ be $\cal C^1$on $U$, and $\Omega \subseteq U$ be Jordan measurable such that $S = \partial \Omega$ be a piecewise surface and $\Omega \cup S \subseteq U$, then

$$ \int_\Omega \nabla \cdot F = \oint_{S=\partial \Omega} F \cdot \, d\sigma $$

where $\sigma$ is a simple parametrization of $S$ that induce the normal vectors pointing “outward” of $\Omega$.

### General Gauss’ Theorem

Let $F =(P,Q, R) :U\subseteq\Bbb R^3\to\Bbb R^3$ be $\cal C^1$on $U$, and $\Omega \subseteq U$ be Jordan measurable such that $\partial \Omega = S_0\cup \cdots \cup S_k$, where $S_0, \dots, S_k$ piecewise surfaces, and $S_0$ being the most exterior and $\Omega \cup S \subseteq U$, then

$$ \begin{align*} \int_\Omega \nabla \cdot F &= \oint_{S=\partial \Omega} F \cdot \, d\sigma \\ & = \sum_{i = 0}^k \oint_{S_i} F \cdot \, d\sigma_i \end{align*} $$

where $\sigma_0, \dots, \sigma_k$ is a simple parametrization of $S_0, \dots, S_k$ that induce the normal vectors pointing “outward”.

## Divergence in $\Bbb R^3$

********Def:******** Let $F :U\subseteq\Bbb R^3\to\Bbb R^3$ be $\cal C^1$on $U$, $x \in U$ and $\{\Omega_\varepsilon\}_{0 < \varepsilon <c}$ be a family of compact Jordan-measurable sets contained in $U$, such that $S_\varepsilon = \partial \Omega_\varepsilon$ is a surface, $x \in \operatorname{int}\Omega_\varepsilon$, for all $0 < \varepsilon < c \in \Bbb R$ and $\lim_{\varepsilon\to 0} \operatorname{diam}(\Omega_\varepsilon) = 0$ , then *_divergence of $F$ at $x$_ is defined as

$$ \operatorname{div} F(x) := \lim_{\varepsilon \to 0} \frac{1}{J(\Omega_\varepsilon)} \oint_{S_\varepsilon} F\cdot\, d\sigma_\varepsilon $$

where $\sigma_ \varepsilon$ is a parametrization of $S_\varepsilon$ that induce the normal vectors pointing “outward”. We know this must converge since we can use the Divergence Theorem to calculate the value and find it is independent of the choice of $\{\Omega_\varepsilon\}_{0 < \varepsilon<c}$.

**Prop:** Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, then we can simplify $\operatorname{div} F$ as follows:

$$ \operatorname{div} F=\nabla \cdot F $$

**Prop:** Let $F, G:U \subseteq\Bbb R^2\to \Bbb R^2$ such that $\operatorname{div} F$ and $\operatorname{div} G$ exists for every $x \in U$, and ${\alpha, \beta\in \Bbb R}$ . Then $\operatorname{div} (\alpha F + \beta G)$ exists for every $x \in U$, and

$$ \operatorname{div} (\alpha F + \beta G ) = \alpha \operatorname{div} F+ \beta \operatorname{div} G $$

**Prop:** Let $F, G:U \to \Bbb R^3$ both being $\cal C^1$ on $U$, then ${\nabla \cdot(F\times G)}$ exists and

$$ \nabla\cdot (F\times G) = (\nabla \times F)\cdot G- F\cdot (\nabla \times G) $$

**Prop:** Let $\phi: U\subseteq\Bbb R^n\to \Bbb R$ be a scalar field and $F:U \to \Bbb R^3$ both being $\cal C^1$ on $U$, then ${\nabla \cdot(\phi F)}$ exists and

$$ \nabla\cdot(\phi F) = \nabla \phi \cdot F + \phi\nabla \cdot F $$

We can use this along with Gauss’ Theorem, and get the following

Let $U$ be a open and connected set, let $\Omega \subseteq U$ be a Jordan-measurable, and $\partial \Omega =S$ be a piecewise surface, and $\Omega \cup S \subseteq U$, then

$$ \int_\Omega \phi \nabla \cdot F = \oint_{S= \partial \Omega} \phi F\cdot \, d\sigma - \int_\Omega \nabla\phi \cdot F $$

with $\sigma$ be parametrization of $S$, that induces the normal vectors pointing upward.

This can be thought as formula of integration by parts of $\Bbb R^3$

**Cor:** Let $F :U\subseteq\Bbb R^3\to\Bbb R^3$ be $\cal C^2$on $U$, then we get the following relation

$$ \nabla \cdot (\nabla \times F )= \bf 0 $$

Def:****** Let $f:U\subseteq\Bbb R^2\to\Bbb R$ be $\cal C^2$on $U$, then we can consider the following

$$ \nabla \cdot (\nabla f) = \nabla ^2 f=\Delta f = \frac{\partial^2 f }{\partial x^2} + \frac{\partial^2 f}{\partial y^2}+ \frac{\partial^2 f}{\partial z^2} $$

This is called the ************_Laplacian of $f$_

**Def:** Let $f:U\subseteq\Bbb R^3\to\Bbb R$ be $\cal C^2$on $U$, if $\Delta f =0$, then $f$ is called [[Harmonic Functions|harmonic]].