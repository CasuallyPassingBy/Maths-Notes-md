---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Formal Power Series Ring of a Single Variable]], [[Polynomial Ring of a Single Variable]]

# Construction

Let us consider the abelian group $$R' := \{f: \Bbb Z\to R \mid f(n) \neq 0 \text{ for $n \in \Bbb Z^-$ is finite}\}. $$
This is the set of functions from $\Bbb Z$ to $R$. We would like to give this group a multiplication that is inspired by the multiplication on $R$. To do this, let $(a_n)_{n \in \Bbb Z}, (b_n)_{n \in \Bbb Z} \in R'$, $$(a_n)_{n \in \Bbb Z} * (b_n)_{n \in \Bbb Z} := \left(\sum_{k\in \Bbb Z} a_k b_{n-k}\right)_{n \in \Bbb Z}.$$

This operation is the *discrete convolution* of the two sequences. We can check that is associative and distributes over the sum. This means that $R'$ is a ring. Just a couple of things we should keep in mind. If $R$ is commutative, then it is easy to check that so is $R'$. Lastly, if $R$ is unital, then $R'$ is also unital with the multiplicative identity being $$(\dots,0, 0, 1, 0, 0 \dots).$$
We usually don't write $R'$. The usual notation is $R[[x]]$, and we write the element $(a_n)_{n \in \Bbb N}\in R'$ as $$\sum_{n = N}^\infty a_n x^n,$$where $N$ is some integer and $x$ is treated as a formal object. The elements of $R((x))$ are called *formal Laurent series*. We call $R((x))$ the *ring of formal Laurent series in the variable $x$ with coefficients in $R.$* 

# Properties

**Prop:** If $F$ is a field, then $F((x))$ is field.

**Prop:** If $F$ is a field, then the field of fractions of $F[[x]]$ is the ring $F((x))$ of formal Laurent series. 

**Def:** We define the map $\nu: F((x))^\times \to \Bbb Z$ by $$\sum_{n = N}^\infty a_n x^n\mapsto N,$$where $a_N$ is the first nonzero coefficient of the series. 

**Obs:** We see that $\nu$ is a discrete valuation on $F((x))$ whose discrete ring is $F[[x]]$, the formal power series ring. 