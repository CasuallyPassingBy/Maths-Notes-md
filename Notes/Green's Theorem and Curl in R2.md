---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Line Integral over a Vector Field]], [[Conservative Fields]], [[Riemann Integral in Rn]]
Def:************ Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, we can define $\nabla \times F$ as follows:

$$ \nabla \times F = \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} $$

## Green’s Theorem
Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, and $\Omega \subseteq U$ be Jordan measurable such that $\Gamma = \partial \Omega$ is a closed simple curve and $\Omega \cup \Gamma \subseteq U$, then

$$ \int_\Omega \nabla \times F = \oint_{\Gamma = \partial \Omega} F \cdot \, d\gamma $$

where $\gamma$ is a counterclockwise parametrization of $\Gamma$ and only traces $\Gamma$ once. Using the other notation we get that

$$ \iint_\Omega \frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y} \, dx\, dy= \int_{\Gamma = \partial \Omega} P(x,y)\, dx + Q(x, y) \, dy $$

### Green’s Theorem General Version

Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, and $\Omega \subseteq U$ be Jordan measurable such that $\partial \Omega = \bigcup _{i = 0}^k \Gamma_i$, $\Gamma_0, \dots, \Gamma_k$ closed simple curves, $\overline\Omega \subseteq U$, and $\Gamma_0$ being the most exterior one. Then

$$ \begin{align*} \int_\Omega \nabla \times F &= \oint_{\partial \Omega }F \cdot \, d\gamma \\ &= \sum_{i = 0}^k\oint_{\Gamma_i} F \cdot \, d\gamma_i \end{align*} $$

where $\gamma_0, \dots, \gamma_k$ are parametrizations of $\Gamma_0, \dots, \Gamma_k$, each just only tracing them once, $\gamma_1, \dots, \gamma_k$ clockwise and $\gamma_0$ counterclockwise.

## Curl in $\Bbb R^2$

********Def:******** Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, $x \in U$ and $\{\Omega_\varepsilon\}_{0 < \varepsilon <c}$ be a family of compact Jordan-measurable sets contained in $U$, such that $\Gamma_\varepsilon = \partial \Omega_\varepsilon$ is a closed simple curve, $x \in \operatorname{int}\Omega_\varepsilon$, for all $0 < \varepsilon < c \in \Bbb R$ and $\lim_{\varepsilon\to 0} \operatorname{diam}(\Omega_\varepsilon) = 0$ , then *_curl of $F$ at $x$_ is defined as

$$ \operatorname{Curl} F(x) := \lim_{\varepsilon \to 0} \frac{1}{J(\Omega_\varepsilon)} \oint_{\Gamma_\varepsilon} F\cdot\, d\gamma_\varepsilon $$

where $\gamma_ \varepsilon$ is a counterclockwise parametrization of $\Gamma_\varepsilon$ and only traces $\Gamma_\varepsilon$ once. We know this must converge since we can use Green’s Theorem to calculate the value and find it is independent of the choice of $\{\Omega_\varepsilon\}_{0 < \varepsilon<c}$.

************Prop:************ Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, then we can simplify the $\operatorname{Curl} F$ as follows:

$$ \operatorname{Curl}F = \nabla \times F $$

************Prop:************ Let $F, G:U \subseteq\Bbb R^2\to \Bbb R^2$ such that $\operatorname{Curl} F$ and $\operatorname{Curl} G$ exists for every $x \in U$, and ${\alpha, \beta\in \Bbb R}$ . Then $\operatorname{Curl} (\alpha F + \beta G)$ exists for every $x \in U$, and

$$ \operatorname{Curl} (\alpha F + \beta G ) = \alpha \operatorname{Curl} F+ \beta \operatorname{Curl} G $$

**Def:** Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, if for any $x \in U$, we have that ${(\nabla \times F)(x) = 0}$, then it is called irrotational.

**********Prop:********** Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$ be conservative, then $F$ is irrotational.

**Th:** Let $F:U\subseteq \Bbb R^2\to \Bbb R^2$ be $\cal C^1$ on $U$, where $U$ is a simply connected region. Then $F$ is conservative iff $F$ is irrotational.  ^b541fe

********Cor:******** Let $\varphi :U \subseteq\Bbb R^2\to \Bbb R^2$ be $\cal C^2$ on $U$, then $(\nabla \times( \nabla \varphi))(x) = 0$, for any $x \in U$.

**Prop:** Let $\phi: U\subseteq\Bbb R^2\to \Bbb R$ be a scalar field and $F:U \to \Bbb R^2$ both being $\cal C^1$ on $U$, then ${\nabla \times (\phi F)}$ exists and
$$ \nabla\times (\phi F) = \nabla \phi \times F + \phi\nabla \times F $$

Which we can use Green’s Theorem to get the following:
Let $U \subseteq \Bbb R^2$ be an open and connected set, let $\Omega \subseteq U$ be a compact Jordan-measurable set, and $\Gamma = \partial \Omega$ a closed simple curve, and $\Omega \cup \Gamma \subseteq U$, then

$$ \int_\Omega (f \nabla \times F) = \oint_{\partial \Omega} (f F) \cdot\, d\gamma - \int_\Omega (f\nabla \times F) $$

which can be thought of a an integration by parts formula in $\Bbb R^2$