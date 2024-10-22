---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Functions]], [[Groups]], [[Subgroups]], [[Integer Partition]], [[Alternating Groups]], [[Commutator Subgroup]]

**Def:** If $X$ is a nonempty set, then a bijective map from $X$ to $X$ is called a *permutation* of $X$. Meaning that $f\in \text{Sym}(X)$ is a permutation, where $\text{Sym}(X)$ represents the set of all bijective maps from $X$ to $X$. 

From the definitions of bijective functions we see that:
- $\text{Id}_X$ behaves like an identity under $\circ$
- $\circ$ is associative
- every $f\in \text{Sym}(X)$ has an inverse

**Prop:** $(S_X, \circ)$ is a group

**Def:** $(S_X, \circ)$ is called the *symmetric group on* $X$. If $X$ is a finite set, $|X| = n$, then we just write $S_n$ instead of $S_X$, and is called the *symmetric group of order* $n$, and it has order $n!$. 

Let $f\in S_n$. Then we can represent $f$ as $$\begin{pmatrix}1 &2 &  3 & \cdots& n \\
f(1) &f(2) &  f(3) & \cdots& f(n)\end{pmatrix}$$where $f(k)$ is placed under $k$ for each between $1$ and $n$.

Let $x_1, x_2, \dots, x_r$, $1\le r\le n$, be $r$ distinct elements of $\{1, 2, \dots, n\}$. The $r$*-cycle* $(x_1, x_2, \dots, x_r)$ is the element of $S_n$ that maps $x_1\to x_2\to x_3 \to \cdots \to x_r \to x_1$, and leaves all elements of $\{1, 2, \dots, n\}$ other than $x_1, x_2, \dots, x_r$ fixed. A $2$-cycle, is called a *transposition*. 

Two cycles $(x_1, x_2, \dots, x_r)$ and $(y_1, y_2, \dots, y_s)$ in $S_n$ are called *disjoint*, with $s, r\ge 2$, if $$\{x_1, x_2, \dots, x_r\} \cap \{y_1, y_2, \dots, y_s\} = \varnothing$$
We can also see that disjoint cycles commute

**Def:** Let $\sigma \in S_n$ be permutation. for an element $x \in \{1, \dots, n\}$ the set $$\mathcal O_\sigma(x) := \{\sigma^k(x) \mid k \in \Bbb Z\}$$is called the *orbit of $x$ under $\sigma$.*

**Prop:** Let $\sigma \in S_n$ a permutation. Then:
- $x \in \mathcal O_\sigma(x)$, therefore the orbits are nonempty
- The orbits are disjoint, meaning that if $\mathcal O_\sigma(x) \cap\mathcal O_\sigma(z) \ne \varnothing$, then $\mathcal O_\sigma(x) = \mathcal O_\sigma(z)$
- The union of orbits is $\{1, \dots, n\}$

**Prop:** If $\sigma \in S_n$ and $x\in \{1, \dots, n\}$, then the restriction $\sigma|_{\mathcal O_\sigma(x)}$ is a cycle of the length of the cardinality of $\mathcal O_\sigma(x)$

**Def**: We say that permutations $\sigma$ and $\tau$ are disjoint if for each $x\in \{1, \dots, n\}$ we have that $\sigma(x) \ne x$, then $\tau(x) = x$, and if $\tau(x) \ne x$ then $\sigma(x) = x$. 

**Prop:** If $\sigma$ and $\tau$ are disjoint permutations then $\sigma \tau = \tau \sigma$. 

**Th:** Let $\sigma \in S_n$. Then there exists disjoint cycles $\sigma_1, \sigma_2, \dots, \sigma_m$ in $S_n$ such that $\sigma = \sigma_1 \circ \sigma_2 \circ \cdots \circ\sigma_m$

**Th:** If $n \ge 2$, then any cycle in $S_n$ can be written as a product of transpositions, and it is given by $$(x_1, x_2, \dots, x_r) = (x_1, x_r) \circ (x_1, x_{r-1}) \circ \cdots \circ (x_1, x_3) \circ (x_1, x_2)$$
**Cor:** If $n \ge 2$, the any element of $S_n$ can be written as a product of transpositions

**Def:** A permutation is *even* if it can be written as a product of an even number of transpositions. It is *odd* if it can be written as the product of an odd number of transpositions. 

**Th:** No permutation is both even and odd

**Def:** With this we can define the *sign* of a permutation $\sigma \in S_n$ that can be expressed as $\sigma = \tau_1 \circ \cdots \circ \tau_r$ as a product of transpositions, as $\text{sgn}(\sigma) = (-1)^r$ since a permutation cannot be odd and even then the function is well defined. 

**Prop:** If $\sigma\in S_n$, the number of transpositions that appear in any factorisation of $\sigma$ is always even or always odd

**Cor:** If $\sigma, \tau \in S_n$, then $\text{sgn}(\sigma\tau) = \text{sgn}(\sigma)\text{sgn}(\tau)$, and $\text{sgn}(\sigma^{-1}) = \text{sgn}(\sigma)$. This is group homomorphism $\text{sgn}: S_n \to \{-1, 1\}$, and $\ker(\text{sgn}) = A_n$

**Prop:** We see that that for any $n \in  \Bbb N^+$, $$[A_n, A_n] \le [S_n, S_n] \le A_n]$$
- for $n \ge 3$, then $[S_n, S_n] = A_n$
- for $n \ge 5$, then $[A_n, A_n] = A_n$, meaning that $A_n$ is perfect. 
### Conjugacy Classes

Given $\sigma, \tau \in S_n$, if there exists $\theta \in S_n$ such that $\sigma = \theta \tau \theta^{-1}$, we say that $\sigma$ is a *conjugate* of $\tau$, and this is an equivalence relation on $S_n$ which equivalence classes are called *conjugacy classes* of $S_n$. 

**Lemma:** Let $c = (x_1, x_2, \dots, x_r) \in S_n$ be an $r$-cycle. Then, for every $\sigma \in S_n$ the element $\sigma c\sigma^{-1}$ is also an $r$-cycle and is of the form: $$\sigma c \sigma^{-1} = (\sigma(x_1), \sigma(x_2), \dots, \sigma(x_r))$$
**Prop:** Let $\alpha, \beta \in S_n$ and suppose that $\beta$ has the following decomposition by cycles: $$\beta = (x_1, \dots, x_k)(y_1, \dots, y_\ell)\cdots(z_1, \dots, z_m)$$Then, $\alpha \beta\alpha^{-1}$ has the same cycle structure as $\beta$ and it is obtained $\alpha$ to the symbols on each cycle of $\beta$, meaning $$\alpha\beta\alpha^{-1} = (\alpha(x_1), \dots, \alpha(x_k))(\alpha(y_1), \dots, \alpha(y_\ell))\cdots(\alpha(z_1), \dots, \alpha(z_m))$$
**Th:** Two permutations $\alpha, \beta\in S_n$ has the same cycle structure iff they are conjugated. 

**Prop:** The number of distinct $k$-cycles in $S_n$ is $n^{\underline k}/k$ 

#### Number of cyclic structures
Let $c_i\ge 0$ integers, for $1 \le i \le k \le n$. Let $\sigma \in S_n$ we say it of the type $(c_1, \dots, c_k)$ if the factorisation of $\sigma$ of cycles of has $c_1$ $1$-cycles, $c_2$ $2$-cycles, $\dots$, $c_k$ $k$-cycles. 

We can say that $c_j = 0$ if there are no $j$-cycles on $\sigma$, then get the following equation: $$\sum_{k = 1}^n k\cdot c_k = n$$Now, we define some auxiliary variables: $$\mu_i := \sum_{k = i}^n c_k$$then $\mu_1 \ge \mu_2 \ge \cdots\ge \mu_n \ge 0$, and we get that $$\sum_{k = 1}^n \mu_k = n$$the numbers $\mu_k \ge 0$ form a *partition* of the integer $n$. 

**Prop:** The number of distinct permutation types on $S_n$ is equal to the number of partitions of the number $n$. 

**Cauchy Formula Again:** The number of distinct permutations of type $(c_1, \dots, x_n)$ is $$n! \prod_{k = 1}^n (k^{c_k} c_k!)^{-1}$$
**Prop:** For $n \ge 2$, the symmetric group $S_n$ is generated is generated by the cycles $(1, 2, \dots, n)$ and $(1,2)$. 

**Cor:** For each $n \ge 2$, the symmetric group $S_n$ is generated by the transpositions of the form $(1, i)$ for $i \ge 2$. 

**Cor:** For each $n \ge 2$, the symmetric group $S_n$ is generated by the transpositions of the form $(i, i+1)$ for $1 \le i \le n-1$. 