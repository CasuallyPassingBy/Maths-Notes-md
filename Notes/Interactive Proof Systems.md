---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[The Complexity Class PSPACE]], [[The Complexity Class NP]], [[The Complexity Class BPP]], [[Probabilistic Algorithms in Complexity Theory]]

Interactive proof systems provide a way to define a probabilistic analogue of the class $\sf NP$, much as probabilistic polynomial time algorithms provide a probabilistic analogue to $\sf P$. The development of interactive proof systems has profoundly affected complexity theory and has lead to important advances in the fields of cryptography and approximation algorithms.

We can rephrase the formulation of $\sf NP$ by creating two entities: a Prover that finds the proofs of membership and a Verifier that checks them. Think of the Prover as if were convincing the Verifier of $w$'s membership in $A$. We require the Verifier to be a polynomial time bounded machine; otherwise it could figure out the answer itself. We don't impose any computational bound on the Prover because finding the proof may be time-consuming.

We need that the Prover and Verifier have two additional features. First, they are permitted to engage in *two-way* dialogue. Second, the Verifier may be a *probabilistic* polynomial time machine that reaches the correct answer with a high degree of, but not absolute, certainty. Such a Prover and Verifier constitute an interactive proof system.

# Definition of the Model

We define the *Verifier* to be a function $V$ that computes its next transmission to the Prover from the message history sent to so far. The function $V$ has three inputs:
- *Input string.*
- *Random Input.*
- *Partial message history.*

The Verifier's output is either the next message $m_{i+1}$ in the sequence or *accept* or *reject* designating the conclusion of the interaction. Thus 