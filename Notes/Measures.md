---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Rings and Algebras of Sets]]

**Def:** A *set function* is a function whose domain is a family of sets. An extended real values set $\mu$ defined on a family $\cal E$ of sets is *additive* if, whenever $E, F, E\cup F \in \cal E$ and $E\cap F = \varnothing$, then $$\mu(E \cup F) = \mu(E) + \mu(F).$$An extended real valued set function $\mu$  defined on a set $\cal E$ is *finitely additive*, if for every disjoint family $\{E_1, \dots, E_n\}$ of sets in $\cal E$ whose union is also in $\cal E$, we have $$\mu\left(\bigcup_{i = 1}^n E_i\right) = \sum_{i = 1}^n\mu(E_i).$$An extended real valued set function $\mu$ defined on a class $\cal E$ is $\sigma$*-additive* if, for every disjoint sequence $\{E_n: n < \omega\}$ of sets in $\cal E$ whose union is also $\cal E$, we have $$\mu\left(\bigcup_{n < \omega} E_n\right) = \sum_{n = 1}^\infty\mu(E_n).$$
**Def:** A *measure* is an extended real valued, non negative, and $\sigma$-additive set function $\mu$, defined on a ring $\cal R$, and such that $\mu(\varnothing) = 0$. 

**Prop:** If $\mu$ is an extended real valued, non negative, and additive set function defined on a ring $\cal R$, and such that exists a $E \in \cal R$ such that $\mu(E) < \infty$, then $\mu(\varnothing) = 0$. 

**Def:** If $\mu$ is a measure on a ring $\cal R$, a set $E \in \cal R$ is said to have *finite measure* if $\mu(E) < \infty;$ the measure of $E$ is $\sigma$-finite if there exists a sequence $\{E_n: n < \omega\}$ of sets in $R$ such that $E \subseteq \bigcup_{n < \omega} E_n$ and $\mu(E_n) < \infty$ for all $n < \omega$. If for each $E\in \cal R$ with $\mu(E) =\infty$ there exists $F\in \cal R$ with $F\subseteq E$ and $0<\mu(F)<\infty$, $\mu$ is called *semifinite.*

**Prop:** If $\cal E$ is a non empty family of sets and $\mu$ a measure on $\cal R(E)$ such that if $E \in \cal E$, then $\mu(E) < \infty$, then $\mu$ is finite on $\cal R(E)$.

**Def:** If the measure of every set $E$ in $\cal R$ is finite or $\sigma$-finite, the measure $\mu$ is called *finite* of $\sigma$-*finite* on $\cal R$. If $X \in \cal R$ (i.e. if $\cal R$ is an algebra) and $\mu(X)$ is finite or $\sigma$-finite, then $\mu$ is called *totally finite* or *totally $\sigma$-finite*, respectively. 

**Prop:** If $\mu$ is a measure on a $\sigma$-ring, then the family of all sets of finite measure is a ring and the family of all sets of $\sigma$-finite measure is a $\sigma$-ring. 

**Prop:** Let $\mu$ be a $\sigma$-finite measure on a $\sigma$-ring. Then the family of all sets of finite measure a $\sigma$-ring iff $\mu$ is finite.

**Prop:** Let $\mu$ be a measure on $(X, {\scr A})$. If is $\sigma$-finite, then there are finite measures $\mu_0, \mu_1,\dots$ on $(X, {\scr A})$ such that $$\mu = \sum_{n<\omega} \mu_n. $$
**Def:** The measure $\mu$ is called *complete* if the conditions $E \in \cal R$, $F \subseteq E$ and $\mu(E) = 0$ imply that $F \in \cal R$. 

**Def:** Let $\cal P$ be a semiring, and $\{E_1, \dots, E_n\}$ a finite pairwise disjoint family of elements of $\cal P$ whose union, $E$ is also in $\cal P$ is called a *$\cal P$-partition* of $E$. Let $\mu$ be an extended real valued, non negative and additive set function. The $\cal P$-partition $\{E_1, \dots, E_n\}$ is called a $\mu$ partition, if for every $F$ in $\cal P$, $$\mu(E \cap F) = \sum_{i = 1}^n \mu(E_i \cap F).$$If $\{E_1, \dots, E_n\}$ and $\{F_1, \dots, F_m\}$ are $\cal P$-partitions of $E$, then $\{E_1, \dots, E_n\}$ is called a *subpartition* of $\{F_1, \dots, F_m\}$ if each set $E_i$ is contained in one of the sets $F_j$. 

**Lemma:** If $\{E_1, \dots, E_n\}$ and $\{F_1, \dots, F_m\}$ are partitions of $E$, then so is their *product*, consisting of all sets of the form $E_i \cap F_j$.

**Lemma:** If a subpartition of a partition $\{E_1, \dots, E_n\}$  is a $\mu$-partition, then $\{E_1, \dots, E_n\}$ is a $\mu$-partition.

**Lemma:** The product of two $\mu$-partitions is a $\mu$-partition.

**Lemma:** If $E = C_0 \subseteq C_1 \subseteq \dots \subseteq C_n = F$, where $C_i \in \cal P$ for $i \in \{0, \dots, n\}$ and if $D_i = C_i - C_{i-1} \in \cal P$, for $i \in \{1, \dots, n\}$, then $\{E, D_1, \dots, D_n\}$ is a $\mu$-partition of $F$. 

**Prop:** Every partition of a set $E$ in $\cal P$ is a $\mu$-partition. Equivalently, we get that If $\mu$ is a extended real valued, non negative and additive set function defined on a Halmos semiring $\cal P$ such that $\mu(\varnothing) = 0$, then $\mu$ is finitely additive.

**Prop:** If $\mu$ is a countably additive and non negative set function on a Halmos semiring $\cal P$, such that $\mu(\varnothing) = 0$, then there is a unique measure $\overline \mu$ on the ring $\cal R(P)$ such that $E\in \cal P$, $\overline \mu(E) = \mu(E)$. If $\mu$ is (totally) finte or $\sigma$-finite, then so is $\overline \mu$. ^29437f

**Def:** An extended real value set function $\mu$ on a family $\cal E$ is *monotone* if, whenever $E, F \in \cal E$, and $E \subseteq F$, then $\mu(E) \le \mu(F)$. 

**Def:** An extended real value set function $\mu$ on a family $\cal E$ is *subtractive* if, whenever $E, F, E\setminus F \in \cal E$, $E \subseteq F$, and $|\mu(E)| < \infty$, then $\mu(F\setminus E) = \mu(F) - \mu(E)$. 

**Th:** If $\mu$ is a measure on a ring $\cal R$, then $\mu$ is monotone and subtractive. 

**Th:** If $\mu$ is a measure on a ring $\cal R$, if $E\in \cal R$, and if $\{E_n: n < \omega\}$ of sets in $\cal R$ such that $E \subseteq \bigcup_{n < \omega} E_n$, then $$\mu(E) \le \sum_{n < \omega} \mu(E_n).$$
**Th:** If $\mu$ is a measure on a ring $\cal R$, if $E \in \cal R$, and if $\{E_n : n  < \omega\}$ inifinite disjoint sequence of sets in $\cal R$ such that $\bigcup_{n < \omega} E_n \subseteq E$, then $$\sum_{n <\omega} \mu(E_n) \le \mu(E).$$
**Th:** If $\mu$ is a measure on a ring $\cal R$ and $\{E_n: n < \omega\}$ is an increasing sequence of sets in $\cal R$ for for which $\lim_{n \to \infty} E_n \in \cal R$, then $$\mu\left(\lim_{n \to \infty} E_n\right) = \lim_{n \to \infty} \mu(E_n).$$
**Th:** If $\mu$ is a measure on a ring $\cal R$ and $\{E_n: n < \omega\}$ is an decreasing sequence of sets in $\cal R$ of which one has finite measure and for which $\lim_{n \to \infty} E_n \in \cal R$, then $$\mu\left(\lim_{n \to \infty} E_n\right) = \lim_{n \to \infty} \mu(E_n).$$
**Def:** An extended real valued set function $\mu$ defined on a family $\cal E$, is *continuous from below* at a set $E$ if for every increasing sequence $\{E_n : n < \omega\}$ of sets in $\cal E$ for which $\lim_{n \to \infty} E_n = E$, we have $\lim_{n \to \infty} \mu(E_n) = \mu(E)$. Similarly, $\mu$ is *continuous from above* at $E$ if, for every decreasing sequence $\{E_n : n <\omega\}$ of sets in $\cal E$ for which $|\mu(E_m)| <\infty$ for at least one value of $m$ and for which $\lim_{n \to \infty} \mu(E_n) = \mu(E)$.  ^d64f4b

**Obs:** The two theorems above, we see that if $\mu$ is a measure, then $\mu$ is continuous from above and from below. 

**Cor:** If $\mu$ is a measure on a ring $\cal R$ and if $\{E_n : n < \omega\}$ is a sequence of sets in $\cal R$ for which $\bigcap_{n \le m < \omega} E_n \in \cal R$, for $m < \omega$ and $\liminf_{n \to \infty} E_n \in \cal R$, then $$\mu\left(\liminf_{n \to \infty} E_n\right) \le \liminf_{n \to \infty} \mu(E_n).$$
**Cor:** If $\mu$ is a measure on a ring $\cal R$ and if $\{E_n : n < \omega\}$ is a sequence of sets in $\cal R$ for which $\bigcup_{n \le m < \omega} E_n \in \cal R$, for $m < \omega$, $\liminf_{n \to \infty} E_n \in \cal R$, and if $\mu\left(\bigcup_{n \le m < \omega} E_m\right) < \infty$ then $$ \limsup_{n \to \infty} \mu(E_n)\le \mu\left(\limsup_{n \to \infty} E_n\right).$$
**Cor:** If $\mu$ is a measure on a ring $\cal R$ and if $\{E_n : n < \omega\}$ is a sequence of sets in $\cal R$ for which $\bigcup_{n \le m < \omega} E_n \in \cal R$, for $m < \omega$, $\liminf_{n \to \infty} E_n \in \cal R$, if $\mu\left(\bigcup_{n \le m < \omega} E_m\right) < \infty$, and $\sum_{n <\omega} \mu(E_n) < \infty$, then $\mu\left(\limsup E_n\right) = 0$. 

**Th:** Let $\mu$ a finite, non negative, and additive set function on a ring $\cal R$. If $\mu$ is either continuous from below at every $E\in \cal R$, or continuous from below at $\varnothing$, then $\mu$ is a measure on $\cal R$.

**Prop:** If $\mu$ is a measure on a ring $\cal R$, then if $E, F\in \cal R$, then $\mu(E) + \mu(F) = \mu(E \cup F) + \mu(E \cap F)$. 

