---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Equivalence Relations and Partitions]]

# Deterministic Finite Automata

Let $M = (Q, \Sigma,\delta, s, F)$ be a deterministic finite automaton. We can define an equivalence relation on $Q$, to minimise the number of states necessary for $L(M)$.

**Def:** We first define an equivalence relation $\approx$ on $Q$ by $$p \approx q \stackrel{\text{def}}{\iff} \forall x\in \Sigma^* (\hat\delta(p, x)\in F \iff \hat \delta(q, x)\in F).$$
We see that $\approx$ is reflexive, symmetric and transitive. 

Now we define a $\sf DFA$ $M/\approx$ called the *quotient automaton*, whose states correspond to $Q/\approx$. 

We define $M /\approx := (Q', \Sigma, \delta', s', F')$ where
- $Q' := Q/\approx$
- $\delta'([p], a) = [\delta(p,a)]$.
- $s' = [s]$.
- $F' := \{[p] \mid p\in F\}$. 

**Lemma:** If $p \approx q$, then $\delta(p,a) \approx \delta(q, a)$. Equivalently, if $[p] = [q]$, then $[\delta(p,a)] = [\delta(q, a)]$. 

**Lemma:** Let $p\in Q$. Then $p\in F$ iff $[p] \in F'$. 

**Lemma:** For all $x\in \Sigma^*$, $\hat\delta'([p],x]) = [\hat \delta(p, x)]$. 

**Th:** $L(M/\approx) = L(M)$.

It is conceivable that after doing the quotient construction once, we might be able to collapse even further by doing it again. It turns out that once is enough. 

Define $[p] \sim [q]$ iff for all $x\in \Sigma^*$, $\hat \delta'([p], x)\in F \iff \hat\delta'([q], x)\in F$. This is exactly the same definition to $\approx$, only applied to $M/\approx$. 
$$\begin{align*}
&[p] \sim [q] \\
&\implies \forall x\in \Sigma^*(\hat \delta'([p], x)\in F \iff \hat\delta'([q], x)\in F) \\
&\implies \forall x\in \Sigma^* ([\hat \delta(p, x)]\in F\iff [\hat\delta(q, x)]\in F) \\
&\implies \forall x\in \Sigma^* (\hat \delta(p, x)\in F \iff \hat\delta(q, x)\in F) \\
&\implies p \approx q \implies [p] = [q]\end{align*}$$
Thus any two states equivalent of $M/\approx$ are in fact equal, and the collapsing relation $\sim$ on $Q/\approx$ is just the identity relation. 

Here is an algorithm for computing the collapsing relation $\approx$ for a given $\sf DFA$ $M$ with no inaccesible states. 
1. Write down a table of all pairs $\{p,q\}$, initially unmarked.
2. Mark $\{p, q\}$ if $p\in F$ and $q\notin F$.
3. Repeat the followign until no more changes occur: if there exists unmarked pair $\{p, q\}$ such that $\{\delta(p, q), \delta(q, a)\}$ is marked for some $a\in \Sigma$, then mark $\{p,q\}$.
4. When done $p\approx q$ iff $\{p, q\}$ is not marked.

**Th:** The pair $\{p,q\}$ is marked by the above algorithm iff there exists $x\in \Sigma^*$ such that $\hat\delta(p, x)\in F$ and $\hat\delta(q, x)\notin F$, or viceversa; i.e., iff $p\not\approx q$. 

# Nondeterministic Finite Automata

**Def:** Let $M := (Q_M , \Sigma, \Delta_M, S_M, F_M)$ and $N:= (Q_N, \Sigma, \Delta_N, S_N, F_N)$ be two $\sf NFA$s. Let $\approx$ be a the binary relation relating states of $M$ with states of $N$. For $B\subseteq Q_N$, define $$C_\approx(B) := \{q\in Q_N \mid \exists q\in B(p \approx q)\}, $$the set of all states that are related via $\approx$ the some state in $B$. Similarly, for $A\subseteq Q_M$, define $$C_\approx (A) := \{q\in Q_N \mid \exists p\in A(p \approx q)\}.$$The relation $\approx$ can be extended in a natural way to *subsets* of $Q_M$ and $Q_N$: for $A\subseteq Q_M$ and $B\subseteq Q_N$, $$
\begin{align*}
A\approx B &\stackrel{\text{def}}{\iff} A \subseteq C_\approx (B) \text{ and }  B \subseteq C_\approx (A) \\
&\iff \forall  p\in A \exists q\in B\; p\approx \text{ and } \forall  q\in B \exists p\in A \;p\approx q.
\end{align*}
$$

**Def:** The relation $\approx$ is called a *strong bisimulation* if the following conditions are met:
- $S_M \approx S_N$,
- if $p \approx q$, then for all $a\in \Sigma$, $\Delta_M (p, a) \approx \Delta_N(q, a)$; and
- if $p\approx q$, then $p\in F_M$ iff $q\in F_N$. 

We say that $M$ and $N$ are *strongly bisimilar* if there exists a bisimulation between them. The *strong bismiliraty class* of $M$ is the family of $\sf NFA$s that are strongly bisimilar to $M$. 

**Lemma:**
- Strong bisimulation is symmetric: if $\approx$ is a strong bisimulation between $M$ and $N$ then its reverse is a strong bisimulation between $N$ and $M$.
- Strong bisimulation is transitive: if $\approx_1$ is a strong bisimulation between $M$ and $N$ and $\approx_2$ is a bisimulation between $N$ and $P$, then their composition $\approx_1\circ\approx_2$ is a strong bisimulation between $M$ and $P$.
- The union of an nonempty family of strong bisimulations between $M$ and $N$ is a bisimulation between $M$ and $N$. 

**Lemma:** Let $\approx$ be a strong bisimulation between $M$ and $N$. If $A\approx N$, then for all $x\in\Sigma^*$, $\hat\Delta_M(A, x) \approx \hat\Delta_N(B, x)$. 

**Th:** Strongly bisimilar automata accept the same set. 

**Def:** Let $\approx$ be a strong bisimulation between $M$ and $N$. The *support* of $M$ is the set $C_\approx(Q_N)$, the set of states of $M$ that are related by $\approx$ to some state of $N$.

**Lemma:** A state of $M$ is in the support of all strong bisimulations involving $M$ iff it is accesible.

### Strong Autobisimulations

**Def:** A string *autobisimulation* is a bisimulation between an automaton to itself.

**Th:** Any nondeterministic automaton $M$ has a coarsest autobisimulation $\equiv_M$. The relation $\equiv_M$ is an equivalence relation. 

Let $\equiv$ be $\equiv_M$ , the maximal strong autobisimilation on $M$.

**Def:** Let $p\in Q$, let $[p]$ denote the $\equiv$-equivalence class of $p$, and let $\gtrsim$ be the relation relating $p$ to its $\equiv$-equivalence class. $\gtrsim := \{(p, [p]) \mid p\in Q\}$. Finally, for any $A\subseteq Q$, define $A' := \{[p] \mid p\in A\}$.

**Lemma:** For all $A, B\subseteq Q$, 
- $A\subseteq C_\equiv(B)$ iff $A' \subseteq B'$,
- $A\equiv B$ iff $A' = B'$, and
- $A \gtrsim A'$. 

We define the quotient automaton $M' ;= (Q', \Sigma, \Delta', S', F)$, where $Q'$, $S'$, and $F'$ refer to the definition above, and $$\Delta'([p], a) := \Delta(p, a)'.$$
**Th:** The relation $\gtrsim$ is a strong bisimulation between $M$ and $M'$

**Lemma:** The only strong autobisimulation on $M'$ is the identity relation $=$.

**Lemma:** Let $M$ be an $\sf NFA$ with no inaccesible states and let $\equiv_M$ be the maximal strong autobisimulation on $M$. The quotient automaton $M'$ is the minimal automaton strongly bisimilar to $M$ and is unique up to isomorphism, 

The following algorithm is a direct generalisation of the algorithm presented for $\sf DFA$s. This algorithm is for computing the maximal bisimulation between any given pair of $\sf NFA$s $M$ and $N$. A pair $(p, q)$ will be marked when a proof is discovered that $p$ and $q$ cannot be related by any strong bisimulation.
1. Write down a table of all pairs $(p, q)$, initially unmarked.
2. Mark $(p,q)$ if $p\in F_M$ and $q\notin F_N$ or viceversa.
3. Repeat the following until no more changed occur: if $(p,q)$ is unmarked, and if for some $a\in \Sigma$, either
	 - there exists $p'\in \Delta_M(p, q)$ such that for all $q'\in \Delta_N(q, a)$, $(p', q')$ is marked, or
	 - there exists $q'\in \Delta_N(q, a)$ such that for all $p'\in\Delta(p, a)$ is marked
	then mark $(p,q)$.
4. Define $p \equiv q$ iff $(p, q)$ is never marked. Check whether $S_M \equiv S_N$. If so then $\equiv$ is the maximal strong bisimulation between $M$ and $N$. If not, then no strong bisimulation between $M$ and $N$ exists.

**Th:** The algorithm above correctly computes the maximal strong bisimulation between two $\sf NFA$s if a strong bisimulation exists. If no bisimulation exists, the algorithm halts and reports failure. If both automata are the same, the algorithm computes the maximal strong autobisimulation. 

