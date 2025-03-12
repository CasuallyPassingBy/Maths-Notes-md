---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Locally Finite Collections]]

**Def:** A family $\{A_\alpha\mid \alpha < \kappa\}$ of subsets of a set $X$ is called a *cover* of $X$ if $\bigcup_{\alpha<\kappa} A_\alpha = X$. If $X$ is a topological space and all the sets $A_\alpha$ are open (closed), we say that the cover $\{A_\alpha\mid \alpha< \kappa\}$ is *open (closed)*. 

We also say that a cover is locally finite if it is a cover and it is [[Locally Finite Collections|locally finite]].

**Def:** Let $\cal C$ is a cover of $X$. A *subcover of $\cal C$* is a subset $\cal D \subseteq C$ such that $\cal D$ is also a cover of $X$. We say that a subcover is finite if it is a finite subset of $\cal C$. 

**Def:** A *refinement* of a cover $\cal C$ of a topological space is a new cover $\cal D$ of $X$ such that every set in $\cal D$ is contained in some set in $\cal C$. Formally $\mathcal D :=\{V_\beta \mid \beta<\lambda\}$ is refinement of $\cal C := \{U_\alpha \mid \alpha<\kappa\}$ if for all $\beta< \lambda$ there exists an $\alpha<\kappa$ such that $V_\beta\subseteq U_\alpha$. 