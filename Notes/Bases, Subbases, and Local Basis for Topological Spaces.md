---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Topological Spaces]]

# Basis

Let $(X, \tau)$ be a topological space. A subcollection $\cal B$ of $\tau$ is a *basis* of $\tau$ if for every element $A \in \tau$, there's $\cal A \subseteq B$  such that $A = \bigcup \cal A$ 

Let $\cal B$ be a subcollection of the topology $\tau$ on $X$ is a basis of $\tau$ iff for each $A \in \tau^+$ and each $x \in A$, there's a $B \in \cal B$ such that $x \in B \subseteq A$

If $\cal B$ is basis of the topology $\tau$ of $X$, then $\cal B$ must cover $X$, i.e., $\bigcup {\cal B} = X$, and for any finite subset $\{B_i\}_{i = 1}^n \subseteq \cal B$, then there exists a $B\in \cal B$ that satisfies $x \in B \subseteq \bigcap\limits_{i = 1}^n B_i$ 

#### Bases for Closed sets
Given a topological space $(X, \tau)$, a family $\cal C$ of closed sets forms a *base for the closed sets* iff for each closed $A$ and each point $x$ not in $A$, there exists an element of $\cal C$ containing $A$ but not containing $x$. 

A family $\cal C$ is a base for the closed sets of $(X, \tau)$ iff, its *dual* in $X$, that is the family $\{X \setminus C \mid C \in {\cal C}\}$ of complements of members of $\cal C$, is a base for the open sets in $X$

Let $\cal C$ be a base of the closed sets of $(X, \tau)$. Then
- $\bigcap \cal C = \varnothing$ 
- For each $C_1, C_2 \in \cal C$, the union $C_1 \cup C_2$ is the intersection of some subfamily of $\cal C$. 


# Subbases
Let $\cal S$ be a subset of the topology $\tau$ on $X$ is a *subbase* for $(X, \tau)$ if ${\cal B} = \left\{\bigcap \cal A \mid A \subseteq S \land 0 < |A| < \aleph_0 \right\}$ is a basis for $\tau$. Meaning, $\cal S\subseteq \tau$  is a subbase of $\tau$, iff for each $A \in \tau^+$, and each $x \in A$, there's a $\cal A  \subseteq S$ nonempty and finite such that $x \in \bigcap {\cal A}\subseteq A$

# Local Basis
Let $x$ be an element of a topological space $(X, \tau)$. A subset $V$ of $X$ is a *neighbourhood of $x$* in the space $(X, \tau)$, if we can find an element $U\in \tau$ that satisfies $x \in U \subseteq V$. The collection of neighbourhoods of $x$ in $X$, we call it a *neighbourhood system of the point $x$* and we denote it as $\cal N(x)$ or $N(x)$. 

A subset $A$ of the space $(X, \tau)$ is open iff for each $x \in A$ there's a neighbourhood $N\in \cal N(x)$ such that $N \subseteq A$. 

For a point $x$ in the topological space $(X, \tau)$, a set ${\cal B(}x) \subseteq {\cal N}(x)$ is a neighbourhood basis of $x$ in $(X, \tau)$ if for each $N \in \cal N(x)$ we can find $B \in {\cal B}(x)$ such that $B \subseteq V$. 

If we have a basis $\cal B$ for the topology $\tau$, then we can always a local basis for each point as ${\cal B}(x) = \{B \in {\cal B} \mid x \in B\}$ 

Let $(X, \tau)$ be a topological space, and suppose that for each $x \in X$ we chose a neighbourhood basis ${\cal B}(x)$. Then it follows that
- If $N_1, N_2 \in {\cal B}(x)$, then there exists a $N_3\in \cal B(x)$ such that $N_3 \subseteq N_1 \cap N_2$
- For each $N \in {\cal B}(x)$ we can choose $N_0 \in {\cal B(}x)$ such that if $y\in N_0$, there exists $W \in {\cal B}(y)$ such that $W \subseteq N$. 
