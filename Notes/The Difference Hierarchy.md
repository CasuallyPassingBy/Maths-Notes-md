---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Time Complexity]], [[The Complexity Class NP]], [[The Complexity Class P]], [[Oracle Machines and Relative Computation]], [[NP-Completeness]]

**Def:** The difference hierarchy $\sf D_i P$ is defined recursively as
- $\sf D_1 P := NP$, and 
- $\mathsf{D_{i+1} P} := \{A \mid A := B \setminus C \text{ for } B \in \mathsf{NP} \text{ and }C \in \mathsf{D_i P}\}$.

We see that a language in $\sf D_2P$ is the difference of two $\sf NP$ languages. Somtimes $\sf D_2P$ is just denoted as $\sf DP$, and may be written $\sf D^P$. Let $$Z := \{\langle G_1, k_1, G_2, k_2\rangle \mid \text{$G_1$ has a $k_1$-clique and $G_2$ doesn't have a $k_2$-clique}\}. $$

**Prop:** $Z$ is complete for $\sf DP$, meaning that $Z$ is $\sf DP$-hard, and is an element of $\sf DP$.

**Prop:** Let $\text{Max-Clique}:= \{\langle G, k\rangle\mid \text{the largest clique in }G \text{ is of exactly }k\}$. Then $\text{Max-Clique}$ is $\sf DP$-complete.