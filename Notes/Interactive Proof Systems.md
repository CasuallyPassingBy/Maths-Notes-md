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
The Verifier's output is either the next message $m_{i+1}$ in the sequence or *accept* or *reject* designating the conclusion of the interaction. Thus $V$ has the following functional form $V: \Sigma^*\times\Sigma^* \times \Sigma^* \to \Sigma^*\cup\{\text{accept, reject}\}.$ $V(w, r, m_1\# \cdots \# m_i) = m_{i+1}$ means the input string $w$, the random input $r$, the current message history is $m_1$ through $m_i$, and the Verifier's next message to the Prover is $m_{i+1}$.

The *Prover* is a party with unlimited computational ability. We define it to to be the function $P$ with two inputs:
- *Input string*.
- *Partial message history.*
The Prover's output is the next message to the Verifier. Formally $P$ has the form $P: \Sigma^* \times \Sigma^* \to \Sigma^*$. $P(w, m_1\# \cdots \# m_i) = m_{i+1}$ means that the Prover sends $m_{i+1}$ to the Verifier after havinf exchanged messages $m_1$ through $m_i$, so far.

Next we define the interaction between the Prover and Verifier. For particular strings $w$ and $r$, we write $(V \leftrightarrow P)(w,r) = \text{accept}$ if a message sequence $m_1$ through $m_k$ exists for some $k$ whereby
- for $0 \le i < k$, where $i$ is an even number, $V(w, r, m_i\# \cdots \#m_i) = m_{i+1}$;
- for $0 \le i < k$, where $i$ is an odd number, $P(w,  m_i\# \cdots \#m_i) = m_{i+1}$; and
- the final message in the message history is $\text{accept}$.

We assume that the lengths of the Verifier's random unput and each of the messages exchanged between the Verifier's random input and each of the messages exchanged between the Verifier and Prover are $p(n)$ for some polynomial that only depends on the Verifier. Furthermore we assume that the total number of messages exchanged is at most $p(n)$. The following definition gives the probability that an interactive proof system accepts an input string $w$. For any string $w$ of length $n$, we define$$P(V \leftrightarrow P \text{ accepts }w) := P[(V \leftrightarrow P)(w, r) = \text{accept}]. $$where $r$ is a randomly selected string of length $p(n)$.

**Def:** Say that language $A$ is in $\sf IP$ if some polynomial time function $V$ and arbitrary function $P$ exists, where for every function $\tilde P$ and string $w$
1. $w\in A$ implies $P(V \leftrightarrow P \text{ accepts }w) \ge \frac23$, and 
2. $w\notin A$ implies $P(V \leftrightarrow \tilde P \text{ accepts }w) \le \frac 13$. 

We may amplify the success probability of an interactive proof system by repetition, as we did in the amplification lemma for bounded probabilistic polynomial time problems to make error probability exponentially small. 

We see that $\sf NP$ and $\sf BPP$ are both contained in $\sf IP$.

**Lemma:** $\sf IP \subseteq PSPACE$. 

**Def:** The *counting problem* for satisfiability to be the language $$\#\text{SAT} := \{\langle \phi, k\rangle \mid \text{$\phi$ is a cnf-formula with exactly $k$ satistying asssignments}\}.$$
**Th:** $\#\text{SAT}\in \sf IP$. 
