---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Intro to Surfaces]], [[Riemann Integral in Rn]]

**********Def:********** Let $S$ be a surface parameterized by $\sigma:A\subseteq\Bbb R^2\to \Bbb R^3$ and $f:S\subseteq \Bbb R^3\to \Bbb R$ such that $f\circ \sigma$ be integrable over $A$. We define the surface integral of $f$ over $S$ with the parameterization $\sigma$, as

$$ \int_S f\, dS=\int_S f \,\|d\sigma\| = \int_A f(\sigma(x,y))\cdot \left\|\frac{\partial \sigma}{\partial x}(x,y) \times \frac{\partial \sigma}{\partial y}(x,y)\right\| $$

Where $dS$ represents the differential area of the surface.

************Prop:************ Let $S$ be a surface parameterized by $\sigma:A\subseteq\Bbb R^2\to \Bbb R^3$ and $f, g:S\subseteq \Bbb R^3\to \Bbb R$ such that $f\circ \sigma$ and $g \circ \sigma$ integrable over $A$, with $\alpha, \beta\in \Bbb R$. Then

$$ \int_S (\alpha f+\beta g) \,\|d\sigma\| =\alpha \int_S f \,\|d\sigma\| + \beta \int_S g \,\|d\sigma\| $$

************Prop:************ Let $S\subseteq \Bbb R^3$ be a surface parameterized by $\sigma:A\subseteq\Bbb R^2\to \Bbb R^3$, and $f:S\subseteq \Bbb R^3\to \Bbb R$ such that $f\circ \sigma$ be integrable over $A$. If $\tilde \sigma :B\subseteq\Bbb R^2 \to \Bbb R^3$ is a reparameterization of $S$, then

$$ \int_S f \, \|d\sigma\| = \int_S f \, \|d\tilde\sigma\| $$

**********Def:********** Let $S = S_1 \cup \cdots\cup S_k\subseteq \Bbb R^3$ be a piecewise surface with $\sigma_i :A_i \subseteq \Bbb R^2\to \Bbb R^3$ be a parametrization of $S_i$, for all $i \in \{1,\dots, k \}$, and $f:S \subseteq \Bbb R^3\to \Bbb R$ be such that for any ${i \in \{1, \dots, k\}}$, $f\circ \sigma_i$ is integrable over $A_i$, then

$$ \int_S f \, \|d\sigma\| = \sum_{i = 1}^k \int_{S_i} f \, \|d\sigma_i\| $$