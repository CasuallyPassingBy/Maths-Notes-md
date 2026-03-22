---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Models Equivalent to Turing Machines]], [[Time Complexity]], [[Space Complexity]], [[The Complexity Class PSPACE]], [[The Complexity Classes L and NL]], [[The Complexity Class P]], [[The Complexity Class coNP]], [[Polynomial Time Hierarchy]]

Alternation is a generalisation of nondeterminism that has proven to be useful in understanding relationships among complexity classes and in classifying specific problems according to their complexity. 

An alternating algorithm may contain instructions to branch a process into multiple child process, just as in a nondeterministic algorithm. The difference between the two lies in the mode of determining acceptance. A nondeterministic computation accepts if any of the initiated process accepts. When an alternating computation divides into multiple process, two possibilities arise. The algorithm can designate that the current process accepts if *any* of the children accept, or it can designate that the process accepts if *all* of the children accept.

**Def:** An *alternating Turing machine* is a nondeterministic Turing machine with an additional feature. Its states, except for $q_\text{accept}$ and $q_\text{reject}$, are divided into *universal states* and *existential states*. When we run an alternating Turing machine on an input string, we label each node of its deterministic computation tree with $\land$ or $\lor$, depending on whether the corresponding configuration contains a universal or existential state. We determine acceptance by designating a node to be accepting if it is labelled with $\land$ and all of its children are accepting or if it is labelled with $\lor$ and any of its children are accepting. 

# Alternating Time and Space

We define the time and space complexity of these machines in the same way that we did for nondeterministic Turing machines, by taking the maximum time or space by any computation branch. 

**Def:**
- $\text{ATIME}(t(n)) := \{L \mid L \text{is decided by an }O(t(n)) \text{ time alternating Turing machine}\}.$ 
- $\text{ASPACE}(t(n)) := \{L \mid L \text{is decided by an }O(t(n)) \text{ space alternating Turing machine}\}.$ 
We define $\sf AP$, $\sf APSPACE$, and $\sf AL$ to be the classes of languages that are decided by alternating polynomial time, alternating polynomial space, and alternating logarithmic space Turing machines, respectively. 

A *tautology* is a Boolean formula that evaluates to $1$ on every assignment to its variables. Let $\text{Taut} := \{\langle \phi \rangle \mid \phi \text{ is a tautology}\}.$ The following alternating shows that $\text{Taut}$ is in $\sf AP$.

"On input $\langle \phi\rangle$:
1. Universally select all assignments to the variables of $\phi$.
2. For a particular assignment, evaluate $\phi$.
3. If $\phi$ evaluates to $1$, accept; otherwise, reject."

Thus, $\text{Taut} \in \sf AP$. Since $\text{Taut}$ is $\sf coNP$-complete, then it means that $\sf coNP \subseteq AP$. We can show something similar that $\text{SAT}\in \sf AP$. Thus, $\sf NP\cup coNP \subseteq AP$.

Let $\phi$ and $\psi$ be two Boolean formulas. Say that $\phi$ and $\psi$ are equivalent if they evaluate to the same value on all assignments to their variables. A *minimal formula* is one that has no shorter equivalent. Let $$\text{Min-Formula} := \{\langle \phi\rangle \mid \text{$\phi$ is a minial Boolean formula}\}.$$
"On input $\phi$:
1. Universally select all formulas $\psi$ that are shorter than $\phi$.
2. Existentially select an assignment to the variables of $\phi$.
3. Evaluate both $\phi$ and $\psi$ on this assignment.
4. Accept if the formulas evaluate to different values. Reject if they evaluate to the same value."

The term *alternation* stems from the ability to alternate, or switch, between universal and existential branching.

**Th:**
- For $f(n) \ge n$ we have $\text{ATIME}(f(n)) \subseteq \text{SPACE}(f(n)) \subseteq \text{ATIME}(f(n)^2)$.
- For $f(n) \ge \log n$ we have $\text{ASPACE}(f(n)) = \text{TIME}(2^{O(f(n))})$. 

**Cor:** $\sf AL = P$.

**Cor:** $\sf AP = PSPACE$.

**Cor:** $\sf APSPACE = EXPTIME$. 

Alternating machines provide a way to define a natural hierarchy of problems within the class $\sf PSPACE$.

**Def:** Let $i$ be a natural number. A *$\Sigma_i$-alternating Turing machine* is an alternating Turing machine that contains at most $u$ runs of universal or existential steps, starting with existential steps. A $\Pi_i$-alternating Turing machine is similar except that it starts with universal steps.

$\Sigma_i \text{TIME}(f(n))$ is the class of languages that a $\Sigma_i$-alternating Turing machine can decide in $O(f(n))$ time. Similarly, the class $\Pi_i \text{TIME}(f(n))$ for $\Pi_i$-alternating Turing machines, and the classes $\Sigma_i\text{SPACE}(f(n))$ and $\Pi_i\text{SPACE}(f(n))$ for space bounded alternating Turing machines. 