---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Groups]]

**Def:** 
1. A ring $(R, +, \times, 0)$ is a set together with two binary operations $+$ and $\times$ (called *addition* and *multiplication*) satisfying the following axioms:
	- $(R, +, 0)$ is an abelian group.
	- $\times$ is associative.
	- The *distributive laws* hold in $R$: for all $a, b, c\in R$ $$(a+b) \times c = a\times c + b \times c, \quad \text{and} \quad a \times (b+c) = a\times b + a \times c.$$
2. The ring $R$ is *commutative* if the multiplication is commutative.
3. The ring $R$ is said to have an *identity* (or *contain* a $1$) if there is an element $1\in R$ with $1 \times a = a \times 1 = a$ for all $a\in R$. If $R$ has an identity, we call it a *unital ring.*

**Prop:** If $(R, +, \times, 0, 1)$ satisfies the following:
- $(R, +, 0)$ is a group;
- $\times$ is associative; 
- the distributive laws hold, and 
- $1$ is an identity for $\times$ operation
Then $(R, +, \times, 0, 1)$ is a unital ring.

**Def:** A unital ring $R$, where $1 \ne 0$, is called a *division ring* or *skew field* if every nonzero element $a\in R$ has a multiplicative inverse, i.e., there's a $b\in R$ such that $ab = ba = 1$. A commutative division ring is called a *field*.

**Prop:** Let $R$ be a ring. Then
- $0a = a0 = 0$ for all $a\in R$.
- $(-a)b = a(-b) = -(ab)$ for all $a, b\in R$.
- $(-a)(-b) =ab$
- If $R$ is unital, then the identity is unique and $-a = (-1) a$. 

**Def:** Let $R$ be a ring.
- A nonzero element $a$ of $R$ is called a *zero divisor* if there is a nonzero element $b\in R$ such that $ab =  0$ or $ba =0$.
- Assume $R$ has an identity $1 \ne 0$. An element $u\in R$ is called a *unit* in $R$ if there is some $v\in R$ such that $uv = vu = 1$. The set of units in $R$ is denoted $R^\times$. 

**Obs:** If $R$ is a unital ring, then $R^\times$ forms a group under multiplication, so $R^\times$ will be referred to as a the *group of units* of $R$. A zero divisor cannot be a unit. Let us note that $(-1)^2 =1$. 

**Def:** A unital commutative ring is called an *integral domain* if it has no zero divisors.

**Prop:** Assume $a, b$ and $c$ are elements of $R$, and $R$ has no zero divisors. If $ab = ac$, then either $a = 0$ or $b = c$. In particular, if $a, b, c \in R$, and $R$ is an integral domain, then either $a = 0$ or $b = c$. 

**Cor:** Any finite integral domain is a field.

**Obs:** If $R$ is an integral domain, and $x^2   =1$ for some $x\in R$, then $x=\pm 1$. 

**Def:** A *subring* of the ring $R$ is a subgroup of $R$ that is closed under multiplication.

**Obs:** To show that a subsets of a ring $R$ is a subring it suffices to check it is *nonempty* and *closed under subtraction and multiplication*. 

**Obs:** Every subring of a field that contains the identity is an integral domain. 

**Def:** Let $R$ be a ring. We define the *centre of $R$* to be $Z(R) := \{z\in R \mid \forall x\in R[zx = xz]\}.$

**Obs:** $Z(R)$ is a subring of $R$. If $R$ is unital then so is $Z(R)$. Finally, if $R$ is a skew-field, then $Z(R)$ is a field. 

**Def:** Let $R$ be a ring and $a\in R$. We define the *centralizer of $a$* to be the set $C(a) := \{r\in R \mid ar = ra\}$. 

**Obs:** Let us note that $C(a)$ is a subring of $R$ for any $a\in R$, and $$Z(R) =\bigcap_{a\in R} C(a).$$Additionally, if $R$ is a skew-field, then so is $C(a)$ for all $a\in R$.

**Def:** A ring $R$ is called a *Boolean ring* if $a^2 =a$ for all $a\in R$. 

**Obs:** Every Boolean ring is commutative.

**Prop:** The only Boolean ring that is an integral domain is $\Bbb Z/2\Bbb Z$. 

**Def:** An element $x$ in $R$ is called *nilpotent* if $x^m = 0$ for some $m \in \Bbb N$.

**Prop:** Let $x$ be a nilpotent element of the ring $R$.
- $x$ is either $0$ or a zero divisor.
- If $R$ is commutative, then $rx$ is also nilpotent for every $r\in R$.
- $1+x$ is a unit
- If $R$ is commutative, then the sum of a nilpotent element and a unit is a unit.

Standard examples for rings:
- [[Integer Numbers]]
- [[Integers modulo n]]
Standard examples for fields are:
- [[Rational Numbers]]
- [[Real Numbers]]
- [[Complex Numbers]]
The most common example of a skew-field is:
- [[Quaternions]]
