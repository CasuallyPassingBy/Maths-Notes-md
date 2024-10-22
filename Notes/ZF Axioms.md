---
tags:
  - Axioms
  - SetTheory
---
Subjects: [[Set Theory]]

## Axiom of Extensionality:

$$ \forall x \forall y[\forall z (z\in x \iff z\in y) \implies x = y] $$

## Axiom of regularity:

$$ \forall x[\exists a (a \in x)\implies \exists y(y \in x \land \lnot\exists
z[z \in y \land z\in x])] $$

## Axiom schema of specification:

$$ \forall x \exists y [\forall z (z \in y \implies z\in x \land \varphi(z))] $$

where $\varphi$ is a _specification._

## Axiom of pairing:

$$ \forall x\forall y\exists z [x\in z \land y\in z] $$

## Axiom of union:

$$ \forall\mathcal{F}\exists 
A\forall y\forall x[(x\in y\land y\in \mathcal{F})\implies x\in A] $$

## Axiom of powerset:

$$ \forall x \exists y \forall z[\forall u(u \in z \implies u \in x)\implies z\in y] $$

## Axiom schema of replacement:

$$ \forall x[\forall y (y \in x \implies \exists! z[\varphi(y,z)])\implies \exists U\forall y(y\in x \implies \exists z[z\in U \land \varphi(y,z)])] $$

## Axiom of infinity:

$$ \exists X[\varnothing \in X \land \forall y (y\in X \implies S(y) \in X)] $$