---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Equivalence Relations and Partitions]]

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

