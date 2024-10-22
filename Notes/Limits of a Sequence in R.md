---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Let $f : \mathbb{N} \to \mathbb{R}$ is defined to be a sequence. Usually denoted as $(a_n)_{n \in \mathbb{N}}$ or $(a_n)_{n = 1}^{\infty}$ since it is easier to work without the number zero in this case.

## **Definition**

_A sequence is defined to converge to a value $a$ if and only if_

$$ \forall \varepsilon > 0\exists N \in \mathbb{N} [ \forall n \geq N (|a_n - a| < \varepsilon)] $$

In this case $a$ is the limit of the sequence, and more informally it is also denoted as $a_n \to a$, and $\lim_{n \to \infty } a_n = a$ will be the more formal way to write it.

## Limits to infinity

We say that $(a_n)$ _tends to_ $\infty$ if and only if

$$ \forall M > 0 \exists N \in \mathbb{N} \left[\forall n \geq N (a_n > M) \right] $$

Similarly for when $(a_n)$ _tends to $-\infty$:_

$$ \forall M < 0 \exists N \in \mathbb{N} \left[\forall n \geq N (a_n < M) \right] $$

Also it will be useful to define a neighborhood around a certain point in particular will be called an $\varepsilon$ neighborhood as:

$$ V_{\varepsilon}(a) =B(a; \varepsilon)= \{x \in \mathbb{R} : |x-a| < \varepsilon\} $$

There are two useful definitions:

- A sequence $(a_n)$ is _eventually_ in a set $A \subseteq \mathbb{R}$ $\Leftrightarrow\exists N \in \mathbb{N}[\forall n\geq N (a_n \in A)]$
- A sequence $(a_n)$ is _frequently_ in a set $A \subseteq \mathbb{R}$ $\Leftrightarrow \forall N \in \mathbb{N} [\exists n \geq N(a_n \in A)]$

Consequently there is a new way to write the convergence of the sequence $(a_n)_{n= 1}^{\infty}$ as a topological version:

$$ \forall \varepsilon > 0\exists N \in \mathbb{N} [ \forall n \geq N (a_n \in V_{\varepsilon} (a))] $$

**The Uniqueness of Limits:** the limit of a sequence, when it exists, is unique.
## Boundedness

_**Definition:** Boundedness of a sequence._ A sequence $(x_n)$ is _bounded_ if and only if $\exists M > 0\forall n\in\mathbb{N}[|x_n| \leq M]$ or in other words the output of the sequence $(x_n)$ is contained in the interval $[-M, M]$.

_**Every convergent sequence is bounded**_

## Cauchy’s Criterion

A sequence $(a_n)$ is Ca_uchy_ if and only if:

$$ \forall\varepsilon>0\exists N \in\mathbb{N}[\forall n,m\geq N(|a_n-a_m| < \varepsilon)] $$

Every Cauchy sequence is bounded.

Every Convergent sequence is Cauchy.

Through, the [[Properties of Limits of Sequences in R#Bolzano–Weierstrass theorem|Bolzano–Weierstrass theorem]], every Cauchy sequence is convergent, thus the real number line is a [[Complete Metric Spaces|complete space]].