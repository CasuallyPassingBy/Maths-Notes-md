---
tags:
  - "#GroupTheory"
---
Subjects: [[Group Theory]]
Links: [[Operations and Structures]]

**Def:**
- A *binary operation* $*$ on a set $G$, is a function $*:G\times G \to G$. For any $a, b\in G$, we shall write $a*b= *(a,b)$.
- A binary operation $*$ on a set $G$ is *associative* if for all $a, b,c \in G$ we have that $a*(b*c) = (a*b)*c$. 
- If $*$ is a binary operation on set $G$ we say elements $a, b\in G$ *commute* if $a*b= b*a$. We say $*$ (or $G$) is *commutative* if for all $a, b\in G$, $a*b = b*a$. 

A *group* is an ordered pair $(G, *)$ where $G$ is a set and $*$ is a binary operation on $G$ satisfying the following axioms:
1. $*$ is associative
2. there exists an element $e\in G$, called the *identity* of $G$, such that for all $a\in G$ we have $a*e = e*a = a$.
3. For each $a\in G$ there exists $a^{-1}\in G$, called the *inverse* of $a$, such that $a*a^{-1} = a^{-1}*a = e$.
The group $(G, *)$ is called *abelian* (or *commutative*) if $a*b = b*a$ for all $a, b\in G$. We say that $G$ is a *finite group* if the set $G$ is finite.

**Prop:** Let $G$ be group, the following equivalent:
- $G$ is abelian
- if for all $a, b\in G$, $(ab)^2 = a^2 b^2$
- there exists $n\in \Bbb N$ such that for all $a,b\in G$, has that $(ab)^k= a^k b^k$, for $k\in\{n, n+1, n+2\}$. 

**Prop:** If $G$ is a group under the operation $*$, then:
- the identity of $G$ is unique
- for each $a\in G$, $a^{-1}$ is uniquely determined
- $(a^{-1})^{-1} = a$ for all $a\in G$
- $(a*b)^{-1} = b^{-1}*a^{-1}$ 
- for any $a_1, a_2, \dots, a_n\in G$ the value $a_1*a_2*\cdots*a_n$ is independent of how the expression is bracketed. This is called the *generalised associative laws*

**Prop:** Let $G$ be a group and let $a, b\in G. The equations $ax = b$ and $ya= b$ have unique solutions for $x, y\in G$. In particular, the left and the right cancellation laws hold in $G$.
- if $au = av$, then $u = v$, and
- if $ub = vb$, then $u = v$

**Def:** An element $e$ is called a *right identity*, if for all $x\in G$, then $e*x = x$, and an element $y$ associated to $x$ is called a *right inverse* of $x$. Similarly for the left definitions

**Prop:** Let $G$ be a set and $*$ an associative binary operation on $G$. Assume that $G$ has a right identity, and every element has a right inverse, then $(G, *)$ is a group. 

**Def:** Let $G = \{g_1, g_2, \dots, g_n\}$ be a finite group with $g_1 = e$. The *multiplication table* or *group table*of $G$ is the $n\times n$ matrix whose $i, j$ entry is the group element $g_i g_j$.

