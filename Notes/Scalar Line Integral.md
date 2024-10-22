---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Rectifiable Curves in Rn]], [[Riemann Integral in R]], [[Real-valued Functions of Rn]]

**********Def:********** Let $\Gamma \subseteq \Bbb R^n$ a piecewise smooth curve, parametrized by piecewise smooth function ${\gamma:[a,b] \to \Bbb R^n}$. If $f:\Gamma \subseteq\Bbb R^n \to \Bbb R$ is such that $f \circ \gamma$ is integrable over $[a,b]$, we define the ****************_line integral of $f$ over $\Gamma$ with the parametrization $\gamma$,_ denoted $(\int_\Gamma f \,\|d\gamma\|)$ as
$$ \int_\Gamma f \,ds=\int_\Gamma f \, \|d\gamma\| = \int_a^b f(\gamma(t)) \cdot \|\gamma'(t)\| dt $$

where $ds$ represents the differential arc-length of the curve and it is given by the formula .

$$ ds: = \|\gamma'(t)\| dt $$
If the curve is closed it can be denoted as follows, but it doesn’t change the nature of the calculation:
$$ \oint_\Gamma f \, \|d\gamma\| = \oint_\Gamma f \, ds $$

Prop:************ Let $\Gamma \subseteq \Bbb R^n$ be piecewise smooth and $\gamma :[a,b] \to \Bbb R^n$ be a piecewise smooth parametrization of $\Gamma$. Let $f, g :\Gamma \subseteq\Bbb R^n \to \Bbb R$ be such that $f\circ\gamma$ and $g\circ \gamma$ be integrable over $[a,b]$, and $\alpha , \beta \in \Bbb R$, then

$$ \int _\Gamma (\alpha f +\beta g)\, \|d\gamma\| = \alpha\int_\Gamma f \, \|d\gamma\| + \beta \int_\Gamma g \, \|d\gamma\| $$

Prop:************ Let $\Gamma, \Delta \subseteq\Bbb R^n$ and piecewise smooth curves parametrized by $\gamma:[a, b]\to \Bbb R^n$ and ${\delta:[c,d]\to \Bbb R^n}$ respectively, such that $\Gamma \cup \Delta$ be piecewise smooth [[Rectifiable Curves in Rn#Concatenation of Paths|parametrized by]] $\gamma * \delta$ . If $f:\Gamma \cup \Delta \subseteq \Bbb R^n \to \Bbb R$ is such that $f\circ \gamma$ and $f\circ \delta$ be integrable over their respective intervals then

$$ \int_{\Gamma \cup \Delta} f\,\|d(\gamma * \delta)\| = \int_\Gamma f \, \|d\gamma\| + \int _\Delta f \, \|d\delta\| $$

Cor:************ Let $\Gamma \subseteq \Bbb R^n$ be a piecewise smooth nonsimple curve parametrized by $\gamma:[a, b]\to \Bbb R^n$, then we can split $\gamma$ into $\gamma_1, \dots, \gamma_k$ simple curves such that $\gamma= \gamma_1 * \cdots *\gamma_k$, then
$$ \int_\Gamma f\, \|d\gamma\| = \sum_{i = 1}^k \int_{\Gamma_i} f\, \| d\gamma_i\| $$
Prop:************ Let $\Gamma \subseteq \Bbb R^n$ be piecewise smooth and $\gamma :[a,b] \to \Bbb R^n$ and $\delta:[c,d]\to \Bbb R^n$ be piecewise smooth parametrizations of $\Gamma$, and $f:\Gamma \subseteq \Bbb R^n\to \Bbb R$ be such that $f\circ \gamma$ and $f\circ \delta$ be integrable over the respective intervals. If there’s and $\alpha :[c, d] \to [a,b]$ be a $\cal C^1$ bijection with the property that ${\delta = \gamma \circ \alpha}$, then
$$ \int_\Gamma f \, \|d\gamma\| = \int_\Gamma f \, \|d\delta\| $$
Prop (Mean Value Theorem for Line Integrals):************ Let $\Gamma \subseteq \Bbb R^n$ be piecewise smooth and $\gamma :[a,b] \to \Bbb R^n$ be a piecewise smooth parametrization of $\Gamma$. Let $f,:\Gamma \subseteq\Bbb R^n \to \Bbb R$ be continuous, then there’s an $x_0 \in \Gamma$ such that
$$ \frac{1}{\Lambda(\Gamma)}\int _\Gamma f\, \|d\gamma\| = f(x_0)  
$$