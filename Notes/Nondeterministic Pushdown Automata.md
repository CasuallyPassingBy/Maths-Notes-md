---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Context-Free Grammars]], [[Finite Automaton]]

### Sipser's Definition

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

### Kozen's Definition

**Def:** A *nondeterministic pushdown automaton*, $\sf NPDA$, is a $7$-tuple $(Q, \Sigma, \Gamma,\delta, s,\bot , F)$ where
- $Q$ is the set of states,
- $\Sigma$ is the input alphabet,
- $\Gamma$ is the stack alphabet,
- $\delta \subseteq (Q\times \Sigma_\varepsilon\times \Gamma) \times (Q\times \Gamma^*)$, $\delta$ is finite and is the *transititon relation*
- $s\in Q$ is the start state,
- $\bot\in\Gamma$ the initial stack symbol,
- $F\subseteq Q$ the set of accept or final states.
If $$((p, a, A), (q, B_1B_2\cdots B_k)) \in \delta  $$this means intuitively that whenever the machine is in the state $p$ reading input symbol $a$ on the input tape and $A$ on the top of the stack, it can pop $A$ off the stack, push $B_1\cdots B_k$ onto de stack ($B_k$ first and $B_1$ last), move its head right one cell past $a$, and enter state $q$. If $$ ((p, \varepsilon, A), (q, B_1B_2\cdots B_k)) \in \delta $$this means intuitively the machine in in the state $p$ with $A$ on the top of the stack, it can pop off $A$ the stack and push $B_1\cdots B_k$ onto the stack, leave the read head where it is, and enter the state $q$.

**Def:** A *configuration* of the machine $M$ is an element $Q\times \Sigma^*\times \Gamma^*$ describing the current state, the portion of the input yet unread, and the current stack contents. A configuration gives complete information about the global state of $M$ at some point during a computation.

The *start configuration* on input $x$ is $(s, x,\bot)$. The *next configuration relation* $\xrightarrow[\, M\,]{\,1\,}$ describes how the machine can move from one configuration to another in one step. It is defined as follows: if $((p, a, A), (q, \gamma))\in\delta$, then for any $y\in \Sigma^*$ and $\beta\in \Gamma^*$  $$(p, ay, A\beta)\xrightarrow[\, M\,]{\, 1\,} (q, y, \gamma \beta),  $$and if  $((p, \varepsilon, A), (q, \gamma)) \in \delta$, then for any $y\in \Sigma^*$ and $\beta\in \Gamma^*$,$$(p, y, A\beta)\xrightarrow[\, M\,]{\, 1\,} (q, y, \gamma \beta). $$
We define the relations $\xrightarrow[\, M\,]{\, n\,}$ and $\xrightarrow[\, M\,]{\, *\,}$ as follows:
- $C \xrightarrow[\, M\,]{\, 0\,} D$ iff $C = D$.
- $C \xrightarrow[\, M\,]{\, n+1\,} D$ iff there's a configuration $E$ such that $C \xrightarrow[\, M\,]{\, n\,} E$ and $E \xrightarrow[\, M\,]{\, 1\,} D$. 
- $C \xrightarrow[\, M\,]{\, *\,} D$ iff there's an $n\ge 0$ such that $C \xrightarrow[\, M\,]{\, n\,} D$. 
We see that $\xrightarrow[\, M\,]{\, *\,}$ is the transitive closure if $\xrightarrow[\, M\,]{\, 1\,}$. We see that $C \xrightarrow[\, M\,]{\, *\,} D$ if the configuration $D$ follows from the configuration $C$ in zero or more steps of the next configuration relation $\xrightarrow[\, M\,]{\, 1\,}$. 

There are two variations on the acceptance in common use: by *empty stack* or by *final state*.
- **Final State.** $M$ *accepts $x$ by final state* if $$(s, x, \bot) \xrightarrow[\, M\,]{\, *\,} (q, \varepsilon, \gamma) $$for some $q\in F$ and $\gamma\in \Gamma^*$. In the right-hand configuration, $\varepsilon$ is the empty string, signifying that the entire input has been read, and $\gamma$ is junk left on the stack.
- **Empty Stack.** *$M$ accepts $x$ by empty stack* if $$(s, x,\bot) \xrightarrow[\, M\,]{\, *\,} (q, \varepsilon, \varepsilon)  $$for some $q\in Q$. In this definition, the $q$ in the right-hand configuration can be any state whatsoever, and the $\varepsilon$ in the second and third positions indicate that the entire input has been read and the stack empty, respectively. 

Let $M = (Q, \Sigma, \Gamma,\delta, s,\bot , F)$ be an $\sf NPDA$ that accepts by empty stack or by final state. Let $u, t$ be two new states not in $Q$, and let $\top$ be a new stack symbol not in $\Gamma$. Define$$
\begin{align*}
G & := \begin{cases}
Q & \text{if $M$ accepts by empty stack,} \\
G & \text{if $M$ acccepts by final state;}
\end{cases}  \\ \\
\Delta & := \begin{cases}
\{\top\} & \text{if $M$ accepts by empty stack,} \\
\Gamma\cup\{\top\} & \text{if $M$ acccepts by final state.}
\end{cases} 
\end{align*}$$
Consider the $\sf NPDA$ $$M' :=(Q\cup\{u, t\}, \Sigma, \Gamma\cup\{\top\}, \delta', u,\top, \{t\})$$were $\delta'$ contains all the transitions of $\delta$, as well as the transitions$$\begin{align*}
&((u,\varepsilon, \top), (s,\bot,\top)), \\
&((q, \varepsilon, A), (t, A)), \qquad q\in G, \quad A\in \Delta, \\
&((t, \varepsilon, A), (t,\varepsilon)), \qquad A\in \Gamma\cup \{\top\}.
\end{align*}  $$Thus the new automaton $M'$ has a new start $u$, a new initial stack symbol $\top$, and a new single final state $t$. In the first step, it pushes the old initial stack symbol $\bot$ on top of $\top$, then entres the old start state $s$. It can then run as $M$ would . At some point it might enter the state $r$ according the second row of new transitions, Moreover, this is the *only* way it can empty the its stack, since it cannot pop $\top$ except in the state $t$. Thus acceptance by empty stack and by final state coincide for $M'$. 

We see that $L(M') = L(M)$ 


# $\sf PDA$s and $\sf CFG$s

**Th:** Every $\sf NPDA$ with one state has an equivalent $\sf CFG$. 

Suppose we are given a $\sf CFG$ $G= (N,\Sigma, R, S)$. We can assume without loss of generality that all productions of $G$ are of the form $$A→cB_1 B_2\cdots B_k,  $$where $c\in \Sigma_\varepsilon$ and $k\ge0$. We construct from $G$ an equivalent $\sf NPDA$ $M$ with only one state that accept by empty stack. Let  $$M := (\{q\},\Sigma, N,\delta, q, S, \varnothing) $$where
- $q$ is the only state,
- $\Sigma$, is the set of terminals of $G$, is the input alphabet of $M$,
- $N$, is the set of nonterminals of $G$, is the stack alphabet of $M$,
- $\delta$ is the transition relation defined below,
- $q$ is the start state,
- $S$, is the start symbol of $G$, is the initial stack symbol of $M$,
- $\varnothing$, is the set of final states. 
The transition relation $\delta$ is defined as follows. If production $$A→cB_1\cdots B_k  $$is in $R$, then $$((q, c, A), (q, B_1\cdots B_k))\in \delta.  $$
**Claim:** For any $x, y\in \Sigma^*$, $\gamma\in N^*$, and $A\in N$, $A \xrightarrow[\, G\,]{\,n\,}z\gamma$ via leftmost derivation iff $(q, zy, A) \xrightarrow[\,M\,]{\,n\,} (q, y,\gamma)$. 

Thus $L(M) = L(G)$. The great part of this construction is that it is reversible, and if we have a $\sf NPDA$ with a single state we can get an $\sf CFG$ that is equivalent to it.

**Th:** Every $\sf NPDA$ can be simulated by a $\sf NPDA$ with one state. 

We can assume without loss of generality that $M := (Q,\Sigma, \Gamma, \delta, s,\bot, \{t\})$; that is, $M$ has a single final state $t$, and $M$ can empty its stack after it entres state $t$.  Let $\Gamma' := Q \times \Gamma \times Q$. Elements of $\Gamma'$ are written $\langle p\; A\; q\rangle$, where $p, q\in Q$ and $A\in \Gamma$. We will construct a new $\sf NPDA$ $$M' :=(\{*\}, \Sigma.\Gamma',\delta', *, \langle s\; \bot\; t\rangle, \varnothing)  $$with one state $*$ that accepts by the empty stack. The new machine $M'$ will be able to scan a string $x$ starting with only $\langle p\; A\; q\rangle$ on its stack and en up with en empty stack iff $M$ can scan $x$ starting in state $p$ with only $A$ on its stack and end up in state $q$ with an empty stack. The transition relation $\delta'$ of $M'$ is defined as follows for each transition$$((p, c, A), (q_0, B_1\cdots B_k))\in \delta,$$where $c\in \Sigma_\varepsilon$, include in $\delta'$ the transition $$((*\; c,\langle p\; A\; q_k\rangle), (*, \langle q_0 \; B_1\; q_1\rangle\langle q_1 \; B_2\; q_2\rangle\cdots \langle q_{k-1} \; B_k\; q_k\rangle))  $$for all possible choices of $q_1,\dots, q_k$. For $k = 0$, this reduces to $$((p, c, A), (q_0,\varepsilon))\in \delta  $$include in $\delta'$ the transition$$((*, c \langle p\; A\; q\rangle), (*, \varepsilon)) $$
**Claim:** Then $$(p, x, B_1 B_2\cdots B_k) \xrightarrow[\, M\,]{\, n\,} (q, \varepsilon, \varepsilon)  $$iff there exists $q_0, q_1,\dots, q_k$ such that $p = q_0$, $q = q_k$, and$$(*, \langle q_0 \; B_1\; q_1\rangle\langle q_1 \; B_2\; q_2\rangle\cdots \langle q_{k-1} \; B_k\; q_k\rangle) \xrightarrow[\, M'\,]{n} (*,\varepsilon, \varepsilon). $$In particular, $$(p, x, B)\xrightarrow[\, M\,]{n} (q, \varepsilon, \varepsilon) \iff (*, x \langle p\; B\; q\rangle) \xrightarrow[\, M'\,]{n} (*, \varepsilon, \varepsilon). $$
Thus $L(M') = L(M)$. 

**Th:** A language is context-free iff some pushdown automaton recognises it.

**Cor:** Every regular language is context-free. 

