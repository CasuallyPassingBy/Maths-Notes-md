---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]]

### Multitape Turing Machines

A *multitape Turing machine* is like an ordinary Turing machine with several tapes. Each tape has its own head for reading and writing. Initially the input appears on tape $1$ and the other start out blank. The transition function is changed to allow for reading, writing and moving the heads on some or all of the tapes simultateously. Formally, it is$$\delta: Q\times \Gamma^k \to  Q \times \Gamma^k\times \{L, R, S\}^k  $$where $k$ is the number of tapes. The expression $$\delta(q_i, a_1, \dots a_k) = (q_j, b_1,\dots, b_k, d_1, \dots, d_k)$$ means that, if the machine is in state $q_i$ and heads $1$ through $k$ are reading symbols $a_1$ through $a_k$, the machine goes to state $q_j$, writes $b_1$ through $b_k$, and directs each head to move left or right, or stay put, as specified.

**Th:** Every multitape Turing machine has an equivalent single-tape Turing machine.

**Cor:** A language is Turing-recognisable iff some multitape Turing machine recognises.

### Nondeterministic Turing Machines

A nondeterministic Turing machine is defined in the expected way. The transition function for a nondeterministic Turing machine has the form $$\delta:Q \times \Gamma \to \mathcal P(Q\times \Gamma\times \{L, R\}).  $$The computation of a nondeterministic Turing machine is a tree whose branches to different possibilities for the machine. If some branch of the computation leads to the accept state, the machine accepts the input. 

**Th:** Every nondeterministic Turing machines has an equivalent deterministic Turing machine.

**Cor:** A language is Turing-recognisable iff some nondeterminisctic Turing machines recognises it.

We call a nondeterministic Turing machine a *decider* if all branches halt on all inpts.

**Cor:** A language is decidable iff some determinisctic Turing machines decides it. 

### Two-Way Infinte Turing Machines

The modification is that instead of just going to infinity to the right, now we have that it is unbouded in both directions. We see that they don't really add much power since they can be trivially simulated by a $2$-tape Turing Machine pretty easily.

**Th:** Every two-way infinite Turing machines has an equivalent deterministic Turing machine.

**Cor:** A language is Turing-recognisable iff some two-way infinite Turing machines recognises it.

### [[Two-Stack Pushdown Automata]]

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

**Th:** Any language accepted by a $\sf 2PDA$ can be accepted by some Turing machine and any accepted by a Turing machine can be accepted by a $\sf 2PDA$. 

**Def:** $n\sf PDA$ refers a deterministic pushdown automaton with $n$ stacks

**Cor:** Any language accepted by a $\sf PDA$ with $n$ stacks, with $n\ge 2$, called an $n\sf PDA$, can also be accepted by some Turing machine. We see that every $n\sf PDA$ can be simulated by some Turing machine. 

**Cor:** A language is Turing-recognisable iff some $n\sf PDA$ recognises it, with $n \ge 2$.

### Enumerators

**Def:** A *Turing machine* is $8$-tuple $E =(Q, \Sigma, \Gamma,\textvisiblespace, \vdash, \#, \delta, q_0)$, where $Q$, $\Sigma$ and $\Gamma$ are finite sets and
- $Q$ is the set of states,
- $\Sigma$ is the input alphabet no containing the *blank symbol* $\textvisiblespace$,
- $\Gamma$ is the tape alphabet,
- $\textvisiblespace\in \Gamma\setminus\Sigma$, the *blank symbol*,
- $\vdash\in \Gamma\setminus \Sigma$, the *left endmarker*,
- $\#\in \Gamma\setminus \Sigma$ a separator separator, 
- $\delta: Q \times \Gamma \to Q \times \Gamma \times \{L, R\}$ is the transition function,
- $q_0\in Q$ is a start state,
together with a disntiguished output tape.
Whenever $E$ write a string $w\in\Sigma^*$ on the output tape, followed by the separator symbol $\#$, we say that $E$ *outputs* $w$.

The language enumerated by $E$ is $$L(E) = \{w\in \Sigma\mid E\text{ outputs $w$ at some finite stage}\}. $$
**Th:** A language is Turing-recognisable iff some enumerator enumerates it.

This is the reason why Turing-recognisable languages are called recursively enumerable.

**Prop:** A language is decidable iff some enumerator enumerates the language in lexicorgraphical order. 

### Queue Automaton

A *queue automaton* is like a push-down automaton except that the stack is replaced by a queue. A *queue* is a tape allowing symbols to be written only on the left-hand end and real only at the right-hand end. Each write operation, called *push*, adds a symbol to the left-hand end of the queue and each read operation, called *pull*, reads and removes a symbol at the right-hand end. As with a $\sf PDA$, the input is placed on a separate read-only input tape, and the head on the input tap can ove only from from left to right. The input tape contains with a cell with a blank symbol following the input, so that the end of the input can be detected. A queue automaton accepts its input by entering a special accept state at any time. 

**Th:** A language can be recognised by a deterministic queue automaton iff the language is Turing-recognisable. 

### Other Variants

Say a *write-once Turing machine* is a single tape Turing machine that can alter each square at most once, including the input portion of the tape. 

**Th:** Every write-once Turing machines has an equivalent deterministic Turing machine.

**Cor:** A language is Turing-recognisable iff some write-once Turing machine recognises it.

A *Turing machine with left reset* is similar to an ordinary machine but the transition function has the form  $$\delta: Q \times \Gamma\to Q \times \Gamma\{R, \text{RESET}\}. $$If $\delta(q, a) = (r, b, \text{RESET})$, when the machine is in state $q$ reading in $a$, the machines's head jumps to the left-hand end of the tape after it writes $b$ on the tape and enters state $r$.

**Th:** Every left-reset Turing machines has an equivalent deterministic Turing machine.

**Cor:** A language is Turing-recognisable iff some left-reset Turing machine recognises it.