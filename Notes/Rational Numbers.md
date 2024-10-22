---
tags:
  - SetTheory
  - NumberTheory
  - RingTheory
---
Subjects: [[Set Theory]], [[Elementary Number Theory]], [[Ring Theory]]
Links: [[Integer Numbers]]

We would like to construct the rationals as the next logical step in the construction of mathematics.

As we did with the [[Integer Numbers]], the idea is to make an arithmetic operation that is only partially defined in the integers, quotient, into a total operation, and belongs more properly in the realm of algebra than set set theory. 

as we can see while defining the quotient, for $a/b$ to be well defined there must be a unique $x$, such that $a = b\cdot x$. A lot of problems arise if we consider where $b = 0$, we get that the equation $a = 0 \cdot x$ has zero solutions or many depending on $a$. So we exclude $b =0$, from the extension.  As we did we would like that $$\frac{a}{b} = \frac{c}{d}$$
but this might not be well defined, and as we did we will consider that $(a,b) \approx (c, d)$ iff $ad = bc$. 

Let $Q = \Bbb Z \times \Bbb Z^*$, and we will consider the $\approx$ relation on $Q$. Let $\Bbb Q := Q/\approx$ be the set of equivalence classes of $Q$ modulo $\approx$. The elements of $\Bbb Q$ are called *rational numbers*; the rational number represented by $a/b$ is denoted as $[a/b]$ 

There's an obvious injective mapping $i: \Bbb Z \to \Bbb Q$, $$i(a) = \left[\frac{a}{1}\right]$$ We now define addition and multiplication of integers as $$ \left[\frac{a}{b}\right] + \left[\frac{c}{d}\right] = \left[\frac{a\cdot b + b\cdot c}{b\cdot d}\right]$$ $$\left[\frac{a}{b}\right] \cdot \left[\frac{c}{d}\right] = \left[\frac{a \cdot c}{b\cdot d}\right]$$ In order to lay the foundations satisfactorily, we proved the following:
- Addition and multiplication of rational are well defined, independent of of choice of representatives
- For integers, the new definitions agree with the old ones, and $i$ is ring homomorphism.
- Addition and multiplication of rationals satisfy the usual laws of algebra
- If $A, B \in \Bbb Q$, and $B \ne [0/1]$, then the equation $A = B\cdot X$ has a unique solution $X\in \Bbb Q$. Thus *division* of rational numbers is defined, as long as the divisor is not zero; we denote this operation $\div$: $X = A \div B$, or more commonly $X = A/B$.

We want to extend to the order of the integers into the rationals. We define the natural ordering of the rationals as $$\left[\frac{a}{b}\right] < \left[\frac{c}{d}\right] \qquad \iff \qquad a\cdot d < b \cdot c \quad\land \quad b, d >0$$
This doesn't depend on the choice of representatives as long as $b, d>0$, that $<$ is a linear ordering, that for $a, b \in \Bbb Z$, and $a<b$, iff $i(a) < i(b)$, and the usual algebraic laws. 

The set $\Bbb Q$ is countable

**Th:** $(\Bbb Q, <)$ is a dense linearly ordered set and has no endpoints. In fact, for every $r \in \Bbb Q$ there exists $n \in \Bbb N$ such that $r< n$.

**Cor:** If $r \in \Bbb Q$ and $r>0$, then there exists $n \in \Bbb N^+$ such that $0< 1/n <r$. 

**Lemma:** Given a rational number $r$, there is a unique integer $e$ such that $e \le r <e+1$. We call $e$ the integer part of $r$, $e = \lfloor r \rfloor$ 

The expansion of integers in base $p$ is well known, and explored in [[Different Basis Representation]]. By the lemma above, we see that $r = \lfloor r\rfloor +q$, with $q \in \Bbb Q$ and $0 \le q < 1$.  We concentrate on the expansion of $q$. 

We construct a sequence of *digits* $0, 1, \dots, p-1$ by recursion, as follows: 
- Find $a_1 \in \{0, \dots, p-1\}$ such that such that $a_1/p \le q < (a_1 +1)/p$, let $a_1 = \lfloor p \cdot q\rfloor$
- Then find $a_2 \in \{0, \dots, p-1\}$ such that $a_1/p + a_2/p² \le q < a_1/p +(a_2 +1)/p²$. Let $a_2 = \lfloor(q - a_1/p)\cdot p²\rfloor$
- In general find $a_k \in \{0, \dots, p-1\}$ such that $$ \frac{a_1}{p}+ \frac{a_2}{p^2} + \cdots + \frac{a_k}{p^k} \le q < \frac{a_1}{p}+ \frac{a_2}{p^2} + \cdots + \frac{a_k+1}{p^k}$$ We take $$a_k = \left\lfloor\left(q-\frac{a_1}{p}- \frac{a_2}{p^2} - \cdots + \frac{a_{k-1}}{p^{k-1}}\right)\cdot p^k\right\rfloor$$
We call the sequence $\langle a_n \mid n \in \Bbb N\rangle$ the *expansion of* $q$ *in base* $p$. When $p = 10$, it is customary to write $q=0.a_1 a_2 a_3 \dots$ 

One can show that
- There's is no $i$ such that for all $j \ge i$, $a_j = p-1$
- There exists $n_0 \in \Bbb N$ and $l >0$ such that $a_{n+l} = a_n$ for all $n \ge n_0$. The expansion is *eventually periodic*, with *period* $l$.

Moreover if $q = a/b$, then we can find a period $l$ such that $l \le |b|$. Conversely, each sequence $\langle a_n \mid n \in \Bbb N\rangle$ with both properties as above is an expansion of some rational number $q$, with $0 \le q <1$. 