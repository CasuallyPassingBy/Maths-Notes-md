---
tags:
  - FieldTheory
---
Subjects: [[Field Theory]]
Links: [[Field Extensions]], [[Classification of Simple Field Extensions]], [[Polynomial Ring of a Single Variable]]

**Def:** A field $F$ is called *algebraically closed* if every polynomial in $F[x]$ has all of its roots in $F.$ Equivalently, every nonconstant polynomial in $F[x]$ is decomposed as a product of linear factors. 

**Prop:** Let $F$ be a field. The following statements are equivalent.
- $F$ is algebraically closed.
- If $L/F$ is an algebraic extension, then $L = F$. 
- If $L/F$ is a finite extension, then $L = F$.

**Prop:** Every algebraically closed field is infinite. 

The proof is actually really similar on how to prove that there are infinitely many primes. 

**Def:** Let $F$ be a field. The *algebraic closure* of $F$ is the extension such tat $L/F$ such that
- $L/F$ is algebraic.
- $L$ is algebraically closed. 

**Th:** Let $F$ be a field. The following statements are equivalent.
- $L/F$ is an algebraic closure of $F$.
- The extension $L/F$ satisfies the following:
	- $L/F$ is an algebraic extension
	- Every irreducible polynomial in $F[x]$ decomposes into linear factors in $L[x]$. 
- $L/F$ is algebraic, and if $L'/L$ is algebraic, then $L' = L$. 

**Steinitz Theorem:** If $F$ is a field, then there exists an algebraic closure $\overline F/F$. 

This proof requieres [[axiom of choice]].

**Prop:** If $\phi: F \to K$ is a field homomorphism with $K$ algebraically closed, and $L/F$ an algebraic extension, then there's a homomorphism $\psi: L \to K$ such that $\psi|_F = \phi$, meaning that $\psi$ is an extension of $\phi$ to $L$. 

This proof also requieres [[Axiom of Choice|choice]]. 

**Th:** Let $F$ be a field, If $\phi_1: F \to L_1$ and $\phi_2: F \to L_2$ are two algebraic closures of $F$, then there exists an isomorphism $\psi: L_1 \to L_2$ such that $\phi_2 = \psi \circ \phi_1$. 

This highlights that for existence and uniqueness of the algebraic closure of a field we must use choice, or to be a little bit more precise Zorn's Lemma.

**Cor:** If $K$ is a countable field, then so is $\overline K$. 

**Prop:** If $F(\alpha)/F$ be a simple transcendental extension over $F$, then $F(\alpha)$ is not closed algebraically. 

The proof is a reinterpretation on why $\sqrt 2 \notin \Bbb Q$, which is magical. 