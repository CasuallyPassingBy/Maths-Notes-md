---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Arithmetic of Cardinal Numbers]], [[Regular and Singular Cardinals]], [[Bases, Subbases, and Local Basis for Topological Spaces]], [[Dense Subsets]]

# Weight and Character

**Def:** Let $(X, \tau)$ be a topological space. We define the *weight of space* $(X, \tau)$ is the $$w((X, \tau)) := \min\{|\mathcal B| \mid \mathcal B \subseteq \tau, \text{ where }\mathcal B \text{ is base for }\tau\}.$$If the topology is clear, then it is denoted $w(X)$.

**Def:** The *character of a point* $x$ in a topological space $(X, \tau)$ is defined as $$\chi(x, (X, \tau)) := \min\{|\mathcal B(x)| \mid B(x) \subseteq \tau, \text{ where }\mathcal B \text{ is a local base for }x\}. $$If the topology is clear is denoted as $\chi(x, X)$. The *character of a topological space* $(X, \tau)$ is defined as $$\chi(X, \tau) := \sup\{\chi(x, (X, \tau)) \mid x \in X\}.$$If the topology is clear, then it is denoted as $\chi(X)$. 

**Obs:** If we have that $\chi(X, \tau) \le \aleph_0$ then we note that this equivalent to the space being [[Separable, First and Second Countable Spaces|first countable]]. If we have that $w(X, \tau) \le \aleph_0$ this is equivalent to the space being [[Separable, First and Second Countable Spaces|second countable]]. 

**Th:** If $w(X) \le \mu$, then for every family $\{U_\alpha \mid \alpha < \kappa\} \subseteq \tau$ there exists a set $S \subseteq \kappa$ such that $|S| \le \mu$ and $$\bigcup_{\alpha \in S} U_\alpha = \bigcup_{\alpha < \kappa} U_\alpha.$$
**Th:** If $w(X)\le \mu$ then for every $\cal B$ for $X$ there exists a $\mathcal B_0$ such that $|\mathcal B_0|\le \mu$ and $\mathcal B_0 \subseteq \mathcal B$. 

**Th:** If $f: X \to Y$ is an open mapping, then for every $x \in X$ we have $\chi(f(x), Y) \le \chi(x, X)$. If, moreover, $f$ is surjective, then $w(Y) \le w(X)$, and $\chi(Y) \le \chi(X)$. 

**Th:** For every [[Kolmogorov Spaces|Kolmogorov space]] we have $|X| \le 2^{w(X)}$.   
# Density

**Def:** The *density of a space $X$* is defined as: $$d(X):= \min\{|D| \mid D \subseteq X, D\text{ is dense in} X\}.$$If $d(X) \le \aleph_0$, then we say that $X$ is separable.

**Prop:** For every topological space $X$ we have that $d(X) \le w(X)$. 

This actually gives us a nice proof for separable implies separable. 

**Th:** If there's a a continuous surjective function $f: X \to Y$, then $d(Y) \le d(X)$.

**Cor:** A continuous image of separable space is separable

**Th:** For every [[Hausdorff Spaces|Hausdorff space]] we have that $|X| \le 2^{2^{d(X)}}$ and $|X| \le [d(X)] ^{\chi(X)}$.

**Th:** For every [[Regular Hausdorff spaces|regular Hausdorff space]] we have $w(X) \le 2^{d(X)}$.

