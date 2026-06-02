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

**Def:** A collection $\scr P$ of closed subsets of a topological space $X$ is said to be a $k$-network for $X$ if, given any open set $U$ and any compact $K \subseteq U$, there is a finite subcollection ${\scr Q} \in [{\scr P}]^{<\omega}$ so that $K \subseteq \bigcup {\scr Q}\subseteq U$. We can also have the stronger version $\sigma$-locally finite $k$-network as a $k$-network that is the union of locally finite closed families.

We see that every base is a $k$-network. 

**Def:** A collection $\scr F$ of subsets of $X$ is called a $wcs$-network if for any $x\in X$, its neighbourhood $U$ and a sequence $x_n$ converging to $x$, there is a finite subcollection $\scr F^*$ of $\scr F$ such that $\{x\}\cup \{x_m \mid n <m<\omega\}\subseteq \bigcup{\scr F^*}\subseteq U$ for some $n<\omega$. $\scr F$ is called a $cs$-network if for any $x\in X$, its neighbourhood $U$ and a sequence $x_n$ converging to $x$, there is an element $F\in \scr F$ such that $\{x\}\cup \{x_m \mid n <m<\omega\}\subseteq F\subseteq U$ for some $n<\omega$.

**Lemma:** Let $\{G_\alpha\mid \alpha<\kappa\}$ be a discrete collection in $X$ with a $\sigma$-closure preserving closed $wcs$-network $\bigcup_{n<\omega} {\scr F}_n$. Then for each $G_\alpha$ we can select a sequential neighbourhood $W_\alpha$ such that $W_\beta\cap W_\alpha = \varnothing$ whenever $\alpha\neq\beta$. Here $W_\alpha$ is called a sequential neighbourhood of $G_\alpha$ if each sequence $(x_n)$ converging to $x\in F_\alpha$ is eventually $W_\alpha$. 

**Th:** The following statements are equivalent for a $T_3$-space $X$.
- $X$ is $\aleph$-space.
- $X$ has a $\sigma$-locally finite $wcs$-network,
- $X$ has a $\sigma$-discrete $k$-network.
- $X$ has a $\sigma$-discrete $wcs$-network.
- 