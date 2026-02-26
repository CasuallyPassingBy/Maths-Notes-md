---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Computation Reducibility]], [[Turing Machines]], [[Decidable and Undecidable Problems]], [[Other Formalisms Equivalent to General Computation]]

# The Post Correspondence Problem

In this note we show that the phenomenon of undecidability is not confined to problems concerning automata. It is called the *Post correspondence problem* or *PCP.*

We can describe this problem easily as a type of puzzle. We begin with a collection of dominos, each containing two strings, one on each side. An individual domino looks like $$\left[\frac{a}{ab}\right]  $$and a collection of dominos looks like $$\left\{\left[\frac{b}{ca}\right], \left[\frac{a}{ab}\right] , \left[\frac{ca}{a}\right], \left[\frac{abc}{c}\right]\right\}.  $$The task is to make it a list of these dominos, repetitions permited, so that the string we get reading off the symbols on the top is the same as the string of symbols on th bottom. The list is called a *match*. An example is  $$\left[\frac{a}{ab}\right]\left[\frac{b}{ca}\right]\left[\frac{ca}{a}\right]\left[\frac{a}{ab}\right]\left[\frac{abc}{c}\right]. $$
Reading off the top string we get that $\verb|abcaaabc|$, with is the same as reading off the bottom.  For some collections of dominos finding a match may not be possible. For example, the collection$$\left\{\left[\frac{abc}{ab}\right], \left[\frac{ca}{a}\right],\left[\frac{acc}{ba}\right] \right\}  $$cannot contain a match every top string is longer than the corresponding bottom string. 

The Post correspondence problem is to determine whether a collection of dominos has a match. 

An instance of the PCP is a collection $P$ of dominos: $$P := \left\{\left[\frac{t_1}{b_1}\right], \left[\frac{t_2}{b_2}\right], \dots, \left[\frac{t_k}{b_k}\right]\right\},  $$and a match is a sequence $i_1, i_2,\dots, i_l$ where $t_{i_1} t_{i_2} \cdots t_{i_l} = b_{i_1}b_{i_2}\cdots b_{i_l}$. The problem is to determine whether $P$ has a match. Let  $$\text{PCP} := \{\langle P \rangle \mid \text{$P$ is an instance of the Post correspondence problem with a match}\}. $$
**Th:** $\text{PCP}$ is undecidable.

We want to reduce the $A_\mathsf{TM}$ to the Post Correspondence Problem using computation histories. We show that from any Turing machine $M$ and input $w$ we can construct an instance $P$ where a match is an accepting computation history for $M$ on $w$. If we could determine whether the instance has a match, we would be able to determine whether $M$ accepts $w$.

First, for convenience in constructing $P$, we assume that $M$ on $w$ never attempts to move it head off the left-hand of the tape. That requires first altering $M$ to prevent this behaviour. Second, if $w = \varepsilon$, we use the string $\textvisiblespace$ in place of $w$ in the construction. Third, we modify the $\text{PCP}$ to requiere that a match starts with the first domino, $$\left[\frac{t_1}{b_1}\right].$$We call this modified Post correspondence problem, $\text{MPCP}$. Let $$\text{MPCP}:= \{\langle P \rangle \mid \text{$P$ is an instance of the PCP with a match that starts with the first domino}\}  $$
Let $R$ decide the $\text{PCP}$ and construct $S$ deciding $A_\mathsf{TM}$. Let $M =(Q, \Sigma, \Gamma, \delta, q_0,q_\text{accept}, q_\text{reject})$, where $Q$, $\Sigma, \Gamma$, and $\delta$, are the state set, input alphabet, tape alphabet, and transition function of $M$, respectively. 

**Part 1:** The construction begins in the following manner. Put $$\left[\frac{\#}{\#q_0w_1\cdots w_n\#}\right]$$into $P'$ as the first domino $$\left[\frac{t_1}{b_1}\right].$$Thus the bottom string begins correctly $C_1 = q_0w_1\cdots w_n$, the first configuration in the accepting computation history for $M$ on $w$. 

In this depiction of the partial matched achieved so far, the bottom string consists $\#q_0w_1\cdots w_n\#$ and the top string only of $\#$. To get a match we need to extend the top string to match the bottom string. 

**Part 2:** For every $a, b\in \Gamma$ and every $q, r, \in Q$, where $q \neq q_\text{accept}$, if $\delta(q, a) = (r, b, R)$, put $$\left[\frac{qa}{br}\right]  $$into $P'$.

**Part 3:** For every $a, b, c\in \Gamma$ and every $q, r, \in Q$, where $q\neq q_\text{reject}$, if $\delta(q, a) = (r, b, L)$, put $$\left[\frac{cqa}{bcr}\right]  $$into $P'$.

**Part 4:** for every $a\in\Gamma$, put $$\left[\frac aa\right]$$into $P'$. 

**Part 5:** Put $$\left[\frac \#\#\right]\quad \text{and}\quad\left[\frac{\#}{\textvisiblespace\#}\right] \quad \text{into }P'.$$
As we construct a match, we are forced to simulate $M$ on input $w$. This process continues untile $M$ reaches a halting state. If an accept state occurs, we want to the let the top of the partial match 'catch up' with the bottom so that the match is complete. We can arrange for that to happen by adding additional dominos.

**Part 6:** For every $a\in \Gamma$, put  $$\left[\frac{aq_\text{accept}}{q_\text{accept}}\right]\quad \text{and}\quad\left[\frac{q_\text{accept} a}{q_\text{accept}}\right] \quad \text{into }P'. $$
This steps has the effect of adding pseudo-steps of the Turing machine after it has halted, where the head 'eats' adjacent symbols until none are left. 

**Part 7:** Finally we add the domino $$\left[\frac{q_\text{accept}\#\#}{\#}\right]$$and complete the match, 

That concludes the construction of $P'$. Since $P'$ is an instance of $\text{MPCP}$ whereby the match simulates the computation of $M$ on $w$. We want to convert $P'$ to an instance of $\text{PCP}$ that still simulates $M$ on $w$.

Let $u = u_1\cdots u_n$ be any string of length $n$. We define $\star u$, $u\star$ and $\star u \star$ to be the three strings.
- $\star u := u_1*u_2*u_3*\cdots*u_n$,
- $u\star := u_1*u_2*u_3*\cdots*u_n*$
- $\star u \star := *u_1*u_2*u_3*\cdots*u_n*$. 

To convert $P'$ to $P$, an instance of the $\text{PCP}$, we do the following. If $P'$ were the collection $$\left\{\left[\frac{t_1}{b_1}\right], \left[\frac{t_2}{b_2}\right], \dots, \left[\frac{t_k}{b_k}\right]\right\}  $$we let $P$ be the collection $$\left\{\left[\frac{\star t_1}{\star b_1\star}\right], \left[\frac{\star t_2}{b_2\star}\right], \dots, \left[\frac{\star t_k}{b_k\star}\right],\left[\frac{*\diamond}{\diamond}\right]\right\}.$$Considering $P$ as an instance of the $\text{PCP}$, we see that the only domino that could possible start a match is the first one $$\left[\frac{\star t_1}{\star b_1\star}\right],$$because it is the only one where both the top and the bottom start with the same symbol. Finally, the domino $$\left[\frac{*\diamond}{\diamond}\right]$$is there to allow the top add the extra $*$ at the end of the match. 

In the proof not only have we seen that the $\text{PCP}$ is undecidable, but it is also equivalent to the $\text{MPCP}$. We also have seen that Post systems can simulate Turing machines. 

# Post Systems

A Post system consists of disjoint finite sets $N$ and $\Sigma$ of *nonterminal* and *termonal symbols,* respectively, a special *start symbol $S\in N$*, as a set of *variables* $X_0, X_1,\dots,$ ranging over $(N \cup\Sigma)^*$, and a finite set of *productions* of the form $$x_0X_1x_1X_2x_2X_3 \cdots X_n x_n \to y_0Y_1y_1Y_2y_2Y_3\cdots Y_m y_m,$$where $x_i$ and $y_j$ are strings in $(N\cup \Sigma)^*$ and each $Y_j$ is some $X_o$ that occurs on the left hand side. If a string in $(N\cup \Sigma)^*$ matches the left-hand side for some assignment of strings to the variables $X_i$, then that string can be rewritten as specified by the right-hand A string $x\in \Sigma^*$ is *generated* by the systems if $x$ can be derived from $S$ by a finite sequence of such rewriting steps.

Post systems and Turing machines are equivalent in computational power. Any Post system can be simulated by a Turing machine that writes the start symbol on a track of its tape, then does the pattern matching and string rewriting according to the productions of the Post system in all posible ways, accepting it its input $x$ is ever generated. Conversely, given any Turing machine $M$, a Post system $P$ can be designed mimics the actions of $M$. The sentential forms of $P$ configurations of $M$.