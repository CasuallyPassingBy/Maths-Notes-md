---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Intro to Surfaces]], [[Riemann Integral in Rn]]
**********Def:********** Let $S$ be a surface parameterized by $\sigma:A\subseteq\Bbb R^2\to \Bbb R^3$ and $F:S\subseteq \Bbb R^3\to \Bbb R^3$ such that each $F_k\circ \sigma$ be integrable over $A$, for $k =1,2,3$. We define the surface integral of $F$ over $S$ with the parameterization $\sigma$, as

$$ \int_S (F \cdot \hat n)\, dS=\int_S F \cdot \,d\sigma = \int_A F(\sigma(x,y))\cdot \left(\frac{\partial \sigma}{\partial x}(x,y) \times \frac{\partial \sigma}{\partial y}(x,y)\right) $$

Where $\hat n$ represents the unit normal vector to the surface.

************Prop:************ Let $S$ be a surface parameterized by $\sigma:A\subseteq\Bbb R^2\to \Bbb R^3$ and $F, G:S\subseteq \Bbb R^3\to \Bbb R$ such that each component $F_k\circ \sigma$ and $G_k \circ \sigma$ integrable over $A$(for $k = 1,2,3$), with $\alpha, \beta\in \Bbb R$. Then

$$ \int_S (\alpha F+\beta G) \cdot \,d\sigma =\alpha \int_S F \cdot \,d\sigma + \beta \int_S G \cdot \,d\sigma $$

************Prop:************ Let $S\subseteq \Bbb R^3$ be a surface parameterized by $\sigma:A\subseteq\Bbb R^2\to \Bbb R^3$, and $f:S\subseteq \Bbb R^3\to \Bbb R$ such that $f\circ \sigma$ be integrable over $A$. If $\tilde \sigma :B\subseteq\Bbb R^2 \to \Bbb R^3$ is a reparameterization of $S$, then

- If $\sigma$ and $\tilde \sigma$ have the same orientation then
    
    $$ \int_S F \cdot \,d\sigma = \int_S F \cdot \,d\tilde\sigma $$
    
- If $\sigma$ and $\tilde \sigma$ don’t have the same orientation then
    

$$ \int_S F \cdot \,d\sigma = -\int_S F \cdot \,d\tilde\sigma $$