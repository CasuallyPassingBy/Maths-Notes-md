---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Context-Free Grammars and Parsing]], [[Finite Automaton]]

**Def:** A *nondeterministic pushdown automaton*, $\sf NPDA$, is a $6$-tuple $(Q, \Sigma, \Gamma,\delta, s , F)$ where $Q, \Sigma, \Gamma$ and $F$ are finite sets, and 
- $Q$ is the set of states,
- $\Sigma$ is the input alphabet,
- $\Gamma$ is the stack alphabet,
- $\delta: Q\times \Sigma_\varepsilon\times \Gamma_\varepsilon \to \mathcal P(Q\times \Gamma_\varepsilon)$ is the transition function,
- $s\in Q$ is the start state, and 
- $F\subseteq Q$ is the set of accept states or final states. 

A pushdown automaton $M= (Q, \Sigma, \Gamma,\delta, s , F)$ computes as follows. It accepts input $w$ if $w$ can be written as $w = w_1w_2\cdots w_m$ where each $w_i\in \Sigma_\varepsilon$ and sequences of states $r_0, r_1,\dots, r_m\in Q$ and strings $s_0, s_1,\dots, s_m\in \Gamma^*$ exist such that satisfy the following three conditions. The string $s_i$ represent the sequence of stack contents that $M$ has on the accepting branch of the computation.
- $r_0 = q_0$ and $s_0 =\varepsilon$. This condition signifies that $M$ starts out properly, in the start state and with an empty stack.
- For $i = 0,\dots, m-1$, we have $(r_{i+1}, b)\in \delta(r_i, w_{i+1}, a)$, where $s_i = at$ and $s_{i+1} = bt$ for some $a, b\in \Gamma_\varepsilon$ and $t\in\Gamma^*$. This condition states that $M$ moves properly according to the state, stack and next input symbol.
- $r_m\in F$. This condition states that an accept state occurs at the end.

**Lemma:** If a language is context-free, then some pushdown automaton recognises it.

**Lemma:** If a pushdown automaton recognises some language, then it is context free.

**Th:** A language is context-free iff some pushdown automaton recognises it.