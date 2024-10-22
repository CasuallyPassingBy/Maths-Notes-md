---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]], [[Normal Subgroups and Quotient Groups]]

**Def:** A subset $H$ of a group $(G,*)$ is called a *subgroup* of $G$ the elements of $H$ form a group under $*$, usually denoted as $H\le G$. A subgroup $H\ne G$ is called *proper*, and it is denoted as $H< G$.

**Th:** Let $H$ be a nonempty subset of a group $G$. Then $H$ is a subgroup of $G$ iff the following are conditions are satisfied:
1. for all $a, b\in H$, $ab\in H$
2. for all $a\in H$, $a^{-1}\in H$

Condition $1.$ is saying that $H$ is *closed* under the operation, and $2.$ is expressed that $H$ is *closed under inverses*.

**Th:** Let $G$ be a cyclic group, then every subgroup of $G$ is cyclic.

**Th:** Let $G$ be a group and let $H$ be a *finite* nonempty subset of $G$. Then if $H$ is closed under multiplication in $G$, $H$ is a subgroup of $G$.

**Th:** Let $H$ and $K$ be subgroups of $G$. Then:
- $H\cap K \le G$
- $H\cup K \le G$ iff one of $H, K$ is contained in the other

**The Fundamental Theorem of Cyclic Groups:** Let $G = \langle x\rangle$ be a cyclic group of order $n$. Then:
- For any positive integer $m$, $G$ has a subgroup of order $m$ iff $m \mid n$
- If in fact $m$ does divide $n$ then $G$ has a *unique* subgroup of order $m$
- Two powers $x^r$ and $x^s$ generate the same subgroup iff $(r, n) = (s, n)$

**Cor:** If $G = \langle x\rangle$ is cyclic of order $n$ and $d_1, d_2, \dots, d_{\tau(n)}$ are the distinct divisors of $n$, then $$\langle x^{d_1}\rangle, \langle x^{d_2}\rangle, \dots, \langle x^{d_{\tau(n)}}\rangle$$
are the distinct subgroups of $G$, where $\tau(n)$ is the [[Divisor Functions|divisor function counting the amount of divisors]].

**Th:** Let $G = \langle x\rangle$ be an infinite cyclic group. Then for any $k\in \Bbb N$, the subgroup $\langle x^k\rangle$ will be a distinct subgroup of $G$.

There are a couple of important subgroups of any group $G$

The first we will consider is called the *centraliser of an element $g \in G$* defined as: $$Z_G(g)=C_G(g) = \{h \in G \mid gh = hg\}$$
We can generalise this concept with $S\subseteq G$, with a group called the *centraliser of $S$* defined as $$Z_G(S) = \bigcap_{g\in S} Z_G(g) = \{h \in G \mid \forall g \in S[gh = hg ]\}$$
The centre of a group $G$, is defined as $$Z(G) = \{g\in G \mid \forall h \in G[gh=hg]\} = \bigcap_{g\in G}Z_G(g)$$
We also have that $Z(G) \trianglelefteq G$. 