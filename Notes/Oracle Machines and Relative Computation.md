---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Computation Reducibility]], [[Decidable and Undecidable Problems]]

**Def:** An *oracle* for a language $B$ is an external device that is capable of reporting whether any string $w$ is a member of $B$. An *oracle Turing machine* is a modified Turing machine that has the additional capability of querying an oracle. We write $M^B$ to describe an oracle Turing machine that has an oracle for language $B$. 

Formally, an oracle Turing machine is Turing machine that in addition to its ordinary read/write tape is equipped with a special one-way-infinite read-only input tape on which some infinite string is written. The extra tape is called the *oracle tape*, and the string written on it is the called the *oracle*. The machine can move its oracle tape head one cell in either direction in each step and make decisions based on the symbols written on the oracle tape.

We usually think of an oracle as a specification of a set of strings. If the oracle is an infinite string over $\{0, 1\}$

**Def:** A language $A$ is *Turing decidable* to language $B$, written $A\le_\text T B$, if $A$ is decidable relative to $B$. 

**Th:** If $A\le_\text TB$ and decidable, then $A$ is decidable.