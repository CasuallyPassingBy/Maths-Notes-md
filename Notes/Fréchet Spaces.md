---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Kolmogorov Spaces]], [[Limit Points and Closure]]

**Def:** We say that a topological space $(X,\tau)$ is a *$T_1$ space,* or that $\tau$ is a $T_1$ *topology*, if for any two distinct points $x, y \in X$, there are $U, V\in \tau$ such that $x \in U \setminus V$ and $y \in V\setminus U$. This kind of space is also called a *Fréchet space*. 

**Prop:** $T_1$ is a topological property. 

**Obs:** $T_1$ is a topological property that is preserved under refinement the topology. This means that if $(X, \tau_1)$ is $T_1$ and $\tau_1 \subseteq \tau_2$ topologies then $(X,\tau_2)$ is $T_1$. 

**Obs:** Every $T_1$ space is a $T_0$ space, and not every $T_0$ space is $T_1$. 

**Th:** A topological space $(X, \tau)$ is a $T_1$ space iff for each $x \in X$, the set $\{x\}$ is a closed subset of $X$. 

**Cor:** A topological space $X$ is $T_1$ iff every finite set of $X$ is closed. 

**Cor:** If $(X, \tau)$ is a $T_1$ space iff $\tau$ contains the [[Complement Topology|cofinite topology]]

**Cor:** If $(X, \tau)$ is a topological space where every sequence defined on it has at most one limit, then $X$ is a $T_1$ space.

**Prop:** The following propositions are equivalent for a topological space $X$
- $X$ is a $T_1$ space.
- each $A \subseteq X$ is the intersection of every open subsets of $X$ that contain $A$.
- For each $x\in X$, the set $\{x\}$ is equal to the intersection of open subsets of $X$ that contain $x.$ 

**Prop:** Let $(X, \tau)$ is a $T_1$ space, and $E \subseteq X$. $x \in \text{Lim}(E)$ iff each $U\in \tau$, if $x \in U$, then $|E \cap U| \ge \aleph_0$. 

**Prop:** Every subspace of a $T_1$ space is $T_1$. $T_1$ is a hereditary property.

**Prop:** If $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ is a family of nonempty $T_1$ spaces, then the product $\prod_{\alpha < \kappa} X_\alpha$ is a $T_1$ space iff for each $\alpha < \kappa$, $X_\alpha$ is a $T_1$ space. 

**Prop:** If $\{(X_\alpha, \tau_\alpha) \mid \alpha < \kappa\}$ is a family of nonempty $T_1$ spaces, then the sum $\bigoplus_{\alpha < \kappa} X_\alpha$ is a $T_1$ space iff for each $\alpha < \kappa$, $X_\alpha$ is a $T_1$ space. 

**Prop:** If $X$ is a $T_1$ space, $Y$ a topological space, and $f: X \to Y$ a closed surjective function, then $Y$ is a $T_1$ space. 

**Prop:** Let $(\mathcal D, \tau_\mathcal D)$ partition space of a topological space $X$. $\mathcal D$ is a $T_1$ space iff the elements of $\mathcal D$ are closed subsets of $X$.

