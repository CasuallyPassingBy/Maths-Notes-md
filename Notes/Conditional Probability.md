---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Measure]], [[Sigma Algebra]], [[Expected Value of Random Variables]], [[Random Variables]]

**Def:** Let $A$, and $B$ be events. The conditional probability of event $A$ given the event $B$, is denoted as ${P(A \mid B)}$ as satisfies the following equation

$$ P(A\mid B) P(B) = P(A\cap B) $$

we can use induction and get that

$$ P(A_1 \cap \dots\cap A_n) = P(A_1) P(A_2\mid A_1) P(A_3 \mid A_1 \cap A_2) \cdots P(A_n \mid A_1 \cap \dots \cap A_{n-1}) $$

********Def:******** Let $\Omega$ be the sample space, we say that the collection of events $\{ B_1, \dots , B_n\}$ is a finite partition of $\Omega$ if

- $B_i \ne \varnothing$ for all $i$
- $B_i \cap B_j = \varnothing$ , for $i \ne j$
- $\bigcup_{i = 1}^n B_i = \Omega$

### Total Probabilty Theorem

Let $B_1, B_2, \dots, B_n$ is a partition of $\Omega$ such that $P(B_i) \ne 0$ for all $i$. Then for any event $A$

$$ P(A) = \sum_{i = 1}^n P(A \mid B_i ) P(B) $$

in particular, we have that if $P(B) \ne 0, 1$, then

$$ P(A) = P(A \mid B) P(B)+P(A \mid \Omega \setminus B) P(\Omega \setminus B) $$

Let $B_1, B_2, \dots$ be a partition of $\Omega$, such that $P(B_i )\ne 0$, for all $i$. Then for any event $A$

$$ P(A) = \sum_{i = 1}^\infty P(A \mid B_i ) P(B) $$

### Bayes Theorem

Let $B_1, \dots, B_n$ a partition of $\Omega$ such that $P(B_i) \ne 0$ for all $i$. Let $A$ be an event such that $P(A) \ne 0$. Then for any $j = 1, 2, \dots, n$

$$ P(B_j \mid A) = \dfrac{P(A\mid B_j ) P(B_j)}{\sum\limits_{i =1}^n P(A\mid B_i)P(B_i)} $$

Let $B_1, B_2, \dots$ be a partition of $\Omega$, such that $P(B_i )\ne 0$, for all $i$. Then for any event. Let $A$ be an event such that $P(A) \ne 0$. Then for any $j = 1, 2, \dots$

$$ P(B_j \mid A) = \dfrac{P(A\mid B_j ) P(B_j)}{\sum\limits_{i =1}^\infty P(A\mid B_i)P(B_i)} $$

### Inependency of Events

**Def:** We say that the events $A$ and $B$ are independent if

$$ P(A\cap B) =P(A)P(B) $$

or equivalently

$$ P(A) = P(A \mid B) $$Independent events and disjoint events are not the same, two events can be independent and not disjoint, and two events can be disjoint and not independent.

**Def:** We say that $n$ events $A_1, \dots, A_n$ are (mutually) independent it satisfies that

$$ \begin{aligned} P\left(A_{i} \cap A_{j}\right) & =P\left(A_{i}\right) P\left(A_{j}\right), \quad i, j \text { distinct } \\P\left(A_{i} \cap A_{j} \cap A_{k}\right) & =P\left(A_{i}\right) P\left(A_{j}\right) P\left(A_{k}\right), \quad i, j, k \text { distinct } \\& \vdots \\P\left(A_{1} \cap \cdots \cap A_{n}\right) & =P\left(A_{1}\right) \cdots P\left(A_{n}\right) .\end{aligned} $$

********Def:******** We say that an infinite collection of events is independent if for any finite subcollection is independent

**Prop:** Let $A_1, \dots, A_n$ are independent events then

$$ P(A_1 \cup \dots \cup A_n) = 1-P(\Omega\setminus A_1)P(\Omega\setminus A_2) \cdots P(\Omega\setminus A_n) $$

## With respect to a $\sigma$-algebra

Let $\mathscr G$ be sub-$\sigma$-algebra, and $E$ and event. Then we can define the the conditional probability with respect to $\mathscr G$. Then the random variable $P(E \mid \mathscr G)$. has the following properties:
- it is $\mathscr G$ measurable
-  For any event $G \in \mathscr G$ $$E[1_G \cdot P(E \mid \mathscr G)] = P(E \cap G)$$
- 