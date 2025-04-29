---
tags:
---
Subject: [[Compilers]]
Links: [[Strings and Grammars]]

Assume that two expressions $e_1$ and $e_2$ generate the languages $L_1$ and $L_2$, respectively. *Concatenation*, is then defined as $e_1 e_2 := \{xy \mid x \in L_1, y\in L_2\}$. *Alternation*, which is denoted as $|$ is the union of the two languages, $e_1 | e_2 := \{x \in L_1 \lor x \in L_2\}$. *Closure*, which is represented by braces $\{\ \}$, denotes the repetition of the expression $n$ times for $n <\omega$, $\{e_1\} := \{x \in L_1^*\}$. 

**Def:** Regular expressions are those expression that can be constructed from the following rules:
- $\phi$ is regular 