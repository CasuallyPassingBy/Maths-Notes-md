---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Green's Theorem and Curl in R2]], [[Line Integral over a Vector Field]]

We can modify our definition of vector line integral to instead of measuring how much the vector field $F$ aligns with the curve with its orientation, to measure how much the vector field is perpendicular to the curve.

**********Def:********** Let $U\subseteq \Bbb R^n$ be an open an connected set, a curve $\Gamma \subseteq U$ and $\gamma:[a,b]\to \Bbb R^n$ be a piecewise smooth function such that $\Gamma = \gamma[[a,b]]$, and the function $F= (F_k )_{k = 1}^n: U \to \Bbb R^n$ a function such that for any $F_k \circ \gamma$ be integrable over $[a,b]$ for any $k \in \{1, \dots, n\}$. We define the integral of $F$ over the curve $\Gamma$ with the parametrization $\gamma$ as

$$ \int_\Gamma F\cdot \hat n \, ds = \int_\Gamma F\cdot \, (d\gamma)^\bot = \int_a^b F(\gamma(t))\cdot(\gamma'(t))^\bot \, dt $$

with $(x,y)^\bot = (y, -x)$, and where $\hat n$ refers to the unit normal vector at $\gamma(t_0)$

This can be simplified as

$$ \int_\Gamma F\cdot \, (d\gamma)^\bot = \int_\Gamma (-F)^\bot \cdot \, d\gamma $$

************Prop:************ Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, then we can define $\nabla \cdot F$ as follows:

$$ \nabla \cdot F = \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} $$

### Divergence Theorem

Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, and $\Omega \subseteq U$ be Jordan measurable such that $\Gamma = \partial \Omega$ is a closed simple curve and $\Omega \cup \Gamma \subseteq U$, then

$$ \int_\Omega \nabla \cdot F = \oint_{\Gamma = \partial \Omega} F \cdot \, (d\gamma)^\bot $$

where $\gamma$ is a counterclockwise parametrization of $\Gamma$ and only traces $\Gamma$ once.

## Divergence in $\Bbb R^2$

********Def:******** Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, $x \in U$ and $\{\Omega_\varepsilon\}_{0 < \varepsilon <c}$ be a family of compact Jordan-measurable sets contained in $U$, such that $\Gamma_\varepsilon = \partial \Omega_\varepsilon$ is a closed simple curve, $x \in \operatorname{int}\Omega_\varepsilon$, for all $0 < \varepsilon < c \in \Bbb R$ and $\lim_{\varepsilon\to 0} \operatorname{diam}(\Omega_\varepsilon) = 0$ , then *_divergence of $F$ at $x$_ is defined as

$$ \operatorname{div} F(x) := \lim_{\varepsilon \to 0} \frac{1}{J(\Omega_\varepsilon)} \oint_{\Gamma_\varepsilon} F\cdot\, (d\gamma_\varepsilon)^\bot $$

where $\gamma_ \varepsilon$ is a counterclockwise parametrization of $\Gamma_\varepsilon$ and only traces $\Gamma_\varepsilon$ once. We know this must converge since we can use the Divergence Theorem to calculate the value and find it is independent of the choice of $\{\Omega_\varepsilon\}_{0 < \varepsilon<c}$.

************Prop:************ Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, then we can simplify $\operatorname{div} F$ as follows:

$$ \operatorname{div} F=\nabla \cdot F $$

************Prop:************ Let $F, G:U \subseteq\Bbb R^2\to \Bbb R^2$ such that $\operatorname{div} F$ and $\operatorname{div} G$ exists for every $x \in U$, and ${\alpha, \beta\in \Bbb R}$ . Then $\operatorname{div} (\alpha F + \beta G)$ exists for every $x \in U$, and

$$ \operatorname{div} (\alpha F + \beta G ) = \alpha \operatorname{div} F+ \beta \operatorname{div} G $$

**********Cor:********** Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, then we get the following relation

$$ \nabla \cdot F = \nabla \times (-F)^\bot $$

**Prop:** Let $\phi: U\subseteq\Bbb R^n\to \Bbb R$ be a scalar field and $F:U \to \Bbb R^n$ both being $\cal C^1$ on $U$, then ${\nabla \cdot(\phi F)}$ exists and

$$ \nabla\cdot(\phi F) = \nabla \phi \cdot F + \phi\nabla \cdot F $$

Which we can use the Divergence Theorem to get the following:

Let $U \subseteq \Bbb R^2$ be an open and connected set, let $\Omega \subseteq U$ be a compact Jordan-measurable set, and $\Gamma = \partial \Omega$ a closed simple curve, and $\Omega \cup \Gamma \subseteq U$, then

$$ \int_\Omega (f \nabla \cdot F) = \oint_{\partial \Omega} (f F) \cdot\, (d\gamma)^\bot - \int_\Omega (f\nabla \cdot F) $$

which can be thought of a another integration by parts formula in $\Bbb R^2$

******Cor:****** Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^2$on $U$, then we get the following relation

$$ \nabla \cdot (\nabla \times F )= 0 $$

Def:****** Let $f:U\subseteq\Bbb R^2\to\Bbb R$ be $\cal C^2$on $U$, then we can consider the following

$$ \nabla \cdot (\nabla f) = \nabla ^2 f=\Delta f=\frac{\partial^2 f }{\partial x^2} + \frac{\partial^2 f}{\partial y^2} $$

This is called the ************_Laplacian of $f$_

**Def:** Let $f:U\subseteq\Bbb R^2\to\Bbb R$ be $\cal C^2$on $U$, if $\Delta u =0$, then $f$ is called [[Harmonic Functions|harmonic]]. 