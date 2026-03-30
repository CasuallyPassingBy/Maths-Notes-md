---
tags:
  - DifferentialGeometry
  - GroupTheory
---
Subjects: [[Differential Geometry]], [[Group Theory]]
Links: [[Lie Groups]], [[Lie Subgroups]], [[Lie Algebras]], [[Lie Algebra of a Lie Group]], [[The Exponential Map on Lie Groups]], [[Normal Subgroups and Quotient Groups]], [[Representations of Groups]], [[Lie Derivative]]

**Lemma:** Let $G$ be a connected Lie group, and let $H \subseteq G$ be a connected Lie subgroup. Let $\frak g$ and $\frak h$ denote the Lie algebras of $G$ and $H$, respectively. Then $H$ is normal in $G$ iff $$(\exp X)(\exp Y)(\exp(-X)) \in H \qquad \text{for all } X\in {\frak g} \text{ and }Y\in {\frak h} .$$

## The Adjoint Representation

Let $G$ be a Lie group and $\frak g$ be its Lie algebra. For any $g\in G$, the conjugation map $C_g: G \to G$ given by $C_g(h) := ghg^{-1}$ is a Lie group homomorphism. We let $\text{Ad}(g) := (C_g)_*: \frak g \to g$ denote its induced Lie algebra homomorphism.

**The Adjoint Representation:** If $G$ is a Lie group with Lie algebra $\frak g$, the map $\text{Ad}: G \to \text{GL}({\frak g})$ is a Lie group representation, called the *adjoint representation of $G$.*

Given a finite-dimensional Lie algebra $\frak g$, for each $X\in \frak g$, define a map $\text{ad}(X): \frak g \to g$ by $\text{ad}(X)Y := [X, Y]$. 

**Prop:** For any Lie algebra $\frak g$, the map $\text{ad}: {\frak g}\to {\frak gl}({\frak g})$ is a Lie algebra representation, called the *adjoint representation of $\frak g$.*

**Th:** Let $G$ be a Lie group, let $\frak g$ be its Lie algebra, and let $\text{Ad}: G \to \text{GL}({\frak g})$ be the adjoint representation of $G$. The induced Lie algebra representation $\text{Ad}_*: {\frak g}\to {\frak gl}({\frak g})$ is given by $\text{Ad}_* = \text{ad}$. 

## Ideals and Normal Subgroups

**Ideals and Normal Subgroups:** Let $G$ be a connected Lie group, and suppose $H \subseteq G$ is a connected Lie subgroup. Then $H$ is a normal subgroup of $G$ iff $\text{Lie}(H)$ is an ideal in $\text{Lie}(G).$

