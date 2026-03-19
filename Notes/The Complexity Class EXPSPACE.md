---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[The Complexity Class PSPACE]], [[Complexity Hierarchy Theorems]], [[Space Complexity]], [[The Complexity Class P]], [[Patterns and Regular Expressions]]

We know that a Turing machine can decide more languages in $\sf EXPSPACE$ that it can in $\sf PSPACE$. We show that a particular language connecting generalised regular expression is complete for $\sf EXPSPACE$ and hence can't be decided in polynomial time or even in polynomial space.

We know that, by allowing regular expressions more operations than the usual regular expressions, the complexity of analysing the expressions may grow dramatically. Let $\uparrow$ the *exponentiation operation*. If $R$ is a regular expression and $k$ is a nonnegative integer, $R \uparrow k$ is equivalent to the concatenation of $R$ with itself $k$ times. We also write $R^k$ as shorthand $R\uparrow k$. In other words,  $$R^k = R\uparrow k:= R \circ R \circ \dots \circ R. $$Generalised regular expressions allow the exponentiation operation in addition to the usual regular expressions. Obviously, these generalised regular expressions still generate the same class of regular languages as do the standard regular expressions because we can eliminate the exponentiation operation