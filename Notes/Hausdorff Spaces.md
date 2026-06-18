---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Fréchet Spaces]], [[Kolmogorov Spaces]], [[Convergence of Sequences]], [[Convergence of Filters]], [[Compactness]]

**Def:** A topological space $(X, \tau)$ is a Hausdorff space or $T_2$ if $X$ satisfies the following condition: for any two distinct points $x, y \in X$, there are $U, V \in \tau$ such that $x \in U$, $y \in V$ and $U \cap V = \varnothing$.

**Prop:** $T_2$ is a topological property, meaning invariant under homeomorphisms. 

**Obs:** $T_2$ is a topological property that is preserved under refinement the topology. This means that if $(X, \tau_1)$ is $T_2$ and $\tau_1 \subseteq \tau_2$ topologies then $(X,\tau_2)$ is $T_2$. 

**Obs:** Every $T_2$ space is a $T_1$ space and $T_0$ space. 

**Prop:** Let $(X, \tau)$ be a $T_2$ space. If $(x_n)_{n<\omega}$ is convergent sequence, then $(x_n)_{n <\omega}$ converges to a unique point. 

**Cor:** Let $(X, \tau)$ be [[Separable, First and Second Countable Spaces|first countable]] space. $X$ is a $T_2$ space iff every sequence in $X$ has at most one limit.

**Prop:** A topological space $X$ is $T_2$ iff every filter has at most one limit.

**Prop:** $T_2$ is a hereditary property.

**Th:** Let $\{X_\alpha \mid \alpha<\kappa\}$ be a family of nonempty topological spaces, and $X = \prod_{\alpha <\kappa} X_\alpha$ the topological product of the family. $X$ is a $T_2$ space iff each $X_\alpha$ is a $T_2$ space.

**Prop:** Let $\{X_\alpha \mid \alpha<\kappa\}$ be a family of nonempty topological spaces, and $X = \bigoplus_{\alpha <\kappa} X_\alpha$ the topological sum of the family. $X$ is a $T_2$ space iff each $X_\alpha$ is a $T_2$ space.

**Prop:** The following statements are equivalent for a topological space $(X, \tau)$:
- $X$ is a $T_2$ space.
- For each $x \in X$, the set $\{x\} = \bigcap \{\text{cl}(U) \mid x \in U \in \tau\}$. 
- The diagonal $\Delta = \{(x, x) \mid x \in X\}$ is a closed subset of $X\times X$.

**Prop:** Let $f: X \to Y$ be a continuous, open, and surjective map. $Y$ is $T_2$ space iff the set $\{(x_1, x_2) \in X\times X \mid f(x_1) = f(x_2)\}$ is closed.

**Cor:** Let $X$ be a topological space, and $\sim$ be an equivalence on $X$. Then $X/\sim$ is a $T_2$ space iff the set $\sim$ is a closed set on $X\times X$.

**Prop:** Let $X$, $Y$  be topological spaces, and $f, g: X \to Y$ are continuous functions. If $Y$ is a $T_2$ space then the set $\{x \in X \mid f(x) = g(x)\}$ is closed.

**Cor:** Let $X$ be a $T_2$ space. If $f: X \to X$ is a continuous function then the set of all fixed points of $f$ is closed, i.e., the set $\{x \in X \mid f(x) = x\}$ is closed.

**Prop:** Let $X$ be an infinite $T_2$ space, then $X$ contains a subspace that is homeomorphic to $\omega$.

**Prop:** If a topological property $P$ is hereditary with respect to both closed subsets and open subsets and is countably multiplicative, then in the class of $T_2$-spaces, $P$ is hereditary with respect to $G_\delta$-sets. 