---
tags:
  - NumberTheory/AlgebraicNumberTheory
---
Subjects: [[Ring Theory]], [[Algebraic Number Theory]]
Links: [[Inverse Limits of Abelian Groups]], [[Completion of a Metric Space]]

# Constructions

**Algebraic Construction:** Let $p$ be a prime, $I = \Bbb N^+$, let $A_i := \Bbb Z/p^i\Bbb Z$, and let $\mu_{ji}$ be the natural projection maps: $$\mu_{ji}: a \pmod{p^j} \mapsto a \pmod{p^i}.$$The inverse limit $\varprojlim \Bbb Z/p^i\Bbb Z$ is called the ring of *$p$-adic integers*, and is denoted by $\Bbb Z_p$. 

### Analytic Construction

**Def:** For any integer $a$, we can write $a = p^n r$ where $p$ and $r$ are relatively prime. The $p$-adic valuation of $a$ is $\nu_p(a) := n$, and the $p$-adic absolute value is $$|a|_p := p^{-\nu_p(a)} = p^{-n}.$$

**Lemma:** For all integers $a, b$ the following are true,
- $\nu_p(a+b) \le \max\{\nu_p(a), \nu_p(b)\}$
- $\nu_p(ab) = \nu_p(a) \nu_p(b)$. 
- $|a+b|_p \le \max\{|a|_p, |b|_p\}$
- $|ab|_p = |a|_p|b|_p$.

**Def:** the ring $\Bbb Z_p$ is the completion of $\Bbb Z$ with respect to the $p$-adic norm. That is, $\Bbb Z_p$ is the set of all equivalence classes of Cauchy sequences $(a_n)$ where $(a_n)$ and $(b_n)$ are equivalent iff $\lim_{n\to \infty}|a_n-b_n|_p = 0$. 

Let $(a_n)$ and $(b_n)$ be representatives in two equivalence classes. We define $(a_n)+(b_n)$ to be $(a_n + b_n)$. We see that $(a_n+ b_n)$ is also a Cauchy sequence, and we can check that addition doesn't depend on representatives. 

Le us define the multiplication $(a_n) \cdot (b_n) = (a_n \cdot b_n)$. We know that it is well defined. 

**Obs:** the integers are contained in the $p$-adic integers. For any integer $n$, we can consider the the Cauchy sequence $(a_m)$ where for each $a_m = n$. so $\Bbb Z \hookrightarrow \Bbb Z_p$. This fact imlpies that an equation can only have a solution in $\Bbb Z$ if it has a solution in $\Bbb Z_p$. Secondly, the $p$-adic norm can be uniquely extended to $\Bbb Z_p$. If $(a_n)$ is a sequence in $\Bbb Z_p$, then we can define $$|(a_n)| := \lim_{n \to\infty}|a_n|_p.$$We know that $|a_n|_p$ must have a limit, as $(a_n)$ is a Cauchy sequence with respect to this absolute value. 

### Power Series Construction

Every element of $\Bbb Z_p$ may be written uniquely as an infinite formal sum $$\sum_{k = 0}^\infty b_k p^k$$ with each $b_k \in\{0,\dots, p-1\}$. 

The disadvantage of this definition of the $p$-adic integers is that defining addition and multiplication is difficult. It is possible to do so, but because we must deal with 'carrying' when a digit is greater than $p-1$, it involves more complicated construction than those for $\Bbb Z/p\Bbb Z[[x]]$. 

For example, if $\alpha = a_0 + a_1p + a_2p^2+\cdots$ and $\beta = b_0 + b_1p + b_2p^2+\cdots$, and $\alpha + \beta = \gamma = c_0 + c_1+c_2p^2+\cdots$, then $c_0 = a_0 + b_0 \pmod p$. To find $c_1$, we have to solve $c_0 + c_1p = a_0 + b_0 + a_1p +b_1 p \pmod{p^2}$. Multiplication has a similar flavour, if $\alpha \cdot \beta = \mu = v_0 + v_1 p + v_2p^2+\cdots$, then $v_0 = a_0 b_0\pmod p$. To find the subsequent terms, we have to consider previous terms. to find $v_1$, we must solve $v_0 + v_1p = (a_0+a_1p)(b_0+b_1p)\pmod{p^2}$. 

In truth, we are just using the properties of the inverse limit definitions, to return it to the formal series definition. 

# Properties

**Prop:** All of the constructions above are equivalent. 

Note that the cardinality of $\Bbb Z_p$ is the same as $\Bbb R$. 

**Prop:** $\Bbb Z_p$ is an integral domain, and $\Bbb Z\hookrightarrow \Bbb Z_p$. 

**Prop:** $\sum_{k = 0}^\infty b_kp^k$ is a unit in $\Bbb Z_p$ iff $b_0\neq 0$. 

**Prop:** Every ideal of  is of the form $p^n \Bbb Z_p$ for some integer $n \ge 0$. In particular,  is a [[Principal Ideal Domain]], and  is a [[Maximal Ideals|local ring]] because it has a unique maximal ideal $p\Bbb Z_p$. 

We can consider the the field of fractions of $\Bbb Z_p$, this would be $\Bbb Q_p$ which are the [[p-adic Numbers]].
