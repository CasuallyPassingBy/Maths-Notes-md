---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Computation Reducibility]]

Let's begin by making a Turing machine that ignores its input and prints out a copy of its own description. We call this machine $\text{SELF}$. 

**Lemma:** There is a computable function $q:\Sigma^*\to\Sigma^*$. where if $w$ is any string $q(w)$ is the description of a Turing machines $P_w$ that prints out $w$ and then halts. 

The Turing machine $\text{SELF}$ is in two parts $A$ and $B$. We think of $A$ and $B$ as being two separate procedures that go together to make up $\text{SELF}$. We wan to $\text{SELF}$ to print $\langle \text{SELF}\rangle = \langle AB\rangle$. 

Part $A$ runs first and upon completion passes control to $B$. The job is to printout a description of $B$, and conversely the job of $B$ is to print out a description of $A$. 

For $A$ we use the machine $P_{\langle B \rangle}$, described by $q(\langle B\rangle)$, which is the result of applying the function $q$ to $\langle B\rangle$. Thus part $A$ is a Turing machine that prints out $\langle B\rangle$. 

We might be tempted to define $B$ with $q(\langle A\rangle)$, but that doesn't make sense. This is because we would get a circular definition. Instead, we define $B$ so that it prints $A$ using a different strategy: $B$ *computes* $A$ from the output that $A$ produces. 

We defined $\langle A\rangle$ to be $q(\langle B\rangle)$. If $B$ can obtain $\langle B\rangle$, it can apply $q$ to that an obtain $\langle A\rangle$. $B$ only needs to look at the tape to obtain $\langle B\rangle$. Then after $B$ computes $q(\langle B\rangle) =\langle A\rangle$, it combines $A$ and $B$ into a single machines and writes its description $\langle AB\rangle = \langle \text{SELF}\rangle$ on the tape. In summary we have
- $A = P_{\langle B\rangle}$, and
- $B =$ "On input $\langle M\rangle$, where $M$ is a portion of a Turing machine:
	1. compute $q(\langle M\rangle)$.
	2. Combine the result with $\langle M\rangle$ to make a complete Turing machine.
	3. Print the description of this Turing machine and halt."

**Recursion Theorem:** Let $T$ be a Turing machine that computes the function $t:\Sigma^* \times \Sigma^* \to\Sigma^*$. There is a Turing machine $R$ that computes a function $r: \Sigma^*\to \Sigma^*$, where for every $w$, $$r(w)= t(\langle R\rangle, w).  $$
We construct a Turing machine $R$ in three parts, $A, B$ and $T$, where $T$ is given by the statement of the theorem;. Here $A$ is the Turing machine $P_{\langle BT\rangle}$ described by $q(\langle BT\rangle)$. To preserve the input $w$, we design $P_{\langle BT\rangle}$ writes its output following any string preexisting on the tape. After $A$ runs, the tape contains $w\langle BT\rangle$. Again $B$ is a procedure that examines its tape and applies $q$ to its contents. The result is $\langle A\rangle$. Then $B$ combines $A, B$ and $YT$ into a single machine and obtains its description $\langle ABT\rangle = \langle R\rangle$. Finally, it encodes that description together with $w$, places the resulting string $\langle R, w\rangle$ on the tape, and passes control to $T$.

The recursion theorem states that Turing machines can obtain their own description and then go on to compute with it. 

We can use the recursion theorem in the following way when designing Turing machine algorithms. If we are designing a machine $M$, you can include the phrase "obtain own description $\langle M \rangle$" in the informal description of $M$'s algorithm. Upon having obtained its own description, $M$ can then go on tu use it as it would use any other computed value. 

### Applications

A *computer virus* is a computer program that is designed to spread itself among computers. Computer viruses are inactive when standing alone as a piece of cod, but when places appropriately in a host computer, thereby 'infecting' it, they can become activated and transmit viruses, including the Internet and transferable machines. In order to carry out its primary task of self-replication, a virus may contain the construction described in the proof of the recursion theorem. 

**Th:** $A_\mathsf{TM}$ is undecidable.
**Proof:** We assume that Turing machine $H$ decides $A_\mathsf{TM}$, for the purposes of obtaining a contradiction. We construct the following machine $B$.
$B =$ "on input $w$:
1. Obtain, via the recursion theorem, own description $\langle B\rangle$.
2. Run $H$ on input $\langle B, w\rangle$.
3. Do the opposite of what $H$ says. That is, *accept* if $H$ rejects and *reject* if $H$ accepts"
Running $B$ on input $w$ does the opposite of what $H$ declares. Therefore $H$ cannot be deciding $A_\mathsf{TM}$.