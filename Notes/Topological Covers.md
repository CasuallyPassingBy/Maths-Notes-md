---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Special Types of Collections in Topology]]

**Def:** A family $\{A_\alpha\mid \alpha < \kappa\}$ of subsets of a set $X$ is called a *cover* of $X$ if $\bigcup_{\alpha<\kappa} A_\alpha = X$. If $X$ is a topological space and all the sets $A_\alpha$ are open (closed), we say that the cover $\{A_\alpha\mid \alpha< \kappa\}$ is *open (closed)*. 

We also say that a cover is locally finite if it is a cover and it is [[Special Types of Collections in Topology|locally finite]].

**Def:** Let $\cal C$ is a cover of $X$. A *subcover of $\cal C$* is a subset $\cal D \subseteq C$ such that $\cal D$ is also a cover of $X$. We say that a subcover is finite if it is a finite subset of $\cal C$. 

**Def:** A *refinement* of a cover $\cal C$ of a topological space is a new cover $\cal D$ of $X$ such that every set in $\cal D$ is contained in some set in $\cal C$. Formally $\mathcal D :=\{V_\beta \mid \beta<\lambda\}$ is refinement of $\cal C := \{U_\alpha \mid \alpha<\kappa\}$ if for all $\beta< \lambda$ there exists an $\alpha<\kappa$ such that $V_\beta\subseteq U_\alpha$. Nagata denotes this as $\mathcal D < \mathcal C$. 

If we drop the requirement for $\cal C$ and $\cal D$ to be covers, but still have the property that for each element $D\in \cal D$ there's a $C \in \cal C$ such that $D \subseteq C$, then we say that $\cal D$ is *inscribed in $\cal C$.*

Note that every subcover is a refinement.

**Def:** If $\cal U$ and $\cal V$ are two covers of $X$, we can define their union and intersection by
$$
\begin{align*} 
\mathcal U \vee \mathcal V & := \mathcal U \cup \mathcal V \\
\mathcal U \wedge \mathcal V & := \{U \cap V \mid U \in \mathcal U \ \land \ V \in \mathcal V\}

\end{align*}
$$

**Obs:** If $\cal U$ and $\cal V$ are open (closed) covers of $X$, then $\cal U \vee V$ and $\cal U \wedge V$ are also open (closed) covers of $X$. We also get the relations $\cal U \wedge V < U < U \vee V$.

We can extend the definition to arbitrary many covering $\{\mathcal U_\alpha \mid \alpha <\kappa\}$ as,
$$
\begin{align*}
\bigvee \{\mathcal U_\alpha \mid \alpha < \kappa\} = \bigvee_{\alpha <\kappa} \mathcal U_\alpha & := \bigcup_{\alpha< \kappa}\mathcal U_\alpha \\
\bigwedge \{\mathcal U_\alpha \mid \alpha < \kappa\} = \bigwedge_{\alpha <\kappa} \mathcal U_\alpha & := \left\{\left.\bigcap_{\alpha < \kappa} U_\alpha\; \right\rvert\;\forall \alpha < \kappa(U_\alpha \in \mathcal U_\alpha)\right\}
\end{align*}
$$
**Def:** Let $\cal U$ be a collection of subsets of $X$, we define $\text{cl}(\mathcal U) := \{\text{cl}(U) \mid U \in \mathcal U\}$.  