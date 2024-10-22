---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Continuity on R]], [[Functional Limits in R]]
We can define that a function might be discontinuous at some point, but it can be right, or left continuous. We formally define $f$ is right-continuous at the point $c$ if the following holds: for any $\varepsilon>0$, there’s a $\delta >0$ such that if $x$ is in the domain, with ${c < x <c+\delta}$, then

$$ |f(x) - f(c) | < \varepsilon $$

In the [[Functional Limits in R#Left and Right Limits|language of limits]], we have that

$$ \lim_{x \to c^+} f(x) = f(c) $$

We have that the [[Probability Functions for Random Variables|cumulative probabilty functions]] are right continuous.
Similarly, we can define the left-continuity as for any $\varepsilon>0$, there’s a $\delta >0$ such that if $x$ is in the domain, with ${c -\delta < x <c}$, then

$$ |f(x) - f(c) | < \varepsilon $$

In the [[Functional Limits in R#Left and Right Limits|language of limits]], we have that

$$ \lim_{x \to c^-} f(x) = f(c) $$

A function is continuous at $c$ iff it is right-continuous and left-continuous at $c$