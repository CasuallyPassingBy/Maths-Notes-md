---
tags:
  - GraphTheory
  - Topology/AlgebraicTopology
---
Subjects: [[Algebraic Topology]], [[Graph Theory]]
Links: [[The Seifert-Van Kampen Theorem]], [[Cell Complexes and CW Complexes]], [[Graphs]], [[Group Presentations]]

# Graphs

**Def:** A *graph* is a CW complex of dimension $0$ or $1$. The $0$-cells of the graph are called its *vertices*, and the $1$-cells are called its *edges*. 

**Def:** A *subgraph* is a subcomplex of a graph. 

**Def:** We see that for each edge $e$, the set $|\overline e \setminus e| =1, 2$; if a vertex $v$ is contained in $\overline e$, we say that *$v$ and $e$ are incident*. An edge that is incident with only one vertex is a *self-loop*. If two or more edges are incident with the same one or two vertices,  they are calles *multiple edges*. A graph with no self-loops or multiple edges is called a *simple graph*. 

**Def:** An *edge path* in a graph is a finite sequence $(v_0, e_1, v_1, \dots, v_{k-1}, e_k, v_k)$ that starts and ends with vertices and alternates between vertices and edges, such that for each $i$, $\{v_{i-1}, v_i\}$ is the et of vertices incident with the edge $e_i$. The vertices $v_0$ and $v_k$ are called the *initial vertex* and *terminal vertex*. We also allow a *trivial edge path* $(v_0)$ consisting of one vertex alone. An edge path is said to be *closed* if $v_0 = v_k$, and *simple* if no edge or vertex appears more than once, except that $v_0$ might be equal to $v_k$.

**Def:** A *cycle* is a nontrivial closed edge path. 

**Prop:** A graph $\Gamma$ is connected iff given any two vertices $v, v'\in \Gamma$, there is an edge path from $v$ to $v'$. Additionally, In a connected graph, any two vertices can be connected by simple edge path.

**Def:** A *tree* is connected graph that contains no cycles. 

**Cor:** Any two vertices in a tree are joined by a unique simple edge path. 

**Lemma:** Every vertex in a finite tree is a strong deformation retract of the tree. 

**Th:** Every finite tree is contractible, and thus simply connected. 

**Def:** Let $\Gamma$ be a graph. A *spanning tree* in $\Gamma$ is a subgraph that is a tree and that contains every vertex of $\Gamma$. A *maximal tree* is a subgraph that is not properly contained in any larger tree in $\Gamma$. 

**Prop:** Every finite connected graph contains a spanning tree. 

Let $\Gamma$ be a finite connected graph. We construct a set of generators for the fundamental group of $\Gamma$ as follows. Choose a vertex $v$ as a base point, and let $T\subseteq \Gamma$ be a spanning tree. Let $e_1,\dots, e_n$ be the edges of $\Gamma$ that are not in $T$, for each $i$ let $\{w_i, w_i'\}$ be the set of vertices incident with $e_i$. We can choose paths $g_i$ and $h_i$ in $T$ from $v$ to $w_i$ and $w_i'$, respectively. Let $f_i$ denote the loop in $\Gamma$ obtained by first following $g_i$ from $v$ to $w_i$, then traversing $e_i$, and the following $\overline h_i$ from $w_i$ to $v$. 

**Fundamental Group of a Finite Graph:** the fundamental group of a finite graph $\Gamma$ based at a vertex $v$ is the free group on the path classes $[f_1],\dots, [f_n]$ constructed above. 

**Obs:** Let $\Gamma$ be  a finite connected graph. The Euler characteristic of $\Gamma$ is $\chi(\Gamma) = V-E$, where $V$ is the number of vertices and $E$ is the number of edges.

**Prop:** Let $\Gamma$ be  a finite connected graph. The fundamental group of $\Gamma$ is a free group on $1-\chi(\Gamma)$ generators. Thus $\chi(\Gamma)$ is a homotopy invaraint, meaning that homotopy equivalent graphs have the same Euler characteristic. 

# Fundamental Groups of CW Complexes

**Prop:** Let $X$ be a path-connected topological space, and let $\widetilde X$ be the space obtained by attaching a closed $2$-cell to $X$ along an attaching map $\varphi: \partial D \to X$. Let $v\in \partial D$, $\widetilde v = \varphi(v)\in X$, and $\gamma = \varphi_*(\alpha) \in \pi_1(X, \widetilde v)$, where $\alpha$ is generator of the infinite cyclic group $\pi_1(\partial D, v)$. Then the homomorphism $\pi_1(X, \widetilde v) \to \pi_1(\widetilde X, \widetilde v)$ induced by the inclusion $X \hookrightarrow \widetilde X$ is surjective, and its kernel is the smallest normal subgroup containing $\gamma$. If $\pi_1(X, \widetilde v)$ has a finite presentation $$\pi_1(X, \widetilde v) \cong \langle \beta_1, \dots, \beta_n\mid \sigma_1,\dots,\sigma_s\rangle,$$then $\pi_1(\widetilde X, \widetilde v)$ has the presentation $$\pi_1(\widetilde X, \widetilde v) \cong \langle \beta_1, \dots, \beta_n\mid \sigma_1,\dots,\sigma_s,\tau\rangle,$$where $\tau$ is an expression for $\gamma \in \pi_1(\widetilde X, \widetilde v)$ in terms of $\{\beta_1, \dots,\beta_n\}$. 

**Prop:** Let $X$ be a path-connected topological space, and let $\widetilde X$ be a space obtained by attaching an $n$-cell to $X$, with $n \ge 3$. Then inlusion $X \hookrightarrow \widetilde X$ induces an isomorphism of fundamental groups.

**Fundamental Group of a finite CW Complex:** Suppose $X$ is a connected finite CW complex, and $v$ is a point in the $1$-skeleton of $X$ that is contained in the closure of every $2$-cell. Let $\beta_1, \dots,\beta_n$ be generators for the free group $\pi_1(\text{skel}_1(X), v)$, and let $e_1,\dots, e_k$ be the $2$-cells of $X$. For each $i = 1,\dots, k$, let $\varphi_i: D_i \to X$ be the corresponding attaching map, let $\alpha_i$ be the generator of $\pi_1(\partial D_i, v_i)$, and let $\sigma_i$ be an expression for $(\varphi_i)_*(\alpha_i)\in \pi_(X_1, v)$ in terms of the generators $\{\beta_i\}$. Then $\pi_1(X, v)$ has the following presentation $$\pi_1(X, \widetilde v) \cong \langle \beta_1, \dots, \beta_n\mid \sigma_1,\dots,\sigma_k\rangle.$$
**Prop:** Let $G$ be a finitely presented group. There is a finite CW complex whose fundamental group is isomorphic to $G$. 