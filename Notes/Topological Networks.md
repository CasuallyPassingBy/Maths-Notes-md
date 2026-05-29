---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Cardinal Functions of Topological Spaces]]

**Def:** A family $\cal N$ of subsets of a topological space $X$ is a *network* for $X$ if for every point $x\in X$ and any $U \in\tau_X$ with $x\in U$ there exists an $M\in \cal N$ such that $x\in M \subseteq U$. 

Clearly, any base of $X$ is a network for $X$: it is a network of a special kind, namely, all members of which are open. The family of all one-point subsets of a space is another example of a network. 

**Def:** The *network weight* of a space $X$ is defined as the smallest cardinal number of the form $|\mathcal N|$, where $\cal N$ is a network for $X$; this cardinal number is denoted by $nw(X)$. Clearly, for every topological space $X$, we have $nw(X) \le w(X)$ and $nw(X) \le |X|$.

**Prop:** Let $X$ be a regular space. If $\mathcal N$ is a network, then $\overline{\cal N}$ is also a network, where $\overline{\cal N} = \{\overline N\mid N\in {\cal N}\}$. 

# $k$-networks

**Def:** A collection $\scr P$ of closed subsets of a topological space $X$ is said to be a $k$-network for $X$ if, given any open set $U$ and any compact $K \subseteq U$, there is a finite subcollection ${\scr Q} \in [{\scr P}]^{<\omega}$ so that $K \subseteq \bigcup {\scr Q}\subseteq U$. We can also have the stronger version $\sigma$-locally finite $k$-network as a $k$-network that is the union of locally finite closed families.

