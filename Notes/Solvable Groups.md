---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Commutator Subgroup]], [[Normal Subgroups and Quotient Groups]]

**Def:** If $G$ is any group, we say that a *normal series* of $G$ is a chain of subgroups $$\{e\} 
= G_n \subseteq \dots \subseteq G_2 \subseteq G_1 \subseteq G_0 := G,$$such that $G_{m + 1} \trianglelefteq G_m$ for every $m$. The quotients of the series are $G_m/G_{m+1}$, and the *length of the series* is the number of strict inclusions. 

**Def:** Let $H \trianglelefteq G$ is said to be a *maximum normal subgroup* if there's no other normal subgroup $K \trianglelefteq G$ such that $H < K < G$. 

**Obs:** $H \trianglelefteq G$ is a maximum normal subgroup iff $G/H$ is [[Simple Groups|simple]]. 

**Def:** A normal series of a group $G$ $$\{e\} 
= G_n \subseteq \dots \subseteq G_2 \subseteq G_1 \subseteq G_0 := G,$$is said to be *composition series* if for each $G_{m+1}$ is a normal maximum normal subgroup of $G_m$ or if $G_{m+1} = G_m$. This means that a normal series of $G$ is a decomposition series iff $G_m/G_{m+1}$ is simple or trivial. 

**Lemma:** If $G$ is a finite group, then $G$ has a decomposition series. 

**Def:** If $$\{e\} 
= G_n \subseteq \dots \subseteq G_2 \subseteq G_1 \subseteq G_0 := G,$$and $$\{e\} 
= G'_m \subseteq \dots \subseteq G'_2 \subseteq G'_1 \subseteq G'_0 := G$$ are normal series of $G$, we say that they are *equivalent* if there's a bijection between the families of the quotients $\{G_k/G_{k+1} \mid 0 \le k < n\}$ and $\{G_k/G_{k+1} \mid 0 \le k < m\}$. 

**Jordan-Hölder Theorem:** Any two decomposition series of a finite group $G$ are equivalent. 

**Def:** A group $G$ is *solvable* if there's a normal series where the quotients $G_k/G_{k+1}$ are abelian for $0 \le k < n$. 

**Obs:** Every abelian group is solvable. A finite nonabelian simple group is not solvable, since its unique normal series $1 \trianglelefteq G$ is doesn't have abelian quotients.

**Prop:** Every finite $p$-group is solvable. Furthermore, if $G$ is a group of order $p^n$, then there's a series of groups $$\{e\} = G_0\subseteq G_1 \subseteq \dots \subseteq G_n = G$$ such that $G_k$ is normal in $G_{k+1}$, $|G_k| = p^k$ for $0 \le k \le n$, and the quotients $G_{k+1}/G_k$ are cyclic of order $p$. 

**Prop:** Let $G$ be a finite group of order $pq$ with $p$ and $q$ primes, then $G$ is solvable.

**Prop:** Let $G$ be a finite group of order $p^2q$ with $p$ and $q$ primes, then $G$ is solvable.

$(*)$ **Burnside Theorem:** Let $G$ be a finite group of order $p^rq^s$ with $p$ and $q$ primes, and $r+s>1$, then $G$ is solvable.

**Def:** Let $G$ be a group. We define the following groups inductively $G^{(0)} := G$, and $$G^{(n+1)} := [G^{(n)}, G^{(n)}]$$for $n \ge 1$. The groups $G^{(2)}$, $G^{(3)}, \dots$ are called the *second derived subgroup, third derived subgroup* and so forth. 

We get the following properties for the derived subgroups:
- $G^{(n+1)} \trianglelefteq G^{(n)}$ for every $n \ge 0$. 
- $G^{(n+1)} \trianglelefteq G$ for every $n \ge 0$. 
- The quotients $G^{(n)} / G^{(n+1)}$ is abelian for every $n \ge 0$.

**Prop:** A group $G$ is solvable iff $G^{(n)} =  1$ for some $n \ge 0$. 

**Th:** Let $G$ be a group. Then,
- If $H \le G$ is a subgroup and $G$ is solvable, then $H$ is solvable. 
- If $H \trianglelefteq G$ and $G$ is solvable, then $G/H$ is solvable.
- If $H \trianglelefteq G$ is such that $H$ and $G/H$ are solvable, then $G$ is solvable. 

This means that the class $\sf Sol$ of solvable groups is closed under subgroups, quotients and [[Group Extensions|extensions]]. 

**Lemma:** If $n \ge 5$ and $G = S_n$, then the derived subgroup $G^{(k)}$ of $G$ has all the $3$-cycles of $S_n$, for $k \ge 1$. 

**Cor:** If $n \ge 5$, the group $S_n$ is not solvable. 