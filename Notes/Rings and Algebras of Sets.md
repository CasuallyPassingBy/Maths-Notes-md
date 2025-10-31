---
tags:
  - MeasureTheory
---
Subjects: [[Set Theory]], [[Measure Theory]]
Links: [[Rings and Algebras of Sets]], [[Regular and Singular Cardinals]], [[Limits of Sets]], [[Borel Sets]], , [[Ordinal Numbers#The Transfinite Induction Principle|Transfinite Induction]]

Let $X$ be a set. 

**Def:** A *Halmos semiring* is a nonempty family $\cal P$ of sets such that:
- If $E, F \in \cal P$, then $E\cap F \in \cal P$, and
- If $E, F \in \cal P$ and $E\subseteq F$, then there is a finite family $\{C_0, C_1, \dots, C_n\}$ of sets in $\cal P$ such that $$E = C_0 \subseteq C_1 \subseteq \dots \subseteq C_n = F,$$and $D_i = C_i \setminus C_{i-1} \in \cal P$ for $i \in \{1, \dots, n\}$.  
This definition is present in Halmos.

**Def:** A *semiring* is a nonempty of $\cal P$ of sets such that:
- If $A, B \in \cal P$, then $A \cap B \in \cal P$
- If $A, B \in \cal P$ implies $A \setminus B = \bigcup\limits_{i = 1}^n C_i$ for disjoint $C_1, \dots, C_n \in \cap P$. 
This a more general definition of semiring than the Halmos' one. Meaning that Every Halmos semiring is a semiring in general. 


**Def:** A *ring* or *Boolean ring* of sets is a nonempty family $\cal R$ of subsets of $X$, such that if $E, F \in R$, then $E \cup F \in R$ and $E\setminus F \in R$. 

**Obs**: We see that $\varnothing \in R$, for every ring $R$. We not only get that but if $E, F\in \cal R$, then $E \ \Delta \ F \in R$, and $E \cap F \in R$. 

**Obs:** If $E \in [\mathcal R]^{< \omega}$, then $\bigcup E \in \cal R$.

**Def:** an *algebra* or *Boolean algebra* of sets is a non empty family $\cal A$ of subsets of $X$ such that:
- If $E, F \in \cal A$, then $E \cup F\in \cal A$, and
- if $E\in \cal A$, then $X\setminus E\in \cal A$. 

**Obs:** We see that if $\cal A$ is an algebra, then $\cal A$ is a ring, and $X\in \cal A$. We have that algebras are precisely the rings such that $X$ is an element of the ring.

**Prop:** If $\cal R$ is a ring of sets, and $\cal A$ is the family of all those sets $E$ such that $E \in \cal R$ or $X\setminus E \in \cal R$, then $\cal A$ is an algebra. 

**Th:** If $\mathcal E\subseteq P(X)$, then there exists a unique ring $\cal R_0$ such that $\cal R_0 \supseteq E$ and such that if $\cal R$ is any other ring containing $\cal E$ then $\cal R_0 \subseteq R$. 

The ring $\cal R_0$, the smallest ring containing $\cal E$, is called the *ring generated* by $E$; it will be denoted as $\cal R(E)$.

**Prop:** Let $\cal P$ be a semiring and let $\mathcal R$ be the family of all the sets of the form $\bigcup_{i = 1}^n E_i$ where $\{E_1, \dots, E_n\}$ is an arbitrary finite, disjoint family of sets of $\cal P$. Then $\cal R = R(P)$.  From this we see that a semiring which is closed under the formation of finite unions is ring.

**Th:** If $\cal E$ is a collection of subsets of $X$, then every set in $\cal R(E)$ may be covered by a finite union of sets in $\cal E$. 

**Th:** If $\cal E$ is a infinite collection of subsets of $X$, then $|\mathcal{R(E)}| = |\mathcal E|$.

**Def:** A $\sigma$-ring is a nonempty collection of subsets $\cal S$ of $X$ such that:
- If $E, F \in \cal S$, then $E\setminus F \in \cal S$, and
- If $E \in [\mathcal S]^{\omega}$, then $\bigcup E\in \cal S$.

**Th:** If $\mathcal E\subseteq P(X)$, then there exists a unique $\sigma$-ring $\cal S_0$ such that $\cal S_0 \supseteq E$ and such that if $\cal S$ is any other $\sigma$-ring containing $E$ then $\cal S_0 \subseteq S$. 

The $\sigma$-ring $\cal S_0$, the smallest ring containing $E$, is called the *$\sigma$-ring generated* by $E$; it will be denoted as $\cal S(E)$.

**Th:** If $\cal E$ is a collection of subsets of $X$ and $E \in \cal S(E)$, then there exists a countable $\cal D \subseteq E$ such that $F \in \cal S(D)$.

**Def:** Let $\mathcal E \subseteq P(X)$, and $A \subseteq X$, then we can define $$\mathcal E \cap A := \{E\cap A \mid E\in \mathcal E\} $$
**Th:** If $\mathcal E \subseteq P(X)$, and $A \subseteq X$, then $${\mathcal S(\mathcal E)} \cap A = \mathcal S(\mathcal E \cap A)$$
**Th:** We can construct the $\sigma$-ring $\cal S(E)$ through transfinite induction. Let $\mathcal E \subseteq P(X)$ such that $\varnothing \in \mathcal E$. Then $\mathcal E_0 = \cal E$, and for $\alpha> 0$ an ordinal, then $$E_\alpha := \left(\bigcup_{\beta < \alpha} \mathcal E_\beta\right)^*,$$where $\mathcal C^*$ refers to the set of the countable union of of differences of sets in $\mathcal C$. Then $$\mathcal S(\mathcal E) = \bigcup_{\alpha < \omega_1} \mathcal E_\alpha.$$
# Monotone Families

**Def:** A non empty family $\cal M$ of subsets of $X$ is *monotone*, if for every monotone sequence $(E_n)_{n < \omega}$  of sets in $\cal M$, we have that $$\lim_{n \to \infty} E_n \in \cal M.$$
**Th:** If $\mathcal E\subseteq P(X)$, then there exists a unique monotone family $\cal M_0$ such that $\cal M_0 \supseteq E$ and such that if $\cal M$ is any other monotone family containing $\cal E$ then $\cal M_0 \subseteq M$. 

The monotone family $\cal M_0$, the smallest ring containing $\cal E$, is called the *monotone family generated* by $E$; it will be denoted as $\cal M(E)$.

**Th:** A $\sigma$-ring is a monotone family; a monotone ring is a $\sigma$-ring.

**Th:** If $\cal R$ is a ring, then $\cal M(R) = S(R)$. Hence if a monotone family contains a ring $\cal R$, then it contains $\cal S(R)$. 

******
# $\sigma$-Algebra

# $\sigma$-algebras

**Def:** A collection $\mathcal A$ of subsets of $X$ is a $\sigma$-algebra if it satisfies:
- $X \in \mathcal A$
- If $A \in \mathcal A$, then $\Omega\setminus A \in \mathcal A$
- If $A_0, A_1, A_2, \dots \in \mathcal A$, then $\bigcup_{n \in \Bbb N} A_n \in \mathcal A$

**Prop:** Let $\mathcal A$ be a $\sigma$-algebra of subsets of $X$. Then
- $\varnothing \in \mathcal A$
- If $A_0, A_1, A_2, \dots \in \mathcal A$, then $\bigcap_{n \in \Bbb N} A_n \in \mathcal A$
- If $A, B \in \mathcal A$, then $A \setminus B \in \mathcal A$ and $A \, \triangle \, B \in \mathcal A$

**Prop:** The intersection of two $\sigma$-algebras is a $\sigma$-algebra

**Prop:** The arbitrary intersection of $\sigma$ -algebras is a $\sigma$-algebra

********Def:******** Let $\mathscr C$ be a nonempty collection of subsets of $X$. The $\sigma$-algebra generated by $\mathscr C$, denoted as $\sigma(\mathscr C)$ is the collection
$$ \sigma(\mathscr C) := \bigcap\{ \mathcal A \mid \mathcal A \text{ is a $\sigma$-algebra and } \mathscr{C \subseteq} \mathcal A\} .$$We call $\scr C$ a generator of $\sigma(\mathscr C)$. In the special case where $X$ is a topological space, then $\sigma(\tau)$ is called the *Borel $\sigma$-algebra* and it is denoted as $\mathscr B(X)$. 

**Prop:** Let $\mathscr C_1$ and $\mathscr C_2$ be two collection of subsets of $\Omega$ such that $\mathscr C_1 \subseteq \mathscr C_2$. Then ${\sigma(\mathscr C_1) \subseteq \sigma(\mathscr C_2)}$. 

We also have that $\sigma(\mathscr C) = \sigma(\sigma(\mathscr C))$, for any $\mathscr C \subseteq \mathcal P(\Omega)$. 

Let $\mathscr A, \mathscr B \subseteq \mathcal P(\Omega)$, if we have that $\mathscr A \subseteq \sigma(\mathscr B)$ and $\mathscr B \subseteq \sigma(\mathscr A)$, then $\sigma(\mathscr A) = \sigma(\mathscr B)$. 

**Prop:** If $\mathcal A$ is a $\sigma$-algebra, then $\sigma(\mathcal A) = \mathcal A$

**Def:** A $\sigma$-algebra $\cal A$ is *countably generated* if there exists a countable generator, i.e., a sequence $(G_n)_{n \in \Bbb N}$ in $\cal A$ such that $\sigma(\{G_n : n \in \Bbb N\})$. 

**Def:** A set $A \in \cal A$, $A\neq \varnothing$, is an *atom* of $\cal A$ if $A$ doesn't contain any proper measurable subset $B\in \cal A$, i.e., $B \in \cal A$ and $B \subseteq A$, then $B = \varnothing$ or $B =A$.