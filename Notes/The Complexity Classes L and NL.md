---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Space Complexity]], [[The Complexity Class P]]

We examine smaller bounds that linear, namely *sublinear* space bounds. In time complexity, sublinear bounds are insufficient for reading the entire input, so we don't consider them here. In sublinear space complexity the machine is able to read the entire input but it doesn't have enough store the input. 

We introduce a Turing machine with two tapes: a read-only input tape and a read/write work tape. On the read-only tape the input head can detect symbols but not change them. We provide a way for the machine to detect when the head on the portion of the tape containing the input. The work tape may be read and written in the usual way. Only the cells scanned on the work tape contribute to the space complexity of this type of Turing machine.

For space bounds that are at least linear, the two-tape Turing machine model is equivalent to the standard one-tape model. For sublinear space bounds, we use only the two tape model.

**Def:** $\sf L$ is the class of languages are decidable in logarithmic space on a deterministic Turing machine. In other words,  $$\mathsf L := \text{SPACE}(\log n). $$$\sf NL$ is the class of languages that are decidable in logarithmic space on a nondeterministic Turing machine. In other words,  $$\mathsf{NL} := \text{NSPACE}(\log n).$$
We focus on $\log n$ space for several reasons that are similar to those for our selection of polynomial time and space bounds. Logarithmic space is just large enough to solve a number of interesting computational problems, and it has attractive mathematical properties such as robustness even when machine model and input encoding method change. Pointers into the input may be represented in logarithmic space, so one way to think about the power of $\log$ space is to consider the power of a fixed number of input pointers.

**Def:** If $M$ is a Turing machine that has a separate read-only input tape and $w$ is an input, a *configuration of $M$ on $w$* is a setting of the state, the work tape, and the position of the two tape heads. The input $w$ is not part of the configuration of $M$ on $w$.

If $M$ runs in $f(n)$ space and $w$ is an input of length $n$, the number of configuration of $M$ on $w$ is $2^{O(f(n))}$. 

Our earlier claim that the time complexity of a machine is at most exponential in its pace complexity remains true for such bounds because $n 2^{O(f(n))}$ is $2^{O(f(n))}$ when $f(n) \ge \log n$.

**Savitch's Theorem:** For any function $f:\Bbb N \to \Bbb R^+$, where $f(n) \ge \log n$, $$\text{NSPACE}(f(n)) \subseteq \text{SPACE}(f^2(n)).$$

# $\sf NL$-Completeness

**Def:** A *log space trasducer* is a Turing machine with a read-only input tape, a write only output tape, and a read/write work tape. The work tape may contain $O(\log n)$ symbols. A log space transducer $M$ computes a function $f: \Sigma^*\to \Sigma^*$, where $f(w)$ is the string remaining on the output tape after $M$ halts when it is started with $w$ on its input tape. We call $f$ a *log space computable function,* Language $A$ is *log space reducible* to language $B$, written $A\le_\text L B$, if $A$ is a mapping reducible to $B$ by means of a $\log$ space computable function $f$.

**Def:** A language $B$ is $\sf NL$-hard if every $A$ in $\sf L$ is log space reducible to $B$. If $B$ is both $\sf NL$-hard and in $\sf NL$, then $B$ is $\sf NL$-complete.

**Th:** If $A\le_\text LB$ and $B\in \sf L$, then $A\in \sf L$.

We have the natural question, if $\sf L = NL$. We suspect that probably $\sf L \neq NL$.

**Obs:** If any $\sf NL$-complete language is in $\sf L$, then $\sf L = NL$.

**Th:** $\text{Path}$ is $\sf NL$-complete.

**Cor:** $\sf NL \subseteq P$.

The classes $\sf NP$ and $\sf coNP$ are generally believed to be different. At first glace, the same appears to gold for the classes $\sf NL$ and $\sf coNL$. 

**Th:** $\sf NL = coNL$.

The fact that $\sf NL = coNL$, as we are about to prove, shows that our intuition about computation still many gaps in it.

We summarise our present knowledge of the relationships among several complexity classes as follows:  $$\sf L \subseteq NL = coNL \subseteq P\subseteq PSPACE.$$It is believed that all of the contentions are proper. 

$(*)$ **Th:** $\sf NL \subset PSPACE$. 

**Cor:** $\sf NL \subset P$ or $\sf P \subset PSPACE$. 