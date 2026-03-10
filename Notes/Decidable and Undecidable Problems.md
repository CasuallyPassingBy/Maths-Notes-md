---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Strings and Languages]], [[Context-Free Languages]], [[Finite Automaton]], [[Context-Free Grammars]], [[Turing Machines]]

## Decidable Problems Concerning Regular Languages

We begin with certain computational problems concerning finite automata. Note that we chose to represent various computational problems by languages. Doing so is convenient because we have already set up terminology for dealing with languages. 

The *acceptance problem* for $\sf DFA$s of testing whether a particular finite automaton accepts a given string can be expressed as a language, $A_{\sf DFA}$. This language contains the encodings of all $\sf DFA$s together with strings that $\sf DFA$s accept. Let $$A_{\sf DFA} := \{\langle B, w\rangle \mid B \text{ is a $\sf DFA$ that accepts the input string }w\}.  $$
The problem of testing whether a $\sf DFA$ $V$ accepts an input $W$ is the same as the problem of whether $\langle B, w\rangle$ is a member of the language $A_{\sf DFA}.$ 

Similarly, we can formulate other computational problems in terms of testing membership of a language. Showing that a language is decidable is the same as showing that the computational problem is decidable. 

**Th:** $A_{\sf DFA}$ is a decidable language.

We can prove a similar theorem for nonderterministic finite automaton. Let $$A_{\sf NFA} := \{\langle B, w\rangle \mid B \text{ is a $\sf NFA$ that accepts the input string }w\}.  $$
**Th:** $A_\mathsf{NFA}$ is a decidable language.

Similarly, we can determine whether a regular expression generates a given string. Let $$A_{\sf REX} := \{\langle R, w\rangle \mid R \text{ is a regular expression that generates a string }w\}. $$

**Th:** $A_\mathsf{REX}$ is a decidable language.

We see that the theorems above illustrate, for decidability porpuses, presenting a Turing machine with $\sf DFA$, $\sf NFA$, or regular expression are all equivalent because the machine is able to convert one form of encoding to another. 

Now we turn to a different kind of problem concerning finite automata: *emptiness testing* for a language of a fintie automaton. In the preceding three theorems we had to determine whether a finite automaton accepts a particular string. Let $$E_\mathsf{DFA} := \{\langle A \rangle \mid A \text{ is a $\sf DFA$ and } L(A) = \varnothing\}.$$

**Th:** $E_\mathsf{DFA}$ is a decidable language. 

The next theorem states that determining whether two $\sf DFA$s recognise the same language is decidable. Let $$EQ_\mathsf{DFA} := \{\langle A,B \rangle\mid \text{$A$ and $B$ $\sf DFA$s and }L(A) = L(B)\}.  $$
**Th:** $EQ_\mathsf{DFA}$ is a decidable language.

Let $$\text{Inf}_\sf{DFA} := \{\langle A\rangle \mid \text{$A$ is a $\sf DFA$ and $L(A)$ in an infinite language}\}.  $$
**Prop:** $\text{Inf}_{\sf DFA}$ is a decidable language.

# Decidable Problems Concerning Context-Free Languages

Here, we describe algorithms to determine whether a $\sf CFG$ generates a particular string and to describe whether the a language of a $\sf CFG$ is empty. Let $$A_\mathsf{CFG} := \{\langle G, w\rangle \mid \text{ $G$ is a $\sf CFG$ that generates a string $w$}\}.$$
**Th:** $A_\mathsf{CFG}$ is a decidable language.

Since we know how to convert between $\sf CFG$s and $\sf PDA$s, then everything we say about the decidability of problems concerning $\sf CFG$s applies equally well to $\sf PDA$s.

Let's turn now to the emptiness testing problem for the language of a $\sf CFG$. As we did for $\sf DFA$s, we can shoe that the problem of determining whether a $\sf CFG$ generates any string at all is decidable. Let $$E_\mathsf{CFG} :=\{\langle G\rangle \mid \text{$G$ is a $\sf CFG$ and $L(G) = \varnothing$}\}.$$
**Th:** $E_\mathsf{CFG}$ is a decidable language. 

Let  $$EQ_\mathsf{CFG} :=\{\langle G, H\rangle \mid \text{ $G$ and $H$ are $\sf CFG$s and $L(G) = L(H)$}\}. $$
**Th:** $EQ_\mathsf{CFG}$ is not a decidable language.

**Th:** Every context-free language is decidable. 

Let $$C_\mathsf{REX} := \{\langle R, S\rangle \mid \text{$R$ and $S$ are regular expressions and }L(R) \subseteq  L(S)\}.  $$
**Prop:** $C_\mathsf{REX}$ is a decidable language.

Let $$\text{Inf}_\sf{PDA} := \{\langle A\rangle \mid \text{$A$ is a $\sf PDA$ and $L(A)$ in an infinite language}\}.  $$**Prop:** $\text{Inf}_{\sf PDA}$ is a decidable language.

# The Halting Problem

**Obs:** We know that every Turing machine can be encoded using a string, and the set of strings, $\Sigma^*$, is countable for every alphabet $\Sigma$; thus, the set of Turing machines is countable. 

**Cor:** Some languages are not Turing-recognisable. Most languages are not Turing-recognisable.

**Def:** Let $$A_\mathsf{TM} := \{\langle M, w\rangle \mid \text{$M$ is a Turing machine and $M$ accepts $w$}\}.  $$
**Th:** The language $A_\mathsf{TM}$ is not Turing-decidable. 

**Th:** A language is decidable iff it is Turing-recognisable and co-Turing-recognisable. 

**Cor:** $\overline{A_\mathsf{TM}}$ is not Turing-recognisable.  

Let $$H_\mathsf{TM} := \{\langle M, w\rangle \mid \text{$M$ is a Turing machine and $M$ halts on $w$}\}.$$Note that $A_\mathsf{TM}\subseteq H_\mathsf{TM}$.

**Th:** The language $H_\mathsf{TM}$ is not Turing-decidable. 