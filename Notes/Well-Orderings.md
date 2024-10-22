---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Orderings]]

**********Def:********** A set $W$ is ******well-orderd****** by the relation $<$ if

- $(W, <)$ is linearly orderd
- Every nonempty subset of $W$ has a least element

**********Def:********** Let $(L,<)$ be a linearly ordered set. A set $S\subseteq L$ is called an _****************initial segement****************_ of $L$ if $S$ is a proper subset of $L$ and if every $a \in S$, all $x <a$ are also elements of $S$

**************Lemma:************** If $(W, <)$ is a well ordered set and if $S$ is an initial segment of $(W, <)$, then there exists $a \in W$ such that $S = \{ x \in W\mid x <a\}$

If $a$ is an element of a well-ordered set $(W, <)$, we call the set

$$ W[a]= \{x \in W \mid x<a\} $$

the **********_initial segement of $W$ given by $a$._

**************Lemma:************** If $(W, <)$ is a well-ordered set and if $f:W\to W$ is an increasing function, then $f(x) \ge x$ for all $x \in W$

**********Cor:**********

- No well-ordered set is isomorphic to an initial segment of itself
- Each well-orderd set has only one automorphism, the identity
- If $W_1$ and $W_2$ are isomorphic well-ordered sets, then the isomorphism between $W_1$ and $W_2$ is unique

********Th:******** If $(W_1, <_1)$ and $(W_2, <_2)$ are well-ordered sets, then exactly one of the following holds:

- either $W_1$ and $W_2$ are isomorohic, or
- $W_1$ is isomorphic to an initial segment of $W_2$, or
- $W_2$ is isomorphic to an initial segment of $W_1$.

In each case, the isomorphism is unique