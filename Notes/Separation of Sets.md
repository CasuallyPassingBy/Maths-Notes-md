---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Separation Axioms]], [[Normal Hausdorff Spaces]], [[Continuous Distributions]], [[Topological Spaces]]

**Def:** In a topological space $X$, and subsets $A$ and $B$ of $X$, we say that $A$ and $B$ are *separated* if $\text{cl}(A) \cap B= A \cap \text{cl}(B) = \varnothing$. This is known as the *Hausdorff-Lennes Separation Condition*. 

We note that this is stronger than being disjoint

**Def:** In a topological space $X$, and subsets $A$ and $B$ of $X$, we say that $A$ and $B$ are *separated by neighbourhoods* if there are neighbourhoods $U$ of $A$ and $V$ of $B$ such that $U$ and $V$ are disjoint. 

We see that if $A$ and $B$ are open and disjoint, then we get that the neighbourhoods are just themselves. Because of that we care about separating closed subsets by neighbourhoods. If every pair of disjoint closed subsets can be separated by 

**Def:** In a topological space $X$, and subsets $A$ and $B$ of $X$, we say that $A$ and $B$ are *separated by closed neighbourhoods* if there are closed neighbourhoods $U$ of $A$ and $V$ of $B$ such that $U$ and $V$ are disjoint. 

**Def:** In a topological space $X$, and subsets $A$ and $B$ of $X$, we say that $A$ and $B$ are *separated by a continuous function* if there exists a continuous function $f: X\to \Bbb R$ such that $A \subseteq f^{-1}\{0\}$ and $B \subseteq f^{-1}\{1\}$. 

**Def:** In a topological space $X$, and subsets $A$ and $B$ of $X$, we say that $A$ and $B$ are *precisely separated by a continuous function* if there exists a continuous functions $f: X\to \Bbb R$ such that $A = f^{-1}\{0\}$ and $B = f^{-1}\{1\}$. 

**Def:** A subset $A$ of a topological space $X$, we say that $A$ is a *zero set* if there's a continuous function $f:X\to I$, such that $A = f^{-1}\{0\}$. Analogously, we say that $A$ is a *co-zero set* if there's a continuous function $f:X \to I$ such that $A = f^{-1}[(0,1]]$. 

**Th:** Any disjoint zero sets $A$, and $B$ in a topological space $X$ are precisely separated by a continuous function. 