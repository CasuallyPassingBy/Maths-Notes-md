---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Scalar Line Integral]], [[Integrals in C]]

**********Def:********** Let $f: \Omega \subseteq \Bbb C \to \Bbb C$ continuous and $\gamma :[a,b]\subseteq \Bbb R \to \Omega$ a piecewise smooth. We define the **********_arc-length integral of $f$ over $\gamma$,_ denoted as

$$ \int_\gamma f(z) \, |dz| := \int_a^b f(\gamma(t)) |\gamma'(t)|\, dt $$

in the special case that $f \equiv 1$, then

$$ \int_\gamma \, |dz| = \Lambda(\gamma) $$

Addtionally, if $\gamma$ is closed it is specially denoted as

$$ \oint_\gamma f(z) \, |dz| $$

************Prop:************ Let $f,g: \Omega\subseteq \Bbb C \to \Bbb C$, and $\gamma:[a,b] \to \Omega$, and $\delta:[c,d] \to \Omega$ be piecewise smooth, then they satisfy the following properties:

$$ \left|\int_\gamma f(z) \ |dz|\right| \le \int_\gamma|f(z)| \, |dz| $$

Let $\alpha, \beta \in \Bbb C$, then

$$ \int_\gamma \alpha f(z) +\beta g(z)\ |dz| = \alpha \int_\gamma f(z) \ |dz| + \beta \int_\gamma g(z) \ |dz| $$

Let $\gamma(b) = \delta (c)$, we can concatete paths, denoted as $\gamma * \delta$, and get:

$$ \int_{\gamma * \delta} f(z) \, |dz| = \int_\gamma f(z) \ |dz|+ \int_\delta f(z) \ |dz| $$

If $\delta$ is a reparemetrization of $\gamma$, then

$$ \int_\delta f(z) \ |dz| = \int_\gamma f(z) \ |dz| $$

in particular

$$ \int_{\gamma^-} f(z) \ |dz| = \int_\gamma f(z) \ |dz| $$