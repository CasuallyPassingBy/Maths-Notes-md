---
tags:
---
Subjects: [[Finite Operator Calculus]]
Links: [[Delta Operators]]

**Def:** A polynomial sequence $s_n(x)$ is called a *Sheffer set* or a set *Sheffer polynomials for the delta operator* $Q$ if
- $s_0(x) = c \ne 0$
- $Qs_n(x) = ns_{n-1}(x)$

A Sheffer set if r the delta operator $Q$ is related to the set of basic polynomials of $Q$ by the following

**Prop:** Let $Q$ be delta operator with basic polynomial set $q_n(x)$. Then $s_n(x)$ is a Sheffer set relative to $Q$ iff there exists an invertible shift invariant operator $S$ such that $$s_n(x) = S^{-1}q_n(x)$$
# Second Expansion Theorem
Let $Q$ be a delta operator with basic polynomials $q_n(x)$, let $S$ be an invertible shift-invariant operator with Sheffer set $s_n(x)$. If $T$ is any shift invariant, and $p(x)$ is any polynomials the following identity holds for all values of the parameter $y$ : $$T p(x+y) = \sum_{n = 0}^\infty \frac{s_n(y)}{n!}Q^nST p(x)$$
**Cor:** If $s_n(x)$ is a Sheffer set relative to the invertible shift invariant operator $S$ and the delta operator $Q$, then $$S^{-1} = \sum_{n = 0}^\infty \frac{s_n(0)}{n!} Q^n$$
**Prop:** Let $Q$ be a delta operator with basic polynomials $q_n(x)$, and let $s_n(x)$ be a Sheffer set relative to $Q$ and some invertible shift-invariant operator $S$. Then the following identity holds $$s_n(x+y) = \sum_{k = 0}^n {n \choose k} s_k(x) q_{n-k}(y)$$
**Cor:** Let $Q$ be a delta operator with basic polynomials $q_n(x)$, and let $s_n(x)$ be a Sheffer set relative to $Q$ and some invertible shift-invariant operator $S$. Then $$s_n(x) = \sum_{k = 0}^\infty {n \choose k} s_k(0) q_{n-k}(x)$$Then the $s_n(0)$ are completely determined by their constant terms

**Prop:** Let $T$ be an invertible shift invariant operator, let $Q$ be a delta operator, and let $s_n(x)$ be a polynomial sequence. Suppose that $$E^af(x) = \sum_{n  = 0}^\infty \frac{s_n(a)}{n!}Q^nT f(x)$$for all polynomial $f(x)$ and all constants $a$. Then the set $s_n(x)$ is the Sheffer set of the operator $T$ relative to the delta operator $Q$. 

We get a simpler proof of the [[Delta Operators#Closed Forms|Rodrigues Formula]] 

**Prop:** Let $Q$ be delta operator, and let $S$ be invertible shift invariant operator. Let $s(t)$ and $q(t)$ be the indicators of $S$ and $Q$, and let $q^{-1}(t)$ be the formal power series to $q(t)$. Then the generating function for the sequence $s_n(x)$ is given by $$\frac1{s(q^{-1}(t))} e^{xq^{-1}(t)} = \sum_{n = 0}^\infty \frac{s_n(x)}{n!}t^n $$
**Prop:** A sequence $s_n(x)$ is a Sheffer set relative to a basic set $q_n(x)$ iff $$s_n(x+y)= \sum_{k = 0}^n {n \choose k} s_k(x) q_{n-k}(y)$$
# Recurrence Formulas

**Prop:** Let $p_n(x)$ be a polynomial sequence with $p_0(x)$, If $p_n(x)$ is a Sheffer et then for every delta operator $A$ there exists a sequence of constants $s_n$ such that $$Ap_n(x)= \sum_{n= 0}^\infty {n \choose k} p_k(x)s_{n-k}$$Also, it this holds for some delta operator $A$ and some sequence $s_n$, then $p_n(x)$ if a Sheffer set. 