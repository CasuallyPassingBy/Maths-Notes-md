---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Strings and Languages]], [[Decidable and Undecidable Problems]], [[Context-Free Grammars]]

A *reduction* is a way of converting one problem to another problem in such a way that a solution to the second problem can be used to solve the first problem. Reducibility always involves two problems, which we call $A$ and $B$. If $A$ reduces to $B$, we can use a solution to $B$ to solve $A$. 

Reducibility plays an important role in classifying problems by decidability and complexity theory. When $A$ is reducible to $B$, solving $A$ cannot be harder than solving $B$ because a solution to $B$ gives a solution to $A$. This means that if $A$ is reducible to $B$, the the following statements are true.
- If $B$ is decidable, then $A$ is also decidable.
- If $A$ is undecidable, then $B$ is also undecidable. 

A Turing machine computes a function by starting with the input to the function on the tape and halting with the output of the function on the tape

**Def:** A function $f:\Sigma^* \to \Sigma^*$ is a *computable function* if some Turing machine $M$, on every input $w$, halts with just $f(w)$ on its tape. 

All usual arithmetic operations are computable functions. 

Computable functions may be transformation of machine descriptions. 

**Def:** A language $A$ is a *mapping reducible* to language $B$, written $A \le_\text m B$, if there is a computable function $f: \Sigma^* \to \Sigma^*$, where for every $w$,  $$w\in A \iff f(w) \in B. $$The function $f$ is called the *reduction* of $A$ to $B$.

A mapping of $A$ to $B$ provides a way to convert questions about membership testing in $A$ to membership testing in $B$.

**Th:** If $A\le_\text m B$ and $B$ is decidable, then $A$ is decidable. 

**Cor:** If $A\le_\text m B$ and $A$ is undecidable, then $B$ is undecidable. 

**Prop:** If $A\le_\text m B$ and $B\le_\text m C$, then $A\le_m C$, meaning that $\le_\text{m}$ is transitive.

**Th:** If $A\le_ \text m B$ and $B$ is Turing-recognisable, then $A$ is Turing-recognisable.

**Cor:** If $A \le_\text m B$ and $A$ is not Turing-recognisable, then $B$ is not Turing-recognisable.

**Obs:** Let $A$ and $B$ be languages. It $A\le_\text m B$ is equivalent to $\overline A \le_\text m \overline B$. 

**Cor:** If $A$ is Turing-recognisable and $A\le_\text m \overline A$, then $A$ is decidable. 

Let $$H_\mathsf{TM} := \{\langle M, w\rangle \mid \text{$M$ is a Turing machine and $M$ halts on $w$}\}.$$Note that $A_\mathsf{TM}\subseteq H_\mathsf{TM}$.

**Th:** The language $H_\mathsf{TM}$ is not Turing-decidable. 

We used a reduction from $A_\mathsf{TM}$ to prove that $H_\mathsf{TM}$ is undecidable, This reduction showed how a decider for $H_\mathsf{TM}$ could be used to give a decider for $A_\mathsf{TM}$. To fo so we must present a computable function $f$ that takes input of the form $\langle M, w\rangle$ and returns output of the form $$\langle M, w\rangle \in A_\mathsf{TM} \iff \langle M', w\rangle\in H_\mathsf{TM}.$$
The halting problem had a decider iff the membership problem has decider.

The theorem illustrates our strategy for proving that a problem is undecidable, This strategy is common to most proofs of undecidability, except for the undecidability of $A_\mathsf{TM}$ itself.

Let $$E_{\sf TM} := \{\langle M\rangle \mid \text{$M$ is a Turing machine and }L(M) = \varnothing\}.$$
**Th:** $E_\mathsf{TM}$ is undecidable. 

**Prop:** $A_\mathsf{TM}$ is not mapping reducible to $E_\mathsf{TM}$. 

Another interesting computational problem regarding Turing machines concerns determining whether a given Turing machine recognises a language that also can be recognised by a simpler computational model. Let $$\text{Reg}_\mathsf{TM} := \{\langle M \rangle \mid \text{$M$ is Turign machine and $L(M)$ is a regular language}\}.  $$**Th:** $\text{Reg}_\mathsf{TM}$ is a undecidable, 

Let $$EQ_\mathsf{TM} := \{\langle M_1, M_2\rangle \mid \text{$M_1$ and $M_2$ are Turing mahcines and }L(M_1) = L(M_2)\}.$$**Th:** $EQ_\mathsf{TM}$ is undecidable.

**Th:** $EQ_\mathsf{TM}$ is neither Turing-recognisable nor co-Turing-recognisable.

**Def:** Let $M$ be a Turing machine and $w$ an empty string. An *accepting computation history* for $M$ on $w$ is a sequence of configurations $C_1, C_2, \dots C_\ell$, where $C_1$ is the start configurations of $M$ on $w$, $C_\ell$ is the accepting configuration of $M$. A *rejecting configuration history* for $M$ on $w$ is defined similarly, except that $C_\ell$ is a rejecting configuration.

**Th:** $E_\mathsf{LBA}$ is undecidable. 

Let $$\text{All}_\mathsf{CFG} := \{\langle G\rangle \mid \text{$G$ is a $\sf CFG$ and }L(G) = \Sigma^*\}.$$**Th:** $\text{All}_\mathsf{CFG}$ is undecidable. 

**Prop:** $EQ_\mathsf{CFG}$ is undecidable. 

**Prop:** $EQ_\mathsf{CFG}$ is co-Turing-recognisable.

**Def:** Let $\Gamma:= \{\vdash, 0, 1, \textvisiblespace\}$ be the tape alphabet for all Turing machines considered. Define the *busy beaver function* $\text{BB}:\Bbb N\to\Bbb N$ as follows. For each value of $k$, consider the $k$-sate Turing machine that halt when started with a blank tape. Let $\text{BB}(k)$ be the maximum number of $1$'s that remain on the tape among all the machines. 

**Prop:** $\text{BB}$ is not computable function. 