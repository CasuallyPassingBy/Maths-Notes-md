---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Alternating Turing Machines]], [[The Complexity Class P]], [[The Complexity Class NP]], [[The Complexity Class coNP]], [[Time Complexity]]

Alternating machines provide a way to define a natural hierarchy of problems within the class $\sf PSPACE$.

**Def:** Let $i$ be a natural number. A *$\Sigma_i$-alternating Turing machine* is an alternating Turing machine that contains at most $u$ runs of universal or existential steps, starting with existential steps. A $\Pi_i$-alternating Turing machine is similar except that it starts with universal steps.

$\Sigma_i \text{TIME}(f(n))$ is the class of languages that a $\Sigma_i$-alternating Turing machine can decide in $O(f(n))$ time. Similarly, the class $\Pi_i \text{TIME}(f(n))$ for $\Pi_i$-alternating Turing machines, and the classes $\Sigma_i\text{SPACE}(f(n))$ and $\Pi_i\text{SPACE}(f(n))$ for space bounded alternating Turing machines. 

We define the *polynomial time hierarchy* to be the collection of classes $$\Sigma_i \mathsf P := \bigcup_{k \ge 0} \Sigma_i\text{TIME}(n^k) \qquad \text{and} \qquad \Pi_i \mathsf P := \bigcup_{k \ge 0} \Pi_i\text{TIME}(n^k).$$
Define ${\sf PH }:= \bigcup_{k \ge 0}\Sigma_k \mathsf P = \bigcup_{k \ge 0}\Pi_k \mathsf P$. 

Clearly, ${\sf NP} = \Sigma_1 \sf P$, and ${\sf coNP} = \Pi_1 \sf P$. Additionally, $\text{Min-Formula}\in \Pi_2 \sf P$. 

**Prop:** If $\sf P = NP$, then $\sf P = PH$.

There are a lot of open questions about the polynomial time hierarchy. The most important is that is the hierarchy infinite? Apparently, it is known that if two levels are the same then the entire hierarchy collapses to where those levels are the same. This brings a generalisation of the question of $\sf P$ vs $\sf NP$. 