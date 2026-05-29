---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Separable, First and Second Countable Spaces]], [[Limit Points and Closure]]

**Def:** The *density of a space $X$* is defined as: $$d(X):= \min\{|D| \mid D \subseteq X, D\text{ is dense in} X\}.$$If $d(X) \le \aleph_0$, then we say that $X$ is separable.

**Prop:** For every topological space $X$ we have that $d(X) \le w(X)$. 

This actually gives us a nice proof for separable implies separable. 

**Th:** If there's a a continuous surjective function $f: X \to Y$, then $d(Y) \le d(X)$.

**Cor:** A continuous image of separable space is separable

**Th:** For every [[Hausdorff Spaces|Hausdorff space]] we have that $|X| \le 2^{2^{d(X)}}$ and $|X| \le [d(X)] ^{\chi(X)}$.

**Th:** For every [[Regular Hausdorff Spaces|regular Hausdorff space]] we have $w(X) \le 2^{d(X)}$.