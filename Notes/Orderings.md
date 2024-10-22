---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Binary Relations]]

Let $R$ be a relation on $A$, if $R$ is reflexive, antisymmetric, and transitive is called a _(partial) ordering_ of $A$. The pair $(A,R)$ is called an _ordered set_.

Let $S$ be a relation on $A$, if $S$ is a asymmetric and transitive, then $S$ is a _strict ordering on $A$._

- Let $R$ be an ordering on $A$, then the relation $S$ on $A$ defined by: $aSb$ iff $aRb$ and $a \ne b$, then $S$ is a strict ordering on $A$.
- Let $S$ be an strict ordering on $A$, then the relation $R$ on $A$ defined by: $aRb$ iff $aRb$ or ${a = b,}$ then $R$ is an ordering on $A$.

Let $a, b \in A$, and let $\le$ be an ordering on $A$, $a$ and $b$ are _comparable_ if $a\le b$ or $b \le a$ holds, and are _incomparable_ if neither $a\le b$ or $b \le a$ holds. Both of the definitions hold for strict ordering.

An ordering $\le$ of $A$ is called _linear_ or _total, $\le$_ is strongly connected.

Let $B \subseteq A$, where $A$ is ordered by $\le$. $B$ is a _chain in $A$_ if $\le$ is strongly connected on $B$.

We can define intervals, given an partial order, let $(A, \le)$, $a \le b$:
- The closed interval $[a. b] := \{ x \in A \mid a \le x \le b\}$, this interval is never empty since $a, b \in [a,b]$
- The open interval $(a,b) := \{x \in A \mid a < x< b\}$, this interval can be empty
- The half-open intervals $[a, b)$, and $(a, b]$ are defined similarly.
- We can can consider the sets $\{x \in X \mid x < a\}$ this is the *initial segment defined by* $a$, and similarly $\{x \in X \mid  a < x\}$ this is the *final segment defined by* $a$. We can denote them as $(\leftarrow, a)$, and $(a, \rightarrow)$, respectively.



### Supremum, Infimum, etc:

**Def:**
Let $\le$ be an ordering of $A$, and $B \subseteq A$:
- $b\in B$ is the _least or minimum_ element of $B$ in the ordering $\le$ if $\forall x \in B[b\le x]$.
- $b\in B$ is the _minimal_ element of $B$ in the ordering $\le$ if $\nexists x \in B[x\le b\land b \ne x]$.
- $a\in A$ is a _lower bound_ of $B$ in the ordering $\le$ if $\forall x \in B[a \le x]$ .
- $a \in A$ is called an _infimum_ of $B$ if it is the greatest of the set of all lower bounds of $B$.
- $b\in B$ is the _greatest or maximum_ element of $B$ in the ordering $\le$ if $\forall x \in B[x\le b]$.
- $b\in B$ is the _maximal_ element of $B$ in the ordering $\le$ if $\nexists x \in B[b\le x\land b \ne x]$.
- $a\in A$ is a _upper bound_ of $B$ in the ordering $\le$ if $\forall x \in B[x \le a]$ .
- $a \in A$ is called an _supremum_ of $B$ if it is the least of the set of all upper bounds of $B$.

**Theorem:**
Let $\le$ be an ordering of $A$, and $B \subseteq A$:

- $B$ has at most least element. $B$ has at most greatest element.
- The least element of $B$ (if it exists) is also minimal. The greatest element of $B$ (if it exists) is also maximal.
- If $B$ is chain, then every minimal element of $B$ is also the least. If $B$ is chain, then every minimal element of $B$ is also the greatest.
- $B$ has at most one infimum. $B$ has at most one supremum.
- If $b$ is the least element of $B$, the $b$ is the infimum of $B$. If $b$ is the greatest element of $B$, the $b$ is the supremum of $B$.
- If $b$ is the infimum of $B$, and $b \in B$, then $b$ is the least element of $B$. If $b$ is the supremum of $B$, and $b \in B$, then $b$ is the greatest element of $B$.
- $b\in A$ is an infimum of $B$ in $(A, \le)$ iff:
    - $\forall x \in B[b \le x]$
    - If $\forall x \in B[b' \le x]$, then $b' \le b$.
- $b\in A$ is an supremum of $B$ in $(A, \le)$ iff:
    - $\forall x \in B[x \le b]$
    - If $\forall x \in B[x \le b']$, then $b \le b'$.

## Derived Orderings
If $(A, \le)$ is an ordered set, then the relation $\le^{-1}$ defined by $a \le^{-1} b$ iff $b\le a$, then ${(A , \le^{-1})}$ is an ordered set. $\le^{-1}$ is the inverse ordering of $(A, \le)$.

If $(A, \le_1)$ and $(B, \le_2)$ are ordered sets, then the relation $\le$ on $A \times B$ defined by:

$$ (a,b) \le (a', b') \iff (a \le_1a') \land (b\le_2 b') $$

then $(A\times B, \le)$ is an ordered sets, and usually called the _product order_ on $A\times B$.

If $(A, \le_1)$ and $(B, \le_2)$ are ordered set, then the relation $\le$ on $A \times B$ defined by:

$$ (a,b) \le (a', b') \iff (a \le_1a') \lor[(a =a')\land(b\le_2 b') ] $$

then $(A\times B, \le)$ is an ordered set, and usually called the _lexicographical order_ on $A\times B$.

If $(A, \le_1)$ and $(B, \le_2)$ are ordered sets and $A \cap B = \varnothing$, then the relation $\le$ on $A \oplus B$ defined by:

$$ a \le b \iff (a \le_1 b) \lor (a\le_2 b ) \lor (a\in A\land b \in B) $$

$A \oplus B$ is the _ordinal or linear sum,_ and $(A \oplus B, \le )$ is an ordered set

An _isomorphism_ between two ordered sets $(P, < )$ and $(Q, \prec)$ is bijection between $P$ and $Q$, such that:

$$ p_1 < p_2 \iff \varphi(p_1) \prec \varphi(p_2) $$

If an isomorphism exists between $(P, <)$ and $(Q, \prec)$, then $(P, <)$ and $(Q, \prec)$ are _isomorphic,_ denoted as $(P, <)\cong(Q, \prec)$.

- $(P, <) \cong (P, <)$
- $(P, <) \cong (Q, \prec)$ then $(Q, \prec) \cong (P, <)$
- $(P, <_1) \cong (P, <_2)$ and $(P, <_2) \cong (P, <_3)$ then $(P, <_1) \cong (P, <_3)$
