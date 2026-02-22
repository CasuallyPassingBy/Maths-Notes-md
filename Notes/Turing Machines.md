---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Finite Automaton]], [[Nondeterministic Pushdown Automata]], [[Deterministic Pushdown Automata]], [[Two-Way Finite Automata]], [[Decidable and Undecidable Problems]]

**Def:** A *Turing machine* is $9$-tuple $(Q, \Sigma, \Gamma,\textvisiblespace, \vdash, \delta, s, q_\text{accept}, q_\text{reject})$, where $Q$, $\Sigma$ and $\Gamma$ are finite sets and
- $Q$ is the set of states,
- $\Sigma$ is the input alphabet no containing the *blank symbol* $\textvisiblespace$,
- $\Gamma$ is the tape alphabet,
- $\textvisiblespace\in \Gamma\setminus\Sigma$, the *blank symbol*,
- $\vdash\in \Gamma\setminus \Sigma$, the *left endmarker*,
- $\delta: Q \times \Gamma \to Q \times \Gamma \times \{L, R\}$ is the transition function,
- $s\in Q$ is the start state,
- $q_\text{accept}\in Q$ is the state, and
- $q_\text{reject}\in Q$, the *reject state*, $q_\text{accept}\neq q_\text{accept}$
Intuitively, $\delta(p,a ) = (q, b, d)$ means, 'when it state $p$ scanning symbol $a$, write $b$ in that tape cell, and move the head in direction $d$, and entre state $q$'. The symbols $L$ and $R$ stand for left and right. 

We restrict Turing Machines so that the left endmarker is bever overwritten with another symbol and the machine never leaves off the tape to the left of the endmarker. Meaning, we requiere for all $p\in Q$ there exists $q\in Q$ such that $$\delta(p, \vdash) = (q, \vdash, R).$$We also require that once the machine entres it accept state, it never leaves it, similarly, for the reject state; that is for all $b\in\Gamma$ there exist $c, c'\in\Gamma$ and $d, d'\in \{L, R\}$ such that
- $\delta(q_\text{accept}, b) = (q_\text{accept}, c, d)$
- $\delta(q_\text{reject}, b) = (q_\text{reject}, c', d')$.
We sometimes refer to the state set and transition function collectively as the *finite control.*

At any point in time, the read/write tape of the Turing machine $M$ contains a semi-infinite string of the form $y\textvisiblespace^\omega$, where $y\in \Gamma^*$, and $\textvisiblespace^\omega$ denotes the semi-infinite string, $$\textvisiblespace^\omega := \textvisiblespace \textvisiblespace\textvisiblespace\textvisiblespace\cdots.$$Although the string is infinite, it always have a finite representation, since all but finitely many of the symbols are the blank symbol $\textvisiblespace$.

**Def:** We define a *configuration* to be an element $Q\times \{y \textvisiblespace^\omega\mid y\in\Gamma^*\}\times \Bbb N$. A configuration is a global state giving a snapshot of all relevant information about a Turing machine computation at some instant time. The configuration $(p, z, n)$ specifies a current state $p$ of the finite control, current tape contents $z$, and current position of the read/write head $n \ge 0$. We usually denote configurations by $\alpha,\beta, \gamma$.

The *start configuration* on input $x\in \Sigma^*$ is the configuration $$(s, \vdash x\textvisiblespace^\omega, 0).  $$
One can define a *next configuration relation* $\xrightarrow[\, M\,]{1}$ as with $\sf PDA$S. For a string $z\in \Gamma^\omega$, let $z_n$ be the $n$th symbol of $z$, and let $\text s^n_b (z)$ denote the string obtained from $z$ by substituting $b$ for $z_n$ at position $n$. 

The relation $\xrightarrow[\, M\,]{1}$ is defined by  $$(p, z, b) \xrightarrow[\, M\,]{1} \begin{cases} (q, \text s_b^n(z), n-1) & \text{if }\delta(p, z_n) = (q, b, L), \\(q, \text s_b^n(z), n+1) & \text{if }\delta(p, z_n) = (q, b, R). \end{cases} $$
We define the reflexive transitive closure $\xrightarrow[\, M\,]{*}$ of $\xrightarrow[\, M\,]{1}$, inductively, as usual:
- $\alpha \xrightarrow[\, M\,]{0} \alpha$,
- $\alpha \xrightarrow[\, M\,]{n+1}\beta$ if there is a configuration $\gamma$ such that $\alpha \xrightarrow[\, M\,]{n}\gamma$ and $\gamma \xrightarrow[\, M\,]{1}\beta$,
- $\alpha \xrightarrow[\, M\,]{*}\beta$ if $\alpha \xrightarrow[\, M\,]{n}\beta$ for some $n \ge 0$.

The machine $M$ is said to *accept* input $x\in \Sigma^*$ if $$(s, \vdash x\textvisiblespace^\omega, 0) \xrightarrow[\,M\,]{*} (q_\text{accept}, y, n), $$for some $y$ and $n$, and *reject* $x$ if $$(s, \vdash x\textvisiblespace^\omega, 0) \xrightarrow[\,M\,]{*}(q_\text{reject}, y, n), $$for some $y$ and $n$. It is said to *halt* on input $x$ if either accepts $x$ or rejects $X$. It is possible that it neither accepts nor rejects, in which case is said to *loop* on input $x$, A Turing machine is said to be *total* if it halts on all inputs; we also call these machines *deciders*. The set $L(M)$ denotes the set of strings accepted by $M$.

We call a set of strings
- *recursively enumerable*, r.e., or *Turing-recognisable* if it is $L(M)$ for some Turing machine $M$,
- *co-r.e.* or *co-Turing-recognisable* if its complement is r.e., and
- *recursive*, *Turing-decidable*, or *decidable* if it is $L(M)$ for some *total* Turing machine $M$.

**Obs:** If $A$ is a Turing-recognisable language and $\Sigma^*\setminus A$ is also a Turing-recognisable, then both $A$ and $\Sigma^*\setminus A$ is Turing-decidable. 

**Prop:** The collection of decidable languages are closed under the operation of 
- union
- concatenation
- star
- complements
- intersection

**Prop:** The collection of Turing-recognisable languages is closed under the operations
- union
- concatenation
- star 
- intersection

**Prop:** Every infinite Turing recognisable language has an infinite decidable subset. 

**Prop:** A single-tape Turing machine that cannot write is computationally equivalent to [[Two-Way Finite Automata]], and thus can only recognise regular languages. 

**Def:** A property $P$ of strings is said to be *decidable* if the set $\{x\in \Sigma^* \mid x\text{ satisfies }P \}$ is Turing-decidable. A property $P$ is said to be *semidecidable* if the set $\{x\in \Sigma^* \mid x\text{ satisfies }P \}$ is Turing-recognisable. 

We see that there's a nice relationship between the terms
- $P$ is decidable iff $\{x\mid P(x)\}$ is recursive or decidable. 
- $A$ is recursive or decidable iff $\text “x\in A\text"$ is decidable.
- $P$ is semidecidable iff $\{x\mid P(x)\}$ is Turing-recognisable.
- $A$ is Turing-recognisable iff $\text “x\in A\text"$ is semidecidable. 

There are other [[Models Equivalent to Turing Machines]]. 

# Universal Turing Machine

A crucial observation about the power of Turing machines: there exist Turing machines that can simulate other Turing machines whose descriptions are presented as part of the input.

First we need to fix a reasonable encoding scheme for Turing machines over the alphabet $\{0, 1\}$. This encoding scheme should be simple enough that all the data associated with the machine $M$ can be interpreted easily by another machine reading the encoded description of $M$. For example, if the string begins with the prefix $$0^n10^m10^k10^s10^t10^r10^u10^v1$$this might indicate that the machine has $n$ states represented by the numbers $0$ to $n-1$; it has $m$ tape symbolds represented by the numbers $0$ to $m-1$, of which the first $k$ represent input symbols; the start, accept, and reject state are $s$, $t$ and $r$, respectively; and the endmerker and blank symbol are $u$ and $v$ respectively, The remainder of the string can consist of a sequence of substrings specifying the transitions in $\delta$. For example, the substring $$0^p10^a10^q10^b10$$might indicate that $\delta$ contains the transition $$(p, a) \to (q, b,L),$$the direction to move the head encoded by the final digit. 

The exact details of the encoding scheme are not important. The only requirements are that it should be easy to interpret and able to encode all Turing machines up to isomorphism. 

Once have a suitable encoding for Turing machines, we can construct a *universal Turing machine* $U$ such that$$L(U) := \{M \# x\mid x\in L(M)\}.  $$In other words, presented with an encoding over $\{0, 1\}$ of a Turing machines $M$ and and encoding over $\{0, 1\}$ of a string $x$ over $M$'s input alphabet, the machines $U$ *accepts* $M\# x$ iff $M$ accepts $x$. The symbol $\#$ is just a symbol in $U$'s input alphabet other than $0$ and $1$ used to delimit $M$ and $x$. 

The machine $U$ first checks its input $M\#x$ to make sure that $M$ is a valid encoding of a Turing machine and $x$ is a valid encoding of a string over $M$'s input alphabet. If not, it rejects.

If the encodings of $M$ and $x$ are valid, the machine $U$ does a step-by-step simulation of $M.$ This might work as follows. The tape $U$ is partitioned into $3$ tracks. The description of $M$ is copied to the top track and the string $x$ to the middle track. the middle track will be used to hold the simulated contents of $M$'s tape. The bottome track will be used to remember the current state of $M$ and the current position of $M$'s read/write head. The machine $U$ then simulates $M$ on input $x$ one step at a time, shuttling back and forth beween the description on its top track and the simulated contents of $M$'s tape on the middle track. In each step, it updates $M$'s state and simulated tape contents as dictated as dictated by $M$'s transititons function, which $U$ can read from the description of $M$. If $M$ halts and accepts or halts and rejects, then $U$ does the same. Note that if $M$ loops on $x$, then $U$ does the same.

In general, each step of $M$ may requiere many steps of $U$ to simulate. 

## Undecidability of the Halting Problem

Since the universal machine $U$ doesn't do any fancy analysis on the machine $M$ to try to determine whether or not it will halt. It just blindly simulates $M$ step by step. If $M$ doesn't halt on $x$, then $U$ will just go on happily simulating $M$ forever. 

It is natural ask whether we can do better than just blind simulation. Might there be a way to analyse $M$ to determine in advance, before doing the simulation, whether $M$ to determine in advance, before the simulation, whether $M$ would eventually halt on $x$. If $U$ could say for sure in advance that $M$ would not halt on $x$, then it could skip the simulation and save itself a lot of useless work. On the other hand, if $U$ could ascertain that $M$ *would* eventually halt on $x$, then it could go ahead with the simulation to determine whether $M$ accepts or rejects. We could then build then a machine $U'$ that takes as input an encoding of a Turing machines and a string $x$, and
- halts and accepts if $M$ halts and accepts $x$,
- halts and rejects if $M$ halts and rejects $x$, and
- halts and rejects if $M$ loops on $x$.

This would say that $L(U') = L(U) = {\sf MP} := \{M \#x \mid x\in L(M)\}$ is a recursive set.

Unfortunately, this is not possible in general. There are certain machines for which it is possible to determine halting by some heuristic or other. However is no general method that gives the right answer for all machines.

We can prove this Cantor's diagonalisation technique. For $x\in\{0, 1\}^*$, let $M_x$ be the Turing machine with input alphabet $\{0, 1\}$ whose encoding over $\{0, 1\}^*$ is $x$. In this way we get a list $$M_\varepsilon, M_0, M_1, M_{00}, M_{01}, M_{10}, M_{11}, M_{000}, M_{001},\cdots$$containing all possible Turing machines with input alphabet $\{0, 1\}$ indexed by strings in $\{0, 1\}^*$. We make sure that the encoding scheme is simple enough that a universal machine can determine $M_x$ from $x$ for the purpose of simulation.

Now we consider an infinite two-dimensional matrix indexed along the top by strings in $\{0, 1\}^*$ and down by the left by Turing machines in the list above. The matrix contains $\sf H$ in position $x, y$ if $M_x$ halts on input $y$ and $\sf L$ if $M_x$ loops on input $y$. 

The $x$th row of the matrix describes for each input string whether or not $M_x$ halts on $y$. 

Suppose, for the sake of a contradiction, that there existed a *total* machine $K$ accepting the set $\sf HP := \{M \# x\mid M \text{ halts on }x\}$; that is, a machine for a given $x$ and $y$ could determine the $x, y$th entry of the table described in finite time. Thus on input $M\# x$,
- $K$ halts and accepts if $M$ halts on $x$, and 
- $K$ halts and rejects if $M$ loops on $x$. 

Now we consider a machine $N$ that on input $x\in \{0, 1\}^*$
- constructs $M_x$ from $x$ and write $M_x\# x$ on its tape;
- runs $K$ on input $M_x\# x$, accepting if $K$ rejects and going into a trivial loop if $K$ accepts. 
Note that $N$ is essentially complementing the diagonal of the matrix described. Then for any $x\in\{0, 1\}^*$,
$$N \text{ halts on $x$} \iff K \text{rejects }M_x \#x \iff M_x \text{loops on $x$.}$$
This says that $N$'s behaviour is different from every $M_x$ on at least one string, namely $X$. But the list was supposed to contain all Turing machines over the input alphabet $\{0, 1\}$, including $N$. Which means $N$ is different from itself, which is a contradiction. 

This means that ${\sf HP}$ must not be decidable. 
## Undecidability of the Halting Problem

The membership problem is also undecidable. We can show this by reducing the halting problem to it. In other words, we show that if there a way to decide the member ship in general, we could use this as a subroutine to decide the halting problem in general. This means that the membership is equivalent to the halting problem, so it must be undecidable. 