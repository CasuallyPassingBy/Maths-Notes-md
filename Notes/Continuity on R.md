---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Functional Limits in R]], [[Open and Closed Sets in R]]

$f:D\to\Bbb{R}$, let $c\in D$, $f$ is a continuous at $c$ iff:

## Definitions

### $\varepsilon$-$\delta$ Definition

$$ \forall\varepsilon>0\exists\delta>0\forall x\in D[|x-c|<\delta\implies|f(x)-f(c)|<\varepsilon] $$

### Sequential Definition

$$ \forall (x_n)_{n\in\Bbb{N}}\subseteq D[ \lim_{n\to\infty}x_n=c\implies\lim_{n\to\infty}f(x_n)=f(c)] $$

### Topological Definition

Given a neighbourhood $V$ of $f(c)$, then there’s a neighbourhood $U$ of $c$, such that $f(U)\subseteq V$.

$$ \forall\varepsilon>0\exists\delta>0\forall x\in D[x\in V_\delta(c)\implies f(x)\in V_\varepsilon(f(c))] $$

Let $O$ be an open subset relative to $f(D)$, $f$ is continuous on $D$ iff $f^{-1}(O)$ is open

### Divergence Criterion

Let $(x_n)$ $\subseteq D$ such that $\lim_{n\to\infty}x_n =c$, such that $\lim\limits_{n\to\infty}f(x_n)\neq f(c)$. Then, $f$ is discontinuous at $c$ .

## Algebraic properties

Let $f, g:D\to\Bbb{R}$, where $f$ and $g$ are continuous at $c$ then:

1. for any $\alpha\in\Bbb{R}, \alpha f$ is continuous at $c$
2. $f+g$ is continuous at $c$
3. $fg$ is continuous at $c$

## Composition of Continuous Functions

Given $f:A\to\Bbb{R}$, and $g:B\to\Bbb{R}$, assume $f(A)\subseteq B$, so that $g\circ f$ is well defined. Let $f$ be continuous at $c$, and $g$ be continuous at $f(c)$, then $g\circ f$ is continuous at $c.$

_**Corollary:**_ If $g$ is continuous, then:

$$ \lim_{x\to c}(g(f(x)) = g(\lim_{x\to c}f(x)) $$

## Preservation of Compactness

Let $f:A\to\Bbb{R}$, where $K$ be a [[Compact Sets in R|compact subset]] of $A$, then $f(K)$ is also compact.

## Extreme Value Theorem

Let $f:K\to\Bbb{R}$, is continuous on $K\subseteq\Bbb{R}$, then $f$ attains a maximum and a minimum value. In other words there are $x_1$ and $x_2$ such that $f(x_1)\le f(x)\le f(x_2)$, for all $x\in K$

## Continuity of the Inverse

Let $f:D\to\Bbb{R}$, is continuous and injective, defining $f^{-1}$ over the $f(D)$ in the natural way: $f(x) = y$ iff $f^{-1}(y) =x$, then $f^{-1}$ is continuous on $f(D)$.


We have stronger version like [[Uniform Continuity on R]]

We can also explore the [[Discontinuities on R]] and how they behave