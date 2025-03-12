---
tags:
---
Subjects: 
Links: [[Lie Algebra]], [[Module and Algebra (Structure)]], [[Graded Ring]]

If $A$ is an algebra over a field $K$, a *derivation* of $A$  is a $K$-linear map $D: A\to A$ such that $$D(ab) = (Da) b + a(Db$$
The set of all derivations of $A$ is closed under addition and scalar multiplication and thus forms a vector space, denoted by $\text{Der}(A)$. We don't have that $\text{Der}(A)$ is an algebra since the composition of derivations isn't necessarily a derivation. 

Let $D_1$ and $D_2$ be two derivations, then $D_1 D_2 - D_2 D_1$ is a derivation, denoted as $[D_1, D_2]$, and it is called the *commutator*of $D_1$ and $D_2$.

**Prop:** For any algebra $A$, the set $\text{Der}(A)$ along with the commutator $[\;, \;]$ is a Lie algebra.

**Obs:** One way to remember the Jacobi identity is to notice that is equivalent to the operador $[D, \;\cdot\;]: \text{Der}(A) \to \text{Der}(A)$ is a derivation of the algebra $\text{Der}(A)$, for each $D \in \text{Der}(A)$. 
# Graded Derivations

Let $A = \bigoplus_{k = 0}^\infty A^k$ be a graded algebra over a field $K$. The *antiderivation* of a graded algebra $A$ is a $K$-linear map $D: A \to A$ such that $a \in A^k$ and $b\in A^\ell$, $$D(ab) = (Da) b + (-1)^k a (Db)$$If there is an integer $m$ such an antiderivation $D$ sends $A^k$ to $A^{k+m}$ for all $k$, then we say that is an antiderivation of degree $m$. By defining $A_k = 0$ for $k <0$, we can extend the grading of a graded algebra $A$ to negative integers. With this extension in mind, the degree $m$ of an antiderivation can be negative.  