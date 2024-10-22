---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Natural Numbers]], [[Ordinal Numbers#The Transfinite Recursion Theorem, Parametric Version|Stronger recursion Theorem]], [[Alephs]]

**Def:** A _binary operation_ on $S$ is a function from $S^2$ into $S$. Nonletter symbols such as $+, \cdot, _, \triangle$, etc. are often used to denote operations. The output of the function is dented as $x_y$ instead of $*(x, y)$.

**Def:** A **unary operation** on $S$ is a function mapping a subset of $S$ into $S$. A *ternary operation* on $S$ is a function on a subset $S^3$ into $S$.

**Def:** A *structure* consists of a set $A$ and of several relations and operations on $A$, usually denoted as an $n$ -tuple.

## $n$-Tuples and Sequences of length $n$

The ordered pair such that

$$ (a_0, a_1) = (b_0, b_1) \iff a_0 = b_0 \land a_1 = b_1 $$

We called $a_0$ the first coordinate of $(a_0, a_1)$, and $a_1$ its second coordinate. In analogy, an $n$-tuple ${(a_0, \dots, a_{n-1})}$ should be a set that uniquely determines its $n$ , we want

$$ (a_0, \dots, a_{n-1}) = (b_0, \dots, b_{n-1}) \iff a_i = b_i \text{ for all }i \in n $$

Using sequences, we find that the ****************_sequence of length $n$, $\langle a_0, \dots, a_{n-1}\rangle$._ The statement that

$$ \langle a_0, \dots, a_{n-1}\rangle = \langle b_0, \dots, b_{n-1} \rangle \iff a_i = b_i \text{ for all }i \in n $$

since it is a comparison of functions. Then we define $n$-tuples as sequences of length $n$.

If $\langle A_i \mid i \in n\rangle$ is a finite sequence of sets, then the $n$-fold Cartesian product $\prod_{i \in n} A_i$, as defined in when talking about the Cartesian product, is the set of $n$ -tuples ${a = \langle a_0, \dots, a_{n-1}\rangle}$, where $a_i \in A_i$ for $i \in n$. If $A_i = A$ for all $i \in n$, then $\prod_{i \in n} A_i = A^n$ is the set of all $n$-tuples with all coordinates from $A$.

We note $A^0 = \{\langle\rangle\}$, and $A^1$ can be identified with $A$.

An $n$-ary relation $R$ in $A$ is a subset of $A^n$. We then write $R(a_0, \dots, a_{n-1})$ instead of ${\langle a_0, \dots, a_{n-1}\rangle \in R}$. Similarly an $n$-ary operation $F$ on $A$ is a function from $A^n$ into $A$; we write $F(a_0, \dots, a_{n-1})$ instead of $F(\langle a_0, \dots, a_{n-1}\rangle)$. If $P(x_0, \dots, x_{n-1})$ is a property with parameters $x_0, x_1, \dots, x_{n-1}$, we write

$$ \{\langle a_0, \dots, a_{n-1}\rangle\mid \forall i \in n[a_i \in A_i] \land P(a_0, a_1, \dots, a_{n-1}\} $$

to denote the set

$$ \left\{a \in \left.\prod_{i \in n}A_i \;\right|\; \text{for some }a_0, a_1, \dots, a_{n-1}, a = \langle a_0, \dots, a_{n-1}\rangle \land P(a_0, \dots, a_{n-1})\right\} $$

A special case is the $0$-ary operation, since it is of the form $\{(\langle\rangle, a)\}$ where $a\in A$. We call them _********constants,********_ and we don’t distinguish them with elements of $A$.

There are problems if we want to define $n$-tuples with recursion as:

$$ (a_0) = a_0 $$$$\forall n \in \Bbb N^+[(a_i)_{i\in n}=(a_0, a_1, \dots, a_n) = ((a_0, a_1, \dots, a_{n-1}), a_n)=((a_i)_{i\in n-1}, a_n)]  
$$

since we need a [[Ordinal Numbers#The Transfinite Recursion Theorem, Parametric Version|stronger recursion Theorem]]
## Structure types

A type $\tau$ is an ordered pair $(\langle r_0, \dots, r_{m-1}\rangle, \langle f_0, \dots, f_{n-1}\rangle)$ of finite sequences of natural numbers, where $r_i >0$ for all $i \in m$. A *****************_structure of type $\tau$_ is a triple

$$ \frak{U} = (A, \langle R_0, \dots, R_{m-1}\rangle, \langle F_0, \dots, F_{n-1}\rangle) $$

where $R_i$ is an $r_i$-ary relation on $A$ for each $i \in m$ and $F_j$ is an $f_j$-ary operation on $A$ for each $j \in n$, in addition we require $F_j \ne \varnothing$ if $f_j = 0$. We call $A$ the ********universe******** of the structure $\frak U$.

**Def:** An *isomorphism* between structures $\frak U$ and $\frak U' = (A', \langle R'_0, \dots, R'_{m-1}\rangle, \langle F'_0, \dots, F'_{n-1}\rangle)$ of the same type $\tau$ is a bijection from $A$ into $A'$ such that

- $R_i(a_0, \dots a_{r_i -1})$ iff $R'_i(h(a_0), \dots, h(a_{r_i-1}))$ holds for all $a_0, \dots, a_{r_i-1}\in A$ and ${i \in m}$
- $h(F_j(a_0, \dots, a_{f_j-1})) = F_j(h(a_0), \dots, h(a_{f_j-1}))$ for all $a_0, \dots, a_{f_j-1}\in A$ and ${j \in n}$, provided that either side is defined.

An isomorphism between $\frak U$ and $\frak U$ is called an _automorphism._ The trivial automorphism is the identity.

**Def:** Consider a fixed structure $\mathfrak{U} = (A, \langle R_0, \dots, R_{m-1}\rangle, \langle F_0, \dots, F_{n-1}\rangle)$. A set $B \subseteq A$ is called **closed** if the result of applying any operation to elements of $B$ is again in $B$. Let $C\subseteq A$; the ********closure******** of $C$, to be denoted $\overline C$, is the least closed set containing all elements of $C$:

$$ \overline C = \bigcap \{ B \subseteq A \mid C \subseteq B \text{ and } B \text{ is closed}\} $$

**Th:** Let $\mathfrak{U} = (A, \langle R_0, \dots, R_{m-1}\rangle, \langle F_0, \dots, F_{n-1}\rangle)$ be a structure and $C \subseteq A$. If the sequence $\langle C_i \mid i \in \Bbb N\rangle$ is defined recursively

$$ C_0 = C $$$$ C_{i+1} = C_i \cup \left(\bigcup_{j \in n}F_j [C_i^{f_j}]\right) $$

then $\overline C = \bigcup_{i \in\Bbb N} C_i$.

********Th:******** Let $P(x)$ be a property. Assume that

- $P(a)$ holds for all $a \in C$
- For each $j \in n$ if $P(a_0), \dots P(a_{f_j-1})$ hold and $F(a_0, \dots, a_{f_j-1})$ is well defined then ${P(F(a_0, \dots, a_{f_j-1}) )}$ holds

Then $P(x)$ holds for all $x \in \overline C$.

## Infinitary Operations

We define $F$ is a (countably) infinitary operation on $A$ if $F$ is a function on a subset of $A^\Bbb N$ (the set of all infinite sequences of elements of $A$) into $A$, and introduce  *structures with infinitary operations*. This can be done formally by extending the definition of type by allowing $f \in \Bbb N \cup \{\Bbb N\}$ and postulating that $F_j$ is an infinitary operation whenever $f_j = \Bbb N$. The definition of a set $B \subseteq A$ being *closed* remains unchanged; if $f_j = \Bbb N$ we require $F_j(\langle a_i \mid i \in \Bbb N\rangle)\in B$ for all $\langle a_i \mid i \in \Bbb N\rangle$ such that $a_i \in B$  for all $i \in \Bbb N$, and $F_j$ is defined. The closure $\overline C$ of $C\subseteq A$  is still the least closed containing all elements of $C$. 

**Th:** Let $\mathfrak{U} = (A, \langle R_0, \dots, R_{m-1}\rangle, \langle F_0, \dots, F_{n-1}\rangle)$ be a structure and let $C\subseteq A$. Let $\overline C$ be the closure of $C$. If $C$ is finite, the $\overline C$ is at most countable; if $C$ is infinite, then $|\overline C| = |C|$. 

**Th:** Let $\mathfrak U = (A, F)$ be a structure where $F$ is a function on a subset of $A^\omega$ into $A$, and let $C\subseteq A$. Let $\overline C$ be the closure of $C$ in $\frak U$, i.e., $$ \overline C = \bigcap \{X \subset A \mid F[X^\omega]\subseteq X \land C\subseteq X\}$$
If $C$ has at least two elements, then $|\overline C| \le |C| ^{\aleph_0}$

We also prove in the same proof that if we define 
$$\begin{align*}
C_0 &= C \\
C_{\alpha+1} &= C_\alpha \cup F[C_\alpha^\omega] \\
C_\alpha&= \bigcup_{\beta <\alpha}C_\beta \quad \text{if }\alpha \text{ is a limit ordinal}
\end{align*}$$
And $$\overline C = \bigcup_{\alpha< \omega_1} C_\alpha$$
