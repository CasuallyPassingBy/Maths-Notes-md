---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Natural Numbers]], [[ZF Axioms]]
# Cardinality of Sets

********Def:******** Sets $A$ and $B$ are _**********equipotent**********_ (have the _same cardinality_) if there is a bijective function $f$ with domain $A$ and range $B$. We denote this by $|A| = |B|$.

********Th:********

- $A$ is equipotent to $A$
- If $A$ is equipotent to $B$, then $B$ is equipotent to $A$
- If $A$ is equipotent to $B$, and $B$ is equipotent to $C$, then $A$ is equipotent to $C$

Note that equipotency is not an equivalence relation, since there cannot exits a set of all sets, which would be required to make the equivalence relation.

**Def:** The cardinality of $A$ is less than or equal to the cardinality of $B$ (notation: $|A| \le |B|$) if there is an injection from $A$ to $B$.

We also write $|A| < |B|$ if there’s an injective function $f$ from $A$ to $B$, but there’s no bijection. Similarly, the cardinality of $A$ is greater or equal to the cardinality of $B$ (notation: $|A| \ge |B|$) if there’s a surjection form $A$ to $B$

**************Lemma:**************

- If $|A| \le |B|$ and $|A| = |C|$, then $|C| \le |B|$
- If $|A| \le |B|$ and $|B| = |C|$, then $|A| \le |C|$
- $|A| \le |A|$
- If $|A| \le |B|$ and $|B | \le |C|$, then $|A| \le |C|$
- If $A \subseteq B$, then $|A| \le |B|$

**Lemma:** If $A_1 \subseteq B \subseteq A$, and $|A| = |A_1|$ , then $|B | = |A|$.

********Cantor-Bernstein Theorem********
If $|X| \le |Y|$ and $|Y| \le |X|$, then $|Y |= |X|$

An alternative proof of the Cantor-Bernstein Theorem, using monotone functions.

**Def:** Let ${F: \mathcal {P}(A) \to \mathcal {P}(A)}$ , a set $X \subseteq A$ is called a _****fixed point****_ of $F$ if $F(X) = X$. The function is called _monotone_ if $X \subseteq Y\subseteq A$ implies $F(X) \subseteq F(Y)$.

**Lemma:** Let ${F: \mathcal {P}(A) \to \mathcal {P}(A)}$ be monotone, then it has a fixed point. Additionally we can construct it by

$$ \overline X := \bigcap \{X\subseteq A \mid F(X) \subseteq X\} $$

This is the least fixed point of $F$, meaning if $F(X) = X$, then $\overline X \subseteq X$.

This lemma can be used to prove Cantor-Bernstein Theorem

**********Def:********** A function ${F: \mathcal {P}(A) \to \mathcal {P}(A)}$ is _**********continuous**********_ if $F[\bigcup_{i\in\Bbb N} X_i] = \bigcup_{i \in \Bbb N} F[X_i]$ holds for any nondecreasing sequence of subsets of $A$. $\langle X_i \mid i \in \Bbb N\rangle$ is nondrecreasing if $i \le j$, then $X_i \subseteq X_j$.

**Th:** Let ${F: \mathcal {P}(A) \to \mathcal {P}(A)}$ be a monotone continuous function, then $\overline X = \bigcup_{i \in \Bbb N} X_i$ is the least fixed point of $F$, where $X_0 = \varnothing$, and

$$ X_{i+1} = F[X_i] $$

Showing us that the proof using the lemma is equivalent to the one using monotone functions.

---

# Finite Sets

**********Def:********** A $S$ is called **finite** if it is equipotent to some natural numbre $n\in \Bbb N$. We then define $|S| = n$ and say that $S$ has $n$ elements. A set if _********infinite********_ if it is not finite.

**************Lemma:************** If $n \in \Bbb N$, then there’s no bijection from $n$ into a proper subset of $n$

**Cor:**

- If $n \Bbb Ne m$, then there’s no bijection form $n$ into $m$
- If $|S| =n$ and $|S| = m$, then $n = m$
- $\Bbb N$ is infinite

********Th:******** If $X$ is finite and $Y \subseteq X$, then $Y$ is finite. Moreover, $|Y| \le |X|$.

********Th:******** If $X$ is finite and $f$ a function, then $f[X]$ is finite. Moreover, $|f[X]| \le |X|$

********Th:******** If $X$ and $Y$ are finite, then $X \cup Y$ is finite. Moreover, $|X\cup Y| \le |X|+|Y|$, and if $X$ and $Y$ are disjoint, then $|X\cup Y| = |X|+|Y|$.

********Th:******** If $S$ is finite, and if every $X \in S$ is finite, then $\bigcup S$ is finite.

********Th:******** If $X$ is finite, then $\mathcal P (X)$ is finite.

********Th:******** If $X$ is infinite, then $|X| > n$ for all $n \in \Bbb N$.

******Th:****** If $X$ and $Y$ are finite, then $|X \times Y |$, and $|X^Y |$ are finite, additionally, we get that ${|X\times Y | = |X| \cdot | Y| = |Y \times X|}$ and $|X^Y| = |X|^{|Y|}$.

********Th:******** If $X$ is finite, then $\mathcal P(X)$ is finite and $|\mathcal P(X)| = 2^{|X|}$

---

# Countable Sets

**********Def:********** A set $S$ is _countable_ if $|S| = |\Bbb N|$. A set $S$ is _at most countable_ if $|S| \le |\Bbb N|$

********Th:******** An infinite subset of a countable set is countable.

********Cor:******** A set is at most countable iff it is either finite or countable.

********Th:******** The range of an infinite sequence $\langle a_n\rangle_{n \in \Bbb N}$ is at most countable. In other words, the image of a countable set under any mapping is at most countable.

**Th:** The union of two countable sets is countable.

**Cor:** The union of a finite system of countable sets is countable

********Th:******** If $A$ and $B$ are countable, then $A\times B$ is countable.

**Cor:** The Cartesian product of a finite number of countable sets is countable. Consequently, $\Bbb N ^m$ is countable for every $m >0$.

**Cor:** Let $\langle A_n \mid n \in \Bbb N\rangle$ be a countable system of at most countable sets, and let $\langle a_n \mid n \in \Bbb N\rangle$ be a system of enumerations of $A_n$, i.e., for each $n \in \Bbb N$, then $a_n = \langle a_n (k) \mid k \in \Bbb N\rangle$ is an infinite sequence, and $A_n = \{ a_n (k) \mid k \in \Bbb N\}$. Then $\bigcup _{n \in \Bbb N} A_n$ is at most countable.

********Th:******** If $A$ is countable, then the set $\operatorname{Seq}(A)$ of all finite sequences of elements of $A$ is countable

**Cor:** The set of all finite subsets of a countable set is countable.

********Th:******** An equivalence relation on a countable set has at most countable many equivalence classes

********Cor:******** The set of all integers $\Bbb Z$ and the set of all rational numbers $\Bbb Q$ are countable.

********Th:******** Let $\frak U$ be a structure with the universe $A$, and let $C\subseteq A$ be at most countable. Then $\overline C$, the closure of $C$, is also at most countable.

**Def:** $|A| = \aleph_0$, for all $A$ countable

**Def:** Let $A$ be a set, then we define $[A]^n := \{ S \subseteq A\mid |S| =n\}$. We can extend this definition using the infinite ordinal $\omega$, and we can get $[A]^{<\omega} := \bigcup\limits_{n \in \Bbb N} [A]^n = \{S \subseteq A \mid S \text{ finite}\}$, extending this even further we can have the countably infinite subsets of $A$, denoted as $[A]^\omega$. Finally if we want all the countable subsets of $A$, it can be denoted as $[A]^{\le \omega}$. 

**Th:** Let $A$ be countable, then $[A]^n$ is countable for $n >0$