---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Binary Relations]], [[Cartesian Product]]

# Functions

A binary relation $F$ is called a _function_ iff $aFb_1$ and $aFb_2$, then $b_1 = b_2$, for any $a$, $b_1$ and $b_2$. This means that every $a \in \text{dom} F$, there’s a unique $b\in \text{ran}F$, that $aFb$. This unique $b$ is called the _value of $F$ at $a$,_ denoted as $F(a)$ or $F_a$. If $F$ is a function that $\text{dom} F = A$, and $\text{ran}F \subseteq B$, then it is written as $F:A \to B, \langle F(a) \mid a \in A\rangle, \langle F_a \mid a \in A\rangle, \langle F(a)\rangle_{a \in A}$, or $A \xrightarrow{F} B$.

The range of the function can be denoted as $\{F(a) \mid a\in A\}$ or $\{F(a)\}_{a\in A}$.

Let $F$ and $G$ be functions, then $F = G$ iff $\text{dom}\,F= \text{dom}\,G$, and ${\forall x \in \text{dom}F[F(x) = G(x)]}$

Let $F$ be a function and $A$ and $B$ sets:

- $F$ is a function _on_ $A$ iff $\text{dom}\, F = A$
    
- $F$ is a function _into_ $B$ iff $\text{ran}\,F \subseteq B$
    
- The _restriction_ of the function $F$ _to $A$_ is the function:
    $$ F|_A =\{(a,b) \in F\mid a \in A\} $$
    
    If $G$ is a restriction of $F$ to some $A$, then $F$ is an _extension_ of $G$.
    

Let $f$ and $g$ be functions. Then $g\circ f$ is a function.

$$ \def\dom{\text{dom}\,} \dom(g\circ f) = \dom f \cap f^{-1}[\dom g] $$

Also $(g\circ f)(x) = g(f(x)),$ for all $x \in \text{dom}\, (g\circ f)$.

Let $A$ and $B$ be sets . The set of all functions on $A$ into $B$ is denoted $B^A$. Since $f \subseteq A \times B$, then $f \in \mathcal{P}(A\times B)$, then $B^A \subseteq \mathcal P(A\times B)$, thus $B^A$ must exist for any $A$ and $B$.

Let’s consider a family of indexed sets $S =\langle S_i \mid i \in I \rangle$, then the _product_ of the indexed set $S$ is:

$$ \prod_{i\in I} S_i = \left\{ \left. f:I\to \bigcup_{i\in I}S_i \right| \forall i \in I[f(i) \in S_i]\right\} $$

if for any $i \in I$, $S_i= B$, then

$$ \prod_{i\in I}S_i = \prod_{i\in I} B= B^I $$

There are other notations: $\prod S$, $\prod\langle S_i \mid i \in I \rangle$ and $\prod_{i\in I}S(i)$.

A is a set _indexed by $S$_ if:

$$ A = \{S_i \mid i\in I\} = \text{ran}\, S $$

Where $S$ is a function on $I$. It is expected to write:

$$ \bigcup A = \bigcup \{S_i \mid i \in I \} = \bigcup_{i\in I} S_i $$

### Compatible Functions

**Def:**

Functions $f$ and $g$ are _compatible_ iff $\def \dom{\text{dom}\,} \forall x \in \dom f\cap \dom g[f(x) = g(x)]$

A set of functions $\cal F$ is _compatible_ iff $\forall f, g \in \mathcal{F}[f, g\text{ are compatible]}$.

**Theorems:**

Functions $f$ and $g$ are compatible iff $f\cup g$ is a function

Functions $f$ and $g$ are compatible iff $\def \dom{\text{dom}\,} D =\dom f \cap \dom g$, $f|_D= g|_D$.

If $\cal F$ is a compatible system of functions, then $\bigcup \cal F$ is a function, with $\def \dom{\text{dom}\,} {\dom F = \bigcup_{f\in \cal F} \dom f}$. The function $\bigcup \cal F$ extends all $f \in \cal F$

### Properties

Let $X$, $Y$ be sets, $f:X\to Y$ be a function, $A_1, A_2 \subseteq X$ and $B_1, B_2\subseteq Y$. Then

- If $A_1 \subseteq A_2$ then $f[A_1] \subseteq f[A_2]$
- $f[A_1 \cup A_2] = f[A_1] \cup f[A_2]$
- $f[A_1\cap A_2] \subseteq f[A_1] \cap f[A_2]$
- $f[A_1\setminus A_2] \supseteq f[A_1] \setminus f[A_2]$
- If $B_1 \subseteq B_2$ then $f^{-1}[B_1] \subseteq f^{-1}[B_2]$
- $f^{-1}[B_1 \cup B_2] = f^{-1}[B_1] \cup f^{-1}[B_2]$
- $f^{-1}[B_1\cap B_2] = f^{-1}[B_1] \cap f^{-1}[B_2]$
- $f^{-1}[B_1\setminus B_2] = f^{-1}[B_1] \setminus f^{-1}[B_2]$
- $f^{-1}[f[A_1]]\supseteq A_1$
- $f[f^{-1}[B_1]] \subseteq B_1$

## Injective and Surjective functions

Let $f$ be a function is _injective_ if for any $a_1, a_2 \in \text{dom}\,f$, if $a_1 \ne a_2$, then $f(a_1) \ne f(a_2)$. The set of all injective functions from $A$ to $B$ is usually denoted as $\text{Inj}(A, B)$

Let $f:A \to B$, then $f$ is _surjective_ if $\text{ran}\, f = B$. The set of all surjective functions from $A$ to $B$ is usually denoted as $\text{Sur}(A, B)$

Let $f:A \to B$, $f$ is _bijective_ if it is injective and surjective. The set of all bijective functions from $A$ to $B$ is usually denoted as $\text{Bij}(A, B)$, and in the special case where $A =B$ it is denoted as $\text{Sym}(A)$ or $S_A$ , and is the [[Symmetric Groups|symmetric group of]] $A$. 

- Equivalences of injectivity
    Let $f:X \to Y$, with $X \ne \varnothing$. Then all are equivalent:
    - $f$ is injective
    - for all $A \subseteq X$, $f^{-1}[f[A]] = A$
    - for any $A_1, A_2\subseteq X$, then $f[A_1\setminus A_2] = f[A_1]\setminus f[A_2]$
    - for any $A_1, A_2\subseteq X$, then $f[A_1\cap A_2] = f[A_1]\cap f[A_2]$

- Equivalences of surjectivity
    $f: X\to Y$ . Then the following are equivalent:
    - $f$ is surjective
    - for all $\varnothing \ne B \subseteq Y$, $f^{-1}[B] \ne \varnothing$
    - for all $B \subseteq Y$, $f[f^{-1}[B]] = B$
    - For all $A \subseteq X$, $f[X\setminus A] \supseteq Y \setminus f[A]$

$f: X\to Y$, then $f$ is bijective iff for any $A \subseteq X$, $f[X\setminus A] = Y \setminus f[A]$

- Properties, let $f:X\to Y$, and $g:Y\to Z$:
    - If $f,g$ are injective, then $g\circ f$ is injective.
    - If $f,g$ are surjective, then $g\circ f$ is surjective.
    - If $f,g$ are bijective, then $g\circ f$ is bijective.
    - If $g \circ f$ is bijective, then $f$ is injective, and $g$ is surjective

Let $f:X \to Y$:

- A function $g:Y\to X$, it’s called a _left inverse_ if, $g\circ f= \text{id}_X$
- A function $g:Y\to X$, it’s called a _right inverse_ if, $f\circ g= \text{id}_Y$

There’s a way to express if a function $f$ is injective or surjective. Let $f:X \to Y$:

- $f$ is injective iff $f$ has a left inverse.
- $f$ is surjective iff $f$ has a right inverse.

Let $f$ be bijective, iff $f$ has left and right inverse. More so, $f$ has a unique _inverse $g:Y\to X$,_ such that $g\circ f= \text{id}_X$ and $f\circ g= \text{id}_Y$, usually denoted as $f^{-1}$.

$f$ is injective iff for any set $Z$, and any function $g, h:Z \to X$, if $f\circ g = f \circ h$, then $g = h$

$f$ is surjective iff for any set $Z$, and any function $g, h:Y \to Z$, if $g\circ f = h \circ f$, then $g = h$