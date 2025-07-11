---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Topological Covers]]

**Def:** A family $\{A_\alpha \mid \alpha < \kappa\}$ of subsets of a topological space $X$ is *locally finite (locally countable)* if for every point $x\in X$ there exists a neighbourhood such that the set $\{\alpha < \kappa \mid U \cap A_\alpha\}$ is finite (countable). If every point $x \in X$ has a neighbourhood that intersects at most one set of a given family, then we say that the family is *discrete*. 

**Obs:** A discrete family, as well as any finite family, is locally finite. 

**Def:** A family $\{A_\alpha \mid \alpha < \kappa\}$ of subsets of a set $X$ is called *point-finite/point-countable* if for every $x\in X$ the set $\{\alpha <\kappa\mid x\in A_\alpha\}$ is finite/countable. 

We see that every locally finite cover is point-finite. 

**Th:** For every locally finite family $\mathcal A =\{A_\alpha \mid \alpha < \kappa\}$ we have the equality $$\bigcup\text{cl}(\mathcal A) = \text{cl}\left(\bigcup\mathcal A\right).$$
**Th:** Let $\mathcal F$ be a locally finite family and $F = \bigcup \cal F$. If all members of $\cal F$ are closed, then $F$ is closed set and if all members of $\cal F$ are clopen, then $F$ is a clopen set. 

**Th:** If $\cal A$ is a locally finite (discrete) family, then the family $\text{cl}(\mathcal A)$ is also locally finite (discrete). 

**Def:** Given a point $x\in X$, $A\subseteq X$ and a collection of subsets $\cal U$, we define the *star of $x$* with respect to $\cal U$ as the set $$\text{st}(x, \mathcal U) := \bigcup \{U \in \mathcal U \mid x\in U\}.$$Now  we can define the *star of $A$* with respect to $\cal U$ as the set $$\text{st}(A,\mathcal U) := \bigcup_{x\in A} \text{st}(x, \mathcal U) = \bigcup \{U \in \mathcal U \mid A \cap U \neq \varnothing\}.$$With these, we can define recursively the $n$th star of a point or a set with respect to $\cal U$, as 
$$\begin{align*}

\text{st}^1(x, \mathcal U):= \text{st}(x, \mathcal U) \qquad \text{st}^{n+1}(x, \mathcal U) &:= \text{st}(\text{st}^n (x, \mathcal U), \mathcal U) \\
\text{st}^1(A, \mathcal U):= \text{st}(A, \mathcal U) \qquad
\text{st}^{n+1}(A, \mathcal U) &:= \text{st}(\text{st}^n (A, \mathcal U), \mathcal U).
\end{align*}$$
Let us note, that is $\mathcal U$ is collection of open sets, then $\text{st}^n(x, \mathcal U)$ and $\text{st}^n(A, \mathcal U)$ are open for every $x\in X$, $A\subseteq X$ and $n <\omega$. 

With this in mind, we can now define new operations on collection of subsets of $X$. Let $\mathcal U \subset \mathcal P(X)$: 
$$
\begin{align*}
\mathcal U^\Delta &:= \{\text{st}(x, \mathcal U) \mid x\in X\}\\
\mathcal U^* &:= \{\text{st}(U, \mathcal U)\mid U \in \mathcal U\}
\end{align*}
$$
We can do a slight abuse in notation given that $\mathcal U^{\Delta \Delta}$ or $\mathcal U^{**}$ we take it to mean $(\mathcal U^\Delta)^\Delta$ and $(U^*)^*$, respectively. If $\cal U$ is formed by open subsets of $X$, then $\mathcal U^\Delta$ and $\mathcal U^*$ will also be formed by open subsets of $X$. 

**Def:** Let $\cal U$ and $\cal V$ be coverings of $X$. If $\mathcal U^\Delta < \mathcal V$, then we say that $\cal U$ is a *barycentric refinement of $\cal V$.* Similarly, if $\mathcal U^* <\mathcal V$, then we say that $\cal U$ is a *star-refinement of $\cal V$*. Additionally, a cover $\mathcal U$ is called a *normal cover* if there is a sequence $\{\mathcal U_n \mid n <\omega\}$ of open covers such that $\mathcal U > \mathcal U_0$ and $\mathcal U_n^* > \mathcal U_{n+1}$ for every $n <\omega$. 

**Prop:** $\mathcal U < \mathcal U ^\Delta < \mathcal U ^* < \mathcal U ^{\Delta \Delta}$ for every cover $\cal U$ of $X$. 

**Prop:** Let $\cal A, B, C$ be collections of subsets of $X$. If $\cal A$ is a barycentric refinement of $\cal B$, and $\cal B$ is a barycentric refinement of $\cal C$, then $\cal A$ is a star-refinement of $\cal C$.

**Def:** Let $\cal U$ be a collection in topological space $X$. If every $U\in \cal U$ intersects finitely (countably) many members of $\cal U$, then $\cal U$ is called *star-finite* (*star-countable*). Additionally, if for every $\cal V\subseteq U,$ $$\text{cl}\left(\bigcup \mathcal V\right) = \bigcup \text{cl}(\mathcal V),$$then $\cal U$ is called *closure-preserving*. Finally, let $\cal U$ and $\cal V$ be collections; then we say that $\cal V$ is *cushioned in* $\cal U$ if for every $V\in \cal V$ we can assign a $U(V) \in \cal U$ such that for every $\cal W \subseteq V$, 
$$
\text{cl}\left(\bigcup \{V \in V \in \mathcal W\} \right) \subseteq \bigcup \{U(V) \mid V\in \mathcal W\}.
$$

**Remark:** Every locally finite collection is closure-preserving.

**Def:** If $\cal U$ be a collection such that there's a sequence of locally finite collections $\{\mathcal U_n \mid n <\omega\}$ such that $\mathcal U = \bigcup_{n <\omega} \mathcal U_n$, then $\cal U$ is a *$\sigma$-locally finite collection*. We can define similarly for $\sigma$-discrete, $\sigma$-star-finite, $\sigma$-closure-preserving, and $\sigma$-cushioned.

**Obs:** We can get the following scheme gives us the relationships between this concepts:
$$
\text{discrete} \implies \text{star-finite} \implies \text{locally finite} \implies \text{closure preserving} \implies \text{cushioned}
$$
In this scheme the implication $\text{star-finite} \implies \text{locally finite}$ is valid only for open collections, and $\text{closure-preserving} \implies \text{cushioned}$ should be understood to mean the following: If $\cal U$ is a closure-preserving collection, then $\cal U$ is cushioned in $\text{cl}(\mathcal U)$. 