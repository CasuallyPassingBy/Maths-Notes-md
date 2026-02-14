---
tags:
---
Subject: [[Compilers]]
Links: [[Strings and Languages]], [[Finite Automaton]]

**Def:** Say that $R$ is a *regular expression* if $R$ is
1. $a$ for some $a$ in the alphabet $\Sigma$,
2. $\varepsilon$,
3. $\varnothing$,
4. $(R_1 \cup R_2)$, where $R_1$ and $R_2$ are regular expressions,
5. $(R_1 \circ R_2)$, where $R_1$ and $R_2$ are regular expressions,
6. 6. $(R_1^*)$, where $R_1$ is a regular expression.
7. $(R_1^*)$, where $R_1$ is a regular expression.

A definition of this type is called an *inductive definition*.

**Def:** Let $R$ be a regular expression. We use the shorthand $R^+ := R \circ R^* = R^*\cup \varepsilon$. In addition, we let $R^1 := R$, and $R^{k+1} := R^k \circ R$, for $k\in\Bbb N^+$.

We want to distinguish between a regular expression $R$ and the language it describes, we write $L(R)$ to be the language of $R$. 

**Lemma:** If a language is described by a regular expression, then it is regular.

**Def:** A *generalised nondeterministic finite automaton* if a $5$-tuple, $(Q, \Sigma, \delta, q_\text{start}, q_\text{accept})$, where
1. $Q$ is the finite set of states,
2. $\Sigma$ si the input alphabet,
3. $\delta: (Q\setminus\{q_\text{accept}\})\times (Q\setminus\{q_\text{start}\})\to \mathcal R$, where $\cal R$ is the set of all regular expressions, is the transition function,
4. $q_\text{start}$ is the start state, and
5. $q_\text{accept}$ is the accept state.

A $\sf GNFA$ accepts a string in $\Sigma^*$ if $w = w_1w_2\cdots w_k$, where each $w_i$ is in $\Sigma^*$ and a sequence of states $q_0,\dots, q_k$ exists such that
1. $q_0 = q_\text{start}$ is the start state,
2. $q_k = q_\text{accept}$ is the accept state, and
3. for each $i$, we have $w_i \in L(R_i)$, where $R_i = \delta(q_{i-1}, q_i)$; in other words, $R_i$ is the expression on the arrow from $q_{i-1}$ to $q_i$.

We use a recursive algorithm to convert from a $\sf GNFA$ with $k$ states to one with $k-1$ states till we get a $\sf GNFA$ with $2$ states. 

**Algorithm:**  Let $G = (Q, \Sigma, \delta, q_\text{start}, q_\text{accept})$ be a $\sf GNFA$.
- Let $k$ be the number of states of $G$.
- If $k = 2$, then $G$ must consist of a start state, an accept state, and a single arrow connecting them labelled with a regular expression $R$.
- If $k> 2$, we select any state $q_\text{rip}\in Q\setminus \{q_\text{start}, q_\text{accept}\}$, and let $G'$ be the $\sf GNFA$ $(Q', \Sigma, \delta', q_\text{start}, q_\text{end})$, where $$Q' := Q\setminus \{q_\text{rip}\},  $$and for any $q_i \in  Q'\setminus\{q_\text{accept}\}$ and any $q_j \in Q'\setminus \{q_\text{start}\}$ let $$\delta'(q_i, q_j) := (R_1)(R_2)^*(R_3) \cup (R_4),  $$for $R_1 := \delta(q_i, q_\text{rip})$, $R_2 := \delta(q_\text{rip},q_\text{rip} )$, $R_3 = $\delta(q_\text{rip}, q_j)$, and $R_4 := \delta(q_i, q_j)$.

**Lemma:** For any $\sf GNFA$ $G$, then $G'$ obtained from the procedure described above is equivalent to $G$. 

**Cor:** For any $\sf GNFA$ $G$, there's an equivalent $2$ state $\sf GNFA$. 

**Lemma:** If a language is regular, then it is described by a regular expression.

**Th:** A language is regular iff some regular expression describes it.

# Nonregular Expressions

Let's take the language $B := \{0^n 1^n \mid n \ge 0\}$ of the alphabet $\Sigma := \{0, 1\}$. If we attempt to find a $\sf DFA$ that recognises $V$, we discover that the machines seems to need to remember how many $0$s have been seen so far as it reads the input. Because the number of $0$s is not limited, the machines will have to keep track of an unlimited number of possibilities. But it cannot do so with a finite number of states. While this is not a proof that $B$ is not a regular language is an intuitive argument of why it is.

**Pumping Lemma:** If $A$ is a regular language, then there is a number $p$, the pumping length, where, if $s$ is any string in $A$ of length at least $p$, then $s$ mayb be divided into three pieces, $s = xyz$, satisfying the following conditions.
1. for each $n \ge 0$, $xy^n z\in A$,
2. $|y| > 0$, and 
3. $|xy| \le p$. 

We see that $B$, in the example above, cannot be a regular language by the pumping lemma. 

**Prop:** Let $B$ be any language over the alphabet $\Sigma$. Then $B = B^+$ iff $B\circ B \subseteq B$. 

**Examples:** Of languages over $\Sigma: = \{0, 1\}$ that are not regular, and can be shown that they aren't by the pumping lemma.
- $C := \{w \in \Sigma^* \mid w \text{ has an equal number of }0\text{s and }1\text{s}\}$, we can consider the string $0^p1^p$, where $p$ is the pumping length if it was regular.
- $F := \{ww \mid w\in \Sigma^*\}$, we consider the the string $0^p10^p1$, where $p$ is the pumping length if it was regular.
- $D := \{1^{n^2}\in \Sigma^* \mid n \in \Bbb N\}$. We simply use that fact that squares grow apart much faster than the separation of the pumping lemma allows.
- $E := \{0^i 1^j \mid i > j\}$,  we can consider the string $0^{p+1}1^p$, where $p$ is the pumping length if it was regular.

**Def:** A *finite state transducer* ($\sf FST$) is a type of deterministic finite automaton whose output is a string and just *accept* or *reject*. 