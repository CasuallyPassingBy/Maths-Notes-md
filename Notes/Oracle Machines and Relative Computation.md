---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Computation Reducibility]], [[Decidable and Undecidable Problems]]

**Def:** An *oracle* for a language $B$ is an external device that is capable of reporting whether any string $w$ is a member of $B$. An *oracle Turing machine* is a modified Turing machine that has the additional capability of querying an oracle. We write $M^B$ to describe an oracle Turing machine that has an oracle for language $B$. 

Formally, an oracle Turing machine is Turing machine that in addition to its ordinary read/write tape is equipped with a special one-way-infinite read-only input tape on which some infinite string is written. The extra tape is called the *oracle tape*, and the string written on it is the called the *oracle*. The machine can move its oracle tape head one cell in either direction in each step and make decisions based on the symbols written on the oracle tape.

We usually think of an oracle as a specification of a set of strings. If the oracle is an infinite string over $\{0, 1\}$, then we can regard it as the characteristic function of a set $B\subseteq \Bbb N$, where the $n$th bit of the oracle string is $1$ iff $n\in\Bbb N$. In that way we can study computation relative to the set $B$.

**Def:** For $A, B\subseteq \Sigma^*$, we say that $A$ is *recursively enumerable in $B$* if there is an oracle Turing machine $M$ with oracle $B$ such that $A= L(M)$. In addition, if $M$ is total, we write $A\le_\text{T}B$ and say that $A$ is *recursive in $B$* or $A$ *Turing reduces to $B$*, 

**Prop:** The relation $\le_\text T$ is transitive. 

**Th:** If $A\le_\text TB$ and $B$ is decidable, then $A$ is decidable.