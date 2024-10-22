---
tags:
---
Subjects: [[Finite Operator Calculus]]
Links: [[Fields]], [[Polynomial Ring]]

**Def:** By a *polynomial sequence* we shall denote a sequence of polynomials $p_i(x)$ $i \in \Bbb N$, where $p_i(x)$ is exactly of degree $i$ for all $i$. 

**Def:** A Polynomial sequence is said to be of *binomial type* if it satisfies the infinite sequence of identities $$p_n(x+y) = \sum_{k \ge 0} {n \choose k} p_k(x)p_{n-k}(y) \qquad \text{for } n \in \Bbb N$$We see that the simplest sequence of binomial type is of course $x^n$.  

The most important operators, for this theory,  are the shift operators written $E^a$, and $E^ap(x) = p(x+a)$. 

**Def:** An operator $T$ which commutes with all shift invariant operators is called a *shift-invariant operator*. In symbols, $TE^a= E^aT$, for all real $a$ in the field

We are interested in the interplay between the algebra of polynomials and $\Sigma$ the *algebra of shift-invariant operators*. All operators are assumed to be *linear*.

**Def:** We define a *delta operator*, usually denoted by the letter $Q$, as a shift-invariant operator for which $Qx$ is a nonzero constant

**Prop:** If $Q$ is a delta operator, then $Qa = 0$ for every constant $a$.  

**Prop:** If $p(x)$ is a polynomial of degree $n$ and $Q$ is a delta operator, then  $Qp(x)$ is a polynomial of degree $n-1$. 

**Def:** Let $Q$ be a delta operator. A polynomial sequence $p_n(x)$ is called the sequence of *basic polynomials* for $Q$ if:
- $p_0(x) = 1$
- $p_n( 0) = 0$, whenever $n >0$
- $Qp_n(x) = np_{n-1}(x)$
If we apply this last property $k$ times we get that $Q^k p_n(x) = n ^{\underline k} p_{n-k}(x)$ for $k < n$ and we are using the [[Falling and Rising Factorials and Pochhamer Symbols|Falling Factorials notation]]

**Prop:** Every delta operator has a unique sequence of basic polynomials

**Th:** 
- if $p_n(x)$ is a basic sequence for some delta operator $Q$, then it is a sequence of polynomials of binomial type
- If $p_n(x)$ is a sequence of polynomials of binomial type, then it is a basic sequence for some delta operator. 

# First Expansion Theorem

Let $T$ be a shift-invariant operator, and let $Q$ be a delta  operator with a basic set $p_n(x)$. Then $$ T= \sum_{k = 0}^\infty \frac{a_k}{k!}Q^k$$with $$a_k = [Tp_k(x)]_{x = 0}$$
**Th:** Let $Q$ be a delta operator, and let $\Bbb F$ be the ring of formal power series in the $t$ variable over the same field. Then there exists an isomorphism from $\Bbb F$ onto the ring $\Sigma$ of shift-invariant operators, which carries $$f(t) = \sum_{k = 0}^\infty \frac{a_k}{k!}t^k \longrightarrow \sum_{k = 0}^\infty \frac{a_k}{k!}Q^k $$
**Cor:** A shift-invariant operator $T$ is invertible iff $T1 \ne 0$. 

**Cor:** Let $P$ shift-invariant operator and $p(t)$ a formal power series, such that $P = p(Q)$. Then $P$ is a delta operator iff $p(0) = 0$ and $p'(0) \ne 0$. 

We have that every formal power series $p(t)$ such that $p(0) = 0$ and $p'(t) \ne 0$ there corresponds a unique inverse power series $p^{-1}(t)$, meaning that $p(p^{-1}(t)) = t$

**Cor:** Let $Q$ be a delta operator with basic polynomials $p_n(x)$, and let $q(D) = Q$. Let $q^{-1}(t)$ be the inverse of the formal power series. Then $$\sum_{n = 0}^\infty \frac{p_n(x)}{n!}u^n = \exp(x q^{-1}(u))$$
**Cor:** Any two shift-invariant operators commute

# Pincherle Derivative

We are going to look at non shift-invariant operator. The simples is the multiplication by $x$. We call this the *multiplication operator* denoted by $\mathbf x$. Thus $\mathbf x : p(x) \mapsto xp(x)$. 

**Def:** For any operator $T$ defined on $\Bbb F[x]$, the operator $$T' = T\mathbf x - \mathbf x T$$will be called the *Pincherle derivative* of the operator $T$. 

**Prop:** If $T$ is a shift-invariant operator, then its Pincherle derivative $$T' = T\mathbf x - \mathbf x $$is also a shift-invariant operator. 

**Def:** Let $T$ be a shift-invariante derivative, then it can be expressed in terms of $D$, that is $$T = \sum_{k = 0}^\infty \frac{a_k}{k!}D^k $$where $a_k = [Tx^k]_{x = 0}$. The the formal power series corresponding to $T$ is $$f(t) = \sum_{k = 0}^\infty \frac{a_k}{k!}t^k$$we call $f(t)$ is the *indicator* of $T$. 

**Prop:** If $T$ has a indicator $f(t)$, then its Pincherle derivative $T'$ has indicator $f'(t)$ as its indicator. 

**Prop:** $(TS)' = T'S+ TS'$

**Prop:** $Q$ is a delta operator iff $Q = DP$ for some shift-invariant operator $P$, where the inverse operator $P^{-1}$ exists. 

#### Closed Forms
If $p_n(x)$ is a sequence of basic polynomials for the delta operator $Q = DP$, then $n>0$:
- $p_n(x) = Q' P^{-n-1}x^n$ 
- $p_n(x) = P^{-n}x^n - (P^{-n})' x^{n-1}$
- $p_n(x) = x P^{-n} x^{n-1}$ 
- (Rodrigues Formula) $p_n(x) = x (Q')^{-1}p_{n-1}(x)$

**Cor:** Let $R = DS$ and $Q = DP$ be delta operators with basic polynomials $r_n(x)$ and $p_n(x)$, respectively, where $S^{-1}$ and $P^{-1}$ exists. Then:
- $p_n(x) = Q' (R')^{-1} P^{-n-1}S^{n+1}r_n(x)$, for $n \ge 0$
- $p_n(x) = x (SP^{-1})^n x^{-1} r_n(x)$, for $n \ge 1$

**Th:** Let $P$ be an invertible shift-invariant operator. Let $p_n(x)$ be a sequence of basic polynomials satisfying $$[x^{-1} p_n(x)]_{x = 0} = n [P^{-1}p_{n-1}(x)]_{x = 0}$$for all $n>0$. Then $p_n(x)$ is the sequence of basic polynomials of the delta operator $Q = DP$. 

**Cor:** Given any sequence $c_{n,1}$ $n \in \Bbb N^+$, with $c_{1,1} \ne 0$ there exists a unique sequence of basic polynomials $p_n(x)$ such that $$[x^{-1}p_n(x)]_{x = 0} = c_{n,1}$$that is $$p_n(x) = \sum_{k \ge 1} c_{n,k} x^k, \qquad n \in \Bbb N^+$$
**Cor:** Let $g(x)$ be the indicator of $Q$. Then $g = f^{-1}$, where $$f(t) = \sum_{k \ge 1} \frac{c_{k,1}}{k!}t^k$$Meaning that the sequence of basic polynomials is completely determined by the coefficients in their first power $x$. This fact can be made the starting point for a connection between the present theory and the theory of [[Compound Poisson Processes]].

This last corollary gives an explicit interpretation to the generating function of a sequence of basic polynomials, which can be now restated as $$\sum_{n = 0}^\infty \frac{p_n(x)}{n!}t^n = \exp\left(x \sum_{k = 1}^\infty \frac{c_{k, 1}}{k!}t^k\right)$$a form which makes it almost evident. 