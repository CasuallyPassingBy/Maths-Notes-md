---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Sequences in Rn]], [[Rn]], [[Compact Sets in R]]

**********Def:********** A set $K \subseteq \Bbb R^n$ is _sequentially compact_ if for every sequence $(x_n)$ contained in $K$ there’s a convergent subsequence that converges in $K$.

************Th:************ A set $K \subseteq \Bbb R^n$ is sequentially compact iff $K$ is close and bounded

## Open Covers

**********Def:********** Let $A \subseteq \Bbb R^n$. An **************open cover************** for $A$ is a (possibly infinite) collection of open sets ${\{U_\lambda \mid \lambda \in \Lambda\}}$ whose union contains the set $A$; that is $A \subseteq \bigcup_{\lambda\in \Lambda} U_\lambda$. Given an open cover for $A$, a ****************finite subcover**************** is a finite subcollection of open sets from the original open cover whose union still manages to completely contain $A$.

********Def:******** A set $K \subseteq \Bbb R$ is called ********compact******** if for every open cover there’s a finite subcover

### Lindelöf Theorem

Let $U \subseteq \Bbb R^n$ be an open set, and $\{U_\lambda \mid \lambda \in \Lambda\}$ be a collection of open sets such that ${U = \bigcup_{\lambda \in \Lambda} U_\lambda}$. Then there exists a countable subcollection $\{U_i\}_{i \in \Bbb N}$ of $\{U_\lambda\}_{\lambda\in \Lambda}$ so that

$$ U = \bigcup_{i =1}^\infty U_i $$

### Heine-Borel Theorem
Let $K \subseteq \Bbb R^n$. All of the following statements are equivalent:

- $K$ is sequentially compact
- $K$ is compact
- $K$ is closed and bounded

### Nested Compact Set Property

Let $(K_n)_{n \in \Bbb N}$ be a nested sequence of nonempty compact sets, then

$$ \bigcap_{n \in \Bbb N} K_n \ne \varnothing $$

### Distance Lemma
Suppose $K$ is compact, $C$ is closed, and $K \cap C = \varnothing$. Then the distance $d(K, C) >0$ .