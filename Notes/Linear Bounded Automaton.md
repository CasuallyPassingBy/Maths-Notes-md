---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Strings and Languages]], [[Finite Automaton]], [[Nondeterministic Pushdown Automata]], [[Deterministic Pushdown Automata]], [[Turing Machines]], [[Decidable and Undecidable Problems]]

**Def:** A *linear bounded automaton*, $\sf LBA$, is a restricted type of Turing machine wherein the tape head isn't permitted to move off the portion of the tape containing the input. If the machine tries to move its head off either input, the head stays where it is, in the same way the head will not move off the left-hand end of an ordinary Turing machine's end. 

Using a tape alphabet larger than the input alphabet allows the available memory to be increased up to a constant factor. Hence we say that for an input length $n$, the amount of memory available is linear in $n$, the name of this model.

Despite the memory constrain, $\sf LBA$s are quite powerful. The deciders for $A_\mathsf{DFA}$, $A_\mathsf{CFG}$, $E_\mathsf{DFA}$, and $E_\mathsf{CFG}$ all are $\sf LBA$s. 

Here, $A_\mathsf{LBA}$ is the problem of determining whether on $\sf LBA$ accepts its input. Let $$A_\mathsf{LBA} := \{\langle M, w\rangle\mid \text{$M$ is an $\sf LBA$ that accepts string }w\}.$$
**Lemma:** Let $M$ be an $\sf LBA$ with $q$ states and $g$ symbols in the tape alphabet. There are exactly $qng^n$ distinct configurations of $M$ for a tape of length $n$. 

**Th:** $A_\mathsf{LBA}$ is decidable. 

Let $$E_\mathsf{LBA} := \{\langle M\rangle\mid \text{$M$ is an $\sf LBA$ and }L(M) = \varnothing\}.$$**Th:** $E_\mathsf{LBA}$ is undecidable. 