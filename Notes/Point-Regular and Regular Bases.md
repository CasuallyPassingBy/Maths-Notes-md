---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Metrization Theorems]], [[Topological Developability]], [[Paracompacteness]], [[Metacompactness]],[[Separable, First and Second Countable Spaces]]

**Def:** We say that a base $\cal B$ for a topological space $X$ is *point-regular* or *uniform* if for every point $x\in X$ and any $U\in \tau_X$ with $x\in U$, then $|\{B\in \mathcal B \mid x\in B \ \land \ B \cap (X\setminus U) \neq \varnothing \}| < \omega$. 

**Def:** We say that a base $\cal B$ for a topological space $X$ is *regular* if for every point $x\in X$ and any $U\in \tau_X$ with $x\in U$, there's an open set $V\in \tau_X$ such that $x\in V \subseteq U$ and $|\{B \in\mathcal B \mid V \cap B \neq \varnothing \ \land \ B\cap (X \setminus U) \neq \varnothing\}| <\omega$. 

**Prop:** Let $X$ be a topological space. $\cal B$ is point-regular base for $X$ iff for every $x\in X$ any $\mathcal C \in [\mathcal B]^\omega$ such that $x\in \bigcap \cal C$, then $\cal C$ is local base for $X$ on $x$. 

**Obs:** We see that a regular base is also point-regular. If a space is has a point-regular base, then the space is first countable.

**Lemma:** If $X$ is a $T_1$ space has a regular base, then $X$ is $T_3$.

**Def:** Let $\mathcal A \subseteq \mathcal P(X)$, then we define $\mathcal M(\mathcal A) := \{A\in \mathcal A\mid \subseteq-\text{maximal elements of }\mathcal A\}$. 

**Def:** Let $X$ be a topological space. We define the *isolated points of $X$* as $I(X) := \tau_X \cap [X]^1$.  

**Lemma:** If $\cal B$ is a point-regular (resp., regular) base for a topological space $X$, then the family $\mathcal M(\mathcal B)$ is a point finite (resp., locally finite) cover of $X$.

**Lemma:** If $\cal B$ is a base for a $T_1$ space, then for every point-finite cover $\mathcal C\subseteq \cal B$ the family $\mathcal D := (\mathcal B\setminus \mathcal C) \cup I(X)$ is a base for $X$. Additionally, if $\mathcal B$ is a point-regular (resp., regular) then $\mathcal D$ is also point-regular (resp., regular).

**Lemma:** Let $X$ be a topological space and $\cal B$ be a point-regular base for $X$ with $\varnothing \notin \cal B$. If fo each $n <\omega$ we define, $$\mathcal{B}_0 := \mathcal{M}(\mathcal{B}) \quad \text{and} \quad \mathcal{B}_{n+1} := \mathcal{M}\left(\left(\mathcal{B}\setminus \bigcup_{m\leq n} \mathcal{B}_m\right)\cup I(X)\right),$$then $\mathcal B = \bigcup_{n <\omega} \mathcal B_n$. 

**Cor:** Let $X$ be $T_1$ space and $\cal B$ is a point regular (resp., regular) for $X$ with $\varnothing \in \cal B$. If $\{\mathcal B_n \mid n <\omega\}$ is the sequence of the lemma above, then $\cal B = \bigcup_{n<\omega} \mathcal B_n$ and for each $n <\omega$ it satisfies that $\mathcal B_n$ is a open point-finite (resp., locally finite) cover of $X$.

**Lemma:** If $X$ is $T_1$ space and has point-regular base, then $X$ is developable.

**Obs:** We cannot weaken the the hypothesis, since there are spaces with regular spaces, that aren't developable. 

**Arhangel'skiĭ Metrization Theorem:** A space $X$ is metrizable iff $X$ is $T_1$ and has a regular base.

**Prop:** The following statements are equivalent for a $T_1$ space $X$.
- $X$ has a point-regular base.
- $X$ is metacompact and developable.
- $X$ is point finite developable.

**Obs:** We can show that given a $T_1$ space with a point regular base, then we don't necessarily will have that it will be $T_2$.

**Alexandroff Metrization Theorem:** A topological space is metrizable iff it is $T_1$, collectionwise normal and has a point-regular base.

**Def:** We say that a base $\cal B$ for a topological space $X$ is $\cal K$-regular if for every compact subset $K \subseteq X$ and every $U \in \tau_X$ with $K \subseteq U$, then $|\{B \in \mathcal B \mid B \cap K \neq \varnothing \ \land \ B\cap (X \setminus U) \neq \varnothing\}| <\omega$. 

**Obs:** Note that every $\cal K$-regular base is point-regular

**Arhangel'skiĭ Metrization Criterion:** The following statements are equivalent for a $T_1$ space $X$.
- $X$ is metrizable.
- $X$ has a $\cal K$-regular base.

**Prop:** Let $\cal B$ be a base for a topological space. $\cal B$ is regular iff it is $\cal K$-regular.