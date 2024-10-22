---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Orderings]], [[Finite and Countable Sets]]

**Def:** Linearly ordered sets $(A, <)$ and $(B, \prec)$ are **similar** if they are isomorphic.

**************Lemma:************** Every linear ordering on a finite set of a well-ordering

**Th:** If $(A_1, <_1)$ and $(A_2, <_2)$ are linearly ordered sets and $|A_1| = |A_2|$ is finite, then $(A_1<_1)$ and $(A_2, <_2)$ are similar.

********Lemma:******** If $(A, <)$ is a linear ordering, then $(A, <^{-1})$ is also a linear ordering

**************Lemma:************** Let $(A_1, <_1)$ and $(A_2, <_2)$ are linearly ordered sets, then:

- If $A_1 \cap A_2 = \varnothing$, then the linear sum $(A_1 \oplus A_2, <)$ is a linear ordering
- The lexicografical sum of $(A_1 \times A_2, <)$ is a linear ordering

**Th:** Let $\langle (A_i, <_i) \mid i \in I\rangle$ be an indexed system of linearly ordered sets, where $I \subseteq \Bbb N$. The relation $\prec$ on $\prod_{i \in I} A_i$ defined by

$$ \begin{align*} f \prec g \iff & \operatorname{diff}(f, g)=\{i \in I \mid f_i \Bbb Ne g_i \}\Bbb Ne \varnothing \text{ and } f_{i_0} < _{i_0} g_{i_0} \\ & \text{where ${i_0}$ is the least element of } \operatorname{diff}(f,g) \end{align*} $$

**Def:** An ordered set $(X, <)$ is **dense** if it has at least two elements and if for all $a, b \in X$, $a< b$ implies that there exists $x \in X$ such that $a< x<b$. Let us call the least and greatest elements of a linearly ordered set (if they exist) the _********endpoints********_ of the set

********Th:******** Let $(P, \prec)$ and $(Q, <)$ be countable dense linearly ordered sets without endpoints. Then $(P, \prec)$ and $(Q, <)$ are similar.

**Th:** Every countable linearly ordered set can be mapped isomorphically into any countable dense linearly ordered set without endpoints.

---

# Complete Linear Ordering

**Def:** Let $(P, <)$ be a linearly ordered set. A **gap** is a pair $(A, B)$ of sets such that

- $A$ and $B$ are nonempty disjoint subsets of $P$ and $A\sqcup B= P$
- If $a \in A$ and $b \in B$, then $a < b$
- $A$ does not have a greatest element and $B$ doesn’t have a least element

**Def:** We call a set $P$ a subset of a linear ordering, **bounded above** if it has a upper bound. Similarly, when we call it **bounded below**, if it has a lower bound. Finally we say $P$ is **bounded** if it bounded below and above.

From these definitions, we see that the gap $(A, B)$ of $P$, then $A$ is bounded above, and $B$ bounded below. If $c$ was the supremum of $A$, then either $c \in A$ or $c \in B$, but if $c \in A$, then $A$ would have a greatest element. If $c \in B$, then $c$ would be the least element. Then we say that the supremum of $A$ doesn’t exist, similarly for the infimum of $B$.

On the other hand, let $S$ be bounded above. Let

$$ A = \{x \mid \exists s \in S[x \le s] \} \\ B = \{ x \mid \forall s \in S[x > s]\} $$

Then we can see that $S$ has a no supremum iff $(A, B)$ is a gap

**************Def:************** Let $(P, <)$ be a dense linearly ordered set. $P$ is **complete** if every nonempty $S\subseteq P$ bounded above has a supremum. Note that $(P, <)$ is complete iff it doesn’t have gaps.

**Th:** Let $(P, <)$ be a dense linearly ordered set without endpoints. Then there exists a complete linearly ordered set $(C , \prec)$ such that

- $P \subseteq C$
- If $p, q \in P$, then $p< q$ iff $p \prec q$ ($\prec$ coincides with $<$ on $P$)
- $P$ is dense in $C$, i.e., for any $a, b \in C$ such that $a\prec b$, there exists $p \in P$ such that ${a \prec p \prec b}$
- $C$ doesn’t have endpoints

Moreover, this complete linearly ordered set $(C, \prec)$ is unique up to isomorphism over $P$. In other words, if $(C^*, \prec^*)$ is a complete linearly ordered set that satisfies the conditions above, then there exists $\phi$ between $(C, \prec)$ and $(C^*,\prec^*)$ such that $\phi(x) = x$, for $x \in P$. The linearly ordered set $(C, \prec)$ is called the **completion** of $(P, <)$

**Def:** A cut is a pair $(A, B)$ of subsets such that

- $A$ and $B$ are nonempty disjoint subsets of $P$ and $A\cup B= P$
- If $a \in A$ and $b \in B$, then $a < b$

**Def:** A cut $(A, B)$ is a **Dedekind cut** if $A$ doesn’t have a greatest element.

We have two types of Dedekind cuts $(A, B)$:

- Those where $B = \{ x \in P \mid x \ge p\}$ for some $p \in P$; we denote $(A,B) = [p]$
- Gaps

Let $C$ be the set of all Dedekind cuts $(A,B)$ in $(P, <)$ and the order of $C$, as

$$ (A, B) \preceq (A', B') \iff A \subseteq A' $$

The set $P' = \{ [p] \in C\mid p \in P\}$ is isomorphic to $P$, and $C$ is the completion of $P$.

**Def:** The completion of $(\Bbb Q, <)$ is denoted $(\Bbb R, <)$; the elements of $\Bbb R$ are the **real numbers.**

**Th:** $( \Bbb R, <)$ is the unique (up to isomorphism) complete linearly ordered set without endpoints that has a countable subset dense in it.

---

# Uncountable Sets

********Th:******** The set $\Bbb R$ of all real numbers is uncountable

**Th:** The set of all sets of natural numbers is uncountable: in fact $|\mathcal P(\Bbb N) |>|\Bbb N|$

**Th:** $|\mathcal P(\Bbb N) | = \left|2^\Bbb N\right| = |\Bbb R|$