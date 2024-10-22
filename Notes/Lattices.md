---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Orderings]]

Let $(S, \le)$ be a partially ordered set, $S$ is a _meet-semilattice_ if for any $a,b \in S$, then $\inf\{a,b\}$ exists and denoted as $a \wedge b$. It can also be thought as $(S, \land)$ as a algebraic structure, with these properties:

- $\forall x, y, z \in S[x \wedge (y \wedge z) = (x \wedge y) \wedge z]$, associativity
- $\forall x, y \in S[x \wedge y = y \wedge x]$, commutativity
- $\forall x \in S[x \wedge x= x]$, indempotency

$(S, \wedge)$ is bounded if there’s an element $1$ such that $x \wedge 1 = x$, for all $x \in S$. Denoted as $(S, \wedge, 1)$.

The order definition can be recovered by $a \wedge b = a$ iff $a \le b$.

Similarly, $S$ is a a _join-semillattice_ if for any $a, b\in S$, then $\sup\{a,b\}$ exists and denoted as $a \vee b$. t can also be thought as $(S, \vee)$ as a algebraic structure, with these properties:

- $\forall x, y, z \in S[x \vee (y \vee z) = (x \vee y) \vee z]$, associativity
- $\forall x, y \in S[x \vee y = y \vee x]$, commutativity
- $\forall x \in S[x \vee x= x]$, indempotency

$(S, \wedge)$ is bounded if there’s an element $0$ such that $x \vee 0 = x$, for all $x \in S$. Denoted as $(S, \vee, 0)$.

The order definition can be recovered by $a \vee b = b$ iff $a \le b$.

Both the algebraic and the order definition of a semilattice are equivalent.

Let $(L, \le)$ is a _lattice_ if it’s both a joint and meet semilattice. It can also be thought of $(L, \vee, \wedge)$, with the additional absorption laws:

- $\forall a, b \in L[a\vee (a\wedge b)=a]$
- $\forall a, b \in L[a\wedge (a\vee b)=a]$

A lattice $L$ is bounded if it’s both a bounded meet and join semilattice. It can be denoted as $(L, \vee, \wedge, 0, 1)$ where $1$ is the greatest element, and $0$ is the least element of $L$.

A lattice is _complete_ if for every non-empty $A \subseteq L$, $A$ has a an infimum and supremum, denoted as $\bigwedge A$ and $\bigvee A$, respectively.

A Lattice is _distributive_ if

- $\forall a, b, c \in L[a\vee (b \wedge c) =(a\vee b) \wedge(a\vee c)]$, $\vee$ distributive over $\wedge$
- $\forall a, b, c \in L[a\wedge(b \vee c) =(a\wedge b) \vee(a\wedge c)]$, $\wedge$ distributive over $\vee$

A Lattice $L$ is _complemented_ if $L$ is bounded and:

$$ \forall a \in L \exists a' \in L[a\vee a' = 1, a \wedge a'=0 ] $$

A lattice that is complemented and distributive is called _**boolean.**_ This is sometimes called a Boolean algebra. 

A common example, of a Boolean algebra, is the partially ordered set $({\cal P}(X), \subseteq)$, 