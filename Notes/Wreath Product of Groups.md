---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Semidirect Product of Groups]], [[Direct Product of Groups]], [[Direct Sum of Groups]]

Let $A$ and $Q$ groups, with $Q$ a finite group, and $K = A^Q$ as the direct product of $A$ $|Q|$ times. We can define the action of $Q$ on $K$ as follows: $\theta(f, y)= f^y$, where $f^y(x) = f(xy)$, for every $f\in K$ and $x\in Q$. 

**Def:** We can define the semidirect product of $K= A^Q$ by $Q$ that is called the *wreath product* of $A$ by $Q$, and is denoted by $$A \wr Q := A^Q \rtimes Q = A^Q \rtimes_\theta Q.$$
We can generalise this definition a tiny bit. Let $A$ and $Q$ be groups, and $\Omega$ be a left $Q$-set. The direct product $A^\Omega$ of $A$ with itself $\Omega$ is the set of functions from $\Omega$ to $A$ with pointwise multiplication. The action of $Q$ on $\Omega$ can be extended to an action on $A^\Omega$ by: $$ \theta(x,f)(\omega) := f(x^{-1} *\omega)$$for all $x\in Q$ and $f\in A^\Omega$. Then the *unrestricted wreath product $A\text{ Wr}_{\Omega} Q$ or $A\wr_\Omega Q$* of $A$ by $Q$ is the semidirect product $A^\Omega \rtimes_\theta Q$ with the action of $H$ on $A^\Omega$ given above. The subgroup $A^\Omega$ of $A^\omega\rtimes Q$ is called the *base* of the wreath. 

The *restricted wreath product* $A \text{ wr}_\Omega Q$ is constructed in the same way as the unrestricted wreath product expect that one uses the direct sum as the base of the wreath as the base of the wreath. In this case, the base consists of all finite support functions $A^\Omega$. 

In the most common case, $\Omega = Q$, and $Q$ acts on itself by left multiplication. In this case, the unrestricted and restricted wreath product may be denoted by $A \text{ Wr } Q$, or $A \wr Q$, and $A \text{ wr } Q$. This is calle the *regular wreath product.*

Note that $A \text{ wr}_\Omega Q\le A \wr_\Omega H$. 