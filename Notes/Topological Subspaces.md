---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Topological Spaces]], [[Bases, Subbases, and Local Basis for Topological Spaces]]

Given a topological space $(X, \tau)$, and $Y \subseteq X$, we can define the set
$$
\tau|Y = \tau_Y = \tau|_Y = \{ A \cap Y \mid A  \in \tau\} 
$$
We can see that $\tau|_Y$ is a topology on $Y$, and we call it the relative topology of $Y$ with respect to $(X, \tau)$, and say that $(Y, \tau|_Y)$ is a subspace of $(X, \tau)$. 

[[Topology on Metric Spaces#Topology of Submetric Spaces|Submetric Spaces]] are just the topological subspace of a metric space. 

Let $(X, \tau)$ is a topological space, $Y\subseteq X$ and $y \in Y$.
- If $\cal B$ is a basis (subbase) for $\tau$, then ${\cal B}_Y =\{B \cap Y \mid B \in {\cal B}\}$ is a basis (subbase) for $\tau|_Y$ 
- If ${\cal B}(y)$ is a local basis of $y$ for $\tau$, then $\{B \cap Y \mid B \in {\cal B}(y)\}$ is a local basis of $y$ in $(Y, \tau|_Y)$.  
