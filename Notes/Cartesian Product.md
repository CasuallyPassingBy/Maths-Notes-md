---
tags:
  - SetTheory
---
Subjects: [[Set Theory]]
Links: [[Basic Set Theoretic Operations]]

There are a couple of definitions for $(a,b)$. The Kuratowski’s definition:

$$ (a,b) = \{ \{a\}, \{a,b\}\} $$

Then $(a, b) =(a', b')$ , iff $a =a'$ and $b =b'$.

If we define the Cartesian product as:

$$ A \times B=\{(a,b) \in \mathcal{P(P(}A\cup B))\mid a\in A \land b \in B\} $$

Then $(a,b) \in A \times B$ , then $(a,b) \in \mathcal{P(P(}A\cup B))$, and thus $A\times B \subseteq \mathcal{P(P(}A\cup B))$ which is useful to since $A \times B$ can be gotten only using the [[ZF Axioms|ZF Axioms]].

### Algebraic Properties
There are some algebraic interactions using the [[Basic Set Theoretic Operations|other set operations]]: 
$\def\t{\times} A \t(B \cup C) = (A\t B)\cup (A\t C); (A\cup B)\t C = (A\t C)\cup (B\t C)$ $\def\t{\times} A \t(B \cap C) = (A\t B)\cup (A\t C); (A\cup B)\t C = (A\t C)\cap (B\t C)$$\def\t{\times} A \t(B \cup C) = (A\t B)\setminus (A\t C); (A\cup B)\t C = (A\t C)\setminus (B\t C)$ $\def\t{\times} \def\tr{\,\triangle\,} A \t(B \cup C) = (A\t B)\tr (A\t C); (A\cup B)\t C = (A\t C)\tr (B\t C)$
The Cartesian product is not commutative nor associative:

$$ \def \t {\times} A \t B \neq B \t A  $$$$(A\t B) \t C \neq A \t (B \t C) $$