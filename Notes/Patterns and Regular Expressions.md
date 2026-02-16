---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Strings and Languages]], [[Kleene Algebras]]

**Def:** Let $\Sigma$ be a finite alphabet. A *patterns* is a string of symbols form representing a language over $\Sigma$. The set of patterns is defined formally by induction. We need to define *atomic patterns*. 

As we define patterns, we will tell which tell strings $x\in \Sigma^*$ *match* them. The set of strings in $\Sigma^*$ matching a given pattern $\alpha$ will be denoted $L(\alpha)$. Thus $$L(\alpha) =\{x\in \Sigma^* \mid x \text{ matches }\alpha\}.$$
The *atomic patterns* are
- $a$, for each $a\in \Sigma$, matched by the symbol $a$ only; in symbols, $L(a) := \{a\}$.
- $\varepsilon$, matched only by $\varepsilon$, the null string; in symbols $L(\varepsilon) = \{\varepsilon\}$.
- $\varnothing$, matched by nothing; in symbols $L(\varnothing) = \varnothing$.
- $\#$, matched by any symbol in $\Sigma$; in symbols, $L(\#) = \Sigma$.
- $@$, matched by any string in $\Sigma^*$; in symbols, $L(@) = \Sigma^*$. 

*Compound patterns* are formed inductively using binary operations $+, \cap$, and $\cdot$ and unary operators $\;^+$, $\;^*$ and complementation. If $\alpha$ and $\beta$ are patterns, then so are $\alpha+\beta$, $\alpha \cap \beta$, $\alpha^*$, $\alpha^+$, $\lnot\alpha$, and $\alpha\beta$. 

Suppose we have already defined the sets of strings $L(\alpha)$ and $L(\beta)$ matching $\alpha$ and $\beta$, respectively. Then we'll say that 
- $x$ matches $\alpha+\beta$ matches either $\alpha$ or $\beta$: $$L(\alpha + \beta ) := L(\alpha)\cup L(\beta);  $$
- $x$ matches $\alpha\cap \beta$ matches both $\alpha$ and $\beta$: $$L(\alpha \cap \beta) := L(\alpha) \cap L(\beta);  $$
- $x$ matches $\alpha\beta$ if $x$ can be broken down as $x = yz$ such that $y$ matches $\alpha$ and $z$ matches $\beta$: $$L(\alpha)L(\beta) := L(\alpha)L(\beta); $$
- $x$ matches $¬\alpha$ if $x$ does not match $\alpha$: $$L(¬\alpha) := \Sigma^*\setminus L(\alpha).;$$
- $x$ matches $\alpha^*$ if $x$ cab be expressed as a concatenation of zero or more strings, all of which match $\alpha$:$$L(\alpha^*) := L(\alpha)^*   $$The empty string $\varepsilon$ always matches $\alpha^*$, since $\varepsilon$ is a concatenation of zero strings, all of which match $\alpha^*$. 
- $x$ matches $\alpha^+$ if $x$ can be expressed as concatenation of one or more strings, all of which match $\alpha$:  $$L(\alpha^+) := L(\alpha)^+.  $$

**Def:** patterns $\alpha$ and $\beta$ are *equivalent* if $L(\alpha) = L(\beta)$. 

**Obs:** Let see which operators are redundant. We can get rid of $\varepsilon$ since it is equivalent to $¬(\#@)$ and also to $\varnothing^*$. We can get rid of $@$ since it is equivalent to $\#^*$. We can get rid of $\; ^+$ since $\alpha^+$ is equivalent to $\alpha\alpha^*$. We can get rid of $\#$, since if $\Sigma = \{a_1,\dots, a_n\}$, then $\#$ is equivalent to the pattern $\alpha_1+\cdots+a_n$. The operator $\cap$ is also redundant $\alpha\cap \beta$ is equivalent to $¬(¬\alpha+¬\beta)$. 

**Def:** Every pattern is equivalent to one using only using atomic patterns $\alpha\in \Sigma$, $\varepsilon, \varnothing$ and operators $+, \cdot$, and $\;^*$. Patterns using only these are called *regular expressions*. 

Since the binary operators $+$ and $\cdot$ are associative, then we see that can write $\alpha+\beta+\gamma$ and $\alpha\beta\gamma$ without ambiguity. We adopt the convention that the concatenation operator $\cdot$ has higher precedence than $+$, so $\alpha+\beta \gamma$ is equivalent to $\alpha+(\beta\gamma)$. Similarly, we assign $^*$ higher precedence than $+$ or $\cdot$, so that $\alpha +\beta^*$ is equivalen to $\alpha + (\beta)^*$. 

**Th:** Let $A\subseteq \Sigma^*$. The following three statements are equivalent:
- $A$ is regular, that is, $A = L(M)$ for some finite automaton $M$;
- $A = L(\alpha)$ for some pattern $\alpha$;
- $A = L(\alpha)$ for some regular expression $\alpha$. 

**Def:** For regular expressions, $\alpha$, $\beta$ if $L(\alpha) = L(\beta)$, we write $\alpha \equiv \beta$ and say that $\alpha$ and $\beta$ are *equivalent*. The relation $\equiv$ on regular expressions is an equivalence relation; that is, it is
- Reflexive: $\alpha \equiv \alpha$ for all $\alpha$;
- Symmetric: if $\alpha \equiv \beta$, then $\beta\equiv\alpha$; and
- Transitive: if $\alpha\equiv \beta$ and $\beta\equiv \gamma$, then $\alpha \equiv \gamma$.
Similarly, if $\alpha$ and $\beta$, then $\alpha \le \beta$ iff $L(\alpha)\subseteq L(\beta)$. 

Here are a few laws that can be used to simplify expressions.
1. $\alpha + (\beta+\gamma) \equiv (\alpha+\beta) + \gamma$.
2. $\alpha +\beta \equiv \beta+\alpha$.
3. $\alpha + \varnothing \equiv \alpha$.
4. $\alpha +\alpha \equiv \alpha$. 
5. $\alpha(\beta\gamma) \equiv (\alpha\beta)\gamma$.
6. $\varepsilon \alpha \equiv \alpha\varepsilon \equiv \alpha$.
7. $\alpha(\beta+\gamma) \equiv \alpha\beta + \alpha\gamma$.
8. $(\alpha+\beta)\gamma \equiv \alpha\gamma+\beta\gamma$.
9. $\varnothing \alpha \equiv \alpha\varnothing \equiv \varnothing$.
10. $\varepsilon + \alpha\alpha^* \equiv \alpha^*$. 
11. $\varepsilon + \alpha^* \alpha \equiv \alpha^*$. 
12. $\beta + \alpha\gamma \le \alpha \implies \alpha^*\beta \le \gamma$.
13. $\beta +\gamma\alpha \le \gamma\implies \beta\alpha^*\le \gamma$. 
14. $\alpha \le \beta\iff  \alpha +\beta \equiv \beta$. 
15. $(\alpha\beta)^*\alpha \equiv \alpha(\beta\alpha)^*$.
16. $(\alpha^*\beta)^*\alpha^* \equiv (\alpha+\beta)^*$.
17. $\alpha^*(\beta\alpha^*)^* \equiv (\alpha+\beta)^*$.
18. $(\varepsilon + \alpha)^* \equiv \alpha^*$.
19.  $\alpha\alpha^* \equiv \alpha^*\alpha$.

### Converting Automata to Regular Expressions

Given an $\sf NFA$ $M = (Q, \Sigma, \Delta, S, F)$ a subsets $X\subseteq Q$, and states $u, v\in Q$, we show how to construct a regular expression $\alpha_{uv}^X$ representing the set of all strings $x$ such that there is a path from $u$ to $v$ in $M$ labelled $x$ and all the states along the path with the possible exception of $u$ and $v$, lie in $X$.

The expressions are constructed inductively in the size of $X$. For the basis $X = \varnothing$, let $a_1,\dots, a_k$ be all the symbols in $\Sigma$ such that $v\in \Delta(u, a_i)$. For $u\neq v$, take $$\alpha_{uv}^\varnothing  := \begin{cases}
a_1+ \cdots + a_k & \text{if }k \ge 1,\\
\varnothing & \text{if } k = 0;
\end{cases}  $$
and for $u = v$, take $$\alpha_{uv}^\varnothing  := \begin{cases}
a_1+ \cdots + a_k+ \varepsilon & \text{if }k \ge 1,\\
\varepsilon & \text{if } k = 0.
\end{cases}  $$
For nonempty $X$, we can choose any element $q\in X$ and take $$\alpha_{uv}^X := \alpha_{uv}^{X\setminus\{q\}}+\alpha_{uq}^{X\setminus\{q\}}\left(\alpha_{qq}^{X\setminus\{q\}}\right)^*\alpha_{qv}^{X\setminus\{q\}}  $$

Now we use this to give a regular expression to an arbitrarily given deterministic finite automaton $M = (Q, \Sigma, \delta, s, F)$. Assume without loss of generality that $Q = \{1,\dots, n\}$. For each $q\in Q$, let $X_q$ denote the set of strings in $\Sigma^*$ that would be accepted by $M$ is $q$ where the start states; that is, $$X_q:= \{x \in \Sigma^* \mid \delta(q, x)\in F\}. $$The $X_q$ satisfy the following system of equations:$$X_q = \begin{dcases}
\sum_{a\in \Sigma} a X_{\delta(q, a)} & \text{if }q\notin F, \\ \\
\sum_{a\in \Sigma} a X_{\delta(q, a)} +1 & \text{if }q\in F.
\end{dcases}   $$
Moreover, the $X_q$ give the least solution with respect to $\subseteq$. As above, these equations can be arranged in a single matrix-vector equation of the form $$X = AX + b,  $$where $A$ is an $n \times n$ matrix containing sums of elements of $\Sigma$, $b$ is a $0,1$ vector length $n$, and $X$ is a vector consisting of $X_1,\dots, X_n$. The vector $X$ is the least solution of $X = AX+b$. By a theorem of [[Kleene Algebras]]$$X = A^* b.$$
A regular expression for $L(M)$ can be read off from the $s$th entry of $A^*b$, where $s$ is the start state of $M$. 

# Generalised Nondeterministic Finite Automaton

**Def:** A *generalised nondeterministic finite automaton* is $5$-tuple $(Q,\Sigma, \delta, q_\text{start}, q_\text{accept})$, where
1. $Q$ is the finite state of states,
2. $\Sigma$ is the input alphabet, 
3. $\delta: (Q\setminus\{q_\text{accept}\}) \times (Q \setminus\{q_\text{start}\})\to \mathcal R$ is the transition function, where $\cal R$ is the collection of all regular expressions over the alphabet $\Sigma$.
4. $q_\text{start}$ is the start state, and
5. $q_\text{accept}$ is the accept state.

A $\sf GNFA$ accepts a string $w$ in $\Sigma^*$ if $w = w_1\cdots w_k$, where each $w_i$ is in $\Sigma^*$ and a sequence of states $q_0,\dots, q_k$ exists such that
1. $q_0 = q_\text{start}$ is the start state
2. $q_k = q_\text{accept}$, is the accept state, and
3. for each $i$, we have $w_i \in L(\alpha_i)$, where $\alpha_i= \delta(q_{i-1}, q_i)$; in other words, $R_i$ is the expression on the arrow from $q_{i-1}$ to $q_i$.

We can convert a $\sf GNFA$ with $k$ states, with $k >2$, to a another one with $k-1$ states.

**Convert:** Let $G  = (Q,\Sigma, \delta, q_\text{start}, q_\text{accept})$.
1. let $k$ be the number of states of $G$.
2. If $k = 2$, the $G$ must consists of a start state, and an accept state, and a single arrow connecting them and labelled with a regular expression $\alpha$. 
3. If $k>2$, we select a state $q_\text{rip}\in Q\setminus \{q_\text{start}, q_\text{accept}\}$ and let $G'$ be the $\sf GNFA$ $(Q',\Sigma, \delta', q_\text{start}, q_\text{accept})$, where $Q' := Q \setminus \{q_\text{rip}\}$ and for $q_i \in Q'\setminus \{q_\text{accept}\}$ and $q_j \in Q\setminus \{q_\text{start}\}$ let $$\delta'(q_i, q_j) := \alpha_1 (\alpha_2)^* \alpha_3 + \alpha_4,$$for $\alpha_1 := \delta(q_i, q_\text{rip})$, $\alpha_2 := \delta(q_\text{rip}, q_\text{rip})$, $\alpha_3 := \delta(q_\text{rip}, q_j)$, and $\alpha_4 := \delta(q_i, q_j)$. 

**Lemma:** For any $\sf GNFA$ $G$, then $G'$ defined above is equivalent to $G$.

