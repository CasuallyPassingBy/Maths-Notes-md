---
tags:
---
Subjects: 
Links:

**Def:** A *Kleene algebra* $\cal K$ consists of a nonempty set with two distinguished constants $0$, and $1$, two binary operations $+$ and $\cdot$, and a unary operation $^*$ satisfying the following axioms.
1. $a+(b+c) = (a+b) +c$.
2. $a+ b= b+a$.
3. $a+a = a$.
4. $a+0 = a$.
5. $a(bc) = (ab)c$.
6. $a1=1a=a$.
7. $a0 = 0a = 0$.
8. $a(b+c) = ab+ac$.
9. $(a+b)c = ac +bc$.
10. $1+a^*a = a^*$.
11. $1+ a^*a  =a^*$
12. $b+ac \le c \implies a^*b \le c$.
13. $b + ca \le c \implies ba^*\le c$.
We mean that $\le$ refers to the naturality defined order$$\alpha \le \beta \stackrel{\text{def}}{\iff} a+ b = b. $$
We see that the axioms $(1.)- (9.)$ discuss the properties of addition and multiplication in Kleene algebra. These axioms can be summed up briefly by saying that $\cal K$ is an [[Idempotent Semirings|idempotent semiring]]. The axioms $(10.)-(13.)$ discuss the properties of the operator $^*$.

All the operators are monotone with respect to $\le$; in other words, if $a\le b$, then $ac \le bc$, $ca\le cb$, $a+c \le b+c$, and $a^*\le b^*$.

**Lemma:** In an Kleene algebra, $a^* b$ is the $\le$-least solution of the equation $x = ax+b$. 

**Prop:** Instead of $(12.)$ and $(13.)$ axioms, we might take the equivalent axioms
- $ac \le c\implies a^*c \le c$.
- $ca \le c\implies ca^*\le c$. 

Let $\cal K$ be a Kleene algebra. We can get the following identities from the axioms.
1. $a^* a^* = a^*$.
2. $(a^*)^* = a^*$.
3. $(a^* b ) a^* = (a+b)^*$.
4. $a(ba)^* = (ab)^* a$.
5. $a^* = (aa)^* + a(aa)^*$. 

An example, of Kleene algebra is the family $\mathcal P(\Sigma^*)$ with constants $\varnothing$ and $\{\varepsilon\}$ and operations $\cup$, $\cdot$, and $^*$, where $\Sigma$ is an [[Strings and Languages|alphabet]]. 

Another example of a Kleene algebra is the family of all [[binary relations]] on a set $X$ with the empty relation for $0$, the identity relation $$\iota := \{(u, u) \mid u \in X\}  $$for $1$, $\cup$ for $+$, relation composition $$R \circ S := \{(u, w) \mid \exists v\in X(u, v) \in R \land (v, w)\in S\}  $$ for $\cdot$, and reflexive [[Operations and Structures|transitive closure]] for $^*$:$$R^* := \bigcup_{n \ge 0} R^n, $$where $$\begin{align*} R^0 &:= \iota,\\ R^{n+1} &:= R^n \circ R.\end{align*}  $$

# Matrices

Given an arbitrary Kleen algebra $\cal K$, the set of $n\times n$ matrices over $\cal K$, which we will denote by $\mathcal M(n, \mathcal K)$. 

**Lemma:** If $\cal K$ is a Kleene algebra, then so is $\mathcal M(n, \mathcal K)$.

Suppose we are given a set of $n$ variables $x_1,\dots, x_n$ ranging over $\cal K$ and a system of $n$ equations of the form $$x_i = a_{i1}x_1+ \cdots + a_{in}x_n + b_i, \qquad 1\le i \le n,  $$where $a_{ij}$ and $b_i$ are elements of $\cal K$. Arranging the $a_{ij}$ in an $n \times n$ matrix $A$, and $b_i$ in a vector $b$ of length $n$, and the $x_i$ in a vector $x$ of length $n$, we obtain the matrix valued equation $$x = Ax + b.$$
**Th:** The vector $A^* b$ is a solution to $x = Ax+b$; moreover, it is the $\le$-least solution in $\mathcal K^n$. 