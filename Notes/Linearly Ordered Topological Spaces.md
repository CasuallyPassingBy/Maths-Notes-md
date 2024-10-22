---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Linear Orderings]], [[Topological Spaces]], [[Ordinal Numbers]]

Let $(X, \le)$ be a linearly ordered set, and $x, y \in X$, we say that $x$ is the immediate ancestor of $y$, if $x < y$, and the interval $(x, y)$ is empty. We can also say that $y$ is the immediate successor of $x$.

We can consider the topology induced by $\le$ on $X$, as the topology induced by the base 
$$
\mathcal B = \{(a, b) \subseteq X \mid a, b \in X\}
$$
or the subbase
$$
\mathcal S = \{(\leftarrow, a)\subseteq X \mid a \in X\} \cup \{(a, \to) \subseteq X \mid a \in X \}
$$
If $Y$ is a subset of $X$, $X$ a totally ordered set, then $Y$ inherits a total order from $X$. The set $Y$ has an order topology, the *induced order topology*. As a subset of $X$, $Y$ also has a subspace topology. The subspace topology is always at least as fine as the induced topology, but they are generally not the same. 

Meaning $\tau_X|_Y$ the subspace topology of $Y$, and $\tau_{\le_Y}$ the order topology of $Y$, we have that $\tau_{\le_Y}\subseteq \tau_X|_Y$. 

We have the pro

# Left and Right Order Topologies

The right order topology on $X$ is the topology having the base of all intervals of the form $(a, \to)$, together with the set $X$ itself.

The left order topology on $X$ is the topology having the base of all intervals of the form $(\leftarrow, a)$, together with the set $X$ itself.

[[Cofinal and Coinitial Subsets|Cofinal]] subsets are precisely the dense sets with respect to the right order topology. Similarly, the [[Cofinal and Coinitial Subsets|coinitial]] subsets are precisely the dense sets with respect to the left order topology

# Ordinals

Any ordinal can be made a topological space using the order topology: in the absence of an indication to the contrary, it is always the order topology that is meant when an ordinal is a topological space.

The set of all limit points of an ordinal $\alpha$ is precisely the set of limit ordinals less than $\alpha$. Zero and the successor ordinals less than $\alpha$ are isolated points in $\alpha$. 