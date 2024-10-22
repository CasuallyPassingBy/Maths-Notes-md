---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Well-Orderings]], [[Natural Numbers]]
**Def:** A set $T$ is _**transitive**_ if every element of $T$ is a subset of $T$. In other words, a transitive set has the property that $u \in v \in T$ implies $u \in T$

**Def:** A set $\alpha$ is an _**************ordinal number**************_ if:

- $\alpha$ is transitive
- $\alpha$ is well-ordered by $\in_\alpha$

********Th:******** Every natural number is an ordinal

We defined the operation $S(x) = x\cup\{x\}$ and introduced the natural number as elements of the smallest set containing $0$ and closed under $S$. Then we have the quirk that ${n = \{ m \in \Bbb N \mid m < n\}}$. We define $\omega$ to be _********************************************the least transfinite number********************************************_, to be set $\Bbb N$ of all natural numbers $\omega = \Bbb N$

Then we can continue this process having
$$ S(\omega) = \{0, 1, \dots, \omega\}\\ S(S(\omega)) = \{0, 1, \dots, \omega, S(\omega)\} $$

We use some suggestive notation of $S(\omega) = \omega+1$, and $S(S(\omega)) = \omega+2$

In this fashion we can continue till
$$ \omega\cdot2 = \omega + \omega = \{0, 1, \dots, \omega, \omega+1, \omega+2, \dots\} $$

We can continue to push it further and get o

$$ \omega \cdot \omega = \{0, 1 \dots, \omega, \omega+1, \dots, \omega\cdot2, \dots, \omega\cdot3,\dots, \omega\cdot4,\dots\} $$

**************Lemma:************** If $\alpha$ is an ordinal number, then $S(\alpha )$ is also an ordinal number

********Th:******** Let $\alpha$, $\beta$ and $\gamma$ be ordinal numbers
- if $\alpha < \beta$ and $\beta< \gamma$ , then $\alpha < \gamma$
- $\alpha < \beta$ and $\beta < \alpha$ cannot both hold
- either $\alpha < \beta$, $\alpha = \beta$ or $\alpha > \beta$ holds
- every nonempty set of ordinal numbers has a $<$-least element. Consequently, ever set of ordinal numbers is well-ordered by $<$
- For every set of ordinal number $X$, there is an ordinal number $\alpha \not\in X$. (In other words, “the set of all ordinal numbers” doesn’t exist)

**************Lemma:************** If $\alpha$ is an ordinal number $\alpha \not \in \alpha$

**Lemma:** Every element of an ordinal number is an ordinal number

**************Lemma:************** If $\alpha$ and $\beta$ are ordinal numbers such that $\alpha \subseteq \beta$, then $\alpha \in \beta$

********Th:******** The natural numbers are exactly the finite ordinal numbers. This is tell us that the ordinal numbers are a generalization of the natural numbers

**Def:** An ordinal number $\alpha$ that isn’t the successor of another ordinal is called a _**limit ordinal.**_ In this case if $\alpha$ does’t have a greatest element, and $\alpha = \sup\{ \beta \mid \beta < \alpha\}$.

**Obs:** Let $X$ be a set of ordinal numbers, then we can get $\sup X$, by just taking $\bigcup X$. Then ${\sup X = \bigcup X}$. Similarly, we get that $\inf X = \bigcap X$. If $X$ doesn’t have greatest element, then $\sup X$ is a limit ordinal

********Th:******** Every well-ordered set is isomorphic to a unique ordinal number

**Def:** If $W$ is a well-ordered set, then the _**order type_** of $W$ is the unique ordinal number isomorphic to $W$

---

# Transfinite Induction and Recursion

### The Transfinite Induction Principle

Let $P(x)$ be a property (possibly with parameters). Assume that, for all ordinal numbers $\alpha$

$$ \text{if }P(\beta) \text{ holds for all }\beta < \alpha, \text{ then }P(\alpha) $$

Then $P(\alpha)$ holds for all ordinals $\alpha$

### The Transfinite Induction Principle V.2.

Let $P(x)$ be a propety. Assume that

- $P(0)$ holds
- $P(\alpha)$ implies $P(\alpha +1)$ holds for all ordinals $\alpha$
- For all limit ordinals $\alpha \ne 0$, if $P(\beta)$ holds for all $\beta < \alpha$, then $P(\alpha)$ holds.

Then $P(\alpha)$ holds for all ordinals $\alpha$

**Th:** Let $\Omega$ be an ordinal number, $A$ a set, and $S = \bigcup_{\alpha < \Omega}A^\alpha$ the set of all transfinite sequences of elements of $A$ of length less than $\Omega$. Let $g:S\to A$ be a function. Then there exists a unique function $f: \Omega\to A$ such that

$$ f(\alpha) =g(f|_\alpha) \quad \text{for all }\alpha <\Omega $$

### The Transfinite Recursion Theorem
Let $G$ be an operation: then the property $P(x,y)$ such that

- $x$ is an ordinal number and $y = t(x)$ for some computation $t$ of lenght $x$ based on $G$
- or, $x$ is not an ordinal number and $y = \varnothing$

defines an operation $F$ such that $F(\alpha) = G(F|_\alpha)$

We call $t$ a computation of length $\alpha$ based on $G$ if $t$ is a function, $\operatorname{dom} t= \alpha +1$ and for all ${\beta \le \alpha}$, $t(\beta) = G(t|_\beta)$

### The Transfinite Recursion Theorem, Parametric Version

Let $G$ be an operation. The property $Q$ such that

- $x$ is an ordinal number and $y = t(x)$ for some computation $t$ of lenght $x$ based on $G$ and $z$
- or, $x$ is not an ordinal number and $y = \varnothing$

defines an operation $F$ such that $F(z, \alpha) = G(z , F_z|_\alpha)$ for all ordinals $\alpha$ and all sets in $z$.

We call a $t$ a computation of legnth $\alpha$ based on $G$ and $z$ if $t$ is a function $\operatorname{dom} t= \alpha +1$, and for all $\beta \le \alpha$, $t(\beta)= G(z, t|_\beta)$

********Th:******** Let $G_1, G_2$ and $G_3$ be opertions, and let $G$ be the operation defined $G(x) = y$ iff either

- $x = \varnothing$ and $y = G_1(\varnothing)$, or
- $x$ is a function, $\operatorname{dom} x = \alpha +1$ for an ordinal $\alpha$ and $y = G(x(\alpha))$, or
- $x$ is a function, $\operatorname{dom} x= \alpha$ for a limit ordinal $\alpha \ne 0$ and $y = G_3(x)$, or
- $x$ is none of the above and $y = \varnothing$

Then the property $P(x,y)$ defined as

- $x$ is an ordinal number and $y = t(x)$ for some computation $t$ of lenght $x$ based on $G$
- or, $x$ is not an ordinal number and $y = \varnothing$

defines the operation $F$ such that

$$ \begin{align*} F(0) &= G_1(\varnothing) \\ F(\alpha+1) &= G_2(F(\alpha) \quad\text{for all } \alpha \\ F(\alpha)) &= G_3(F |_\alpha) \quad\text{for all limite } \alpha \ne 0 \end{align*} $$

### Double Transfinite Recursion Theorem
Let $G$ be an operation in two variables. Then there’s an operation $F$ such that ${F(\beta, \alpha) =G(F|_{\beta\times \alpha})}$ for all ordinals $\beta$ and $\alpha$. The computations are functions of ${(\beta+1) \times (\alpha+1)}$

An application of The Transfinite Recursion, parametric version is that: there’s a binary operation $F$such that

- $F(x,1) =0$ for all $x$
- $F(x, n+1) = 0$ iff there’s $y$ and $z$ such that $x = (y,z)$ and $F(y, n) = 0$

We say that $x$ is an $n$-tuple (where $n \in \omega$ and $n >0$) if $F(x, n) =0$. This definition of $n$-tuples coincides with the naïve approach of defining them as

- $(a_0) = a_0$
- $(a_0, a_1, \dots, a_n) =((a_0, a_1, \dots, a_{n-1}), a_n)$