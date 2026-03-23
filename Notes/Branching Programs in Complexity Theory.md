---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[The Complexity Class BPP]], [[The Complexity Class coNP]], [[Finite Fields]]

A *branching program* is a model of computation used in complexity theory and in certain practical areas such as computer-aided design. This model represents a decision process that queries that values of input variables and bases decisions about the way to proceed on the answers to those queries. We present this decision process as a graph whose nodes correspond to the particular variable queried at that point in the process.

**Def:** A *branching program* is a directed acyclic graph where all nodes are labelled by variables, except for two *output nodes* labelled $0$ or $1$. The nodes that are labelled by variables are called *query nodes*. Every query node has two outgoing edges, one labelled $0$ and the other labelled $1$. Both output nodes have no outgoing edges. One of the nodes in a branching program is designated the start node. 

A branching program determines a Boolean function as follows. Take any assignment to the variables appearing on its query nodes and, beginning at the start node, follow the path determined by taking the outgoing edge from each query node according to the value assigned to the indicated variable until one of the output is reached. 

Branching programs are related to the [[The Complexity Classes L and NL|class L]] in a way that is analogous to the relationship between Boolean circuits and the class $\sf P$. 

**Prop:** If $A$ is a language in $\sf L$, a family of branching programs $(B_1,B_2,\dots )$ exists wherein each $B_n$ accepts exactly the strings in $A$ of length $n$ and is bounded in sise by a polynomial in $n$. 

**Prop:** If $A$ is a regular language, a family of branching programs $(B_1,B_2,\dots )$ exists wherein each $B_n$ accepts the strings in $A$ of length $n$ and is bounded in size by a constant times $n$. 

Two branching programs are equivalent if they determine equal functions. 

**Prop:** Let $\text{EQ}_\mathsf{BP} := \{\langle B_1,B_2\rangle \mid B_1 \text{ and } B_2\text{ are equivalent branching programs}\}.$ Then $\text{EQ}_\mathsf{BP}$ is $\sf coNP$-complete. 

If we consider a restricted form of branching programs. A *read-once branching program* is one that can query each variable at most one time on every directed path from the start node to an output node. Let $$\text{EQ}_\mathsf{ROBP} := \{\langle B_1, B_2\rangle \mid \text{$B_1$ and $B_2$ are equivalent read-once branching program}\}.$$
**Lemma:** For every $d\ge 0$, a degree-$d$ polynomial $p$ on a single variable $x$ either has at most $d$ roots, or everywhere equal to $0$. 

**Lemma:** Let $\cal F$ be a finite field with $f$ elements and let $p$ be a nonzero polynomial on the variables $x_1$ through $x_m$, where each variable has degree at most $d$. If $a_1$ through $a_m$ are selected randomly in $\cal F$, then $P[p(a_1,\dots, a_m) = 0] \le md/f.$

**Th:** $\text{EQ}_\mathsf{ROPB}$ is in $\sf BPP$. 