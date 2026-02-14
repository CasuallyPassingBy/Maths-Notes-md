---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Functions]], [[Finite and Countable Sets]], [[Operations and Structures]]

Strings of characters are fundamental building blocks in computer science. The alphabet over which the strings are defined may vary with the application. 

We begin a discussion of strings by formally defining a string. To do so, we must introduce the notion of an alphabet and the operation of concatenation. An *alphabet* $\Sigma$ is a finite nonempty set of symbols.

The *concatenation* of two alphabetic characters of sequences of characters $x_1\dots x_n$ and $y_1\dots y_m$ is $x_1\dots x_n \circ y_1 \dots y_m := x_1\dots x_n y_1\dots y_m$. 

A *string* over an alphabet $\Sigma$ is either a letter from the alphabet $\Sigma$ of a sequence of letters derived from concatenation of zero or more characters from the alphabet $\Sigma$. With this in mind, we can define recursively as  $$\Sigma^1:= \Sigma \qquad \Sigma^{n+1} := \Sigma\circ \Sigma^n,\qquad  \text{for $0< n <\omega$}$$where $A \circ B := \{a\circ b \mid a \in A, b\in B\}$. Then we define $$\Sigma^+:= \bigcup_{0<n<\omega} \Sigma^n.$$Additionally, we can define $\varepsilon$ as the empty string. We can now define $\Sigma^0 := \{\varepsilon\}$, and $$\Sigma^* := \bigcup_{n <\omega} \Sigma^n = \{\varepsilon \} \cup \Sigma^+.$$We can now see the importance of $\varepsilon$ it is the identity of the composition, meaning that for every $x\in \Sigma^*$ it satisfies that $x \circ \varepsilon = \varepsilon \circ x = x$. Then we see that $(\Sigma^*, \circ, \varepsilon)$ is a monoid. 

Let $x$, $y$ and $z$ be strings over an alphabet where $z = xy$. The string $x$ is a called a *prefix* of *head* of $z$. if $y\neq \varepsilon$, then $x$ is called a *proper prefix* or *proper head*. Similarly, $y$ is called a *suffix* of *tail* of $z$, and if $x \neq \varepsilon$, then $y$ is called a *proper suffix* or *proper tail*.

**Def:** Let $\Sigma$ be a finite alphabet, then a language $L$ is defined as $L \subseteq \Sigma^*$. 

**Def:** Let $A$ and $B$ be languages. We define the **regular operations** *union*, *concatenation*, and *star* as follows:
- *Union:* $A \cup B$
- *Concatenation:* $A\circ B$
- *Star:* $A^*$

