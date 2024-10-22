---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Topological Spaces]], [[Bases, Subbases, and Local Basis for Topological Spaces]]

### From a Basis
Let $\cal B$ be a a family of subsets of $X$, that satisfy:
- $X = \bigcup \cal B$
- let $B_1, B_2 \in B$ , and $x \in B_1 \cap B_2$, then there exists $B \in \cal B$ such that $x \in B \subseteq B_1\cap B_2$
Then, the collection $\tau_{\cal B} = \{A \subseteq X \mid \exists {\cal A \subseteq B}(A =\bigcup {\cal A})\}$ is a topology of $X$ that has $\cal B$ as a basis.
### From a Subbase
From a nonempty collection of subsets of $X$, ${\cal S}\subseteq {\cal P}(X)$, that covers $X$, meaning $\bigcup {\cal S} = X$, we can generate a topology $\tau_{\cal S}$. To make this we generate the the collection ${\cal B_{S}} = \{B \subseteq X \mid \exists {\cal S}_0 \in [{\cal S}]^{<\omega} [{\cal S}_0 \ne \varnothing \land \bigcap {\cal S}_0 = B]\}$. This new collection of subsets is a basis, thus we can generate a topology $\tau_{\cal S}$, with a basis ${\cal B_{S}}$ and a subbase ${\cal S}$. 

We also get that $\tau_{\cal S} = \bigcap \{\tau \in \tau(X) \mid S \subseteq \tau\}$ 
### From a closed Base
Let $\cal C$ be a family of subsets of $X$. Then
- $\bigcap \cal C = \varnothing$ 
- For each $C_1, C_2 \in \cal C$, the union $C_1 \cup C_2$ is the intersection of some subfamily of $\cal C$. 

Then, the collection ${\cal F} = \{A \subseteq X \mid \exists {\cal A}\subseteq {\cal C} [{\cal A}\ne \varnothing \land A = \bigcap {\cal A}]\}$, and the the set $\tau = \{X \setminus A \mid A \in {\cal F}\}$ is a topology for $X$, $\cal F$ is the set of all closed sets in that topology, and $\cal C$ is a base for the closed sets in $X$. 
### From a Neighbourhood System
If for every element $x \in X$, we can choose a family ${\cal N}(x)\ne \varnothing$ of subsets of $X$ such that the collections ${\cal N}(x)$ have the following properties:
- If $U\in {\cal N}(x)$, then $x \in U$
- If $U, V \in {\cal N}(x)$, then $U \cap V \in {\cal N}(x)$ 
- For each $U \in {\cal N}(x)$, there's $V \in {\cal N}(x)$ such that $U \in {\cal N}(y)$, for each $y \in V$
- If $U \in {\cal N}(x)$, and $U \subseteq V \subseteq X$, then $V \in {\cal N}(x)$
Then the set 
$$
\tau = \{\varnothing\} \cup \{A \subseteq X \mid \forall x \in A\exists V\in {\cal N}(x) [V \subseteq A] \}
$$
is a topology on $X$ and each ${\cal N}(x)$ results as the neighbourhood system of $x$ of the topology
### From a Local Basis
If for every element $x \in X$, we can choose a family ${\cal B}(x)\ne \varnothing$ of subsets of $X$ such that the collections ${\cal B}(x)$ have the following properties:
- If $N_1, N_2 \in {\cal B}(x)$, then there exists $N_3. \in {\cal B}(x)$ such that $N_3 \subseteq N_1 \cap N_2$ 
- For each $N \in {\cal B}(x)$ we can choose $N_0 \in {\cal B(}x)$ such that if $y\in N_0$, there exists $W \in {\cal B}(y)$ such that $W \subseteq N$. 
Then the set $\tau = \{A \subseteq X \mid \forall x \in A\exists N \in {\cal B}(x)[N \subseteq A]\}$ is a topology on $X$, and each ${\cal B}(x)$ happens to be a local basis for each $x$ in the topology.

