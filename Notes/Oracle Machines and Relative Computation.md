---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Computation Reducibility]], [[Decidable and Undecidable Problems]]

**Def:** An *oracle* for a language $B$ is an external device that is capable of reporting whether any string $w$ is a member of $B$. An *oracle Turing machine* is a modified Turing machine that has the additional capability of querying an oracle. We write $M^B$ to describe an oracle Turing machine that has an oracle for language $B$. 

Formally, an oracle Turing machine is Turing machine that in addition to its ordinary read/write tape is equipped with a special one-way-infinite read-only input tape on which some infinite string is written. The extra tape is called the *oracle tape*, and the string written on it is the called the *oracle*. The machine can move its oracle tape head one cell in either direction in each step and make decisions based on the symbols written on the oracle tape.

We usually think of an oracle as a specification of a set of strings. If the oracle is an infinite string over $\{0, 1\}$, then we can regard it as the characteristic function of a set $B\subseteq \Bbb N$, where the $n$th bit of the oracle string is $1$ iff $n\in\Bbb N$. In that way we can study computation relative to the set $B$.

**Def:** For $A, B\subseteq \Sigma^*$, we say that $A$ is *recursively enumerable in $B$* if there is an oracle Turing machine $M$ with oracle $B$ such that $A= L(M)$. In addition, if $M$ is total, we write $A\le_\text{T}B$ and say that $A$ is *recursive in $B$* or $A$ *Turing reduces to $B$*, 

**Prop:** The relation $\le_\text T$ is transitive. 

**Th:** If $A\le_\text TB$ and $B$ is decidable, then $A$ is decidable.

# Relation to $\sf P$ and $\sf NP$

Let ${\sf P}^A$ be the class of languages decidable with polynomial time oracle machine that uses oracle $A$. Define ${\sf NP}^A$ similarly.

We see that $\sf NP \subseteq P^\text{SAT}$. Furthermore $\sf coNP \subseteq P^\text{SAT}$, being a deterministic complexity class, is closed under complementation. 

**Prop:** If $A\in \sf P$, then ${\sf P}^ A = \sf P$. 

The diagonalisation method is a simulation of one Turing machine by another. The simulation is done so that the simulating machine can determine the behavior of the other machine and then behave differently. Suppose that both of these Turing machines were given identical oracles. Then, whenever the simulated machine queries the oracle, so can the simulator, and therefore the simulation can proceed as before. Consequently, any theorem proved about Turing machines by using only the diagonalisation method would still hold if both machines were given the same oracle. 

**Th:**
- An oracle $A$ exists whereby ${\sf P}^A \neq {\sf NP}^A$.
- An oracle $B$ exists whereby ${\sf P}^B = {\sf NP}^B$.

This means that if we could prove $\sf P$ and $\sf NP$ were different by diagonalising, we could conclude that they are different relative to any oracle as well. But ${\sf P}^B$ and ${\sf NP}^B$ are equal, so that conclusion is false. Hence diagonalisation isn't sufficient to separate two classes. Similarly, no proof that relies on a simple simulation could show that the two classes are the same because that would show that they are the same relative to any oracle, but in fact ${\sf  P}^A$ and ${\sf NP}^ A$ are different.

In summary, the relativisation method tells us that to solve the $\sf P$ vs $\sf NP$ question we must *analyse* computations, not just simulate them. Hence we use [[Boolean Circuit Complexity]] to just that. 

**Prop:** If $\sf NP = P^\text{SAT}$, then $\sf NP = coNP$.

**Prop:** $\text{MAX-CLIQUE}$ is in $\sf P^\text{SAT}$, where $\text{MAX-CLIQUE}$ is $\sf DP$-complete in [[the difference hierarchy]]

**Prop:** Define the *unique-sat* problem to be  $$\text{USAT} := \{\langle \phi \rangle \mid \text{$\phi$ is a Boolean formula that has a single satisfying assignment}\}. $$Then $\text{USAT} \in \sf P^\text{SAT}$. 

**Th:** There exists an oracle $C$ such that ${\sf NP}^C \ne {\sf coNP}^C$. 