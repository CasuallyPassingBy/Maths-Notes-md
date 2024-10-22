---
tags:
  - "#NumberTheory"
---
Subjects: [[Elementary Number Theory]]
## Greatest Common Divisor
For any $a, b \in \Bbb Z$, we say that $a$ _divides $b$,_ denoted as $a \mid b$ iff ${\exists k \in \Bbb Z[ak = b]}$, in addition we can use the notation $a^m\parallel b$ to refer that $m$ is the highest power of $a$ that divides $b$, or $a ^m \mid b$ but $a^{m+1} \nmid b$ .

This relation satisfies a few things:

- $\forall a \in \Bbb Z[a \mid a]$, reflexivity
- $\forall a, b,c \in \Bbb Z[(a\mid b \land b\mid c) \implies a \mid c)$, transitivity
- $\forall a, b \in \Bbb Z[(a \mid b \land b \mid a) \implies |a| = |b|]$, almost reflexivity

This makes $(\Bbb Z, \mid )$ a pre-ordered set, but if we try to quotient to get a proper ordered set we get that $(\Bbb Z/\sim, \mid ) \cong (\Bbb N,\mid)$, then we can infer that $\Bbb N$ under $\mid$ is an ordered set

## Properties
Given $a, b,c,d ,x,y \in \Bbb Z$:
- $d \mid a \land d \mid b \implies d \mid ax+by$
- $d\mid a \implies dx \mid ax$
- $d \mid a \implies \frac{a}{d} \mid a$
- $a \mid b \implies |a| \le |b|$
- $a \mid b \land c\mid d \implies ac \mid bd$
- $a \mid 1 \implies |a| = 1$

A common divisor of $a, b$ is a number $c$ such that $c \mid a \land c\mid b$.

### GCD
The greatest common divisor $d$ of $a, b\in \Bbb Z^*$, usually denoted as $d = \gcd(a,b)$, is the number satisfying all of these properties:

- $d > 0$
- $d \mid a \land d\mid b$
- if $c \mid a \land c \mid b$, then $c \le d$

Two numbers $a, b$ are called _coprime_ iff $\gcd(a,b) = 1$

### Bezout’s Identity
Given $a, b \in \Bbb Z^*$, then there exist $x, y \in \Bbb Z$ such that $\gcd(a,b) = ax +by$ , and for any ${x,y \in \Bbb Z}$ the numbers of the form $ax +by$ are multiples of $\gcd(a,b)$

_Corollary:_ Given two numbers $a ,b\in \Bbb Z$, and there are $x,y \in \Bbb Z$ such that $ax+by = 1$, iff ${\gcd(a,b) =1}$

### Positive Preorder Supremum
Let $a, b\in \Bbb Z^*$, then $d = \gcd(a,b)$ iff:
- $d > 0$
- $d \mid a \land d \mid b$
- if $c \mid a \land c \mid b$, then $c \mid d$

### Properties
- $\gcd(a,b) = \gcd(a,c) = 1 \implies \gcd(a,bc) = 1$
- $\gcd(a, b) = \gcd(a, b+an)$, for any $n \in \Bbb Z$
- $\gcd(a, b) = d$, iff $\gcd\left(\frac{a}{d}, \frac{b}{d}\right)= 1$
- $a \mid c \land b\mid c \land \gcd(a,b) = 1$, then $ab\mid c$.
- $\gcd(a^n-1, a^m-1) = a^{\gcd(n,m)}-1$
- $\gcd(a, a+n) \mid n$, then $\gcd(a, a+1) = 1$
- Let $k \ne 0$, then $\gcd(ka, kb) = |k|\gcd(a,b)$

The greatest common divisor of more than two integers can be defined as ${\gcd(a_i)_{i = 1}^n = \gcd( \gcd(a_i)_{i = 1}^{n-1}, a_n)}$

### Euclid’s Lemma
if $a\mid bc$ and $\gcd(a,b) =1$, then $a \mid c$

along with the [[Lowest Common Multiple]], we can create a lattice:

### Lattice Properties

- Commutativity
    $\gcd(a,b) = \gcd(b,a)$
    $\operatorname{lcm}(a,b) = \operatorname{lcm}(b,a)$
    
- Associativity
    $\gcd(a,\gcd(b,c)) = \gcd(\gcd(a,b),c)$
    $\operatorname{lcm}(a,\operatorname{lcm}(b,c)) = \operatorname{lcm}(\operatorname{lcm}(a,b),c)$
    
- Absorption Laws
    $\operatorname{lcm}(a\gcd(a,b))= a$
    $\gcd(a, \operatorname{lcm}(a,b))= a$
    
- Idempotent Laws
    $a = \operatorname{lcm}(a,a)$
    $a = \gcd(a,a)$
    
- Preorder through operations
    $a \mid b \iff a = \gcd(a,b)$
    $a \mid b \iff b = \operatorname{lcm}(a,b)$
    
- Distributive Properties
    $\gcd(a, \operatorname{lcm}(b,c))= \operatorname{lcm}(\gcd(a,b), \gcd(a,c))$
    $\operatorname{lcm}(a,\gcd(b,c))= \gcd(\operatorname{lcm}(a,b), \operatorname{lcm}(a,c))$
    