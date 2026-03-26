---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Boolean Circuit Complexity]], [[The Complexity Classes L and NL]], [[The Complexity Class P]]

A *parallel computer* is one that can perform multiple operations simultaneously. Parallel computers may solve certain problems much faster than *sequential computers*, which can only do a single operation at a time. In practice, the distinction between the two is slightly blurred because most real computers are designed to use some parallelism as they execute individual instructions. We focus here on *massive* parallelism whereby a huge number of processing elements are actively participating in a single computation.

# Uniform Boolean Circuits

One of the most popular models in theoretical work on parallel algorithms is called *Parallel Random Access Machine* or *PRAM*. In the PRAM model, idealised processors with a simple instruction set patterned on actual computers interact with shared memory. 

Boolean circuits have certain advantages and disadvantages as a parallel computation model. On the positive side, the model is simple to describe, which make proof easier. Circuits also bear an obvious resemblance to actual hardware designs and in the sense the model is realistic. On the negative side, circuits are awkward to 'program' because the individual processors are so weak. 

In the Boolean circuit model of a parallel computer, we take each gate to be an individual processors, so we define the *processor complexity* of a Boolean circuit to be the size. We consider each processor to compute its function in a single time step, so we define *parallel time complexity* of a Boolean circuit to be its depth, or the longest distance from an input variables to the output gate. 

Any particular circuit has a fixed number of input variables, so we use circuit families for recognising languages. We need to impose a requirement on circuit families so that they correspond to parallel computations such as PRAMs where a single machine is cable of handling all input lengths. This *uniformity* requirement is reasonable because knowing that a small circuit exists for recognising certain elements of a language isn't very useful if the circuit itself is hard to find. 

**Def:** A family of circuits $(C_1,C_2, \dots)$ is *uniform* if some log space transducer $T$ outputs $\langle C_n \rangle$ when $T$'s input is $1^n$.

Here, we consider the *simultaneous* size and depth of a single circuit family in order to identify how many processors we need in order to achieve a particular parallel time complexity or vice versa. Say that a language has *simultaneous size-depth* circuit complexity at most $(f(n), g(n))$ if a uniform circuit family exists for that language with size complexity $f(n)$ and depth complexity $g(n)$.

# The Class NC

**Def:** For $i \ge 1$ let ${\sf NC}^i$ be the class of languages that can be decided by a uniform family with polynomial size and $O(\log^i n)$ depth. Let $\sf NC$ be the class of languages that are ${\sf NC}^i$ for some $i$. Functions that are computed by such a circuit are called *${\sf NC}^i$ computable* or *$\sf NC$ computable. 

Defining uniformity in terms of log space transducers is standard for ${\sf NC}^i$ when $i \ge 2$ but gives a nonstandard result for ${\sf NC}^1$, which contains the standard ${\sf NC}^1$ as a subset

**Th:** ${\sf NC}^1\subseteq \sf L$.

**Th:** ${\sf NL \subseteq NC}^2$. 

**Th:** $\sf NC \subseteq P$. 

# $\sf P$-completeness

**Def:** If every $A$ in $P$ is log space reducible to $B$, then we say that $B$ is *$\sf P$-hard.* If $B$ is both in $\sf P$ and $\sf P$-hard, then $B$ is $\sf P$-complete.

**Prop:** If $A \le_\text L B$ and $B$ is in $\sf NC$, then $A$ is in $\sf NC$. 

For a circuit $C$ and input $x$ we write $C(x)$ to be the value of $C$ on $x$. Let $$\text{Circuit-Value} := \{\langle C, x\rangle\mid C \text{ is a Boolean circuit and }C(x) = 1\}.$$
**Th:** $\text{Circuit-Complete}$ is $\sf P$-complete.