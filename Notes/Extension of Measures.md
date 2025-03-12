---
tags:
  - MeasureTheory
---
Subjects: [[Measure Theory]]
Links: [[Measures]], [[Rings and Algebras of Sets]]

**Prop:** If $\mu$ is a measure on a ring $\cal R$, $\mu^*$ is the induced outer measure on $\cal H(R)$ and $\overline \mu$ is the measure induced by $\mu^*$ on the $\sigma$-ring $\overline{\mathcal S}$ of all $\mu^*$-measurable sets, then every set in $\mathcal S(R)$ is $\mu^*$-measurable. 

**Th:** If $E\in \cal H(R)$, them $$\begin{align*}
\mu^*(E) &= \inf\{\overline\mu(F) \mid E \subseteq G \in \overline{\cal S}\} \\
& = \inf\{\overline\mu(F) \mid E\subseteq F \in \mathcal{S(R)}\}.
\end{align*}$$This is equivalent that the outer measure induced by $\overline \mu$ on $\cal S(R)$ and the outer measure induced by $\overline \mu$ on $\overline{\cal S}$ both coincide with $\mu^*$.

**Def:** If $E \in \cal H(R)$ and $F \in \cal S(R)$, we shall say that $F$ is *measurable cover* of $E$ if $E\subseteq F$ and if, for every set $G \in \cal S(R)$ for which $G\subseteq F \setminus E$, we have $\overline\mu(G) = 0$. Loosely speaking, a measurable cover of a set $E$ in $\cal H(R)$ is a minimal set in $\cal S(R)$ which covers $E$.  ^feda7d

**Th:** If a set $E \in \cal H(R)$ is a $\sigma$-finite measure, then there exists a set $F \in \cal S(R)$ such that $\mu^*(E) = \overline\mu(F)$ and such that $F$ is a measurable cover of $E$.

**Th:** If $E \in \cal H(R)$ and $F$ is a measurable cover of $E$, then $\mu^*(E) = \overline\mu(F)$; if both $F_1$ and $F_2$ are measurable covers of $E$, then $\overline\mu(F_1 \; \triangle\; F_2) = 0$. 

**Cor:** If $\mu$ on $\cal R$ is $\sigma$-finite, then so are the measure $\overline \mu$ on $\cal S(R)$ and $\overline \mu$ on $\overline{\cal S}$. 

**Def:** Let $\mu^*$ is an outer measure, $\overline \mu$ be the induced measure, and $\overline \mu^*$ is the outer measure induced by $\overline \mu$. In general we have that $\mu^*$ and $\overline \mu^*$ are not the same, if, however, the induced outer measure $\overline \mu^*$ does coincide with the original outer measure $\mu^*$, then $\mu^*$ is called *regular*.

**Prop:** If $\mu^*$ is a regular outer measure on a hereditary $\sigma$-ring $\cal H$ and if $\{E_n : n < \omega\}$ an increasing sequence of sets in $\cal H$ with $\lim_{n \to \infty} E_n = E$, then $\mu^*(E) = \lim_{n \to \infty}\mu^*(E_n)$. This result cannot be generalised to non regular outer measure. 

# Extension, Completion and Approximation

**Th:** If $\mu$ is a $\sigma$-finite measure on a ring $\cal R$, then there is a unique measure $\overline \mu$ on the $\sigma$-ring $\cal S(R)$ such that, for $E$ in $\cal R$, $\overline \mu(E) = \mu(E)$; the measure in $\overline \mu$ is $\sigma$-finite.

The measure $\overline \mu$ is called the *extension* of $\mu$. 

**Th:** If $\mu$ is a measure on a $\sigma$-ring $\cal S$, then the class $\overline{\cal S}$ of all sets of the form $E\ \triangle \ N$, where $E \in \cal S$ and $N$ is a subset of a measure zero set in $\cal S$, is a $\sigma$-ring, and the set function $\overline \mu$ defined by $\overline \mu(E \ \triangle \ N) = \mu(E)$ is a complete measure on $\overline{\cal S}$. 

The measure $\overline \mu$ is called the *completion* of $\mu$. 

**Prop:** Suppose that $\mu$ is a measure on a $\sigma$-ring $\cal S$ and that $\overline \mu$ on $\overline{\cal S}$ is its completion. If $A, B \in \cal S$ and if $A \subseteq E \subseteq B$, and $\mu(B\setminus A) = 0$, then $E \in \overline{\cal S}$. 

**Th:** If $\mu$ is a $\sigma$-finite measure on a ring $\cal R$, and if $\mu^*$ is the outer measure induced by $\mu$, then the completion of the extension of $\mu$ to $\cal S(R)$ is identical with $\mu^*$ on the family of $\mu^*$-measurable sets.

**Prop:** If $\mu$ is a $\sigma$-finite measure on a ring $\cal R$, then, for every set $E$ of finite measure in $\cal S(R)$ and for every $\varepsilon>0$, there exists a set $E_0 \in \cal R$ such that $\mu(E \ \triangle \ E_0) \le \varepsilon$.

