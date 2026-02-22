---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Strings and Languages]], [[Decidable and Undecidable Problems]]

A *reduction* is a way of converting one problem to another problem in such a way that a solution to the second problem can be used to solve the first problem. Reducibility always involves two problems, which we call $A$ and $B$. If $A$ reduces to $B$, we can use a solution to $B$ to solve $A$. 

Reducibility plays an important role in classifying problems by decidability and complexity theory. When $A$ is reducible to $B$, solving $A$ cannot be harder than solving $B$ because a solution to $B$ gives a solution to $A$. This means that if $A$ is reducible to $B$, the the following statements are true.
- If $B$ is decidable, then $A$ is also decidable.
- If $A$ is undecidable, then $B$ is also undecidable. 

Let $$H_\mathsf{TM} := \{\langle M, w\rangle \mid \text{$M$ is a Turing machine and $M$ halts on $w$}\}.$$Note that $A_\mathsf{TM}\subseteq H_\mathsf{TM}$.

**Th:** The language $H_\mathsf{TM}$ is not Turing-decidable. 

The theorem illustrates our strategy for proving that a problem is undecidable, This strategy is common to most proofs of undecidability, except for the undecidability of $A_\mathsf{TM}$ itself.

Let $$E_{\sf TM} := \{\langle M\rangle \mid \text{$M$ is a Turing machine and }L(M) = \varnothing\}.$$

**Th:** $E_\mathsf{TM}$ is undecidable. 

Another interesting computational problem regarding Turing machines concerns determining whether a given Turing machine recognises a language that also can be recognised by a simpler computational model. Let $$\text{Reg}_\mathsf{TM} := \{\langle M \rangle \mid \text{$M$ is Turign machine and $L(M)$ is a regular language}\}.  $$
**Th:** $\text{Reg}_\mathsf{TM}$ is a undecidable, 

Let $$EQ_\mathsf{TM} := \{\langle M_1, M_2\rangle \mid \text{$M_1$ and $M_2$ are Turing mahcines and }L(M_1) = L(M_2)\}.$$
**Th:** $EQ_\mathsf{TM}$ is undecidable.

# Reductions via Computations Histories

**Def:** Let $M$ be a Turing machine and $w$ an empty string. An *accepting computation history* for $M$ on $w$ is a sequence of configurations $C_1, C_2, \dots C_\ell$, where $C_1$ is the start configurations of $M$ on $w$, $C_\ell$ is the accepting configuration of $M$. A *rejecting configuration history* for $M$ on $w$ is defined similarly, except that $C_\ell$ is a rejecting configuration.

