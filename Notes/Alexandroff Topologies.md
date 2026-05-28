---
tags:
  - Topology
aliases:
  - Alexandrov Topologies
---
Subjects: [[Topology]]
Links: [[Topological Spaces]], [[Pre-orderings]], [[Limit Points and Closure]], [[Interior Points]]

**Def:** Let $X$ be a topological space. We call $X$ call an *Alexandroff-discrete space* or *finitely generated spaces* if every arbitrary intersection of open sets is open. The topology on $X$ is called an *Alexandroff topology.*

**Th:** Alexandroff topologies have numerous characterisations. In a topological space $X$, the following conditions are equivalent.
- *Open and closed set characterisations:*
	- An arbitrary intersection of open sets is open.
	- An arbitrary union of closed sets is closed.
- *Neighbourhood characterisations:*
	- Every point has a smallest neighbourhood.
	- The neighbourhood filter of every point is closed under arbitrary intersections.
- *Interior and closure algebraic characterisations:*
	- The interior operator distributes over arbitrary intersections of subsets.
	- The closure operator distributes over arbitrary union of subsets.
- *Preorder characterisations:*
	- The topology is the finest topology among topologies on $X$ with the same specialisation preorder, where $x\le y$ iff $x\in \overline{\{y\}}$. 
	- The open sets are precisely the upper for some preorder on $X$. 