---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Line Integral over a Vector Field]], [[Riemann Integral in R]], [[Arc-Length Integral in C]], [[Integrals in C]]

**********Def:********** Let $f: \Omega \subseteq \Bbb C \to \Bbb C$ continuous and $\gamma :[a,b]\subseteq \Bbb R \to \Omega$ a piecewise smooth. We define the **********_contour integral of $f$ over $\gamma$,_ denoted as

$$ \int_\gamma f=\int_\gamma f(z) \, dz := \int_a^b f(\gamma(t)) \gamma'(t)\, dt $$

Addtionally, if $\gamma$ is closed it is specially denoted as

$$ \oint_\gamma f= \oint_\gamma f(z) \, dz $$

If the parametrization isn’t important we can use $\Gamma = \operatorname{Im}(\gamma)$, and use $\Gamma$ instead of $\gamma$

$$ \int_\Gamma f=\int_\Gamma f(z) \, dz \quad \text{ and }\quad \oint_\Gamma f = \oint_\Gamma f(z)\, dz $$

************Prop:************ Let $f,g: \Omega\subseteq \Bbb C \to \Bbb C$, and $\gamma:[a,b] \to \Omega$, and $\delta:[c,d] \to \Omega$ be piecewise smooth, then they satisfy the following properties:

$$ \left|\int_\gamma f(z) \ dz\right| \le \int_\gamma|f(z)| \, |dz| $$

Let $\alpha, \beta \in \Bbb C$, then

$$ \int_\gamma \alpha f(z) +\beta g(z)\ dz = \alpha \int_\gamma f(z) \ dz + \beta \int_\gamma g(z) \ dz $$

Let $\gamma(b) = \delta (c)$, we can concatete paths, denoted as $\gamma * \delta$, and get:

$$ \int_{\gamma * \delta} f(z) \, dz= \int_\gamma f(z) \ dz+ \int_\delta f(z) \ dz $$

If $\delta$ is a reparemetrization of $\gamma$, and preserves orientation then

$$ \int_\delta f(z) \ dz = \int_\gamma f(z) \ dz $$

If $\delta$ reverses the orientation of $\gamma$, then

$$ \int_\delta f(z) \ dz = -\int_\gamma f(z) \ dz $$

In particular

$$ \int_{\gamma^-} f(z) \ dz = -\int_\gamma f(z) \ dz $$

### Fundamental Theorem of Contour Integrals
Let $\gamma:[a,b] \to \Bbb C$ be piecewise smooth, and $F$ is function defined and holomorphic on $G$ an open connected set containing $\gamma$. Then

$$ \int_\gamma F' = F(\gamma(b))-F(\gamma(a)) $$

In particular if $\gamma$ is closed, then

$$ \oint_\gamma F' = 0 $$

### Path-Independence Theorem

Let $f: \Omega\subseteq \Bbb C \to \Bbb C$ continuous. Then the following are equivalent:

- The function $f$ has a primitive on $\Omega$. In other words, there’s $g:\Omega\to \Bbb C$ holomorphic on $\Omega$, such that $g'=f$ on $\Omega$
- For any curve $\gamma:[a,b]\to \Omega$ piecewise smooth and closed, then

$$ \oint_\gamma f =0 $$

- For any curve $\gamma:[a,b] \to \Omega$ piecewise smooth, the value of the integral $\int_\gamma f$ only depends on the endpoints. In other words, let $\delta:[c,d] \to \Omega$ is another piecewise smooth such that $\delta(c) = \gamma(a)$ and $\delta(d) = \gamma(b)$, then

$$ \int_\delta f = \int_\gamma f $$

### Change of Variable for Contuour Integration

Let $C$ be a contour, $\zeta$ is holomorphic $C$ and $f$ is continuous on $\zeta[C]$, then

$$ \int_{\zeta[C]} f(\zeta)\, d\zeta = \int_C f(\zeta(z))\zeta'(z)\, dz $$

Like [[The Fundamental Theorem of Calculus#Substitution Theorem|Change of Variable in R]]
### Integration by Parts for Contuour Integration

Let $f$ and $g$ be holomorphic in $Ω$, and such that $f$ and $g$ are continuous on $C$. Let ${γ : [a, b] → Ω}$ be a parametrization of $C$. Then,

$$ \int_C f(z)g'(z)\, dz = (fg)(\gamma(b)) - (fg)(\gamma(a)) - \int_C f'(z)g(z)\, dz $$

Like  [[The Fundamental Theorem of Calculus#Integration by Parts|Integration by Parts in R]]
### Differentiating under the Integral Sign for Countour Integration

Let $f: A\times \Gamma \subseteq \Bbb C^2 \to \Bbb C$ be continuous function of $z, w$ for $z$ in a region $A$ and $w$ on a curve $\gamma$. For each $w$ on $\gamma$ that $f$ is holomorphic in $z$. Let

$$ F(z) = \int_\Gamma f(z, w) \, dw $$

Then $F$ is holomorphic and

$$ F' (z) = \int_\Gamma \frac{\partial f}{\partial z}(z, w) \, dw $$

where $\partial_z f$ denotes the deriviative of $f$ with respect to $z$ with $w$ held fixed.

Like [[Differentiation under the integral sign]]

### Green's Theorem Analogue

Let $f: U\subseteq\Bbb C \to \Bbb C$ have continuous Wirtinger derivatives, and let $\Omega \subseteq U$ be a Jordan measurable set in $\Bbb R^2$, such that $\partial \Omega = \bigcup\limits_{i = 1}^n \gamma_i$ , where each $\gamma_i$ is a Jordan curve, with $\overline \Omega \subseteq U$, and $\gamma_0$ being the most exterior, then 
$$
\oint_{\partial \Omega} f(z)\, dz = 2i \iint_{\Omega} \frac{\partial f}{\partial \overline z} \, dA(z)
$$
where $z = x+iy$, $dz = dx + i dy$, $dA(z) = dx\, dy$. This is an analogue of [[Green's Theorem and Curl in R2|Green's theorem]], where the curl is replace with the [[Wirtinger Derivatives]]. 