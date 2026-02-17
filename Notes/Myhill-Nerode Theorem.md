---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Strings and Languages]], [[Automaton State Minimisation]], [[Equivalence Relations and Partitions]]

**Def:** Two deterministic finite autoamata $M := (Q_M, \Sigma,\delta_M, s_M , F_M)$ and $N := (Q_N, \Sigma, \delta_N, s_N, F_N)$ are said to be *isomorphic* if there is a bijection $f: Q_M \to Q_N$ such that
- $f(s_M) = s_N$,
- $f(\delta_(p, q)) = \delta_N(f(p), a)$ for all $p\in Q_N$ and $a\in \Sigma$, and
- $p\in F_M$ iff $f(p)\in F_N$.

# Myhill-Nerode Relations

Let $R\subseteq\Sigma^*$ be a regular language, and let $M := (Q, \Sigma,\delta, s_M , F)$  be the $\sf DFA$ for $R$ with no inaccesible states. The automaton $M$ induces an equivalence relation $\equiv_M$ on $\Sigma^*$ defined by $$x\equiv_M y \iff \hat\delta(s, x) = \hat\delta(s, y). $$

We can see that $\equiv_M$ is an equivalence relation. In addition $\equiv_M$ satisfies a few other properties.
- It is a *right congruence:* for any $x, y\in \Sigma^*$ and $a\in \Sigma$, if $x\equiv_M y$, then $xa \equiv_M ya$.
- If refines $R$, for any $x, y\in \Sigma^*$, if $x\equiv_M y$, then $x\in R$ iff $y\in R$. 
- It is of *finite index*, that is, it has only finitely many equivalence classes. 

Let us call an equivalence relation $\equiv$ on $\Sigma^*$ a *Myhill-Nerode relation for $R$* if it satisfied the properties above; that is a right congruence of finite index refining $R$.

Since we can construct a Myhill-Nerode relation from an $\sf DFA$, then we would like to show that a Myhill-Nerode relation produces an $\sf DFA$.

Let $R\subseteq \Sigma^*$, and let $\equiv$ be an arbitrary Myhill-Nerode relation for $R$. The $\equiv$-class of the string $x$ is $$[x] := \{y\mid y\equiv x\}.  $$
Now we define the $\sf DFA$ $M_\equiv := (Q,\Sigma, \delta, s, F)$ where
- $Q:= \{[x] \mid x\in \Sigma^*\}$,
- $s = [\varepsilon]$,
- $F := \{[x] \mid x\in R\}$,
- $\delta([x], a) := [xa]$.

We want to prove that $L(M_\equiv) =R$. 

**Lemma:** For any $y\in\Sigma^*$, then $\hat\delta([x], y) = [xy]$. 

**Th:** $L(M_\equiv) = R$. 

We have described two natural constructions, one taking a given automaton $M$ for $R$ with no inaccesible states to a corresponding Myhill-Nerode relation $\equiv_M$ for $R$, and one taking a given Myhill-Nerode relation $\equiv$ for $R$ to a $\sf DFA$ for $M_\equiv$ for $R$. We would like to know how these two construction interact with each other.

**Lemma:** 
- If $\equiv$ is a Myhill-Nerode relation for $R$, and if we apply the construction $\equiv \mapsto M_\equiv$ and then apply the construction $M \mapsto \equiv_M$ to the reulst, the resulting relation $\equiv_{M_\equiv}$ is identical to $\equiv$.
- If $M$ is a $\sf DFA$ for $R$ with no inaccesible states, and if we apply the construction $M \mapsto \equiv_M$ and the apply the construction $\equiv \mapsto M_\equiv$ to the result, then the $\sf DFA$ $M_{\equiv_M}$ is isomorphic to $M$.

**Th:** Let $\Sigma$ be a finite alphabet. Up to isomorphism of automata, there is a one-to-one correspondence between deterministic finite automata over $\Sigma$ with no inaccesible states accepting $R$ and Myhill-Nerode relations for $R$ on $\Sigma^*$. 

**Def:** A relation $\equiv_1$ is said to *refine* another $\equiv_2$ if $\equiv_1 \subseteq\equiv_2$ considered as sets of ordered pair. In other words, $\equiv_1$ *refines* $\equiv_2$ if for all $x$ and $y$ $x\equiv_1 y$ implies $x\equiv_2 y$.

The relation of *refinement* between equivalence relations is a partial order. This is trivial to see as the set of equivalence relations is a subset of $\mathcal P(X \times X)$ for some set $X$. since $(\mathcal P(X \times X), \subseteq)$ is a poset, then we can consider the subposet of the set of equivalence relations. The finest relation is the identity relation and the coarsest relation is the universal relation $X\times X$.

**Def:** Let $R\subseteq \Sigma^*$. We define an equivalence relation $\equiv_R$ on $\Sigma^*$ in terms of $R$ as follows:$$x \equiv_R y \stackrel{\text{def}}{\iff} \forall z\in \Sigma^* (xz \in R \iff xy\in R ).  $$

**Lemma:** Let $R\subseteq\Sigma^*$. The relation $\equiv_R$ defined above is a right congruence refining $R$ and is the coarsest such relation on $\Sigma^*$. 

**Myhill-Nerode Theorem:** Let $R\subseteq \Sigma^*$. The following statements are equivalent.
- $R$ is regular;
- there exists a Myhill-Neroede relation for $R$;
- the relation $\equiv_R$ is of finite index.

