---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Green's Theorem and Curl in R2]], [[Line Integral over a Vector Field]], [[Vector Surface Integral]]
**********Def:********** Let $F: U\subseteq \Bbb R^3 \to \Bbb R^3$ be a $\cal C^1$ on $U$, an open and connected set. Then we define ${\nabla \times F}$ as

$$ \nabla \times F = \begin{pmatrix} \dfrac{\partial F_z}{\partial y} - \dfrac{\partial F_y}{\partial z} \\ \\ \dfrac{\partial F_x}{\partial z} - \dfrac{\partial F_z}{\partial x} \\ \\ \dfrac{\partial F_y}{\partial x} - \dfrac{\partial F_x}{\partial y}\end{pmatrix} $$

### Stokes’ Theorem

Let $S \subseteq U \subseteq \Bbb R^3$ be a surface parametrized by $\sigma :A\subseteq \Bbb R^2\to \Bbb R^3$ be $\cal C^1$, $\gamma :[a,b] \to \Bbb R^2$ be a parametrization of $\partial A$ (be a closed simple curve), the passes through it once in the counterclockwise direction, and ${F: U\subseteq \Bbb R^3 \to \Bbb R^3}$ be a $\cal C^1$ on $U$. Then

$$ \int_S \nabla \times F \cdot \, d\sigma = \oint_{\partial _\sigma S} F \cdot\, d\tilde \gamma $$

where $\tilde \gamma = \sigma \circ \gamma: [a,b] \to \Bbb R^3$ and $\partial_\sigma S = \sigma [\partial A]$.

### General Stokes’ Theorem

Let $S \subseteq U \subseteq \Bbb R^3$ be a surface parametrized by $\sigma :A\subseteq \Bbb R^2\to \Bbb R^3$ and ${F: U\subseteq \Bbb R^3 \to \Bbb R^3}$ be a $\cal C^1$ on $U$. If $\partial A = \Gamma_0 \cup \cdots \cup \Gamma_k$, with $\Gamma_0, \dots, \Gamma_k$ closed simple curves, and $\Gamma_0$ being the “most outer one”, then

$$ \begin{align*} \int_S \nabla \times F \cdot \, d\sigma &= \oint_{\partial _\sigma S} F \cdot\, d\tilde \gamma \\ & = \sum_{i = 0}^k \oint_{\Gamma_i} F\cdot \, d\tilde \gamma_i \end{align*} $$

where $\partial_\sigma S = \sigma [\partial A]$, and $\tilde \Gamma_i = \sigma[\Gamma_i]$, and $\tilde \gamma_i = \sigma \circ \gamma$ be a parametrization of $\Gamma_i$, that traces it only once, clockwise for $i \ge 1$, and counterclockwise for $i = 0$.

## Curl in $\Bbb R^3$

**********Def:********** Let $F: U \subseteq \Bbb R^3 \to \Bbb R^3$ be a $\cal C^1$ function on $U$, and $\sigma :A\subseteq\Bbb R^2\to \Bbb R^3$ be a $\cal C^1$ function such that $\sigma[A] \subseteq U$, and $(u_0, v_0) \in \operatorname{int}(A)$, such that

$$ \frac{\partial \sigma}{\partial u}(u_0, v_0) \times \frac{\partial \sigma}{\partial v}(u_0, v_0) \ne \bf 0 $$

Let $\{A_\varepsilon\}_{0 < \varepsilon< c}$ a family of connected subsets of $A$ such that:

- $(u_0, v_0)\in \operatorname{int}(A_\varepsilon)$
- $\Gamma_\varepsilon = \partial A_\varepsilon$ is a closed simple curve
- $\lim_{\varepsilon \to 0} \operatorname{diam}(A_\varepsilon) =0$

If the surface $S_\varepsilon$ is a parameterized by $\sigma |_{A_\varepsilon}$ for each $0 < \varepsilon <c$, then we can define the ****_curl of a vector field $F$ at $x_0$_

$$ \operatorname{Curl } F(x_0) \cdot \hat n

=\lim_{\varepsilon \to 0}\frac{1}{A(S_\varepsilon)} \oint_{\partial_\sigma S_\varepsilon} F \cdot\, d\tilde \gamma_\varepsilon $$

where $\tilde \gamma_\varepsilon = \sigma \circ \gamma_\varepsilon$, and $\gamma_\varepsilon$ is a parameterization of $\Gamma_\varepsilon$ that traces it only once and counterclockwise, for each $0 < \varepsilon< c$, and $x_0 = \sigma(u_0, v_0)$ and

$$ \hat n = \frac{\frac{\partial \sigma}{\partial u}(u_0, v_0) \times \frac{\partial \sigma}{\partial v}(u_0, v_0)}{\|\frac{\partial \sigma}{\partial u}(u_0, v_0) \times \frac{\partial \sigma}{\partial v}(u_0, v_0)\|} $$

We know this must converge since we can use the Stokes’ Theorem to calculate the value and find it is independent of the choice of $\{A_\varepsilon\}_{0 < \varepsilon<c}$.

************Prop:************ Let $F =(P,Q) :U\subseteq\Bbb R^2\to\Bbb R^2$ be $\cal C^1$on $U$, then we can simplify the $\operatorname{Curl} F$ as follows:

$$ \operatorname{Curl}F = \nabla \times F $$

************Prop:************ Let $F, G:U \subseteq\Bbb R^2\to \Bbb R^2$ such that $\operatorname{Curl} F$ and $\operatorname{Curl} G$ exists for every $x \in U$, and ${\alpha, \beta\in \Bbb R}$ . Then $\operatorname{Curl}(\alpha F + \beta G)$ exists for every $x \in U$, and

$$ \operatorname{Curl}(\alpha F + \beta G ) = \alpha \operatorname{Curl} F+ \beta \operatorname{Curl}G $$

**Def:** Let $F :U\subseteq\Bbb R^3\to\Bbb R^3$ be $\cal C^1$on $U$, if for any $x \in U$, we have that ${(\operatorname{Curl}F)(x) = \bf 0}$, then it is called irrotational.

**Prop:** Let $F :U\subseteq\Bbb R^3\to\Bbb R^3$ be $\cal C^1$on $U$ be conservative, then $F$ is irrotational.

**Th:** Let $F:U\subseteq \Bbb R^3\to \Bbb R^3$ be $\cal C^1$ on $U$, where $U$ is a simply connected region. Then $F$ is conservative iff $F$ is irrotational.   ^c0e398

********Cor:******** Let $\varphi :U \subseteq\Bbb R^3\to \Bbb R$ be $\cal C^2$ on $U$, then $(\nabla \times( \nabla \varphi))(x) = \bf 0$, for any $x \in U$.

**Prop:** Let $F, G:U \to \Bbb R^3$ both being $\cal C^1$ on $U$, then ${\nabla \times (F\times G)}$ exists and

$$ \nabla \times (F\times G) = F(\nabla \cdot G) -G(\nabla \cdot F) + (G\cdot \nabla)F- (F\cdot\nabla)G $$

**Prop:** Let $\phi: U\subseteq\Bbb R^3\to \Bbb R$ be a scalar field and $F:U \to \Bbb R^3$ both being $\cal C^1$ on $U$, then ${\nabla \times (\phi F)}$ exists and

$$ \nabla\times (\phi F) = \nabla \phi \times F + \phi\nabla \times F $$

Which we can use Stokes’ Theorem to get the following:

Let $S \subseteq U \subseteq \Bbb R^3$ be a surface parametrized by $\sigma :A\subseteq \Bbb R^2\to \Bbb R^3$ be $\cal C^1$, $\gamma :[a,b] \to \Bbb R^2$ be a parametrization of $\partial A$, and $\Omega \cup \Gamma \subseteq U$, then

$$ \int_S(f \nabla \times F) = \oint_{\partial_\sigma S} (f F) \cdot\, d\tilde\gamma - \int_\Omega (f\nabla \times F) $$

where $\tilde \gamma = \sigma \circ \gamma: [a,b] \to \Bbb R^3$ and $\partial_\sigma S = \sigma [\partial A]$.

which can be thought of a an integration by parts formula in $\Bbb R^3$