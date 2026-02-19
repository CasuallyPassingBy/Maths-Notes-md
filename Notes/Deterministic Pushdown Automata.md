---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Nondeterministic Pushdown Automata]], [[Finite Automaton]], [[Context-Free Grammars]]

**Def:** A *deterministic pushdown automaton*, $\sf DPDA$, is an $8$-tuple $(Q,\Sigma, \Gamma,\delta, \bot, \dashv, s, F)$ where
- $Q$ is the set of states,
- $\Sigma$ is the input alphabet,
- $\Gamma$ is the stack alphabet,
- $\delta:  (Q\times (\Sigma_\varepsilon \cup\{\dashv\})\times \Gamma) \to (Q\times \Gamma^*)$, *deterministic transititon relation*, with the additional restriction that all transition involving $\bot$ must be of the form $((p, a,\bot), (q, \beta\bot))$,
- $s\in Q$ is the start state,
- $\bot\in\Gamma$ the initial stack symbol,
- $\dashv$ is a special symbol not in $\Sigma$, called the *righ endmarker* (similar to what we use for [[Two-Way Finite Automata]]), and 
- $F\subseteq Q$ the set of accept or final states.

The definitions of configurations and acceptance by final state are the same as with $\sf NPDA$s. The start configuration on input $x\in \Sigma^*$ is $(s, x\dashv,\bot)$, and $x$ is accepted iff$$(s, x\dashv,\bot)\xrightarrow[\,M\,]{*} (q, \varepsilon,\beta)  $$for some $q\in F$ and $\beta\in \Gamma^*$. 

**Def:** A language accepted by a $\sf DPDA$ is called a *deterministic context-free language*, $\sf DCFG$. 

Surely every $\sf DCFG$ is a $\sf CFG$, since every $\sf DPDA$ can be simulated in an $\sf NPDA$. But every regular language is also a $\sf DCFG$. Notice that a $\{0^n 1^n\mid n \ge 0\}$ is not a regular language because of the pumping lemma, but it is recognised by a deterministic pushdown automaton. 

We want to show $\sf DCFL$ are closed under complement, but $\sf CFL$s are not closed under complements. Thus we shows that $\sf DCFL$s must be a strict subset of $\sf CFL$s. This means, that unlike $\sf DFA$s, $\sf NPDA$s have strictly more power than $\sf DPDA$s. 

We want to construct for any given $\sf DPDA$ $M$ with input alphabet $\Sigma$, a new $\sf DPDA$ $M'$ such that $L(M') =\Sigma^*\setminus L(M)$. 

### Checking for End of Input

We duplicate the finite control $Q$ to get a new copy $Q' = \{q' 'mid q\in Q\}$ disjoint from $Q$ and add a new transition$$\delta(p', a, A) = (q', B)  $$for each transitions $\delta(p, a, A) = (q, B)$. We remove any transition of the form $\delta(p, \dashv, A) = (q, \beta)$ and replace it with $\delta(p, \dashv, A) = (q', B)$. The primed states thus behave exactly like the unprimed original states, except that we jump from unprimed state to a primed state when we can the endmarker. The start will be $s$, but we will take as $F' := \{q'\mid q\in F\}$. The new machine is deterministic, since there is still exacltly one transition that applies in any configuration. It accepts the same set since $$(s, x\dashv, \bot) \xrightarrow[\, M\,]{*} (q, \varepsilon,\gamma), \qquad q\in F  $$in the old machine there must be some intermediate transition that reads $\dashv$: $$(s, x\dashv, \bot)\xrightarrow[\, M\,]{* }(p, \dashv, A\beta) \xrightarrow[\, M\,]{1} (r, \varepsilon, \alpha\beta)\xrightarrow[\, M\,]{* }(q,\varepsilon, \gamma ).  $$In the new machine it becomes $$(s, x \dashv, \bot) \xrightarrow[\, M'\,]{* } (p, \dashv, A\beta) \xrightarrow[\, M'\,]{1}  (r',\varepsilon, \alpha\beta) \xrightarrow[\, M'\,]{* } (q', \varepsilon, \gamma). $$Conversely, if $(s, x\dashv, \bot) \xrightarrow[\, M'\,]{* }(q', \varepsilon, \gamma)$ for some $q'\in F'$ in the new machine, then we can just remove the primes and get that $$(s, x\dashv, \bot) \xrightarrow[\, M\,]{* } (q, \varepsilon, \gamma), \qquad q\in F$$in the old machine.

### Getting Rid of Spurious Loops

We include two nonaccept states $r$ and $r'$ and transitions $$\begin{align*}
&\delta(r, a, A) = (r, A), \qquad a\in \Sigma, A\in \Gamma, \\
&\delta(r, \dashv, A) = (r', A), \qquad  A\in \Gamma,\\
&\delta(r', \varepsilon, A) = (r', A), \qquad A\in \Gamma.
\end{align*} $$We can think of $r'$ as a reject state. If the machine is in state $r$, it will always scan to the end of the input and enter state $r'$, leaving the stack intact. 

Let $x$ be any input. Because of determinism there is a unique infinite sequence of configurations the machine goes through on input $x$. Let $\gamma_i$ denote the stack contents at time $i\in\Bbb N$. There exists an infinite sequence fo times $i_0 < i_1 <i_2 <\cdots$ such that for all $i_k$, $$|\gamma_{i_k} |\le |\gamma_i|, \quad i \ge i_k.  $$We can take $i_0 = 0$, since $\gamma_0 =\bot$ and $|\gamma_0| = 1$, and the machine never empties its stack. Proceeding inductively, we can take $i_{k+1}$ be the earliest time after $i_k$ such that $|\gamma_{i_{k+1}}|$ is minimum among all $|\gamma_i|$, with $i > i_k$. 

Now we pick an infinite subsequence $j_0 < j_1 <j_2 <\cdots$ of $i_0< i_1<i_2<\cdots$ such that the transition, say $(p,\varepsilon, A) \to (q,\beta)$ is applied at times $j_0, j_1,\dots$. Such a subsequence exists by the pigeonhole principle. The states $p, q$ can be primed or unprimed. The transition must be an $\varepsilon$-transition since it must be applied infinitely many times, and there are only finitely many input symbols to scan.

We know that the machines never sees any stack symbol below the top symbol of $\gamma_{j_k}$ after time $j_k$ and the top symbol is $A$. Thus the only stack symbols it sees after time $j_k$ are those it pushes after time $j_k$. Since the machine is deterministic, once it applies transition $(p,\varepsilon, A) \to (q,\beta)$, it is in a loop and will go through the same periodic sequence of $\varepsilon$-transitions forever, since it sees nothing that can force it to do anything different. Moreover, this behaviour is independent of the input. Thus is $p$ is not an accept state, then the input is not accepted. We might as well remove the transition $(p,\varepsilon, A) \to (q,\beta)$ from $\delta$ and replace it with the transition $(p,\varepsilon, A) \to (r,A)$ if $p$ is an unprimes state or $(p,\varepsilon, A) \to (r', A)$ if $p$ is primed. The language accepted by the automaton is not accepted. 

If this is done for all transitions $(p,\varepsilon, A) \to (q,\beta)$ causing such spurious loops, we obtain a machine equivalent to $M$ that any input scans the entire input string and the endmarker $\dashv$ and enters either an accept state or the state $r'$. To get the machine $M'$ accepting the complement of $L(M)$ make $r'$ the unique accept state of $M'$. 

**Cor:** $\sf DCFL$ are closed under complements. 