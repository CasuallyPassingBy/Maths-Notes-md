---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Time Complexity]], [[Asymptotic Notation]], [[Turing Machines]], [[The Complexity Class NP]], [[Graph Colouring]], [[Parallel Computing in Complexity Theory]]

For a lot of purposes, polynomial differences in running time are considered to be small, whereas exponential differences are considered to be large. Let's look at why we chose to make this separation between polynomials and exponentials rather than between some other classes of functions. 

Exponential time algorithms typically arise when we solve problems by exhaustively searching through a space of solutions, called *brute-force search*. Sometimes, brute-force search may be avoided through a deeper understanding of a problem, which may reveal a polynomial time algorithm of greater utility. 

All reasonable deterministic computational models are *polynomially equivalent*. That is, any one of them can simulate another with only a polynomial increase in running time. When we say that all reasonable deterministic models are polynomially equivalent, we do not attempt to define *reasonable*.

**Th:** Let $t(n)$ be a function, where $t(n) \ge n$. Then every $t(n)$ time multitape Turing machines has an equivalent $O(t^2(n))$ time single-tape Turing machine.

This means that a deterministic single-tape and multitape Turing machine models are polynomially equivalent. 

In this context, we focus on aspect of time complexity theory that are unaffected by polynomial differences in running time. We consider such differences to be insignificant and ignore them. Doing so allows us to develop theory in a way that doesn't depend on our selection of model of computation. 

**Def:** $\sf P$ is the class of languages that are decidable in polynomial time on a deterministic single-tape Turing machine. In other words, $$\mathsf P := \bigcup_{k \in \Bbb N}\text{TIME}(n^k).  $$
The class $\sf P$ plays a central role in our theory and is important because
- $\sf P$ is invariant for all models of computation that are polynomially equivalent to the deterministic single-tape Turing machine, and
- $\sf P$ roughly corresponds to the class of problems that are realistically solvable by a computer.

when a problem is in $\sf P$, we have a method of solving in that runs in time $n^k$ for some constant $k$. Whether this running time is practical depends on $k$ and the application. Of course if $k \ge 100$ it is unlikely to be practical use. Nevertheless, calling polynomial time the threshold of practical solvability has proven to be useful. Once a polynomial time algorithm has been found for a problem that formerly appeared to require exponential time, some key insight into it has been gained, and further reductions in its complexity usually follows, often to the point of actual practical utility. 

**Prop:** $\sf P$ is closed under union, concatenation, and complement. 

**Prop:** Let $f:\Bbb N \to \Bbb N$ be any function where $f(n) = o(n\log n)$. Then $\text{TIME}(f(n))$ contains only regular languages. 

# Examples of Problems in $\sf P$

The first problem concerns directed graphs. A directed graph $G$ contains nodes $s$ and $t$. the $\text{Path}$ problem is to determine whether a directed path exists from $s$ to $t$. Let $$\text{Path}:= \{\langle G, s, t\rangle\mid \text{$G$ is directed graph that has directed path from $s$ to $t$}\}.$$
**Th:** $\text{Path}\in \sf P$.

Let $\text{RelPrime}$ be the problem of testing whether two numbers are relatively prime. Thus$$\text{RelPrime}:= \{\langle x,y \rangle \mid \text{$x$ and $y$ are relatively prime}\}.  $$
**Th:** $\text{RelPrime}\in\sf P$.

**Th:** Every context-free language is a member of $\sf P$. We see that in it [[Parsing with Context-Free Grammars|here]], since we can see that the CYK algorithm is $O(n^3)$.

**Prop:** Let $\text{Connected}:= \{\langle G\rangle \mid G\text{ is a connected undirected graph}\}$. We see that $\text{Connected}\in\sf P$.

**Prop:** A *triangle* in an undirected graph is a $3$-clique. If $\text{Triangle} := \{\langle G\rangle\mid G\text{ contains a triangle}\}$, then $\text{Triangle}\in\sf P$.

**Prop:** $\text{All}_\mathsf{DFA}\in\sf P$. 

**Prop:** let $\text{ModExp} := \{\langle a, b, c, p\mid a,b,c \text{ and }p \text{are binary integers such that} a^b \equiv c\pmod p\}.$ Then $\text{ModExp}\in\sf P$. 

**Prop:** Let $2\text{Color} := \{\langle G\rangle \mid G \text{ is an undirected graph that can be coloured with only }2\text{ colours}\}$. Then $2\text{Color}\in\sf P$. 

**Prop:** Let $\text{SPath}:= \{\langle G, a, b, k\rangle \mid G \text{ contains a simple path of length at most }k\text{ from }a \text{ to  }b\}$. Then $\text{SPath}\in \sf P$.

Let $\text{CNF}_k := \{\langle \phi \rangle \mid \phi \text{ is a satisfiable cnf-formula where each variable appears in at most }k \text{ places}\}.$
**Prop:** $\text{CNF}_2 \in \sf P$.

A *$2$cnf-formula* is an $\text{AND}$ of clauses, where each clause is an $\text{OR}$ of at most two literals. Let $2\text{SAT} := \{\langle \phi\rangle \mid \phi \text{ is a satisfisable 2cnf-formula}\}$. 

**Prop:** $2\text{SAT}\in \sf P$. 

**Th:** $\sf AL = P$. 

**Prop:** A $k$-head pushdown autom

# $\sf P$-completeness

**Def:** If every $A$ in $P$ is[[The Complexity Classes L and NL| log space reducible]] to $B$, then we say that $B$ is *$\sf P$-hard.* If $B$ is both in $\sf P$ and $\sf P$-hard, then $B$ is $\sf P$-complete.

**Prop:** If $A \le_\text L B$ and $B$ is in $\sf NC$, then $A$ is in $\sf NC$. 

For a [[Boolean Circuit Complexity|circuit]] $C$ and input $x$ we write $C(x)$ to be the value of $C$ on $x$. Let $$\text{Circuit-Value} := \{\langle C, x\rangle\mid C \text{ is a Boolean circuit and }C(x) = 1\}.$$
**Th:** $\text{Circuit-Complete}$ is $\sf P$-complete.