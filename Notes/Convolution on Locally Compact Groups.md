---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Topological Groups]], [[Haar Measure]], [[Measures on Hausdorff Spaces]], [[Finite Product of Measures]], [[Space of Continuous Compactly Supported Functions]], [[Finite Products of Measures on Locally Compact Spaces]], [[Lp spaces]], [[Local Compactness]]

**Def:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f$ and $g$ belong to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$. The convolution of $f$ and $g$ is the function $f*g$ from $G$ to $\Bbb F$ defined by  $$(f*g)(t):= \begin{dcases}\int f(s) g(s^{-1}t)\, \mu(ds) & \text{if } s\mapsto f(s)g(s^{-1}t) \text{ is integrable,} \\ \\ 0& \text{otherwise}.\end{dcases}$$
**Lemma:** Let $G$ be a locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f\in {\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$. Then there is a countable family $\{K_n\mid n <\omega\}$ of compact subsets of $G$ such that $f$ vanishes outside of $\bigcup_{n<\omega} K_n$. 

**Lemma:** Let $G$ be a locally compact group, let $\mu$ be a left Haar measure on $G$, and let $F: G\times G \to G\times G$ be defined by $F(s, t) := (s, s^{-1}t)$. Then $F$ is a measure-preserving homeomorphism of $G\times G$ onto itself. That is, $F$ is a homeomorphism such that each Borel subset $A$ of $G\times G$ satisfies $(\mu\times\mu)(A) = (\mu\times\mu)(F^{-1}[A])$. 

**Prop:** Let $G$ be an arbitrary locally compact group, let $\mu$ be a left Haar measure on $G$, and let $f$ and $g$ belong to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$.
- The function $s\mapsto f(s)g(s^{-1}t)$ belongs to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$ for $\mu$-almost every $t\in G$.
- The convolution $f*g$ of $f$ and $g$ belongs to ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$ and satisfies $\|f*g\|_1 \le \|f\|_1\|g\|_1.$

We see that the convolution on ${\scr L}^1(G, \mathcal B(G), \mu, \Bbb F)$ induces an operation on $L^1(G, \mathcal B(G), \mu, \Bbb F)$;