---
tags:
  - SetTheory
---
Subjects: [[Set Theory]] 
Links: [[Finite and Countable Sets]], [[Linear Orderings]]

**************Lemma:************** If $A, B, A', B'$ are such that $|A| = |A'|$, $|B| = |B'|$, and, $A \cap B = \varnothing = A' \cap B'$, then $|A\cup B | = |A' \cup B'|$

**Def:** $\kappa + \lambda = |A\cup B|$ where $|A| = \kappa$, $|B | = \lambda$ and $A \cap B = \varnothing$.

Then we have that the addition of cardinal numbers $\kappa, \lambda$ and $\mu$ respect these properties
- $\kappa + \lambda = \lambda +\kappa$
- $\kappa+(\lambda+\mu)= (\kappa+\lambda)+\mu$
- $\kappa \le \kappa +\lambda$
- If $\kappa_1 \le \kappa_2$ and $\lambda_1 \le \lambda_2$, then $\kappa_1+\lambda_1 \le \kappa_2+\lambda_2$

It is hard to get strict inequalities with cardinal numbers, mainly since they can be infinite and break our intuition

**************Lemma:************** If $A, B, A', B'$ are such that $|A| = |A'|$ and, $|B| = |B'|$, then $|A\times B| = |A'\times B'|$

**Def:** $\kappa \cdot \lambda =|A\times B|$ where $|A| = \kappa$, and $|B | = \lambda$

Then we have that the multiplication of cardinal numbers $\kappa, \lambda$ and $\mu$ respect these properties
- $\kappa \cdot \lambda = \lambda \cdot \kappa$
- $\kappa\cdot (\lambda \cdot \mu) = (\kappa\cdot \lambda) \cdot \mu$
- $\kappa\cdot (\lambda + \mu) = \kappa\cdot \lambda + \kappa\cdot\mu$
- $\kappa \le \kappa \cdot \lambda$ with $\lambda >0$
- If $\kappa_1 \le \kappa_2$ and $\lambda_1 \le \lambda_2$, then $\kappa_1\cdot\lambda_1 \le \kappa_2\cdot\lambda_2$
- $\kappa + \kappa = 2\kappa$
- $\kappa +\kappa \le \kappa \cdot \kappa$, whenever $\kappa \ge 2$

**************Lemma:************** If $A, B, A', B'$ are such that $|A| = |A'|$ and, $|B| = |B'|$, then $|A^ B| = |A'^{B'}|$

Def: $\kappa ^\lambda = |A^B|$, where $|A| = \kappa$, and $|B | = \lambda$

Then we have that the exponentiation of cardinal numbers $\kappa, \lambda$ and $\mu$ respect these properties

- $\kappa \le \kappa ^\lambda$ if $\lambda >0$
- $\lambda \le \kappa ^\lambda$ if $\kappa>1$
- If $\kappa_1 \le \kappa_2$ and $\lambda_1 \le \lambda_2$, then $\kappa_1^{\lambda_1} \le \kappa_2^{\lambda_2}$
- $\kappa \cdot \kappa = \kappa^2$
- $\kappa ^0 =1$
- $\kappa^1 = \kappa$
- $1^\kappa =1$ for all $\kappa$
- $0^\kappa =0$ for $\kappa >0$

********Th:********
- $\kappa^{\lambda +\mu} = \kappa^\lambda \cdot \kappa ^\mu$
- $(\kappa^\lambda)^\mu = \kappa^{\lambda \cdot \mu}$
- $(\kappa\cdot \lambda) ^\mu= \kappa^\mu \cdot \kappa^\lambda$

### Cantor’s Theorem

For every set $X$, $|X| < |\mathcal P(X)|$

********Th:******** For every set $X$, $|\mathcal P(X)| = 2^{|X|}$

This can be reformulated into, for any cardinal number $\kappa$ we have that

$$ \kappa < 2^\kappa $$

**Cor:** For any system of sets $S$ there exist a set $Y$ such that $|Y| > |X|$ holds for all $X \in S$

### Dedekind Infinite

A set $X$ is called **Dedekind infinite** if there’s a bijection from $X$ onto a proper subset of $X$. A **Dedekind finite** set is that is not Dedekind infinite.

Properties of Dedekind infinite sets
- Every countable set is Dedekind infinite
- $X$ is Dedekind infinite iff $X$ contains a countable subset
- If $A$ and $B$ are Dedekind finite, then $A \cup B$ and $A\times B$ are Dedekind finite
- If $A$ is infinite, then $\mathcal{P(P(}A))$ is Dedekind Infinite.

---

# Cardinality of the Continuum

Properties of $\aleph_0$:

- $\kappa < \aleph_0$ iff $\kappa \in \Bbb N$
- $n +\aleph_0 = \aleph_0+\aleph_0= \aleph_0$ for $n \in \Bbb N$
- $n\cdot \aleph_0= \aleph_0\cdot \aleph_0= \aleph_0$, for $n \in \Bbb N$ and $n >0$
- $\aleph_0^n = \aleph_0$, for $n \in \Bbb N$ and $n >0$

********Th (Properties of $2^{\aleph_0}$):**

- $n+ 2^{\aleph_0}= {\aleph_0}+2^{\aleph_0}= 2^{\aleph_0}+2^{\aleph_0}= 2^{\aleph_0}$ for $n \in \Bbb N$
- $n \cdot 2^{\aleph_0} = {\aleph_0} \cdot 2^{\aleph_0}= 2^{\aleph_0}\cdot 2^{\aleph_0}= 2^{\aleph_0}$, for $n \in \Bbb N$ and $n >0$
- $(2^{\aleph_0})^n = (2^{\aleph_0})^{{\aleph_0}}= n^{\aleph_0} =\aleph_0^{\aleph_0}= 2^{\aleph_0}$, for $n \in \Bbb N$ and $n >0$

********Th:******** If $A$ is a countable subset of $B$ and $|B| =2^{\aleph_0}$, then $|B\setminus A| = 2^{\aleph_0}$

### The Continuum Hypothesis

There is no uncountable cardinal number $\kappa$ such that $\kappa < 2^{\aleph_0}$