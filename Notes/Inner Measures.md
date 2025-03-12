---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Outer Measures]], [[Extension of Measures]]

We can describe the dual of an outer measure, an inner measure. We now define the *inner measure $\mu_*$ induced by $\mu$*; for every $E \in \cal H(S)$ we write: $$\mu_*(E) := \sup\{\mu(F) \mid F \subseteq E, F \in \mathcal S\}.$$
For this note, we consider that $\mu$ is a $\sigma$-finite measure on a ring $\cal S$, $\mu^*$ and $\mu_*$ are the outer measure and inner measure induced by $\mu$, respectively, and $\overline \mu$ on $\overline{\cal S}$ is the completion of $\mu$. 

**Th:** If $E \in \cal H(S)$, the $$\mu_*(E) = \sup\{\overline \mu(F) \mid F \subseteq E, F \in \overline{\mathcal  S}\}.$$
**Def:** If $E \in \cal H(S)$ and $F\in \cal S$, we shall say that $F$ is a *measurable kernel* of $E$ if $F \subseteq E$ and if for every $G \in \cal S$ for which $G \subseteq E \setminus F$, we have $\mu(G) = 0$. Loosely speaking a measurable kernel of s set $E\in \cal H(S)$ is maximal set in $\overline S$ which is contained in $E$. We see that a measurable kernel is the dual of a [[Extension of Measures#^feda7d|measurable cover]].

**Th:** Every set $E\in \cal H(S)$ has a measurable kernel.

**Th:** If $E\in \cal H(S)$ and $F$ is a measurable kernel of $E$, the $\mu(F) = \mu_*(E)$; if both $F_1$ and $F_2$ are measurable kernels of $E$, then $\mu(F_1 \ \triangle\ F_2)= 0$. 

**Th:** If $\{E_n \mid n \in \Bbb N\}$ is a disjoint sequence of sets in $\cal H(S)$, then $$\mu_*\left(\bigcup_{n = 0}^\infty E_n\right) \ge \sum_{n = 0}^\infty \mu_*(E_n).$$
**Th:** If $A \in \cal H(S)$ and if $\{E_n \mid n \in \Bbb N\}$ is a disjoint sequence of sets in $\overline{\cal S}$ with $\bigcup_{n = 0}^\infty E_n = E$, then $$\mu_*(A \cap E) = \sum_{n = 0}^\infty \mu_*( A \cap E_n).$$
**Th:** If $E\in \overline{\cal S}$, then $$\mu^*(E) = \mu_*(E) = \overline\mu(E),$$and conversely, if $E \in \cal H(S)$ and $$\mu^*(E) = \mu_*(E) < \infty,$$then $E \in \overline{\cal S}$. 

**Th:** If $E, F\in \cal H(S)$ are disjoint, then $$\mu_*(E \cup F) \le \mu_*(E) + \mu^*(F) \le \mu^*(E \cup F.)$$
**Th:** If $E \in \overline{\cal S}$, then for every subset $A$ of $X$, $$\mu_*(E \cap A) + \mu^*(E \setminus A) = \overline\mu(E).$$
With these results, we can get another approach to the extension theorem. If $\mu$ is a $\sigma$-finite measure on a ring $\cal R$, and if $\mu^*$ is the induced outer measure on $\cal H(R)$, then for every $E \in \cal R$ with $\mu(E) < \infty$ and for every $A \in \cal H(R)$, we have $$\mu_*(E \cap A) = \mu(E) - \mu^*(E \setminus A).$$Whenever $E$ and $F$ are two sets of finite measure in $\cal R$ for which $A \cap E = A \cap F$, then it follows that $\mu(E) - \mu^*(E \setminus A) = \mu(F) - \mu^*(A \setminus F)$, then we may use the equation $\mu_*(A \cap E)$ as a definition of inner measure. With this we can define a set $E \in \cal H(R)$ of finite outer measure to be $\mu^*$-measurable iff $\mu_*(E) = \mu^*(E)$. 

**Prop:** If $E$ is a subset of finite measure in $\overline{\cal S}$, if $F\subseteq E$, and if $\overline\mu(E) = \mu^*(F) + \mu^*(E \setminus F)$, then $F \in \overline{\cal S}$.

**Prop:** If $\mu_*$ is a inner measure on a hereditary $\sigma$-ring $\cal H$, and if $\{E_n \mid n \in \Bbb N\}$ is an decreasing sequence of sets in $\cal H$ with $\lim_{n \to \infty} E_n = E$, and for some $m \in \Bbb N$ satisfies $\mu_*(E_m) < \infty$, then $\mu_*(E) = \lim_{n \to\infty} \mu_*(E_n)$. 

**Prop:** If $E \in \cal H(S)$ and $F$ is a measurable cover of $E$, for every $\mu^*$-measurable set $M$, it satisfies $\overline\mu(F\cap M) = \mu^*(E \cap M)$. Conversely, any set $F$ with this property and such that $E\subseteq F \in \cal S$ isa measurable cover of $E$. Similarly, $F$ is a measurable kernel of $E$ iff $F \subseteq E$, $F \in \cal S$ and $\overline\mu(F \cap M) = \mu_*(E \cap M)$ for every $M \in \overline{\cal S}$.