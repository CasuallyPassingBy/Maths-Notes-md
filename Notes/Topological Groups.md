---
tags:
  - GroupTheory
  - Topology
---
Subjects: [[Group Theory]], [[Topology]]
Links: [[Product Topology]], [[Groups]], [[Continuous Functions and Homeomorphims]], [[Subgroups]], [[Topological Subspaces]], [[Product Topology]], [[Homogeneous Spaces]], [[Topological Indistinguishability]], [[Topological Vector Spaces]]

**Def:** Let $(G, *)$ be a group. Let $\tau$ be topology on the set $G$. We say that the triple $(G, *, \tau)$ is a *topological group* if the function $\mu: G \times G \to G$ and $\iota: G \to G$, defined as $\mu(x,y) = x* y$ and $\iota(x) = x^{-1}$, are continuous. 

**Def:** Let $G$ be a topological group, we say that $G$ is discrete if it is equipped with the discrete topology.

**Prop:** If $H$ is subgroup of $(G, *)$, then $\mu$ and $\iota$ are continuous on $H$ with the subspace topology. Then $(H, *, \tau_H)$ is topological group.

**Def:** If $(H, *, \tau_H)$ is a topological group and $H$ is contained in $(G, *, \tau)$ is a topological group$, then $(H, *, \tau_H)$ is a topological subgroup of $(G, *, \tau)$.

**Def:** Let $A$ and $B$ be subsets of the topological group $G$. We will denote $$A* B : = \{a * b \mid a \in A \mid b \in B\},$$ and $$A^{-1}:= \{a^{-1} \mid a \in A\}.$$In the special case where $A$ is a single point, then we will denoted $x*B$ or $xB$ instead of $\{x\}*B$.  

**Prop:** The group operation $*: G \times G \to G$ of a topological group is open, continuous and surjective. 

**Prop:** The Tychonoff product $G = \prod_{\alpha < \kappa} G_\alpha$ of a nonempty collection of topological groups $\{(G_\alpha, *_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ is a topological group when considering the product $f*g$, for elements $f, g\in G$, as the element on $G$ that for every $\beta < \kappa$, the element $f(\beta)*_\beta g(\beta) \in G_\beta$. Meaning that we get that $\pi_\beta \circ * = *_\beta \circ (\pi_\beta \times \pi_\beta)$. This makes the following diagrams commute

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
G \times G \arrow[r, "*"] \arrow[d, "\pi_\beta \times \pi_\beta"'] &G \arrow[d, "\pi_\beta"] \\ 
G_\beta \arrow[r, "*_\beta"']& G_\beta
\end{tikzcd}
\end{document}
```
and 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}
G  \arrow[r, "\iota"] \arrow[d, "\pi_\beta "'] &G \arrow[d, "\pi_\beta"] \\ 
G_\beta \arrow[r, "\iota_\beta"']& G_\beta
\end{tikzcd}
\end{document}
```

**Prop:** Since $(\Bbb R, +, \tau)$ is a topological group, then for any set $X$ the set $\Bbb R^X$ is a topological group. If $X$ is also a topological space the set of continuous functions $\mathcal C^0(X)$ is a topological subgroup of $\Bbb R^X$.

**Prop:** We see that for any topological group $(G, *, \tau)$ and any fixed $a\in G$, the $\ell_a(x) =ax$ and $r_a(x) = xa$ are homeomorphisms.

**Prop:** Every topological group is [[Homogeneous Spaces|homogeneous]]. 

**Cor:** If $A$ is a subset of a topological group $G$. If $x$ is an interior point $A$, then there's a an open set $e\in V \in \tau$, such that $xV \subseteq A$. 

**Cor:** A subgroup $H$ of a topological group $G$ is discrete iff $H$ has an isolated point. 

**Prop:** A topological subgroup $H$ of  $G$ is open iff its interior is nonempty. 

**Prop:** Let $A$ and $B$ be subsets of a topological group $G$, then $(\text{cl}_G A) * (\text{cl}_G B) \subseteq \text{cl}_G(A * B)$, and $(\text{cl}_G A)^{-1} = \text{cl}_G(A^{-1})$. 

**Cor:** If $H$ is a topological subgroup of $G$, then $\text{cl}_G H$ is also a topological subgroup of $G$.

**Prop:** Let $G$ be a topological group, and $x, y\in G$. The points $x$ and $y$ are topological indistinguishable if $xy^{-1}\in \text{cl}(\{e\})$. 

**Prop:** Every topological group is regular. 

**Prop:** Every topological group that is $T_0$ it is also $T_1$.

**Prop:** Every topological group that is $T_1$ is also $T_2$. 

**Cor:** A topological group that is $T_0$ iff $T_3$.

**Def:** Let $H$ be a subgroup of $G$, where $G$ is a topological group. We know that $G/H$ is the set of all *left cosets modulo $H$*, we can endow $G/H$ with the topology determined by the natural quotient map $\pi: G \to G/H$ sending each element $g\in G$ to its coset. 