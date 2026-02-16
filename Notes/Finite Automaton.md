---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Strings and Languages]], [[Operations and Structures]]

**Def:** A *deterministic finite automaton* ($\sf DFA$) is a structure $M = (Q, \Sigma, \delta, s, F)$, where
- $Q$ is a finite set; elements of $Q$ are called *states*;
- $\Sigma$ is a finite set, the *input alphabet*;
- $\delta: Q\times \Sigma \to Q$ is the *transition function*;
- $s\in Q$ is the *start state*;
- $F\subseteq Q$; elements of $F$ are called *accept states* or *final states*. 

To be able to accept or reject we need to define a function $\hat \delta: Q\times \Sigma^* \to Q$ from $\delta$ by induction on the length of $x$: $$
\begin{align*}
\hat\delta(q, \varepsilon) &:= q, \\
\hat\delta(q, xa) &:= \delta(\hat\delta(q, x), a).
\end{align*}
$$
The function $\hat \delta$ maps a state $q$ and a string $x$ to a new state $\hat\delta(q, x)$. 

Formally, a string $x$ is said to be *accepted* by the automaton $M$ if $$\hat\delta(s, x) \in F, $$and *rejected* by the automaton $M$ if $$\hat\delta(s, x)\notin F,$$where $s$ is the start state and $F$ is the set of accept states.

**Def:** The *set* or *language accepted* by $M$ is the set of all strings accepted by $M$ and is denoted $L(M)$: $$L(M) := \{x\in \Sigma^* \mid \hat\delta(x,s ) \in F\}.$$A subset $A\subseteq\Sigma^*$ is said to be *regular* if $A = L(M)$ for some finite automaton $M$.

**Prop:** Let $M = (Q, \Sigma, \delta, s, F)$ be an arbitary $\sf DFA$. For all strings $x, y\in \Sigma^*$ and $q\in Q$ $$\hat\delta(q, xy) = \hat\delta(\hat\delta(q, x), y).  $$
**The Product Construction:** Assume that $A$ and $B$ are regular languages. Then there are automata
- $M_1 = (Q_1, \Sigma, \delta_1, s_1, F_1)$,
- $M_2 = (Q_2, \Sigma, \delta_2, s_2, F_2),$
with $L(M_1) = A$ and $L(M_2) = B$. Let $M_3 = (Q_3, \Sigma, \delta_3, s_3, F_3)$, where
- $Q_3 := Q_1\times Q_2$,
- $F_3 = F_1 \times F_2$,
- $s_3 = (s_1, s_2)$
- $\delta_3: Q_3\times\Sigma \to Q_3$ be the transition function by  $$\delta_3((p, q), a) := (\delta_1(p, a), \delta_2(q,a)).$$
The automaton $M_3$ is called the *product* of $M_1$ and $M_2$. 

**Lemma:** For all $x\in \Sigma ^*$ $$\hat \delta_3((p, q), x) = (\hat\delta_1(p, x), \hat\delta_2(q, x)).$$
**Th:** $L(M_3) = L(M_1) \cap L(M_2)$. 

**Th:** If $A$ is a regular language over $\Sigma$, and $M = (Q, \Sigma, \delta, s, F)$ is the deterministic finite automaton that recognises $A$, then $M' = (Q, \Sigma, \delta, s, Q\setminus F)$ recognises $\Sigma^*\setminus A$. 

**Cor:**  Assume that $A$ and $B$ are regular languages. Then there are automata
- $M_1 = (Q_1, \Sigma, \delta_1, s_1, F_1)$,
- $M_2 = (Q_2, \Sigma, \delta_2, s_2, F_2),$
with $L(M_1) = A$ and $L(M_2) = B$. Let $M_3 = (Q_3, \Sigma, \delta_3, s_3, F_3)$, where
- $Q_3 := Q_1\times Q_2$,
- $F_3 = (Q_1 \times F_2 )\cup (F_1\times Q_2)$,
- $s_3 = (s_1, s_2)$
- $\delta_3: Q_3\times\Sigma \to Q_3$ be the transition function by  $$\delta_3((p, q), a) := (\delta_1(p, a), \delta_2(q,a)).$$
Then $L(M_3) = L(M_1) \cup L(M_2)$. 

**Th:** Let $h : \Sigma^* \to \Gamma^*$ be a string homomorphism. If $B\subseteq \Gamma^*$ is regular, then so is its inverse image $h^{-1}[B]$ under $h$. 

**Th:** Let $h : \Sigma^* \to \Gamma^*$ be a string homomorphism. If $A\subseteq \Sigma^*$ is regular, then so is its image $h[A]$ under $h$. 

**Pumping Lemma:** If $A$ is a regular language, then there is a number $p$, the pumping number, where if $s$ is any string in $A$ of length at least $p$, then $s$ may be divided into three pieces $s = xyz$, satisfying the following conditions:
- For each $i \ge 0$, $xy^iz\in A$,
- $|y| > 0$, and
- $|xy| \le p$. 

**Def:** Let $U\subseteq\Bbb N$. The set $U$ is said to be *ultimately periodic* if there exist numbers $n \ge 0$ and $p >0$ such that for all $m \ge n$, $m\in U$ iff $m+p\in U$. The number $p$ is called the *period of $U$*.

**Th:** Let $A\subseteq\{a\}^*$. Then $A$ is regular iff the set $\{m \mid a^m \in A\}$, the set of lengths of strings in $A$, is ultimately periodic. 

**Cor:** Let $A$ be any regular set over any finite alphabet $\Sigma$. Then the set  $\text{length }A := \{|x|\mid x\in A\}$ of lengths of strings in $A$ is ultimately periodic,

# Nondeterminisitc Finite Automata

**Def:** A *nondetermonistic finite automaton* ($\sf NFA$) is a $5$-tuple $N = (Q, \Sigma, \Delta, S, F)$ where 
- $Q$ is a finite set; elements of $Q$ are called *states*;
- $\Sigma$ is a finite set, the *input alphabet*;
- $\Delta: Q\times \Sigma \to \mathcal P(Q)$ is the *transition function*;
- $S \subseteq Q$ is the *set of start state*;
- $F\subseteq Q$; elements of $F$ are called *accept states* or *final states*. 

Intuitively, $\Delta(q, a)$ gives the set of all states that $N$ is allowed to move from $p$ in one step under input symbol $a$. We often write  $p\stackrel{a}{\longrightarrow} q$, if $q\in\Delta(p, a)$. The set $\Delta(p, a)$ can be the empty set $\varnothing$. The function $\Delta$ is called the *transition function*. 

We define the acceptance for $\sf NFA$s. The function $\Delta$ extends in a natural way by induction to a function $$\hat\Delta: \mathcal P(Q) \times \Sigma^* \to \mathcal P(Q)  $$according to the rules$$
\begin{align*}
\hat\Delta(A, \varepsilon) &:= A, \\
\hat\delta(A, xa) &:= \bigcup_{q\in \hat\Delta(A, \varepsilon)} \Delta(q, a)\end{align*}. $$
For $A\subseteq Q$, and $x\in \Sigma^*$. $\hat\Delta(A, x)$ is the set of all states reachable under input string $x$ from *some* state in $A$. Note that for $a\in \Sigma$,  $$\hat\Delta(A, a) = \bigcup_{p\in \hat\Delta(A,\varepsilon)}\Delta(p, a) = \bigcup_{p\in A}\Delta(p, a). $$
The automaton $N$ is said to *accept* $x\in \Sigma^*$ if $$\hat\Delta(S, x) \cap F \neq \varnothing. $$
We define $L(N)$ to be the set go all strings accepted by $N$: $$L(N) :=  \{x\in \Sigma^* \mid N \text{ accepts }x\}. $$

Under this definition, every $\sf DFA$ $(Q, \Sigma, \delta, s, F)$ is equivalent to an $\sf NFA$ $(Q, \Sigma, \Delta, \{s\}, F),$ where $\Delta(p, a) := \{\delta(p,a )\}$. 

**Lemma:** for any $x, y\in\Sigma^*$ and $A\subseteq Q$, $$\hat \Delta(A, xy) = \hat \Delta(\hat\Delta(A, x), y).$$
**Lemma:** The function $\hat\Delta$ commutes with the set union. For any indexed family $\{A_i \mid i \in I\}$ of subsets of $Q$ and $x\in\Sigma^*$, $$\hat\Delta\left(\bigcup_{i \in I} A_i, x\right) = \bigcup_{i\in I} \hat\Delta(A, x).  $$

Let $N = (Q_N, \Sigma, \Delta_N, S_N, F_N)$ be an arbitrary $\sf NFA$. We will produce an equivalent $\sf DFA$. Let $M= (Q_M, \Sigma, \delta_M, s_m, F_M)$ be a $\sf DFA$ where
- $Q_M := \mathcal P(Q_N)$,
- $\delta_M(A, a) :=\hat\delta_N(A, a)$
- $s_M := S_N$
- $F_M := \{A \subseteq Q_N \mid A \cap F_N \neq \varnothing\}$

**Lemma:** For any $A\subseteq Q_n$ and $x\in\Sigma^*$, $$\hat\delta_M(A, x) := \hat\Delta(A, x). $$
**Th:** The automata $M$ and $N$ accept the same language. 

**Prop:** Every $\sf NFA$ can be converted to an equivalent one that has a single accept state.

**Cor:** If $A$ is a regular language, then $\text{rev }A$ is also regular. 

**Def:** An *all-$\sf NFA$* $M$ is a $5$-tuple $(Q, \Sigma, \Delta, S, F)$ that accepts $x\in \Sigma^*$ if *every possible* state $M$ could be in the after reading input $x$ is a state from $F$, meaning that $\hat\Delta(S, x) \subseteq F$. 

**Prop:** All-$\sf NFA$s recognise the class of regular languages. 

# Automata with $\varepsilon$-transitions

there is another extension to finite automata that turns out to be quite useful but really adds no more power.

**Def:** An *$\varepsilon$-transition* is a transition with label $\varepsilon$, a letter that stands for the empty string: $$p \stackrel{\varepsilon}{\longrightarrow} q. $$The automaton can take such a transition anytime without reading an input symbol. 

The main benefit of $\varepsilon$-transitions is convenience. They do not really add any power: a modified construction involving the notion of $\varepsilon$-closure can be used to show that every $\sf NFA$ with $\varepsilon$-transitions can be simulated by a $\sf DFA$ without $\varepsilon$-transitions. 

**Prop:** Let $A$ and $B$ be regular languages, then $AB$ is also a regular language.

**Def:** An $\sf NFA-\varepsilon$ is represented by a $6$-tuple $(Q,\Sigma,\varepsilon, \Delta, s, F)$ consisting of 
- $Q$ is a finite set; elements of $Q$ are called *states*;
- $\Sigma$ is a finite set, the *input alphabet*;
- $\varepsilon$ is a special symbol not in $\Sigma$
- $\Delta: Q\times (\Sigma\cup \{\varepsilon\}) \to \mathcal P(Q)$ is the *transition function*;
- $S \subseteq Q$ is the *set of start state*;
- $F\subseteq Q$; elements of $F$ are called *accept states* or *final states*. 
 and $M_\varepsilon = (Q, \Sigma \cup\{\varepsilon\}, \Delta, S, F)$ is an ordinary $\sf NFA$ over the alphabet $\Sigma\cup\{\varepsilon\}$. We define the accpetance for automata with $\varepsilon$-transitions as follows: for any $x\in \Sigma^*$, $M$ *accepts* $x$ if there exists $y\in (\Sigma\cup\{\varepsilon\})^*$ such that 
 - $M_\varepsilon$ accepts $y$ under the ordinary definition of acceptance for $\sf NFA$s, and
 - $x$ is obtained from $y$ by erasing all occurrences of the symbol $\varepsilon$; that is $x = h(y)$, where $h: (\Sigma\cup\{\varepsilon\})^* \to\Sigma^*$ is the string homomorphism defined by 
	 - $h(a) :=a$, for $a\in \Sigma$,
	 - $h(\varepsilon) := \varepsilon$, where $\varepsilon$ in the input is the special symbol and the one in the output is the empty string.
In other words, $L(M) = h[L(M_\varepsilon)]$. 

**Def:** For a state $q\in Q$, let $E(q)$ denote the set of states that are reachable from $q$ by following $\varepsilon$-transitions in the transition function $\delta$, i.e. $p\in E(q)$ if there is a sequence of states $q_1,\dots, q_k$ such that  
- $q_1 = q$,
- $q_{i+1} \in \delta(q_i,\varepsilon)$ for each $1 \le i < k$, and
- $q_k = p$. 
$E(q)$ is known as the *epsilon closure*, also $\varepsilon$-closure of $q$.

**Th:** Every nondeterministic finite automaton has an equivalent deterministic finite automaton.

**Construction:** Let $N = (Q,\Sigma, \Delta, S, F)$ be the $\sf NFA$ recognising some language $A$. We construct a $\sf DFA$ $M= (Q', \Sigma, \delta, s, F')$ recognising $A$. 
1. $Q' = \mathcal P(Q)$.
2. For $R\in Q'$ and $a\in\Sigma$, let $$\delta'(R,a) := \bigcup_{r\in R} E(\Delta(r, a))  $$
3. $s := S$.
4. $F' = \{ R\in Q' \mid R' \cap F \neq \varnothing\}$. 

# Finite State Transducer

**Def:** A *finite-state transducer* ($\sf FST$) is a structure $M = (Q, \Sigma, \Gamma,\delta s)$, where
- $Q$ is a finite set; elements of $Q$ are called *states*;
- $\Sigma$ is a finite set, the *input alphabet*;
- $\Gamma$ is a finite set, the *output alphabet*;
- $\delta: Q\times \Sigma \to Q\times \Gamma$ is the *transition function*;
- $s\in Q$ is the *start state*;

