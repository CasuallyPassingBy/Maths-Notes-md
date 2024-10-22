---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Binary Relations]]

Let $R$ be a binary relation on $A$, if $R$ is reflexive, symmetric and transitive, then $R$ is an _equivalence relation on $A$._

Let $E$ be an equivalence relation on $A$. The _equivalence class of $a$ modulo $E$_ is the set:

$$ [a]_E = \{x \in A \mid x Ea\} $$

Let $a, b \in A$, then:

- $a$ is equivalent to $b$ modulo $E$ iff $[a]_E = [b]_E$.
- $a$ is not equivalent to $b$ modulo $E$ iff $[a]_E \cap [b]_E = \varnothing$.

A system $S$ of nonempty sets is called a _partition of $A$_ if:

- For any $C, D \in S$, then $C \cap D = \varnothing$, or $S$ is system of mutually disjoint sets.
- $\bigsqcup S = A$.

Let $E$ be an equivalence relation on $A$. The system of all equivalence classes modulo $E$ is denoted by $A/E$; so $A /E = \{[a]_E \mid a \in A\}$.

Let $E$ be an equivalence relation on $A$; then $A/E$ is a partition on $A$.

Let $S$ be a partition on . The relation $E_S$ in $A$ is defined by:

$$ E_S =\{(a,b) \in A \mid \exists C \in S[a, b \in C]\} $$

Then $E_S$ is an equivalence relation on $A$.

If $E$ is an equivalence relation on $A$, and $S=A/E$, then $E_S = E$.

If $S$ is a partition on $A$, and $E_S$ is the corresponding equivalence relation, then $A/E_S = S$.

A set $X \subseteq A$ is called a _set of 
representatives_ for the equivalence $E_S$ (or the partition $S$ of $A$), if for every $C \in S$, $X\cap C =\{a\}$ for some $a\in C$.