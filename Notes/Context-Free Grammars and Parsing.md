---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Strings and Languages]]

**Def:** A *context-free grammar* ($\sf CFG$) is $4$-tuple $(V, \Sigma, R, S)$ where
- $V$ is a finite set called the *variables*,
- $\Sigma$ is a finite set, disjoint from $V$, called the *terminals*,
- $R\subseteq N \times (N \times \Sigma)^*$ is a finite set of *rules*, with each rule being a variable and a string of variables and terminals, and
- $S\in V$ is the start variable. 

If $u$, $v$ and $w$ are strings of variables and terminals, and $A\to w$ is a rule of the grammar, we say that $aAv$ *yields* $uwv$, written $uAv \Rightarrow uwv$. Say that *derives* $v$, written $u \stackrel{*}{\Rightarrow} v$, if $u = v$ or if a sequence $u_1,\dots, u_k$ exists for $k\ge 0$ and $$u \Rightarrow u_1\Rightarrow\cdots \Rightarrow u_k \Rightarrow v,  $$The *language of the grammar* is $\{w\in \Sigma \mid S \stackrel{*}{\Rightarrow} w\}$. 

**Def:** A subset $B\subseteq \Sigma^*$ is a *context-free language*, $\sf CFL$, if $B = L(G)$ for some context-free grammar $G$.

A derivation of a string $w$ in a grammar $G$ is a *leftmost derivation* if at every step the leftmost remaining variable is the one replaced. 

**Def:** A string $w$ is derived *ambiguously* in context-free grammar $G$ if it has two or more different leftmost derivations. Grammar is *ambiguous* if it generates some string ambiguously. 

Sometimes when we have ambiguous grammar we can find an unambiguous grammar that generates the same language. Some context-free languages, however, can be generated only by ambiguous grammars. Such languages are called *inherently ambiguous*. 

# Normal Forms

**Def:** A context-free grammar is in *Chomsky normal form*, $\sf CNF$, if every rule is of the form $$\begin{align*} A &\to BC \\ A &\to a\end{align*}    $$where $a$ is any terminal and $A, B$ and $C$ are any variables, except that $B$ and $C$ may not be the start variable. A *Greiback normal form*, $\sf GNF$, if all productions are of the form $$A \to aB_1B_2\cdots B_k  $$for some $k \ge 0$, where $A, B_1,\dots, B_k\in N$ and $a\in\Sigma$. 

**Def:** We call an $\varepsilon$-production to be of the form $A \to \varepsilon$, and a *unit production* if $A\to B$. 

**Lemma:** For any $\sf CFG$ $G = (V, \Sigma, R, S)$, there is a $\sf CFG$ $G'$ with no $\varepsilon$- or unit productions such that $L(G') = L(G)\setminus\{\varepsilon\}$.

**Th:** For any $\sf CFG$ $G$, there is a $\sf CFG$ G'$ in Chomsku normal form and a $\sf CFG$ $G''$ in Greibach normal form such that$$L(G'') =L(G') = L(G)\setminus\{\varepsilon\}. $$
Just as is the case in many proofs in theoretical computer science, the proof gives us an algorithm.

**Algorithm:** 
- First, we add a new variable $S_0$ and the rule $S_0 \to S$, where $S$ was the original start variable. 
- Second, we take care of all $\varepsilon$ rules. We remove an $\varepsilon$-rule $A \to \varepsilon$, where $A$ is not the start variable. 
- Then for each occurrence of an $A$ on the right-hand side of a rule, we add a new rule with the occurrence deleted. 
	- In other words, if $R \to uAv$ is a rule in which $u$ and $v$ are strings of variables and terminals, we add rule $R\to uv$. We do so each *occurance* of an $A$, so the rule $R \to uAvAw$ causes us to add $R\to uv Aw$, $Ru\to uAvw$, and $R\to uvw.$ 
	- If we have the rule $R\to A$, we add $R\to \varepsilon$ unless we had previously removed the rule $R\to \varepsilon$. 
- Third, we handle the unit rules. We remove the unit rule $A \to B$. Then, whenever $B \to u$ appears, we add the rule $A \to u$ unless this was a unit rule previously removed. As before, $u$ is a string of variables and terminals. We repeat this steps until we eliminate all unit rules. 
- Finally, we convert all remaining rules into the proper form. We replace each rule $A \to u_1u_2\cdots u_k$, where $k \ge 3$ and each $u_i$ is a variable or terminal symbol with rules $A \to u_1 A_1$, $A_1\to u_2A_2$, $A_2 \to u_3A_3,\dots,$ and $A_{k-2} \to u_{k-1}u_k$. The $A_i$'s are new variables. If $k = 2$, we replace any terminal $u_i$ in the preceding rules with the new variable $U_i$ and add the rule $U_i\to u_i$. 

**Pumping Lemma for $\sf CFL$s:** If $A$ is a context-free language, then there is a number $p$, then pumping length, where, if $s$ is any string in $A$ of length at least $p$, then $s$ may be divided into five pieces $s = uvxyz$ satisfying the conditions
- for each $i \ge 0$, $uv^ixy^iz\in A$,
- $|vy| > 0$, and
- $|vxy| \le p$. 