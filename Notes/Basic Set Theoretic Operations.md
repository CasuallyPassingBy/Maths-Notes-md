---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
## Union

$$ A\cup B := \{x\mid x\in A \lor x\in B\} $$

This operation is well defined thanks to the [[ZF Axioms]], in particular the Axiom of Union
1. $A, B\subseteq A\cup B$
3. $A\cup \varnothing = A\cup A =A$
4. $(A\cup B)\cup C =A\cup (B\cup C)$
5. $A \cup B = B\cup A$
6. $A\cup B = A\iff B\subseteq A$
7. $A\subseteq B \implies A\cup C \subseteq B\cup C$
8. $A, B\subseteq C\implies A\cup B \subseteq C$

## Intersection

$$ A\cap B:= \{x\mid x\in A\land x\in B\} $$

This operation is well defined thanks to the [[ZF Axioms]], in particular the Axiom of Specification.
1. $A\cap B \subseteq A, B$
2. $A\cap \varnothing = \varnothing$
3. $A\cap A = A$
4. $(A\cap B) \cap C= A\cap (B\cap C)$
5. $A\cap B = B\cap A$
6. $A\cap B = B \iff B\subseteq A$
7. $A\subseteq B \implies A\cap C \subseteq B\cap C$
8. $C\subseteq A, B\implies C\subseteq A\cap B$

## Distributive Identities

1. $A \cup (B\cap C) = (A\cup B)\cap (A\cup C)$
2. $A \cap (B\cup C) = (A\cap B)\cup (A\cap C)$

## Difference

$$ A\setminus B :=\{x\mid x \in A\land x\not\in B\} $$

This operation is well defined thanks to the [[ZF Axioms]], in particular the Axiom of Specification
1. $C\setminus (A\cup B) = (C\setminus A) \cap (C\setminus B)$
2. $C\setminus(A\cap B) = (C\setminus A) \cup (C\setminus B)$
3. $(A\cap B)\setminus C = A\cap (B \setminus C)$
4. $A\setminus B = \varnothing \iff A\subseteq B$
5. $A\setminus B = A \iff A\cap B = \varnothing$
6. $X\setminus A= A^c$

## Symmetric Difference

$$ A\,\triangle\,B := \{x\mid x \in A \veebar x\in B\} $$

This operation is well defined thanks to the [[ZF Axioms]], in particular the Axiom of Specification
1. $A\,\triangle\, B = (A\cup B)\setminus(A\cap B) =(A\setminus B)\cup (B\setminus A)$
2. $A\,\triangle\, B =\varnothing \iff A = B$
3. $A\, \triangle\, B = B\, \triangle\, A$
4. $A\,\triangle\,(B\,\triangle\,C) = (A\,\triangle\,B) \,\triangle\,C$