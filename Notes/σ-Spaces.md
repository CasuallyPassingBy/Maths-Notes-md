---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Topological Networks]], [[Metrization Theorems]], [[Regular Hausdorff Spaces]], [[Topological Developability]], [[Paracompacteness]]

**Def:** Just as we can have a $\sigma$-locally finite base, a base that is the countable union of locally open families, we can generalise this to $\sigma$-locally finite network, meaning that it is a network that is the countable union of locally finite families. If a space has a $\sigma$-locally finite network it is called a *$\sigma$-space*. 

**Obs:** We see, by Nagata-Smirnov, that every metric space is $\sigma$-space. 

**Obs:** Every regular $\sigma$-space is [[Subparacompactness and Submetacompactness|subparacompact]]. 

**Prop:** Every regular developable space is a $\sigma$-space.

**Th:** For a regular space $X$ the following statements are equivalent.
- $X$ has a $\sigma$-closure-preserving network
- $X$ is a $\sigma$-space.
- $X$ has a $\sigma$-discrete network. 

**Prop:** Let $f$ be a closed continuous mapping of $X$ onto a space $Y$. If $X$ has $\sigma$-closure preserving network, then $Y$ has a $\sigma$-closure preserving network.

**Prop:** Let $f$ be a closed continuous map from a regular $\sigma$-space $X$ onto a topological space $Y$, then $Y$ is a $\sigma$-space. 

**Def:** Let $X$ be a topological space and $\cal C$ is a closed cover of $X$. We say that $\cal C$ *dominates* $X$ if the following holds: a subset $F$ of $X$ is closed if there is a subcollection $\mathcal D\subseteq \cal C$ such that $F\subseteq\bigcup \cal D$ and such that for every $D\in \cal D$ the set $D\cap F$ is closed. 

**Th:** Let $X$ be a $\sigma$- space The followings statements are true.
- If $Y\subseteq X$, then $Y$ is a $\sigma$-space
- If $\{X_n\mid n<\omega\}$ is a collection of $\sigma$-spaces, then $\prod_{n<\omega} X_n$ is a $\sigma$-space.
- If $\{X_n\mid n<\omega\}$ is a cover of $X$  consisting of closed $\sigma$-spaces, then $X$ is a $\sigma$-space.
- If $X$ is a regular space and dominated by a close cover $\{X_\alpha\mid \alpha<\kappa\}$ consisting of $\sigma$-spaces, then $X$ is also a  $\sigma$-space.
	- Let $\{X_\alpha \mid \alpha <\kappa\}$ be a $\sigma$-locally finite closed covering of a space $X$ consisting of $\sigma$-spaces, then $X$ is a $\sigma$-space.
- If $X$ is a $\sigma$-space, and there is a perfect map $f:X \to Y$, then $Y$ is a $\sigma$-space.

**Lemma:** A $T_2$ space $X$ is a $\sigma$-space iff $\mathcal F\langle X\rangle$ is a $\sigma$-space for any $n<\omega$, where $\mathcal F_n\langle X\rangle$ is [[Finite Vietoris Hyperspace|the Vietoris finite set topology with cardinality of at most n]].  

**Prop:** A $T_2$ space $X$ is a $\sigma$-space iff $\mathcal F\langle X\rangle$ is a $\sigma$-space, where $\mathcal F\langle X\rangle$ is [[Finite Vietoris Hyperspace|Vietoris finite set topology]]. 

**Cor:** Let $X$ be a regular paracompact space. If for each point $x$ of $X$ there exists a neighbourhood $U$ of $x$ such that $U$ is a $\sigma$-space, then $X$ is a $\sigma$-space.

**Cor:** Every regular collectionwise normal $\sigma$-space is paracompact. Every collectionwise $T_4$ $\sigma$-space is paracompact.

**Prop:** Every regular $\sigma$-space is perfect.

**Prop:** Let $X$ be a regular space. If $X$ is collectionwise normal $\sigma$-space, then $X$ is hereditarily paracompact. 

**Cor:** If $X$ is a collectionwise $T_4$ $\sigma$-space, then $X$ is hereditarily paracompact.

**Th:** Let $X$ be a collectionwise $T_4$ $\sigma$-space. then the following statements are equivalent.
- $X$ is separable.
- $X$ is Lindelöf.
- $X$ satisfies the countable chain condition. 

**Prop:** Let $X$ and $Y$ be paracompact $T_2$ $\sigma$-space, then so is the product space $X\times Y$.

**Prop:** Let $\{X_n\mid n <\omega\}$ be a collection of topological spaces. If $\prod_{k < n}X_k$ is $T_6$ and paracompact for every $n<\omega$, then $\prod_{n<\omega} X_n$ is $T_6$ and paracompact. 

**Th:** If $\{X_n \mid n<\omega\}$ is a collection of paracompact $T_2$ $\sigma$-spaces, then so is the product space $\prod_{n<\omega}X_n$. 

**Cor:**  A topological space $X$ is a paracompact $T_2$ $\sigma$-space iff $\mathcal F\langle X\rangle$ is a paracompact Hausdorff $\sigma$-space, where $\mathcal F\langle X\rangle$ is [[Finite Vietoris Hyperspace|Vietoris finite set topology]].  