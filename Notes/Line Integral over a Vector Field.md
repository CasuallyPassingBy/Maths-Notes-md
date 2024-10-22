---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Rectifiable Curves in Rn]], [[Riemann Integral in R]], [[Vector Valued Functions of Rn]]

Def: Let $U\subseteq \Bbb R^n$ be an open an connected set, a curve $\Gamma \subseteq U$ and $\gamma:[a,b]\to \Bbb R^n$ be a piecewise smooth function such that $\Gamma = \gamma[[a,b]]$, and the function ${F= (F_k )_{k = 1}^n: U \to \Bbb R^n}$ a function such that for any $F_k \circ \gamma$ be integrable over $[a,b]$ for any $k \in \{1, \dots, n\}$. We define the integral of $F$ over the curve $\Gamma$ with the parametrization $\gamma$ as

$$ \int_\Gamma F\cdot \,dr = \int_\Gamma F \cdot \, d\gamma = \int_a^b F(\gamma(t)) \cdot \gamma'(t) \, dt $$

Where $dr$ is representing the differential of position, in a weireder notation we get that

$$ \int_\Gamma F\cdot \, dr = \int_\Gamma \sum_{k = 1}^n F_i \, dx_i $$

If the curve is closed it can be denoted as follows, but it doesn’t change the nature of the calculation:

$$ \oint_\Gamma f \cdot\, d\gamma = \oint_\Gamma f \cdot \, dr $$

********Prop:********* Let $U\subseteq \Bbb R^n$ be a open and connected set, and $\Gamma \subseteq U$ be piecewise smooth and ${\gamma :[a,b] \to \Bbb R^n}$ be a piecewise smooth parametrization of $\Gamma$. Let $F, G :U \to \Bbb R^n$ be such that $F_k\circ\gamma$ and $G_k\circ \gamma$ be integrable over $[a,b]$ for any $k \in \{1, \dots, n\}$, and $\alpha , \beta \in \Bbb R$, then

$$ \int _\Gamma (\alpha F +\beta G)\cdot\, d\gamma = \alpha\int_\Gamma F \cdot\, d\gamma + \beta \int_\Gamma G \cdot\, d\gamma $$

Prop:************ Let $U\subseteq \Bbb R^n$ be a open and connected set, and $\Gamma, \Delta \subseteq U$ and piecewise smooth curves parametrized by $\gamma:[a, b]\to \Bbb R^n$ and ${\delta:[c,d]\to \Bbb R^n}$ respectively, such that $\Gamma \cup \Delta$ be piecewise smooth [[Rectifiable Curves in Rn#Concatenation of Paths|parametrized by]] $\gamma * \delta$ . If $F:U \to \Bbb R$ is such that $F_k\circ \gamma$ and $F_k\circ \delta$ be integrable over their respective intervals for any $k \in \{1, \dots, n\}$ then

$$ \int_{\Gamma \cup \Delta} f\cdot \, d(\gamma * \delta) = \int_\Gamma f \cdot \, d\gamma + \int _\Delta f \cdot \, d\delta $$

Cor:************ Let $\Gamma \subseteq \Bbb R^n$ be a piecewise smooth nonsimple curve with a finite number of intersections parametrized by $\gamma:[a, b]\to \Bbb R^n$, then we can split $\gamma$ into $\gamma_1, \dots, \gamma_k$ simple curves such that $\gamma= \gamma_1 * \cdots *\gamma_k$

$$ \int_\Gamma f\, \cdot d\gamma = \sum_{i = 1}^k \int_{{\Gamma_i}} f\,\cdot d{\gamma_i} $$

Prop:************ Let $U\subseteq \Bbb R^n$ be a open and connected set, and $\Gamma \subseteq U$ be piecewise smooth and ${\gamma :[a,b] \to \Bbb R^n}$ and $\delta:[c,d]\to \Bbb R^n$ be piecewise smooth parametrizations of $\Gamma$, and ${F:U\to \Bbb R^n}$ be such that $F_k\circ \gamma$ and $F_k\circ \delta$ be integrable for in their respective intervals for any $k \in \{1, \dots, n\}$. If there’s and $\alpha :[c, d] \to [a,b]$ be a $\cal C^1$ bijection with the property that ${\delta = \gamma \circ \alpha}$, then

- If $\alpha$ preserves orientation, then
    $$ \int_\Gamma F \cdot\, d\gamma = \int_\Gamma F \cdot\, d\delta $$
- If $\alpha$ changes orientation, then
    $$ \int_\Gamma F \cdot\, d\gamma = -\int_\Gamma F \cdot\, d\delta $$
    In particular
    
    $$ \int_\Gamma F \cdot\, d\gamma = -\int_\Gamma F \cdot\, d\gamma^- $$