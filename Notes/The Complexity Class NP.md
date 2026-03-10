---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Time Complexity]], [[Asymptotic Notation]], [[Models Equivalent to Turing Machines]], [[The Complexity Class P]], [[NP-Completeness]]

**Def:** A *verifier* for a language $A$ is an algorithm $V$, where $$A = \{w\mid \text{$V$ accepts $\langle w, c\rangle$ for some string $c$}\}.$$We measure the time of a verifier only in terms of the length of $w$, so a *polynomial time verifier* runs in polynomial in the length of $w$. A language $A$ is *polynomially verifiable* if it has a polynomial time verifier. We can write this as $$w\in A \iff \exists c\in \Sigma^{p(|w|)} \text{ s.t. } V(w, c) = \text{accept}.   $$

A verifier uses additional information, represented by the symbol $c$ in the definition above, to verify the string $w$ is a member of $A$. This information is called a *certificate*, or *proof*, of membership in $A$. 

**Def:** $\sf NP$ is the class of languages that have polynomial time verifiers. 

The term $\sf NP$ comes from *nondeterministic polynomial time* and is derived from an alternative characterisation by using nondeterministic polynomial time Turing machines. Problems in $\sf NP$ are sometimes called $\sf NP$-problems. 

**Th:** A language is in $\sf NP$ iff it is decidable by some nondeterministic polynomial time Turing machine.

**Def:** Let $t:\Bbb N \to \Bbb R^+$ be function. Then we define an analogue for nodeterministic Turing machine for $\text{TIME}(t(n))$. $$\text{NTIME}(t(n)) := \{L \mid \text{$L$ is a language decided by a $O(t(n))$ time $\sf NTM$}\}.  $$
**Cor:** $$\mathsf{NP} := \bigcup_{k \in \Bbb N}\text{NTIME}(n^k).$$
Verifying that something is *not* present seems to be difficult than verifying that *is* present. We make a separate complexity class $\sf coNP$, which contains the languages that are complements of languages in $\sf NP$. We don't know whether $\sf coNP$ is different from $\sf NP$. 

**Prop:** $\sf NP$ is closed under union, concatenation, and the star operation. 

## Examples of $\sf NP$-problems

A *Hamiltonian path* in a directed graph $G$ is a directed path that goes through each node exactly once. We consider the problem of testing whether a directed graph contains a Hamiltonian path connecting two specified nodes. Let $$\text{HamPath} := \{\langle G, s, t\rangle \mid \text{$G$ is a directed graph with a Hamiltonian path from $s$ to $t$}\}.  $$
**Th:** $\text{HamPath}\in \sf NP$.

A *clique* in an undirected graph is a subgraph, wherein every two nodes are connected by an edge. A *$k$-clique* is a clique that contains $k$ nodes. The clique problem is to determine whether a graph contains a clique of a specified size. Let $$\text{Clique} :=\{\langle G, k\rangle\mid \text{$G$ is an undirected graph with a $k$-clique}\}. $$
**Th:** $\text{Clique}\in\sf NP$.

In the next problem we have a collection of numbers $x_1,\dots, x_k$ and a target number $t$. We want to determine whether the collection contains a subcollection that adds up to $t$. Thus $$\text{Subset-Sum} := \left\{\langle S,t\rangle\mid \text{$S := \{x_1,\dots, x_k\}$ and for some $A \subseteq S$, we have $\sum_{x\in A} x = t$}\right\}.$$
**Th:** $\text{Subset-Sum}\in\sf NP$.

**Prop:** Let $\text{Iso} := \{\langle G, H\rangle\mid G\text{ and }H\text{ are isomorphic graphs}\}$. Then $\text{Iso}\in \sf NP$. 

**Prop:** Let $\text{Primes} := \{ m \mid m\text{ is a prime number in binary}\}\in \sf NP\cap coNP.$ 

# $\sf P$ vs $\sf NP$

We can summarise a characterisation of $\sf P$ and $\sf NP$, where we loosely refer to polynomial time solvable as solvable 'quickly'
- $\sf P =$ the class of languages for which membership can be *decided* quickly.
- $\sf NP =$ the class of languages for which membership can be *verified* quickly.

The power of polynomial verifiability seems much greater than the of the polynomial decidability. But, hard as it may to imagine, $\sf P$ and $\sf NP$ could be equal. We are unable to *prove* the existence of a single language in $\sf NP$ that is not in $\sf P$. 

The question of whether $\sf P = NP$ is one of the greatest unsolved problems in theoretical computer science and contemporary mathematics. If these classes were equal, any polynomially verifiable problem would be polynomially decidable. This question is presently beyond scientific reach. 

The best method known for solving languages in $\sf NP$ deterministically uses exponential time. In other words can prove that  $$\mathsf{NP} \subseteq \mathsf{EXPTIME} := \bigcup_{k \in\Bbb N}\text{TIME}\left(2^{n^k}\right),$$where we don't know whether $\sf NP$ is contained in a smaller deterministic time complexity class. 

**Prop:** If $\sf P = NP$, then every language $A\in \sf P$, except $A = \varnothing$ and $A = \Sigma^*$, is $\sf NP$-complete.