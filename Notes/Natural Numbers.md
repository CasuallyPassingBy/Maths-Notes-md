---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[ZF Axioms]], [[Orderings]]
We can define the natural numbers as

$$ 0:= \varnothing $$

and $1:= \{\varnothing\} = \{ 0\}$, and $2 =\{\varnothing, \{\varnothing\}\}$. The idea mainly being, $n$ being a set such that is defined by $\{0, 1, \dots, n-1\}$.

**Def:** The **successor** of a set $x$ is the set $S(x)= x\cup \{x\}$. In the case of the natural numbers $S(n)$ is written as $n+1$. Then $n+1:= n \cup \{n\}$.

**Prop:** There’s no set $z$, such that $x \subset z \subset S(x)$, for any set $x$

********Def:******** A set $I$ is called **inductive** if

- $0 \in I$
- If $n \in I$, then $n+1 \in I$.

**Def:** The set of all natural numbers is the set

$$ \Bbb N := \{ x \mid x \in I \text{ for every inductive set } I\} $$

Using the [[ZF Axioms#Axiom of infinity|Axiom of infinity]], we can assert that there exists infinite sets, in particular inductive sets. Thus $\Bbb N$ is well defined. We can define also $\Bbb N^+:= \Bbb N \setminus \{0\}$. 

**************Lemma: $\Bbb N$** is inductive. If $I$ is any inductive set, then $\Bbb N \subseteq I$.

**Def:** The relation $<$ on $\Bbb N$ is defined by: $m < n$ iff $m \in n$. The relation $\le$ on $\Bbb N$ is defined by: $m \le n$ iff $m < n$ or $m =n$.

### Induction Principal

Let $P(x)$ be a property (possibly with parameters). Assume that

- $P(0)$ holds
- For all $n \in \Bbb N$, $P(n)$ implies $P(n+1)$

Then $P$ holds for all natural numbers.

**Lemma:**

- $0 \le n$ for all $\Bbb N$
- for all $k, n \in \Bbb N$, $k < n+1$iff $k \le n$

********Th: $(\Bbb N, <)$** is a strictly linearly [[Orderings|ordered set]]

### Induction Principal V.2. (Strong Induction)

Let $P(x)$ be a property (possibly with parameters). Assume that for all $n \in \Bbb N$,

$$ \text{If }P(k) \text{ holds for all } k < n, \text{ then } P(n) $$

Then $P$ holds for all natural numbers $n$.

**Def:** A linear ordering $\prec$ of a set $A$ is a **well-ordering** if every nonempty subset of $A$ has a least element. The ordered set $(A, \prec)$ is called a **well-ordered set**.

********Th: $(\Bbb N, <)$** is a well-ordered set.

********Th:******** If a nonempty set of natural numbers has an upper bounded in the ordering $<$, then it has a greatest element.

### Finite Induction Principle

Let $P(x)$ be a property. Assume that $k \in \Bbb N$ and

- $P(0)$
- For all $n <k$, $P(n)$ implies $P(n+1)$

Then $P(n)$ holds for $n \le k$.

### Double Induction
Let $P(x, y)$ be a property. Assume
- If $P(k,l)$ holds for all $k, l \in \Bbb N$ such that $k <m$ or ($k = m$ and $l < n$). then $P(m,n)$ holds
Then $P(m,n)$ holds for all $n, m \in \Bbb N$.

---
# Recursion Theorem

**********Def:********** A sequence is a function whose domian is a natural number or $\Bbb N$. A sequence whose domain is a natural number $n\in \Bbb N$ is called a ***********finite sequence of length $n$*, and it is denoted

$$ \langle a_i \mid i < n\rangle \quad\text{or}\quad \langle a_i \mid i =0, 1, \dots, n-1\rangle \quad\text{or}\quad \langle a_0, a_1, \dots, a_{n-1}\rangle $$

In particular the sequence $\langle\rangle = \varnothing$ is the unique sequence of length $0$, the **************empty sequence**************. Then we can define $\operatorname{Seq}(A) = \bigcup_{n \in \Bbb N} A^n$ denotes the set of all finite sequences of elements of $A$. If the domain of a sequence is $\Bbb N$, we call it an _**infinite sequence**_ and denote it

$$ \langle a_i \mid i \in \Bbb N\rangle \quad\text{or}\quad \langle a_i \mid i =0, 1, \dots\rangle \quad\text{or}\quad \langle a_i \rangle_{i = 0}^\infty $$

So infinite sequences of elements of $A$ are just elements of $A^N$. The notation simply specifies a function with am appropiate domain, whise vake at $i$ is $a_i$,. We also use the notation $\{a_i \mid i \in \Bbb N\}$, $\{a_i\}_{i = 0}^\infty$, etc fof the ranglee of the sequence $\langle a_i \mid i \in \Bbb N\rangle$ . Similarly, $\{ a_i \mid i < n\}$ or $\{ a_0, \dots, a_{n-1}\}$ for the ranglee of $\langle a_i \mid i < n\rangle$ .

### Recursion Theorem

For any set $A$, any $a \in A$, and any function $g:A \times \Bbb N \to A$, there exists a unique infinite sequence $f:\Bbb N \to A$ suuch that

- $f_0 = a$
- $f_{n+1} = g(f_n, n)$ for all $n \in \Bbb N$.

********Th:******** Let $(A, \prec)$ be a nonempty linearly ordered set with the properties:

- for every $p \in A$, there is $q \in A$ such that $q \succ p$
- Every nonempty subset of $A$ has a $\prec$-least element
- Every nonempty subset of $A$ that has an upper bound has a $\prec$-greatest element.

Then $(A, \prec)$ is isomorphic to $(\Bbb N, <)$.

### Recursion Theorem V.2.

For any set $S$ and any function $g: \operatorname{Seq}(S) \to S$ there exists a unique sequence $f: \Bbb N \to S$ such that

$$ f_n = g(f|_n) = g(\langle f_0, f_1, \dots, f_{n-1} \rangle) $$

### Recursion Theorem V.3.

Let $a :P \to A$ and $g: P \times A\times \Bbb N \to A$ be functions. There exists a unique function ${f: P \times \Bbb N \to A}$ such that

- $f(p, 0) = a(p)$ for all $p \in P$
- $f(p, n+1) = g(p, f(p, n), n)$