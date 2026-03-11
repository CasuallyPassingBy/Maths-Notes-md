---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[The Complexity Class NP]], [[NP-Completeness]]

Verifying that something is *not* present seems to be difficult than verifying that *is* present. We make a separate complexity class $\sf coNP$, which contains the languages that are complements of languages in $\sf NP$. We don't know whether $\sf coNP$ is different from $\sf NP$. 

There's an important question about the question if $\sf NP \cap coNP = P$. This is still an important open question. 

**Prop:** Let $\text{Primes} := \{ m \mid m\text{ is a prime number in binary}\}\in \sf NP\cap coNP.$ 

**Prop:** Call a regular expression *star-free* if it does not contain any star operations. Let $\text{EQ}_\mathsf{SF - REX} := \{\langle R, S\rangle \mid R\text{ and } S \text{ are equivalent star-free regular expressions}\}.$ Then $\text{EQ}_\mathsf{SF-REX}$ is in $\sf coNP$. 