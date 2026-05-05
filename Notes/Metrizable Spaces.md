---
tags:
  - Topology
  - Analysis
---
Subjects: [[Topology]]
Links: [[Paracompacteness]], [[Collectionwise Normal Spaces]], [[Topological Developability]], [[Metric Spaces]], [[Total Boundedness]], [[Complete Metric Spaces]]

**Def:** A topological space is *metrizable* if there's a metric that induces the same as the original topology. Similarly, a topological space is *pseudometrizable* if there's a pseudometric that induces the original topology.

**Def:** Let $(X, d)$ be a metric space and $A \subseteq X$; we say that $A$ is $\varepsilon$-dense in $(X,d)$ if for every $x\in X$ there's a $y\in A$ such that $d(x,y) < \varepsilon$. A metric space is *totally bounded* if for every $\varepsilon>0$ there exists a finite set $A\subseteq X$ which is $\varepsilon$-dense in $(X, d)$; a metric on a set $X$ is *totally bounded* if the space $(X, d)$ is totally bounded. Lastly, a topological space $X$ is *metrizable by a totally bounded metric* if there exists a totally bounded metric on $X$.

**Def:** A topological space is completely metrizable if there is a complete metric on the space $X$.

**Obs:** Metric spaces are metrizables, and pseudometric spaces are pseudometrizables. Note that discrete space are metrizable with the discrete metric. 

We can bound the metric by $1$, and still generates the same metric/pseudometric.

**Obs:** Every (pseudo)metric space is first countable; in fact, they are developable.

**Prop:** Every metrizable space is $T_6$. 

**Prop:** The following statements are equivalent for a metrizable space $X$.
- $X$ is compact.
- $X$ is countably compact.
- $X$ is sequentially compact.

**Prop:** The following statements are equivalent for a metrizable space $X$.
- $X$ is second countable.
- $X$ is separable.
- $X$ is Lindelöf.

**Prop:** The sum $\bigoplus_{\alpha < \kappa} X_\alpha$ is (completely) metrizable iff all the spaces $X_\alpha$ are (completely) metrizable. Additionally, the sum $\bigoplus_{\alpha < \kappa} X_\alpha$ is totally bounded iff all the spaces $X_\alpha$ are totally bounded and $\kappa < \omega$. 

**Prop:** Let $\{X_n \mid n  <\omega\}$ be a family of (completely) metrizable spaces and let $d_n$ be a metric on $X_n$ bounded by $1$. The topology induced on the set $\prod_{n <\omega} X_n$ by the (complete) metric $$ d(x, y) := \sum_{n <\omega} \frac1{2^n} d_n(x,y)$$coincides with the natural topology on $\prod_{n <\omega} X_n$. Additionally, if each $X_n$ is totally bounded, then $\prod_{n < \omega} X_n$ is totally bounded.

**Cor:** The Hilbert cube $[0, 1]^\omega$ is metrizable by a totally bounded metric; the one given in the theorem above.

**Cor:** The metric $d$ on a metrizable space $X$ is a continuous function $d:X\times X\to \Bbb R$. 

**Urysohn Metrization Theorem:** A second countable space is metrizable iff it is $T_{3\frac12}$. 

**Th:** A $T_2$ compact space is metrizable iff it is second countable.

**Th:** The Hilbert cube $[0,1]^\omega$ is universal for all compact metrizable spaces and for all separable metrizable spaces.

**Th:** A metrizable space is metrizable by a totally bounded metric iff it is separable.

**Cor:** A topological space is metrizable by a totally bounded metric iff it is a $T_3$ second-countable space.

**Th:** Every metric space is ismotric to a subspace of a complete metric space. 

**Cor:** Every metrizable space is embedable in a completely metrizable space.

**Def:** Let $X$ be a topological space $(Y, d)$ be a metric space and $f: A \to Y$ is a continuos mapping defined on a dense subset of the space $X$; we say that the *oscilation of the mapping $f$ at a point $x\in X$ is equal to $0$* if for every $\varepsilon >0$ there exists a neighbourhood $U$ of the point $x$ such that $\text{diam}(f[A \cap U]) <\varepsilon$. 

**Obs:** We can get that the points of osculation equal to zero must be a $G_\delta$-set containing $A$. 

**Lemma:** If $X$ is a topological space, $(Y, d)$ a complete metric space and $f:A \to Y$ a continuous mapping defined on a dense subset $A$ of the space $X$, then the mapping $f$ is extendable to a continuous function $F: B \to Y$ defined on the set $B$ consisting of all points of which $X$ is equal to $0$.

**Cor:** If $Y$ is a completely metrizable, then every continuous function $f:A \to Y$ from a dense subset $A$ of a topological space $X$ to the space $Y$ is extendable to a continuous mapping $F:B \to Y$ defined on a $G_\delta$-set $A \subseteq B\subseteq X$. 

**Prop:** If $(X, d)$ is a metric space and $(Y, d')$ a complete metric space, then every mapping $f: A\to Y$ from a dense subset $A$ of the space $X$ to the space $Y$ which is uniformly continuous with respect to $d|_A$ and $d'$ is extendable to a mapping $F:X\to Y$ uniformly continuous with respect to $d$ and $d'$.

**Cor:** If $(X, d)$ and $(Y, d')$ are complete metric space, then every isometry of $(A, d|_A)$ into, surjectively, $(B, d'|_B)$ where $A$ and $B$ are dense subsets of $X$ and $Y$ respectively, is extendable to an isometry of $(X, d)$ into, surjectively, $(Y, d')$.

**Th:** For every metric space $(X, d)$ there exists exactly one (up to isometry) complete metric space $(\overline X, \overline d)$ such that $\overline X$ contains a dense subspace isometric to $(X, d)$. Moreover, we have that $w(\overline X) = w(X)$, and if $(X, d)$ is totally bounded, the so is $(\overline X, \overline d)$. 

This implies that the procedure on [[Completion of a Metric Space]] is the unique completion of a metric space.

**Lavrentieff's Theorem:** Let $X$ and $Y$ be completely metrizable spaces and let $A\subseteq X$ and $C\subseteq Y$ be arbitrary subspaces. Every homeomorphism $f: A\to C$ is extendable to a homeomorphism $F:B\to D$, where $A\subseteq B \subseteq X$, $C\subseteq D \subseteq X$, and $B$ and $D$ are $G_\delta$-sets in $X$ and $Y$, respectively.

**Lemma:** Every $G_\delta$ set in matrizable space $X$ is homeomorphic to a closed subspace of the product space $X\times \Bbb R^\omega$.

**Th:** Complete metrizability is hereditary with respect to $G_\delta$-sets.

**Alexandroff's Theorem:** If a subspace $M$ of metrizable space $X$ is completely metrizable, then $M$ is a $G_\delta$-set in $X$.

**Cor:** A separable metrizable space is completely metrizable iff it is embeddable in $\Bbb R^\omega$ as a closed subspace.

**Th:** Every metric on a compact is totally bounded and complete.

**Th:** A metrizable space $X$ is compact off on the space $X$ there exists a metric $d$ which is both totally bounded and complete.

**Cor:** The completion of a metric space $(X, d)$ is compact iff $(X, d)$ is totally bounded.o