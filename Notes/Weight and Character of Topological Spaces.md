---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Bases, Subbases, and Local Basis for Topological Spaces]]

**Def:** Let $(X, \tau)$ be a topological space. We define the *weight of space* $(X, \tau)$ is the $$w((X, \tau)) := \min\{|\mathcal B| \mid \mathcal B \subseteq \tau, \text{ where }\mathcal B \text{ is base for }\tau\}.$$If the topology is clear, then it is denoted $w(X)$.

**Def:** The *character of a point* $x$ in a topological space $(X, \tau)$ is defined as $$\chi(x, (X, \tau)) := \min\{|\mathcal B(x)| \mid B(x) \subseteq \tau, \text{ where }\mathcal B \text{ is a local base for }X \text{ at } x\}. $$If the topology is clear is denoted as $\chi(x, X)$. The *character of a topological space* $(X, \tau)$ is defined as $$\chi(X, \tau) := \sup\{\chi(x, (X, \tau)) \mid x \in X\}.$$If the topology is clear, then it is denoted as $\chi(X)$. Additionally, we can define the character for a set $A\subseteq X$ as $$\chi(A, (X, \tau)) := \min\{|\mathcal B(x)| \mid B(x) \subseteq \tau, \text{ where }\mathcal B \text{ is a local base for }X \text{ at }A\}. $$

**Obs:** If we have that $\chi(X, \tau) \le \aleph_0$ then we note that this equivalent to the space being [[Separable, First and Second Countable Spaces|first countable]]. If we have that $w(X, \tau) \le \aleph_0$ this is equivalent to the space being [[Separable, First and Second Countable Spaces|second countable]]. 

**Th:** If $w(X) \le \mu$, then for every family $\{U_\alpha \mid \alpha < \kappa\} \subseteq \tau$ there exists a set $S \subseteq \kappa$ such that $|S| \le \mu$ and $$\bigcup_{\alpha \in S} U_\alpha = \bigcup_{\alpha < \kappa} U_\alpha.$$
**Th:** If $w(X)\le \mu$ then for every $\cal B$ for $X$ there exists a $\mathcal B_0$ such that $|\mathcal B_0|\le \mu$ and $\mathcal B_0 \subseteq \mathcal B$. 

**Th:** If $f: X \to Y$ is an open mapping, then for every $x \in X$ and $A\subseteq X$ we have $\chi(f(x), Y) \le \chi(x, X)$ and $\chi(F[A], Y) \le \chi(A, X)$. If, moreover, $f$ is surjective, then $w(Y) \le w(X)$, and $\chi(Y) \le \chi(X)$. 

**Th:** For every [[Kolmogorov Spaces|Kolmogorov space]] we have $|X| \le 2^{w(X)}$.   

**Obs:** Let $M$ be a subspace of $X$. If $A\subseteq M$, and $x\in M$, then $\chi(A, M) \le \chi(A, X)$, and $\chi(x, M) \le \chi(x, M)$. 

**Prop:** If $X$ be a regular space, and $M$ is dense subset of $X$, then any $x\in M$ will satisfy $\chi(x, M) \le \chi(x, X)$.

**Cor:** Let $X$ be a topological space, and $M$ be a dense in $X$. If $A\subseteq M$ satisfies that for every closed $B\subseteq X$ that is disjoint from $A$ there are $U, V\in \tau_X$ such that $A\subseteq U$, $B\subseteq V$ and $U \cap V = \varnothing$, then $\chi(A, M) = \chi(A, X)$.

**Cor:** If $X$ is a [[Normal Hausdorff Spaces|normal space]], $M$ is dense in $X$ and $A \subseteq M$, then $\chi(A, M) = \chi(A, X)$. 

**Prop:** Let $X$ be a topological space. If $M$ is a closed subspace of $X$, and $A\subseteq X$, then $\chi(A \cap M, M) \le \chi(A, X)$. 

**Prop:** If $f:X \to Y$ is a closed continuous function, and $B\subseteq Y$, then $\chi(f^{-1}[B], X) \le \chi(B, Y)$, additionally, if $f$ is surjective, then $\chi(f^{-1}[B], X) = \chi(B, Y)$.

**Th:** Every infinite $T_2$ compact space $X$ satisfies $|X| \le \exp(\chi(X))$

**Cor:** very infinite first countable $T_2$ compact space $X$ satisfies $|X| \le \frak c$.