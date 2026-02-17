---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Strings and Languages]], [[Myhill-Nerode Theorem]]

Two-way finite automata are similar to the machines we have been studying, except that they can read the input string in either direction. We think of them as having a *read head*, which can move left or right over the input string. Like ordinary finite automata, they have a finite set $Q$ of *states* and can either be deterministic, $\sf 2DFA$, or nondeterministic, $\sf 2NFA$. 

**Def:** Formally a $\sf 2DFA$ is an $8$-tuple $M= (Q,\Sigma,\vdash,\dashv, \delta, s, t, r)$ where
- $Q$ is a finite set (the *states*),
- $\Sigma$ is a finite set (the *input alphabet*),
- $\vdash$ is the *left endmarker*, $\vdash \notin \Sigma$,
- $\dashv$ is the *right endmarker*, $\dashv\notin \Sigma$,
- $\delta: Q \times (\Sigma\cup\{\vdash, \dashv\}) \to (Q \times \{L, R\})$ is the *transitiojnn function* ($L, R$ stand for left and right, respectively),
- $s\in Q$ is the *start state*,
- $t\in Q$ is the *accept state*, and
- $r\in Q$ is the *reject state*, $r \neq t$. 
such that for all states $q$, $$\begin{align*} \delta(q, \vdash) &= (u, R) \quad \text{for some }u \in Q, \\
\delta(q, \dashv) &= (v, L) \quad \text{for some }v\in Q, \end{align*}$$and for all symbols $b\in \Sigma \cup\{\vdash\}$, $$\begin{align*}\delta(t, b) = (t, R),& \qquad \delta(r, b) = (r, B), \\ \delta(t, \dashv) = (t, L), &\qquad \delta(r, \dashv) = (r, L).\end{align*}$$
## Configurations and Acceptance

Fix an input $x\in \Sigma^*$, say $x = a_1\cdots a_n$. Let $a_0 = \;\vdash$ and $a_{n+1} = \;\dashv$. Then $$a_0\cdots a_{n+1} =\; \vdash x \dashv.$$
A *configuration* of the machine on input $x$ is a pair $(q, i)$ such that $q\in Q$ and $0\le i \le n+1$. Informally, the pair $(q, i)$ gives the current state and current position of the read head. The *start configuration* is $(s, 0)$, meaning that the machine is in its start $s$ scanning the left endmarker. 

A binary relation $\xrightarrow[\;x\;]{\;1\;}$ describes one step of the machine on input $x$. We define the relation $\xrightarrow[\;x\;]{\;n\;}$ inductively, $n \ge 0$:
- $(p, i) \xrightarrow[\;x\;]{\;0\;} (p, i)$; and
- if $(p,i) \xrightarrow[\;x\;]{\;n\;} (q, j)$ and $(q, j) \xrightarrow[\;1\;]{\;n\;} (u, k)$, then $\xrightarrow[\;x\;]{\;n+1\;} (u, k)$.

The relation $\xrightarrow[\;x\;]{\;n\;}$ is just the $n$-fold composition of $\xrightarrow[\;x\;]{\;1\;}$. The relations $\xrightarrow[\;x\;]{\;n\;}$ are functions, that is, for any configuration, there is exactly one configuration $(q, j)$ such that $(p, i) \xrightarrow[\;x\;]{\;n\;} (q, j)$. Now define $$(p, i)\xrightarrow[\;x\;]{\;*\;} (q, j) \stackrel{\text{def}}{\iff} \exists n \ge 0 (p, i) \xrightarrow[\;x\;]{\;n\;} (q, j). $$Note that the definitions of these relations depend on the input $x$, The machiine is said to *accept* the input $x$ if $$(s, 0) \xrightarrow[\;x\;]{\;*\;}  (t, i) \qquad \text{for some } i.$$In other words, the machine enters its accepts state at some point. The machine is said to *reject* the input $x$ if $$(s, 0) \xrightarrow[\;x\;]{\;*\;} (r, i) \qquad \text{for some }i. $$The machine is said to *halt* on input $x$ if it either accepts $x$ or rejects $x$. It is possible that the machine neither accepts not rejects $x$, in which case it is said to *loop* on $x$. The set $L(M)$ is defined to be the set of strings accepted by $M$. 

**Th:** If $A\subseteq \Sigma^*$ is recognised by the $\sf 2DFA$, then there exists a $\sf DFA$ such that it also recognises $A$.
