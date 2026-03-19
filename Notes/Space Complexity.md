---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Time Complexity]], [[Models Equivalent to Turing Machines]]

**Def:** Let $M$ be a deterministic Turing machine that halts on all inputs. The *space complexity* of $M$ is the function $f: \Bbb N \to \Bbb N$, where $f(n)$ is the maximum number of tape cells that cells that $M$ scans on any input of length $n$. If the space complexity of $M$ is $f(n)$, we also say that $M$ runs in space $f(n)$. 

If $M$ is a nondeterministic Turing machine wherein all branches halt on all inputs, we define its space complexity $f(n)$ to be the maximum number of tape cells that $M$ scans on any branch of its computation for any input of length $n$. 

**Def:** Let $f:\Bbb N \to \Bbb R^+$ be a function. the *space complexity class*, $\text{SPACE}(f(n))$ and $\text{NSPACE}(f(n))$, are defined as follows. 
$$\text{SPACE}(f(n)) := \{L \mid L \text{ is a language decided by an }O(f(n)) \text{ space deterministic TM}\}.$$
$$\text{NSPACE}(f(n)) := \{L \mid L \text{ is a language decided by an }O(f(n)) \text{ space nondeterministic TM}\}.$$

We can also define if $$\text{coSPACE}(f(n)) := \{ \Sigma^*\setminus A \mid A\in \text{SPACE}(f(n))\}, $$and $$\text{coNSPACE}(f(n)) := \{ \Sigma^*\setminus A \mid A\in \text{NSPACE}(f(n))\}, $$

**Savitch's Theorem:** For any function $f:\Bbb N \to \Bbb R^+$, where $f(n) \ge n$, $$\text{NSPACE}(f(n)) \subseteq \text{SPACE}(f^2(n)).$$
There are important classes to study regarding space complexity
- [[The Complexity Class PSPACE]]
- [[The Complexity Classes L and NL]]
- [[The Complexity Class EXPSPACE]]