---
tags:
  - SetTheory
  - NumberTheory
  - RingTheory
---
Subjects: [[Set Theory]], [[Elementary Number Theory]], [[Ring Theory]]
Links: [[Natural Numbers]], [[Equivalence Relations and Partitions]], [[Arithmetic of Natural Numbers]]

We would like to construct the integers as the next logical step in the construction of mathematics.

The idea is to make an arithmetic operation that is only partially defined in the naturals, subtraction, into a total operation, and belongs more properly in the realm of algebra than set set theory. 

As we can see in while defining [[Arithmetic of Natural Numbers#Difference or Subtraction|subtraction]], we see that we only defined the subtraction on pairs $(n, m)$ where $n \ge m$. This is because there's a unique $k \in \Bbb N$, such that $n = m+k$, and we define $n - m = k$. If $n < m$, there's no such $k \in \Bbb N$. 

We would like to create a new object and as so we are going to use just tuples to represent it, $(n , m)$ instead of writing $n - m$. We would like that for example $(2, 5)$ and $(6, 9)$ represent the same quantity. In general, we would like that $(n_1, m_1)$ and $(n_2, m_2)$ represent the same integer if $n_1-m_1 = n_2 - m_2$. Since it might not be defined the operation, we can rewrite it as $$ n_1+m_2 = n_2+m_1$$
Which only involves only addition of natural numbers. 

Let $Z = \Bbb N \times \Bbb N$, and we define $\approx$ on $Z$, by $(a, b) \approx (c, d)$ iff $a+d= b+c$. The relation $\approx$ is an equivalence relation on $Z$. Let $\Bbb Z := Z/\approx$ be the set of all equivalence classes of $Z$ modulo $\approx$.  We call $\Bbb Z$ the *set of all integers*; its elements are *integers*. 

The set $\Bbb Z$ is countable.

Next, we define the relation $<$ on $\Bbb Z$, as follows: $[(a, b)] < [(c, d)]$ iff $a+d < b+c$. We see that $<$ is well defined, since it doesn't depend on the choice of representatives, and it is a linear ordering.

We observe if we have the integer $[(a, b)]$, either $a \ge b$, in which case $(a, b) \approx (a-b, 0)$, where $-$ represents the natural number's subtraction, or $a < b$, in which case $(a, b) \approx (0, b-a)$. It follows that each integer contains a unique pair of the form $(n, 0)$, $n \in \Bbb N$ or $(0, n)$, $n\in \Bbb N^+$. So $[(n, 0)]$ are the positive integers, and $[(0, n)]$ are the negative ones. The mapping $F: \Bbb N \to \Bbb Z$ defined as $F(n) = [(n , 0)]$ is injective and order preserving. We identify each integer of the form $[(n, 0)]$ with the corresponding natural number $n$, and denote each integer of the form $[(0, n)]$ as $-n$.

We can prove that $(\Bbb Z, <)$ has no endpoints and $\{x \in \Bbb Z \mid a < x< b\}$, $a, b \in \Bbb Z$, $a < b$ has a finite number of elements. Also, every nonempty set of integers bounded from above has a greatest element, and every nonempty set of integers bounded from below has a least element. 

One can define *addition* and *multiplication* of integers by $$[(a,b)] + [(c, d)] = [(a+c, b+d)]$$ $$[(a, b)]\cdot [(c, d)] = [(ac+bd, ad+bc)]$$
and these operations satisfy the usual laws of algebra:
- commutativity
- associativity
- distributivity of multiplication over addition

and that for those integers that are natural numbers, addition and multiplication of integers agree with addition and multiplication of natural numbers. 

We define *subtraction* by $$ [(a, b)] -[(c, d)] = [(a,b)] + (-[(c, d)])$$ Where $-[(c,d)] = [(0, 1)] \cdot [(c, d)] = [(d, c)]$ is the *opposite* of $[(c,d)]$. Which coincides  with our previous notation.

*Absolute value* of an integer $a$, $|a|$ is defined by $$|a| = \begin{cases} a & a\ge 0 \\-a & a < 0\end{cases}$$There remains an inconvenience of the integers, that division cannot always be performed.

We say that an integer $a$ is *divisible* by an integer $b$ if there exists a unique integer $x$ such that $a = b \cdot x$; this unique $x$ is called the *quotient* of $a$ and $b$. We extend this notion of division into the [[Rational Numbers|rationals]]. A consequence of asking that the number $x$, be unique we see that $a  = 0 \cdot x$ has either no solutions or many solutions, depending $a = 0$, or $a\ne 0$. The best we can hope for an extension in which for all $a$ and all $b\ne 0$ there is a unique $x$ such that $a = b\cdot x$. 

Small bit of notation, we will define $\Bbb Z^* := \Bbb Z \setminus \{0\}$ 