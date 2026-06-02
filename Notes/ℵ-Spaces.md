---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Networks]], [[σ-Spaces]], [[Regular Hausdorff Spaces]], [[Subparacompactness and Submetacompactness]]

**Def:** A collection $\scr P$ of closed subsets of a topological space $X$ is said to be a $k$-network for $X$ if, given any open set $U$ and any compact $K \subseteq U$, there is a finite subcollection ${\scr Q} \in [{\scr P}]^{<\omega}$ so that $K \subseteq \bigcup {\scr Q}\subseteq U$. We can also have the stronger version $\sigma$-locally finite $k$-network as a $k$-network that is the union of locally finite closed families.

We see that every base is a $k$-network. 

**Def:** A collection $\scr F$ of subsets of $X$ is called a $wcs$-network if for any $x\in X$, its neighbourhood $U$ and a sequence $x_n$ converging to $x$, there is a finite subcollection $\scr F^*$ of $\scr F$ such that $\{x\}\cup \{x_m \mid n <m<\omega\}\subseteq \bigcup{\scr F^*}\subseteq U$ for some $n<\omega$. $\scr F$ is called a $cs$-network if for any $x\in X$, its neighbourhood $U$ and a sequence $x_n$ converging to $x$, there is an element $F\in \scr F$ such that $\{x\}\cup \{x_m \mid n <m<\omega\}\subseteq F\subseteq U$ for some $n<\omega$.

**Def:** A space $X$ is called an $\aleph$-space if it is $T_3$ and has a $\sigma$-locally finite $k$-network. If $X$ is a $T_3$ countable $k$-network is called an $\aleph_0$-space.

**Obs:** We see that every $\aleph$-space is a $\sigma$-space. All metrizable spaces are $\aleph$-spaces. Every $\aleph$-space are subparacompact, perfect and have a $G_\delta$-diagonal.

**Th:** The classes of $\aleph$-spaces, $\aleph_0$-spaces, and paracompact $\aleph$-spaces are hereditary and countably productive.

**Obs:** We see that $\aleph_0$-spaces have a countable network, they are hereditarily Lindelöf and herdiarily separable.  

**Th:** Let $X$ be a topological space. The following statements are equivalent.
- $X$ is a quotient of a separable metric space.
- $X$ is a $k$[[k1-Spaces|-space]] and $\aleph_0$-space.