---
tags:
  - SetTheory
  - RealAnalysis
  - RingTheory
---

Subjects: [[Set Theory]], [[Real Analysis]], [[Ring Theory]]
Links: [[Rational Numbers]], [[Linear Orderings]], [[Operations and Structures]]

We already defined them, as the completion of the [[Rational Numbers]] using linear orderings.

**Lemma:** for every $x\in \Bbb R$ and $n \in \Bbb N^+$, there exists $r, s \in \Bbb Q$ such that $r < x \le s$ and $s-r \le 1/n$

**Def:** Let $x, y \in \Bbb R$. We let $x+y = \inf\{r+s \mid r, s \in \Bbb Q, x \le r, y \le s\}$. The symbol inside the set is the sum of the rationals. We note the the infimum always exist since it is complete linear ordering.

**Lemma:** Let $x, y, z \in \Bbb R$ 
- $x + y = y+x$
- $(x+y)+z = x+(y+z)$
- $x+0 = x$
- There exists a unique $w \in \Bbb R$ such that $x+w = 0$. We denote $w = -x$, the *opposite* of $x$
- If $x < y$ then $x +z < y+z$

We denote $\Bbb R^+ := \{x \in \Bbb R \mid x >0\}$

**Def:** Let $x, y \in \Bbb R^+$. We let $x\cdot y = \inf\{r\cdot s \mid r, s \in \Bbb Q, x \le r, y \le s\}$ 

**Lemma 1:** Let $x, y, z \in \Bbb R^+$:
- $x\cdot (y+z) = x\cdot y + x\cdot z$
- $x\cdot y = y \cdot x$ 
- $(x \cdot y) \cdot z = x \cdot (y \cdot z)$
- $x \cdot 1 = x$
- There exists a unique $w \in \Bbb R^+$ such that $x \cdot w = 1$. We denote $w = 1/x$, the *reciprocal* of $x$
- if $x < y$, then $x \cdot z < y \cdot z$

We define the absolute value for real numbers, let $x \in \Bbb R$, then $$ |x|  = \begin{cases}x  & x \ge 0 \\-x & x < 0\end{cases}$$
and notice that if $x\ne 0$, the $|x| \in \Bbb R^+$.

**Def:** Let $x, y \in \Bbb R$, we let $$x\cdot y = \begin{cases}|x|\cdot |y|& x, y >0 \lor x, y <0 \\
-(|x|\cdot|y|) & x>0, y<0 \lor x <0, y>0 \\
0 & x = 0 \lor y = 0\end{cases}$$
**Lemma 2:** Let $x, y, z\in \Bbb R$: 
- $x\cdot (y+z) = x\cdot y + x\cdot z$
- $x\cdot y = y \cdot x$ 
- $(x \cdot y) \cdot z = x \cdot (y \cdot z)$
- $x \cdot 1 = x$
- For each $x\ne 0$ there exists a unique $w \in \Bbb R$ such that $x \cdot w = 1$. We denote $w = 1/x$, the *reciprocal* of $x$
- if $x < y$, and $z>0$ then $x \cdot z < y \cdot z$

We define *division* by a nonzero real number $x$: as $y \div x= y \cdot (1/x)$ 

A structure $\mathfrak U = (A, <, +, \cdot, 0, 1)$ where $<$ is a linear ordering, $+$ and $\cdot$ are binary operations and $0, 1$ are constants such that all properties of lemma 1 and lemma 2 are satisfied is called an *ordered field* in algebra. So the contents of lemma 1 and 2, can be summarized as the real numbers are an ordered field. As the ordering of the real numbers is complete, they are a *complete ordered field*

**Th:** The structure $\mathfrak R = (\Bbb R, <, +, \cdot, 0, 1)$ is a complete ordered field. It is in fact unique up to isomorphism. If $\mathfrak U$ is also a complete ordered field, then $\frak U$ and $\frak R$ are isomorphic. 

**Th (Expansion of real numbers in base $p$)**
Let $p\ge 2$ be a natural number. For every $0\le a <1$ there is a unique sequence of natural numbers $\langle a_n\rangle_{n \in \Bbb N^+}$ such that
- $0\le a_n < p$ for every $n \in \Bbb N^+$
- There is no $n_0$ such that $a_n = p-1$ for all $n > n_0$
- $a_1/p +\cdots + a_n/p^n\le a < a_1/p +\cdots + (a_n+1)/p^n$, for each $n \ge 1$
The real number $a$ is rational iff $\langle a_n\rangle_{n \in \Bbb N^+}$ is eventually periodic

	# Using the Cauchy Sequence Completion

We can also consider them the [[Completion of a Metric Space|completion]] of the rational numbers as a metric space

If we decide to do this we have that is a complete metric space by construction, the thing we get stuck on is the order. 

Let's take $(a_n)_{n \in \Bbb N}$ and $(b_n)_{n \in \Bbb N}$ be Cauchy sequences of rational numbers, we say that $(a_n)_{n \in \Bbb N} \sim (b_n)_{n \in \Bbb N}$, iff for every $p>0$, there's $N \in \Bbb N$, such that $n \ge N$, $|a_n -b_n | < p$ (this feels like $\lim a_n - b_n = 0$). 

We would like to consider a pre-order on the set of all Cauchy sequences of rationals $C$. The preorder is as follows: we say that $(a_n)_{n \in \Bbb N} \lesssim (b_n)_{n \in \Bbb N}$ iff for every $p>0$, there's an $N \in \Bbb N$ such that $n \ge N$, $a_n -b_n < p$, and according to gpt, we consider $\limsup a_n -b_n \le 0$, which can be a bit problematic since $\Bbb Q$ is not complete.

We know that $\sim$ is an equivalence relation on $C$

Also $\lesssim$ is a preorder on $C$, and the natural equivalence relation from the preorder is actually $\sim$, so $C/\sim$, will have an order induced by the preorder. 

And we have the ordered set $C/\sim$ is a complete ordered field, inhereting a lot of these s properties from $\Bbb Q$, then $C/\sim$ is isomorphic to $\Bbb R$. 