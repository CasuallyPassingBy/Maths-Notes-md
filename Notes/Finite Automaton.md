---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Strings and Languages]], [[Operations and Structures]], [[Finite and Countable Sets]]

**Def:** A *finite automaton* is a $5$-tuple $(Q, \Sigma, \delta, q_0, F)$, where
1. $Q$ is a finite set called the *states*,
2. $\Sigma$ is a finite set called the *alphabet*,
3. $\delta: Q\times \Sigma \to Q$ is the *transition function*,
4. $q_0\in Q$ is the *start state*, and
5. $F\subseteq Q$ is the *set of accept states* or *set of final states*. 

**Def:** Let $M = (Q, \Sigma, \delta, q_0, F)$ be a finite automaton and let $w = w_1 \cdots w_n$ be a string where $w_i$ is a member of the alphabet $\Sigma$. Then $M$ *accepts* $w$ if sequence of states $r_0, r_1, \dots, r_n\in Q$ exists with three conditions:
- $r_0 = q_0$,
- $\delta(r_i, w{i+1}) = r_{i+1}$, for $i = 0, \dots, n-1$ and
- $r_n \in F$.
We say that $M$ recognises language $A$ if $A = \{w\in \Sigma^* \mid M \text{ accepts }w\}$. 

**Def:** A language is called a *regular language* if some finite automaton recognises it. 

**Th:** The class of regular languages is closed under the union operation. In other words, if $A_1$ and $A_2$ are regular languages, so is $A_1 \cup A_2$.

# Nondeterministic Finite Automaton

Nondeterminism is useful concept that has had great impact on the theory of computation. When the machine is in a given state and reads the next input symbol, we know that the next state will be, it is determined. We call this *deterministic* computation. In a *nondeterministic* machine several choices exists for the next state at any point. 

Nondeterminism is a generalisation of determinism, so every finite automaton is automatically a nondeterministic finite automaton. The difference between a deterministic finite automaton, abbreviated $\sf DFA$, and nondeterministic finite automaton $\sf NFA$, is immediately apparent. 

The formal definition of a nondeterministic finite automaton is similar to that of a deterministic finite automaton. However, they differ in one essential way: in the type of transition function. In a $\sf DFA$ the transition functions takes a state and an input symbol and procedes to the next state. While in a $\sf DFA$ the transition functions takes a state and an input symbol and produces the next state, in an $\sf NFA$ the transition function takes a state and an input symbol *or the empty string* and produces *the set of possible next states*. 

**Def:** For any alphabet $\Sigma$ we write $\Sigma_\varepsilon := \Sigma \cup \{\varepsilon\}$. 

**Def:** A *nondeterministic finite automaton* is a $5$-tuple $(Q, \Sigma, \delta, q_0, F)$ where
1. $Q$ is a finite set called the *states*,
2. $\Sigma$ is a finite set called the *alphabet*,
3. $\delta: Q\times \Sigma_\varepsilon \to\mathcal P( Q)$ is the *transition function*,
4. $q_0\in Q$ is the *start state*, and
5. $F\subseteq Q$ is the *set of accept states* or *set of final states*. 

**Def:** Let $N = (Q, \Sigma, \delta, q_0, F)$ be an $\sf NFA$ and $w$ is a string over the alphabet $\Sigma$. Then we say that $N$ **accepts** $w$ if we can write $w = y_1 y_2 \cdots y_n$ where $y_i$ is a member of $\Sigma_\varepsilon$ and a sequence of states $r_0,\dots, r_m$ exists in $Q$ with three conditions:
1. $r_0 = q_0$.
2. $r_{i+1} \in \delta(r_i, y_{i+1})$, for $i = 0,\dots, m-1$, and
3. $r_m \in F$.

**Def:** We say that two machines are *equivalent* if they recognise the same language.

**Th:** Every nondeterministic finite automaton has an equivalent deterministic finite automaton. 

From the proof we get an algorithm to transform between $\sf NFA$ and $\sf DFA$.

**Algorithm:** Let $N = (Q, \Sigma, \delta, q_0, F)$ be the $\sf NFA$ recognising some language $A$. Now we deal with $\varepsilon$ arrow/transitions. To do so we set up an extra bit of notation. For any state $R\in Q$, we define $$R(E):=\{q\in Q \mid q \text{ can be reached from }R \text{ by traveling along }0 \text{ or more }\varepsilon \text{ arrows}\}. $$ We construct a $\sf DFA$, $M:= (Q',\sigma, \delta', q_0', D)$ recognising $A$. 
1. $Q' := \mathcal P(Q)$. 
2. For $R\in Q'$ and $a\in\Sigma$, let $$\delta'(R, a) := \bigcup_{r\in R} E(\delta(r, a)).  $$
3. $q_0' := \{q_0\}$.
4. $F' = \{R\in Q' \mid R \cap F \neq \varnothing\}$. 

**Cor:** A language is regular iff some nondeterministic finite automaton recognises it.

Using this equivalence we get simpler proofs for the following theorem. The class of regular languages is closed under the union operation. 

**Th:** The class of regular languages is closed under concatenation operation.

**Th:** The class of regular languages is closed under the star operation.

**Prop:** Every $\sf NFA$ can be converted to an equivalent one that has a single accept state.