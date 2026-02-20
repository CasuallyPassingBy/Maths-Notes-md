---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Nondeterministic Pushdown Automata]], [[Deterministic Pushdown Automata]], [[Two-Way Finite Automata]]

**Def:** A *Turing machine* is $9$-tuple $(Q, \Sigma, \Gamma,\textvisiblespace, \vdash, \delta, s, q_\text{accept}, q_\text{reject})$, where $Q$, $\Sigma$ and $\Gamma$ are finite sets and
- $Q$ is the set of states,
- $\Sigma$ is the input alphabet no containing the *blank symbol* $\textvisiblespace$,
- $\Gamma$ is the tape alphabet,
- $\textvisiblespace\in \Gamma\setminus\Sigma$, the *blank symbol*,
- $\vdash\in \Gamma\setminus \Sigma$, the *left endmarker*,
- $\delta: Q \times \Gamma \to Q \times \Gamma \times \{L, R\}$ is the transition function,
- $s\in Q$ is the start state,
- $q_\text{accept}\in Q$ is the state, and
- $q_\text{reject}\in Q$, the *reject state*, $q_\text{accept}\neq q_\text{accept}$
Intuitively, $\delta(p,a ) = (q, b, d)$ means, 'when it state $p$ scanning symbol $a$, write $b$ in that tape cell, and move the head in direction $d$, and entre state $q$'. The symbols $L$ and $R$ stand for left and right. 

We restrict Turing Machines so that the left endmarker is bever overwritten with another symbol and the machine never leaves off the tape to the left of the endmarker. Meaning, we requiere for all $p\in Q$ there exists $q\in Q$ such that $$\delta(p, \vdash) = (q, \vdash, R).$$We also require that once the machine entres it accept state, it never leaves it, similarly, for the reject state; that is for all $b\in\Gamma$ there exist $c, c'\in\Gamma$ and $d, d'\in \{L, R\}$ such that
- $\delta(q_\text{accept}, b) = (q_\text{accept}, c, d)$
- $\delta(q_\text{reject}, b) = (q_\text{reject}, c', d')$.
We sometimes refer to the state set and transition function collectively as the *finite control.*

At any point in time, the read/write tape of the Turing machine $M$ contains a semi-infinite string of the form $y\textvisiblespace^\omega$, where $y\in \Gamma^*$, and $\textvisiblespace^\omega$ denotes the semi-infinite string, $$\textvisiblespace^\omega := \textvisiblespace \textvisiblespace\textvisiblespace\textvisiblespace\cdots.$$Although the string is infinite, it always have a finite representation, since all but finitely many of the symbols are the blank symbol $\textvisiblespace$.

**Def:** We define a *configuration* to be an element $Q\times \{y \textvisiblespace^\omega\mid y\in\Gamma^*\}\times \Bbb N$. A configuration is a global state giving a snapshot of all relevant information about a Turing machine computation at some instant time. The configuration $(p, z, n)$ specifies a current state $p$ of the finite control, current tape contents $z$, and current position of the read/write head $n \ge 0$. We usually denote configurations by $\alpha,\beta, \gamma$.

The *start configuration* on input $x\in \Sigma^*$ is the configuration $$(s, \vdash x\textvisiblespace^\omega, 0).  $$
One can define a *next configuration relation* $\xrightarrow[\, M\,]{1}$ as with $\sf PDA$S. For a string $z\in \Gamma^\omega$, let $z_n$ be the $n$th symbol of $z$, and let $\text s^n_b (z)$ denote the string obtained from $z$ by substituting $b$ for $z_n$ at position $n$. 

The relation $\xrightarrow[\, M\,]{1}$ is defined by  $$(p, z, b) \xrightarrow[\, M\,]{1} \begin{cases} (q, \text s_b^n(z), n-1) & \text{if }\delta(p, z_n) = (q, b, L), \\(q, \text s_b^n(z), n+1) & \text{if }\delta(p, z_n) = (q, b, R). \end{cases} $$
We define the reflexive transitive closure $\xrightarrow[\, M\,]{*}$ of $\xrightarrow[\, M\,]{1}$, inductively, as usual:
- $\alpha \xrightarrow[\, M\,]{0} \alpha$,
- $\alpha \xrightarrow[\, M\,]{n+1}\beta$ if there is a configuration $\gamma$ such that $\alpha \xrightarrow[\, M\,]{n}\gamma$ and $\gamma \xrightarrow[\, M\,]{1}\beta$,
- $\alpha \xrightarrow[\, M\,]{*}\beta$ if $\alpha \xrightarrow[\, M\,]{n}\beta$ for some $n \ge 0$.

The machine $M$ is said to *accept* input $x\in \Sigma^*$ if $$(s, \vdash x\textvisiblespace^\omega, 0) \xrightarrow[\,M\,]{*} (q_\text{accept}, y, n), $$for some $y$ and $n$, and *reject* $x$ if $$(s, \vdash x\textvisiblespace^\omega, 0) \xrightarrow[\,M\,]{*}(q_\text{reject}, y, n), $$for some $y$ and $n$. It is said to *halt* on input $x$ if either accepts $x$ or rejects $X$. It is possible that it neither accepts nor rejects, in which case is said to *loop* on input $x$, A Turing machine is said to be *total* if it halts on all inputs; we also call these machines *deciders*. The set $L(M)$ denotes the set of strings accepted by $M$.

We call a set of strings
- *recursively enumerable*, r.e., or *Turing-recognisable* if it is $L(M)$ for some Turing machine $M$,
- *co-r.e.* or *co-Turing-recognisable* if its complement is r.e., and
- *recursive*, *Turing-decidable*, or *decidable* if it is $L(M)$ for some *total* Turing machine $M$.

# Variants of Turing Machines

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

# [[Two-Stack Pushdown Automata]]

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

