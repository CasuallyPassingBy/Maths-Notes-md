---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite and Countable Sets]], [[Operations and Structures]]

**Def:** An *alphabet* is any nonempty finite set. We usually denote an alphabet by the Greek letter $\Sigma$. We call elements of $\Sigma$ *letters* or *symbols* and denote them by $a, b, c,\dots$.

A *string* over $\Sigma$ is any finite-length sequence of elements if $\Sigma$. The *length* of a string $x$ is the number of symbols of $x$ is denoted by $|x|$.

There is a unique string of length $0$ over $\Sigma$ called the *null string* or *empty string* and denoted $\varepsilon$. Thus $|\varepsilon| = 0$.

We write $a^n $ for a string of $a$'s of length $n$. Formally, $a^n$ is defined inductively: $$\begin{align*}a^0 &:= \varepsilon\\ a^{n+1} &:= a^n a, \qquad n <\omega.\end{align*}$$
The set of all string over the alphabet $\Sigma$ is denoted by $\Sigma^*$.

By convention, we take $\varnothing^* = \{\varepsilon\}$. 

The operation of *concatenation* takes two strings $x$ and $y$ and makes a new string $xy$ by butting them together end to end. The string $xy$ is called the *concatenation* of $x$ and $y$. There are a couple important properties of concatenation.
- Concatenation is associative, $(xy)z = x(yz)$.
- The empty string $\varepsilon$ is an *identity* for concatenation: $\varepsilon x = x \varepsilon = x$.
- $|xy| = |x| + |y|$.
A special case of the last equation is $a^m a^n = a^{m+n}$ for all $m, n \ge 0$.

We see that if $\Sigma$ is an alphabet, then $(\Sigma^*, \varepsilon, \cdot )$ is a monoid.

**Def:** Let $x$ be a string over an alphabet $\Sigma$. Then we define $x^n$ inductively: $$\begin{align*}x^0 &:= \varepsilon\\ x^{n+1} &:= x^n x, \qquad n <\omega.\end{align*}$$
If $a\in \Sigma$ and $x\in \Sigma^*$, we write $\#a(x)$ for the number of $a$'s in $x$. 

A *prefix* of a string $x$ is an initial substring of $x$; that is a string $y$ for which there exists a string $z$ such that $x =yz$. The null string is a prefix of every string, and every string is prefix of itself. A prefix $y$ of $x$ is a *proper prefix* of $x$ if $y \neq \varepsilon, x$. 

**Def:** Let $\Sigma$ be an alphabet. Then if $w\in \Sigma^*$, we can define its reverse, denoted by $\text{rev}(w)$, to be the same string but in the opposite order. 

**Def:** If $\Sigma$ is an alphabet, then if $A\subseteq \Sigma^*$ then $A$ is called an *language* over $\Sigma$. 

**Def:** Let $A$ and $B$ be languages over $\Sigma$. Then we can define *set concatenation* as  $$AB := \{xy \mid x\in A \land y \in B\}. $$A natural extension is to consider *powers* of $A$. We define them inductively $$\begin{align*}A^0 &:= \varepsilon\\ A^{n+1} &:= AA^n , \qquad n <\omega.\end{align*}$$
The *asterate* $A^*$ of a set $A$ is the union of all the finite powers of $A$:  $$A^* := \bigcup_{n <\omega } A^n. $$Finally, we also consider $A^+$ to be the union of all *nonzero* powers of $A$:$$A^+  := AA^* = \bigcup_{0 <n<\omega} A^n.  $$
We can extend the definition of the reverse of a word, to languages, to get that$$\text{rev }A := \{\text{rev }w \mid w\in A\}.   $$

**Obs:** Since concatenation is associative, then set concatenation is also associative.

**Prop:** Let $\Sigma$ be a an alphabet, and $A, B, C \subseteq \Sigma^*$.
- $\{\varepsilon\} A = A \{\varepsilon\} = A$, meaning that $\{\varepsilon\}$ is an identity for set concatenation.
- $\varnothing A = A \varnothing = \varnothing$, meaning that $\varnothing$ is an *annihilator* for the set concatenation.
- Set concatenation distributes over union: $$\begin{align*}A (B \cup C) &= AB \cup A C,  \\ (A\cup B)C &= AC \cup BC. \end{align*}$$
- If $\{B_i \mid i \in I\}$ is a family of sets indexed by another set $I$, then $$\begin{align*} A\left(\bigcup_{i \in I} B_i\right) &= \bigcup_{i \in I} AB_i, \\
  \left(\bigcup_{i \in I} B_i\right)A &= \bigcup_{i \in I} B_iA.\end{align*} $$

**Prop:** Let $\Sigma$ be a an alphabet, and $A \subseteq \Sigma^*$.
- $A^* A^* = A^*.$
- $(A^*)^* = A^*.$
- $A^* = \{\varepsilon\} \cup AA^* = \{\varepsilon\} \cup A^* A.$
- $\varnothing^*= \{\varepsilon\}$. 

**Def:** A subset $A\subseteq\Sigma^*$ is said to be *regular* if $A = L(M)$ for some finite automaton $M$.

**Closure Properties of Regular Languages:** Let $A$ and $B$ be regular languages over $\Sigma$.
- $A\cap B$ is also regular.
- $\Sigma^*\setminus A$ is also regular.
- $A\cup B$ is also regular.
- $\text{rev A}$ is also regular. 

**Def:** Let $x$ and $y$ be strings and let $L$ be any language. We say that $x$ and $y$ are *distinguishable by $L$* if some string $z$ exists whereby exactly one of the strings $xz$ and $yz$ is a member of $L$: otherwise, for every string $z$, we have $xz\in L$ whenever $yz\in L$ and we say that $x$ and $y$ are *indistinguishable by $L$*. If $x$ and $y$ are indistinguishable  by $L$ we write $x\equiv_L y$. 

**Prop:** Let $L$ be any language. Then $\equiv_L$ is an equivalence relation. 


# Homomorphism

**Def:** A *string homomorphism* is a map $h: \Sigma^* \to \Gamma^*$ such that for all $x, y\in \Sigma^*$  $h(xy) = h(x)h(y).$ 

**Obs:** if $h: \Sigma^* \to \Gamma^*$ is a homomorphism, then $h(\varepsilon) = h(\varepsilon\varepsilon) = h(\varepsilon)h(\varepsilon)$, then this implies that $h(\varepsilon) = \varepsilon$. 

**Prop:** Any map $h: \Sigma \to \Gamma^*$ extends uniquely by induction to a homomorphism defined on all of $\Sigma^*$. This a similar to [[Bases and Dimension|linear transformations with bases]]. 
