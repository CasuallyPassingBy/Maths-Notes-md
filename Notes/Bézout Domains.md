---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Principal Ideal Domains]], [[Ring of Fractions]], [[Integral Domains]]

**Def:** An integral domain $R$ in which every ideal generator by two elements is principal is called a *Bézout Domain.*

**Obs:** Every principal ideal domain is a Bézout domain. 

**Prop:** Let $R$ be an integral domain. $R$ is a Bézout domain iff every pair of elements of $a,b$ of $R$ has a greatest common divisor $d$ in $R$ that can be written as an $R$-linear combination of $a$ and $b$, i.e., $d= ax+by$ for some $x,y\in R$. 

**Prop:** Every finitely generated ideal of a Bézout domain is principal.

**Prop:** Let $F$ be the fraction field of the Bézout domain $R$. Every element of $F$ can be written in the form $a/b$ with $a, b\in R$ and $a$ and $b$ are relatively prime, i.e., $(a,b) = 1$. 

**Th:** Let $R$ be an integral domain. $R$ is a principal ideal domain iff it is a Bézout domain and unique factorisation domain. 

**Prop:** Let $R$ be a Bézout Domain, and let $a, b, N\in  R$. Consider the equation $$ax + by = N.$$ Let $d = (a,b)$ denote the greatest common divisor of $a$ and $b$ (unique up to multiplication by a unit in $R$). Then:
- Existence: The equation $ax + by = N$ has a solution $(x, y)\in \Bbb R^2$ iff $d \mid N$.
- Construction of a Particular Solution: There are $u, v\in R$ such that $$au +bv = d.$$if $d\mid N$, say $N = dm$, then $$x_0 = um,\qquad y_0 = vm $$is a particular solution to $ax+by = N$. 
- General Solutions: If $(x_0, y_0)$ is one particular solution, then all solutions are given by $$ x = x_0 +\left(\frac{b}{d}\right)t, \text{ and, } y = y_0 -\left(\frac{a}{d}\right)t,$$where $t$ ranges over all elements of $R$. 

The proposition above generalises the notion of a [[Linear Diophantine Equations|linear Diophantine equation]].