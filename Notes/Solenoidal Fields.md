---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Vector Surface Integral]], [[Conservative Fields]], [[Gauss's Theorem and Divergence in R3]], [[Connected Sets in Rn]]
**********Def:********** Let $G:U\subseteq \Bbb R^3\to \Bbb R^3$ is continuous on $U$, an open and connected set. We say that $G$ is ************************solenoidal vector field************************ if there’s $F:U\to\Bbb R^3$ be $\cal C^1$ on $U$ such that

$$ G(x)= \nabla \times F(x) \quad\text{ for all $x\in U$} $$

************Prop:************ Let $F:U\subseteq\Bbb R^3\to \Bbb R^3$ be class $\cal C^1$ is a solenoidal field on $U$, then $\nabla \cdot F = 0$, for all $x \in U$

$(*)$************Th:************ Let $F:U\subseteq\Bbb R^3\to \Bbb R^3$ be class $\cal C^1$ is a solenoidal field on $U$, with $U$ a $2$-connected region. If $\nabla \cdot F =0$ on $U$, then $F$ is a solenoidal field.

************Th:************ Let $F:U\subseteq\Bbb R^3\to \Bbb R^3$ be class $\cal C^1$ is a solenoidal field on $U$, with $U$ a star region. If ${\nabla \cdot F =0}$ on $U$, then $F$ is a solenoidal field.

********Th:******** Let $F: U\subseteq \Bbb R^3 \to \Bbb R^3$ be class $\cal C^1$ be a solenoidal field, then for any closed surface $S$ with parametrization $\sigma$, then

$$ \oint_S F \cdot \, d\sigma = 0 $$