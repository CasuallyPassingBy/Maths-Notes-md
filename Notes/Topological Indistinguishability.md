---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Kolmogorov Spaces]], [[Topological Spaces]], [[Bases, Subbases, and Local Basis for Topological Spaces]], [[Pre-orderings]], [[T1 Spaces]], [[Alexandroff Topologies]]

**Def:** Let Let $(X, \tau)$ be a topological space, and $x\in X$, the set of all neighbourhood of $x$ is denoted as $\mathcal N_x$

**Def:** Let $(X, \tau)$ be a topological space. We say that $x$ and $y$ are topologically indistinguishable if $\mathcal N_x = \mathcal N_y$. We denote this as $x\sim y$. 

**Def:** Let $(X, \tau)$ be a topological space. We say that $x$ and $y$ are topologically distinguishable if they are not indistinguishable. Meaning that there is an open set $U \in \tau$ such that $|U \cap \{x, y\}| = 1$. 

A $T_0$ space is a topological space in which every pair of distinct points is topologically distinguishable. 

# Specialisation Preorder

**Def:** The *specialisation preorder* $\le$ on $X$ we define $x \le y$ iff $$x \in \text{cl}\{y\}. $$
**Prop:** $x\le y$ iff $\text{cl}\{x\} \subseteq \text{cl}\{y\}$. Equivalently $x\le y$ iff $\mathcal N_x \subseteq \mathcal N_y$. We see that $\le$ is reflexive and transitive. 

The equivalence relation determined by $\le$ is precisely  topologically indistinguishability. $$x\sim y \iff \mathcal N_x = \mathcal N_y$$
**Prop:** The following statements are equivalent:
- $x\sim y$.
- For each $U \in \tau$, $U$ containes either both $x$ and $y$ or neither.
- $\mathcal N_x = \mathcal N_y$.
- $x \in \text{cl}\{y\}$ and $y \in \text{cl}\{x\}$.
- $x \in  \bigcap \mathcal N_y$ and $y \in\bigcap \mathcal N_x$. 
- $\bigcap\mathcal N_x = \bigcap\mathcal N_y$
- $x \in \text{cl}\{y\}$ and $x \in \bigcap\mathcal N_y$
- $x$ beloongs to every open set and closed set containing $y$.
- A net or a filer converges to $x$ iff it converges to $y$.

A topological space is said to be *symmetric* if the specialization preorder is *symmetric*, i.e.,  $x\le y$ implies $y \le x$. 

**Prop:** The following statements are equivalent if the space is symmetric
- $x\sim y$.
- For each $U \in \tau$, if $x \in U$ then $y \in U$
- $\mathcal N_x \subseteq \mathcal N_y$
- $x \in \text{cl}\{y\}$
- $x \in \bigcap\mathcal N_y$
- $x$ belongs to every closed set containing $y$
- $x$ belongs to every open set containing $y$
- A net or a filer that converges to $x$ converges to $y$.

### Equivalence classes

The lower set of $x$ is just the closure of $\{x\}$. Meaning $$\downarrow x = \text{cl}\{x\}.$$while the upper set of $x$ is the intersection of the neighbourhood system at $x$ $$\uparrow x = \bigcap \mathcal N_x.$$Meaning that the equivalence class of $x$ is the intersection of the lower and upper set of $x$: $$[x] = \downarrow x \;\cap \uparrow x.$$
In general, both the lower and upper sets of $x$ can contain additional points. In symmetric space we have that all of them coincide: $$[x] = \text{cl}\{x\} = \bigcap \mathcal N_x$$