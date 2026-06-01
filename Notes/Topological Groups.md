---
tags:
  - GroupTheory
  - Topology
---
Subjects: [[Group Theory]], [[Topology]]
Links: [[Product Topology]], [[Groups]], [[Continuous Functions and Homeomorphims]], [[Subgroups]], [[Topological Subspaces]], [[Product Topology]], [[Homogeneous Spaces]], [[Topological Indistinguishability]], [[Topological Vector Spaces]], [[Separation Axioms]], [[Space of Continuous Compactly Supported Functions]]

**Def:** Let $(G, *)$ be a group. Let $\tau$ be topology on the set $G$. We say that the triple $(G, *, \tau)$ is a *topological group* if the function $\mu: G \times G \to G$ and $\iota: G \to G$, defined as $\mu(x,y) = x* y$ and $\iota(x) = x^{-1}$, are continuous. 

**Def:** Let $G$ be a topological group, we say that $G$ is discrete if it is equipped with the discrete topology.

**Prop:** If $H$ is subgroup of $(G, *)$, then $\mu$ and $\iota$ are continuous on $H$ with the subspace topology. Then $(H, *, \tau_H)$ is topological group.

**Def:** If $(H, *, \tau_H)$ is a topological group and $H$ is contained in $(G, *, \tau)$ is a topological group$, then $(H, *, \tau_H)$ is a topological subgroup of $(G, *, \tau)$.

**Def:** Let $A$ and $B$ be subsets of the topological group $G$. We will denote $$A* B : = \{a * b \mid a \in A \mid b \in B\},$$ and $$A^{-1}:= \{a^{-1} \mid a \in A\}.$$In the special case where $A$ is a single point, then we will denoted $x*B$ or $xB$ instead of $\{x\}*B$.  The set $A$ is *symmetric* if $A = A^{-1}$. Thus $B$ is symmetric iff the condition $x\in A$ is equivalent to $x^{-1}\in A$. 

**Prop:** The group operation $*: G \times G \to G$ of a topological group is open, continuous and surjective. 

**Prop:** The Tychonoff product $G = \prod_{\alpha < \kappa} G_\alpha$ of a nonempty collection of topological groups $\{(G_\alpha, *_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ is a topological group when considering the product $f*g$, for elements $f, g\in G$, as the element on $G$ that for every $\beta < \kappa$, the element $f(\beta)*_\beta g(\beta) \in G_\beta$. Meaning that we get that $\pi_\beta \circ * = *_\beta \circ (\pi_\beta \times \pi_\beta)$. This makes the following diagrams commute

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
G \times G \arrow[r, "*"] \arrow[d, "\pi_\beta \times \pi_\beta"'] &G \arrow[d, "\pi_\beta"] \\ 
G_\beta \arrow[r, "*_\beta"']& G_\beta
\end{tikzcd}
\end{document}
```
and 

```tikz
\usepackage{tikz-cd} 
\begin{document} 
\begin{tikzcd}[row sep=2cm, column sep=2cm]
G  \arrow[r, "\iota"] \arrow[d, "\pi_\beta "'] &G \arrow[d, "\pi_\beta"] \\ 
G_\beta \arrow[r, "\iota_\beta"']& G_\beta
\end{tikzcd}
\end{document}
```

**Prop:** Since $(\Bbb R, +, \tau)$ is a topological group, then for any set $X$ the set $\Bbb R^X$ is a topological group. If $X$ is also a topological space the set of continuous functions $\mathcal C^0(X)$ is a topological subgroup of $\Bbb R^X$.

**Prop:** We see that for any topological group $(G, *, \tau)$ and any fixed $a\in G$, the $\ell_a(x) =ax$ and $r_a(x) = xa$ are homeomorphisms. Additionally, the function $\iota:G \to G$ is also a homeomorphism. 

**Cor:** Every topological group is [[Homogeneous Spaces|homogeneous]]. 

**Cor:** If $A$ is a subset of a topological group $G$. If $x$ is an interior point $A$, then there's a an open set $e\in V \in \tau$, such that $xV \subseteq A$. 

**Cor:** A subgroup $H$ of a topological group $G$ is discrete iff $H$ has an isolated point. 

**Cor:** Let $G$ be a topological group. If $\scr U$ is a local base around $e$, then $\{gU \mid U \in {\scr U}\}$ is a local basis around $a$ for every $g\in G$. 

**Cor:** If Let $G$ be a topological group. If $K$ and $L$ are compact subsets of $G$, then $gK$, $Kg$, $KL$ and $K^{-1}$ are compact subsets of $G$.

**Prop:** Let $G$ be a topological group, and let $U$ be an open neighbourhood of $e$.
- There is an open neighbourhood $V$ of $e$ such that $VV\subseteq U$.
- There is symmetric open neighbourhood of $e$ that is included in $U$. 

**Prop:** Let $G$ be a topological group, let $K$ be a compact subset of $G$, and let $U$ be an open subset of $G$ that includes $K$. Then there are open neighbourhoods $V_R$ and $V_L$ of $e$ such that $K V_R \subseteq U$ and $V_L K\subseteq U$. 

**Prop:** A topological subgroup $H$ of  $G$ is open iff its interior is nonempty. 

**Prop:** Let $A$ and $B$ be subsets of a topological group $G$, then $(\text{cl}_G A) (\text{cl}_G B) \subseteq \text{cl}_G(A B)$, and $(\text{cl}_G A)^{-1} = \text{cl}_G(A^{-1})$. 

**Cor:** If $H$ is a topological subgroup of $G$, then $\text{cl}_G (H)$ is also a topological subgroup of $G$.

**Prop:** Let $G$ be a topological group, and $x, y\in G$. The points $x$ and $y$ are topological indistinguishable if $xy^{-1}\in \text{cl}(\{e\})$. 

**Prop:** Every topological group is regular. 

**Prop:** Every topological group that is $T_0$ it is also $T_1$.

**Prop:** Every topological group that is $T_1$ is also $T_2$. 

**Cor:** A topological group that is $T_0$ iff $T_3$.

**Prop:** A topological group that is $T_0$ iff $T_{3\frac12}$.

**Def:** Let $H$ be a subgroup of $G$, where $G$ is a topological group. We know that $G/H$ is the set of all *left cosets modulo $H$*, we can endow $G/H$ with the topology determined by the natural quotient map $\pi: G \to G/H$ sending each element $g\in G$ to its coset. 

**Prop:** Every open subgroup of $G$ is also closed.

**Prop:** For any neighbourhood $U$ of $e$, then the subgroup $\langle U\rangle$ generated by $U$ is open and closed in $G$.

**Prop:** For any connected subset $U\subseteq G$ containing $1$, $\langle U \rangle$ is connected.

**Cor:** If $G$ is connected, then every connected neighbourhood of $1$ generates $G$. 

**Def:** A *locally compact topological group*, or simply a *locally compact group*, is a topological group whose topology is a locally compact and Hausdorff. A *compact group* is a topological group whose topology is compact and Hausdorff. 

**Def:** Let $G$ be a topological group, and let $f$ be real/complex-valued function on $G$. Then $f$ is *left uniformly continuous* if for each $\varepsilon>0$ there is an open neighbourhood $U$ of $e$ such that $|f(x)-f(y)|<\varepsilon$ holds whenever $x$ and $y$ belong to $G$ and satisfy $y\in xU$. Likewise, $f$ is *right uniformly continuous* if for each $\varepsilon>0$ there is an open neighbourhood $U$ of $e$ such that $|f(x)-f(y)|<\varepsilon$ holds whenever $x$ and $y$ belong to $G$ and satisfy $y\in Ux$. 

**Obs:** Note that we can replace the neighbourhoods of $e$ appearing in the definition above with smaller symmetric neighbourhoods of $e$ and that for each symmetric neighbourhood $U$ the condition $x\in yU$ is equivalent to the condition $y\in xU$ and the condition $x\in Uy$ is equivalent to the condition $y\in Ux$. Thus $x$ and $y$ do in fact enter our definition symmetrically.

**Prop:** Let $G$ be a locally compact group. Then each function in $\mathcal C_c(G)$ is left uniformly continuous and right uniformly continuous.

**Cor:** Let $G$ be a locally compact group, let $\mu$ be a regular Borel measure on $G$, and let $f$ belong to $\mathcal C_c(G)$. Then the functions $$x\mapsto \int f(xy)\, \mu(dy)\quad \text{and}\quad x\mapsto \int f(yx)\, \mu(dy) $$are continuous. 

**Prop:** Let $G$ be a topological group, and let $H$ be an open subgroup of $G$. Then $H$ is closed. 

**Prop:** Let $G$ be a locally compact group. Then there is a subgroup $H$ of $G$ that is open, closed and $\sigma$-compact. 

**Prop:** Let $G$ be a Hausdorff topological group. If $E$ is compact and $F$ is closed, then $EF$ is closed.