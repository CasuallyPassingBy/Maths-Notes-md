---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Time Complexity]], [[Space Complexity]], [[The Complexity Class PSPACE]], [[The Complexity Class P]], [[The Complexity Classes L and NL]]

**Def:** A function $f: \Bbb N \to\Bbb N$, where $f(n)$ is at least $O(\log n)$, is called *space constructible* if the function that maps the string $1^n$ to the binary representation of $f(n)$ is computable in $O(f(n))$. 

In other words, $f$ is space constructible if some $O(f(n))$ space Turing machine $M$ exists that always hake with the binary representation of $f(n)$ on its tape when started on input $1^n$. 

When showing functions $f(n)$ that are $o(n)$ to be space constructible, we use a separate read only input tape, as we did when we defined sublinear space complexity. 

**Space Hierarchy Theorem:** For any space constructible function $f: \Bbb N\to \Bbb N$ a language $A$ exists that is decidable in $O(f(n))$ space but not in $o(f(n))$ space.

**Cor:** For any two functions $f_1, f_2:\Bbb N \to \Bbb N$, where $f_1(n)$ is $o(f_2(n))$, and $f_2$ is space constructible, $\text{SPACE}(f_1(n)) \subset \text{SPACE}(f_2(n))$.

**Cor:** For any two real numbers $0 \le \varepsilon_1 < \varepsilon_2$, $$\text{SPACE}(n^{\varepsilon_1}) \subset \text{SPACE}(n^{\varepsilon_2}).$$
**Cor:** $\sf NL \subset\text{SPACE}(n) \subseteq PSPACE$.

**Def:** $\sf EXPSPACE$ is the class of languages that are decidable in exponential space on a deterministic Turing machine. In other words, $$\mathsf{EXPSPACE}:= \bigcup_{k \in \Bbb N} \text{SPACE}\left(2^{n^k}\right). $$
**Cor:** $\sf PSPACE \subset EXPSPACE$.

**Def:** A function $t: \Bbb N\to \Bbb N$, where $t(n)$ is at least $O(n\log n)$, is called *time constructible* if the function that maps the string $1^n$ to the binary representation of $t(n)$ is computable in time $O(t(n))$. 

**Time Hierarchy Theorem:** For any time constructible function $t: \Bbb N \to \Bbb N$, a language $A$ exists that is decidable in $O(t(n))$ time but not decidable in time $o(t(n)/\log t(n))$. 

**Cor:** For any two functions $t_1, t_2:\Bbb N \to \Bbb N$, where $t_1(n)$ is $o(t_2(n)/\log t_2)$ and $t_2$ is a time constructible, $\text{TIME}(t_1(n))\subset \text{TIME}(t_2(n))$. 

**Cor:** For any two real numbers $1 \le \varepsilon_1 < \varepsilon_2$. $$\text{TIME}(n^{\varepsilon_1})\subset \text{TIME}(n^{\varepsilon_2}).$$
**Cor:** $\sf P \subset \text{TIME}(2^n) \subseteq \sf EXPTIME$. 