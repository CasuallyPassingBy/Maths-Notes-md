---
tags:
  - RingTheory
---
Subjects: [[Ring Theory]]
Links: [[Normal Subgroups and Quotient Groups]], [[Ring Homomorphisms]]

**Def:** Let $R$ be a ring, $I \subseteq R$ and $r\in R$.
- $rI := \{ra \mid a\in I\}$ and $Ir := \{ar \mid a \in I\}$.
- A subset $I$ of $R$ is a *left ideal* of $R$ if
	- $I$ is a subring of $R$, and
	- $I$ is closed under left multiplication by elements from $R$, i.e., $rI \subseteq I$ for all $r\in R.$ 
- Similarly, $I$ is *right ideal* of $R$ if 
	- $I$ is a subring of $R$, and
	- $I$ is closed under right multiplication by elements from $R$, i.e., $Ir \subseteq I$ for all $r\in R.$ 
- A subset $I$ that is both a left ideal and a right ideal is called an *ideal*, or for added emphasis, a *two-sided ideal*, of $R$. We usually write this relation as $I \le R$.

**Obs:** For commutative rings the notion of left, right and two-sided ideals are the same. 

**Prop:** If $R$ and $S$ are rings, and $\varphi: R \to S$ is a homomorphism, then $\ker \varphi$ is an ideal of $R$.

**Prop:** Let $R$ be a ring and let $I$ be an ideal of $R$. Then the quotient group $R/I$ is a ring under the binary operations: $$(r+I) + (s+I) = (r+s)+I \quad \text{and} \quad (r+I) (s+I) = rs + I,$$for all $r,s\in R$. Conversely, if $I$ is any subgroup such that the above operations are well defined, the $I$ is an ideal of $R$.

**Def:** When $I$ is an ideal of $R$ the ring $R/I$ with the operations in the previous proposition is calle the *quotient ring* of $R$ by $I$. 

**Prop:** If $I$ is an ideal of $R$, then the map $\pi: R \to R/I$ defined by $r \mapsto r+I$ is a surjective ring homomorphism with kernel $I$, this homomorphism is called the *natural projection of $R$ onto $R/I$*. Thus every ideal is the kernel of a ring homomorphism. 

**Def:** Let $R$ be ring. If the only ideals of $R$ are $0$ and $R$, we say that $R$ is a *simple* ring. This is mimicking the idea of [[simple groups]] 

# Operations

**Prop:** Let $\{I_\alpha \mid \alpha< \kappa\}$ be a collection of ideals of $R$, then $\bigcap_{\alpha<\kappa} I_\alpha$ is also an ideal of $R$. 

**Prop:** Let $\{I_n \mid n \in \Bbb N\}$ be an increasing collection of ideals of $R$, then $\bigcup_{n \in \Bbb N} I_n$ is also an ideal in $R$. 

**Def:** Let $I$ and $J$ be ideals of $R$. 
- Define the *sum* of $I$ and $J$ by $$I+J := \{a+b \mid a\in I, b\in J\}.$$
- Define the *product* of $I$ ad $J$, denoted by $IJ$, to be the set of all finite sums of elements of the form $ab$ with $a\in I$ and $b\in J$. 
- For any $n \ge 1$, define the *$n$th power* of $I$, to to be set set of all finite sums of elements of the form $a_1a_2\cdots a_n$ with $a_i \in I$ for all $i$. Equivalently, $I^n$ is defined inductively by defining $I^1 := I$, and $I^{n+1} := I^n I$ for $n \ge 1$. 

**Obs:** We can see that if $I$ and $J$ are left/right/two-sided ideals, then $I+J$ is also a  left/right/two-sided ideal. If $I$ is a left ideal, then $IJ$ is left ideal. Similarly, if $J$ is a right ideal, then $IJ$ is a right ideal. In particular, if $I$ is left ideal and $J$ is a right ideal, then $IJ$ is a two-sided ideal. 

**Prop:** Let $I, J, K \le R$. 
- $I+J$ is the smallest ideal of $R$ containing both $I \cup J$. 
- $I J\subseteq I \cap J$.
- If $R$ is commutative and $I+J =R$, then $IJ = I \cap J$. 
- $I(J+K) = IJ + IK$, and $(I+J) K = IK + JK$
- If $J\subseteq I$, then $I\cap (J+K) =J+(I\cap K).$

**Def:** An ideal $N$ is called *nilpotent* if $N^m = 0$ for some $m \ge 1$. 

# Common Ideals

**Def:** Let $a\in R$. We call the following sets $\{x\in R \mid ax = 0\}$ and $\{y\in R \mid ya = 0\}$ the *left annihilator* and *right annihilator* of $a$ in $R$, we denote them as $\text{Ann}_R(a)$ and $_R\text{Ann}(a)$. We can generalise further this definition, let $S\subseteq R$, then the left annihilator of $S$ is the set $\text{Ann}_R(S) := \{x\in R \mid \forall s\in S[xs = 0]\}$. Similarly, the right annihilator of $S$ is the set $_R\text{Ann}(S) := \{x\in R \mid \forall s\in S [sx = 0]\}$. Note that $\text{Ann}_R(S)$ is a right ideal, and $_R\text{Ann}(S)$ is a left ideal.

**Obs:** Let $a\in R$. The left annihilator of $a$ is a right ideal, and the right annihilator of $a$ is left ideal. If $I$ is left ideal, then $\text{Ann}_R(I)$ is a two-sided ideal. Similarly, if $I$ is a right ideal, then  $_R\text{Ann}(I)$ is a two-sided ideal. 

**Def:** Let $R$ be a commutative ring. The set of nilpotent elements of $R$ is called the *nilradical of $R$* and is denoted by $\text{nilrad}(R)$ or ${\frak N}(R)$ 

**Obs:** The nilradical of a commutative ring $R$ is an ideal. 

**Def:** Let $I$ be an ideal of the commutative ring $R$, we define $$\text{rad } I = \sqrt I := \{r\in R \mid r^n \in I \text{ for some }n \in \Bbb N^+\}, $$called the *radical of $I$*. 

**Prop:** Let $R$ be a commutative ring. If $I \le R$, then $(\text{rad } I) / I = \text{nil}(R/I)$. 

**Def:** An ideal $I$ of a commutative ring $R$ is called a *radical ideal* if $\text{rad } I = I$. 

**Obs:** $0$ is radical ideal in $\Bbb Z/n\Bbb Z$ iff $n$ is a square free. Additionally, then $(n)$ is a radical ideal if $\Bbb Z$ iff $n$ is a product of distinct prime in $\Bbb Z$. 