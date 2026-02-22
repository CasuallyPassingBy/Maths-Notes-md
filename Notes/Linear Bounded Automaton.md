---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Strings and Languages]], [[Finite Automaton]], [[Nondeterministic Pushdown Automata]], [[Deterministic Pushdown Automata]], [[Turing Machines]], [[Decidable and Undecidable Problems]]

**Def:** A *linear bounded automaton*, $\sf LBA$, is a restricted type of Turing machine wherein the tape head isn't permitted to move off the portion of the tape containing the input. If the machine tries to move its head off either input, the head stays where it is, in the same way the head will not move off the left-hand end of an ordinary Turing machine's end. 

Using a tape alphabet larger than the input alphabet allows the available memory to be increased up to a constant factor. Hence we say that for an input length $n$, the amount of memory available is linear in $n$, the name of this model.

Despite the memory constrain, $\sf LBA$s are quite powerful. The deciders for $A_\mathsf{DFA}$, $A_\mathsf{CFG}$, $E_\mathsf{DFA}$, and $E_\mathsf{CFG}$ all are $\sf LBA$s. 