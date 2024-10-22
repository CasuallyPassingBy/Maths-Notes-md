---
tags:
  - Topology
---
Subject: [[Topology]]
## Opens Sets
A topology of a set $X$ is a family of subsets $\tau$ that satisfy the following
1. $\varnothing, X \in \tau$ 
2. Let $\{A_i\}_{i = 1}^n \subseteq \tau$, then $\bigcap\limits_{i = 1}^n A_i \in \tau$ 
3. Let ${\cal A}\subseteq \tau$, then $\bigcup {\cal A}\in \tau$. 

If $\tau$ is a topology of $X$, then the pair $(X, \tau)$ is called a topological space, and the elements of $\tau$ are called the open subsets of $X$. 

We often need to take out the empty set of the topology and it is denoted as $\tau^+$. 

We have special topologies, that are more akin to the trivial ones:
- If we have that the topology $\tau$ is equal to ${\cal P}(X)$. Then it is called the *discrete topology* on $X$, and the pair $(X, {\cal P}(X))$ is the discrete space of $X$. 
- If we have that $\tau =\{\varnothing, X\}$, then $\tau$ is called the *indiscrete topology* on $X$, and $(X, \tau)$ is the indiscrete space on $X$.
- We can also define what is called the *cofinte topology*, and let $X$ be a set, and we define $$ \tau = \{\varnothing\} \cup \{A \subseteq X \mid |X\setminus A| <\aleph_0 \}$$ which is a topology, and we can often write it as $\tau_{\text{cof}}$ 
- Given any [[Metric Spaces|metric space]] $(X, d)$, and the collection $\tau_d = \{\varnothing\} \cup \{E \subseteq X \mid E \text{ is union of balls}\}$ is a topology on $X$ and we call it the topology on $X$ induced by the metric $d$. [[Topology on Metric Spaces]]

## Comparison of Topologies

We can always construct a topologies on any set $X$, and thus we can denote $\tau (X)$ to be the set of all topologies of $X$. Meaning
$$
\tau(X) := \{\tau \subseteq {\cal P}(X) \mid \tau \text{ is a topology on }X\}
$$
We can consider a partial order on $\tau(X)$ defined by the set inclusion:
$\tau_1 \le \tau_2$ iff $\tau_1 \subseteq \tau_2$. In this case we say that $\tau_2$ is finer than $\tau_1$ or that $\tau_1$ is coarser than $\tau_2$. Thus $(\tau(X), \subseteq)$ is a partially ordered set, where the maximum being the discrete topology and minimum being the indiscrete topology

## Closed Sets
Let $(X, \tau)$ be a topological space, and $E\subseteq X$. We say that $E$ is a closed subset of $(X, \tau)$ if $X\setminus E$ is open, i.e., $X\setminus E \in \tau$ 

Let $(X, \tau)$ be a topological space, and let $\cal F$ be the family of closed subsets on $X$. Then $\cal F$ satisfies the following
- $\varnothing, X \in \cal F$
- Let $\{F_i\}_{i = 1}^n \subseteq \cal F$, then $\bigcup\limits_{i = 1}^n F_i \in \cal F$
- For any $\cal G \subseteq F$, with $\cal G\ne \varnothing$, then $\bigcap \cal G \in F$. 