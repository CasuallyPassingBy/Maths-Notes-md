---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Nondeterministic Pushdown Automata]], [[Deterministic Pushdown Automata]]

A two stack $\sf NPDA$, $\sf 2PDA$, is defined as a $9$-tuple: $M = (Q, \Sigma,\Gamma, \Gamma', \delta, s, \bot, \bot', F)$
- $Q$ is the set of states.
- $\Sigma$ is the input alphabet.
- $\Gamma$ the alphabet of the first stack.
- $\Gamma'$ the alphabet of the second stack.
- $\delta: (Q\times \Sigma_\varepsilon\times \Gamma\times \Gamma') \to (Q\times \Gamma^*\times \Gamma'^*)$, $\delta$ is finite and is the *transition relation*,
- $s$ the start state.
- $\bot$ the bottom symbol for the first stack.
- $\bot'$ the bottom symbol for the second stack.
- $F\subseteq Q$ the set of final or accepting states.
If $$((p, a, A, B), (q, A_1A_2\cdots A_k, B_1\cdots B_m)) \in \delta  $$this means intuitively that whenever the machine is in the state $p$ reading input symbol $a$ on the input tape, $A$ on the top of the first stack and $B$ on top of the second stack, it can pop $A$ and $B$ off the stack, push $A_1\cdots A_k$ onto the first stack and $B_1\cdots B_m$ onto the second stack, move its head right one cell past $a$, and enter state $q$. If $$((p, \varepsilon, A, B), (q, A_1A_2\cdots A_k, B_1\cdots B_m)) \in \delta  $$this means intuitively the machine in in the state $p$ with $A$ on the top of the first stack and $B$ on top of the second stack, it can pop $A$ and $B$ off the stack, push $A_1\cdots A_k$ onto the first stack and $B_1\cdots B_m$ onto the second stack, move its head right one cell past $a$, and enter state $q$.

**Th:** Any language accepted by a $\sf 2PDA$ can be accepted by some Turing machine and any accepted by a Turing machine can be accepted by a $\sf 2PDA$. 

**Def:** $n\sf PDA$ refers a deterministic pushdown automaton with $n$ stacks

**Cor:** Any language accepted by a $\sf PDA$ with $n$ stacks, with $n\ge 2$, called an $n\sf PDA$, can also be accepted by some Turing machine. We see that every $n\sf PDA$ can be simulated by some Turing machine. 

**Cor:** A language is Turing-recognisable iff some $n\sf PDA$ recognises it, with $n \ge 2$.