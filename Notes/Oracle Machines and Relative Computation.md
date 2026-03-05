---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Computation Reducibility]], [[Decidable and Undecidable Problems]]

**Def:** An *oracle* for a language $B$ is an external device that is capable of reporting whether any string $w$ is a member of $B$. An *oracle Turing machine* is a modified Turing machine that has the additional capability of querying an oracle. We write $M^B$ to describe an oracle Turing machine that has an oracle for language $B$. 

Formally, an oracle Turing machine is Turing machine that in addition to its ordinary read/write tape is equipped with a special one-way-infinite read-only input tape on which some infinite string is written. The extra tape is called the *oracle tape*, and the string written on it is the called the *oracle*. The machine can move its oracle tape head one cell in either direction in each step and make decisions based on the symbols written on the oracle tape.

We usually think of an oracle as a specification of a set of strings. If the oracle is an infinite string over $\{0, 1\}$, then we can regard it as the characteristic function of a set $B\subseteq \Bbb N$, where the $n$th bit of the oracle string is $1$ iff $n\in\Bbb N$. In that way we can study computation relative to the set $B$.

**Def:** For $A, B\subseteq \Sigma^*$, we say that $A$ is *recursively enumerable in $B$* if there is an oracle Turing machine $M$ with oracle $B$ such that $A= L(M)$. In addition, if $M$ is total, we write $A\le_\text{T}B$ and say that $A$ is *recursive in $B$* or $A$ *Turing reduces to $B$*, 

**Prop:** The relation $\le_\text T$ is transitive. 

**Th:** If $A\le_\text TB$ and decidable, then $A$ is decidable.

# Arithmetic Hierarchy

Once we have the notion of relative computation, we can define a hierarchy of classes follows. Fix the alphabet $\{0, 1\}$ and identify strings in $\{0, 1\}^*$ with the natural numbers defined by $$x\mapsto \#(1x)-1,$$where $\#y$ is the natural number represented by the binary string $y$. Define
- $\Sigma_1^0 := \{\text{recursively enumerable sets}\},$
- $\Delta_1^0:= \{\text{recursive sets}\},$
- $\Sigma_{n+1}^0 := \{\text{sets recursively enumerable in some }B\in \Sigma_n^0\},$
- $\Delta_{n+1}^0 := \{\text{sets recursive in some }B\in \Sigma_n^0\},$
- $\Pi_n^0:= \{\text{complements of sets in }\Sigma_n^0\}.$
Thus $\Pi_1^0$ is the class of co-recursively enumerable sets. The classes $\Sigma_n^0,\Pi_n^0$, and $\Delta_n^0$ compromise what is known as the *arithmetic hierarchy.*

**Def:** A binary relation $R$ on strings over $\{0, 1\}$ is called *recursive* if the set  $$\{x\#y \mid R(x, y)\} $$is a recursive set. Here $\#$ is just another input symbol other than $0$ or $1$.

**Prop:** A set $A\subseteq\{0, 1\}^*$ is recursively enumerable iff there exists a recursive binary relation $R$ such that $$A = \{x \in \{0, 1\}^*\mid \exists y R(x, y)\}. $$
**Cor:**  set $A\subseteq\{0, 1\}^*$ is co-recursively enumerable iff there exists a recursive binary relation $R$ such that $$A = \{x \in \{0, 1\}^*\mid \forall y R(x, y)\}. $$

**Th:** 
- A set $A$ is in $\Sigma_n^0$ iff there exists a decidable $(n+1)$-ary predicate $R$ such that $$A = \{x\mid \exists y_1\forall y_2 \exists y_3\cdots \mathsf Q y_n \; R(x, y_1, \dots, y_n)\},$$where $\mathsf Q = \exists$ if $n$ is odd, and $\forall$ if $n$ is even.
- A set $A$ is in $\Pi^0_n$ iff there exists a decidable $(n+1)$-ary predicate $R$ such that $$A = \{x\mid \forall y_1\exists y_2 \forall y_3\cdots \mathsf Q y_n \; R(x, y_1, \dots, y_n)\},$$where $\mathsf Q = \forall$ if $n$ is odd, and $\exists$ if $n$ is even.
- $\Delta_n^0 = \Sigma_n^0\cap \Pi_n^0$. 

**Examples:**
- The set $\text{Empty} := \{ M \mid L(M ) = \varnothing\}$ is in $\Pi_1^0$, since we can write it as $\text{Empty} = \{M \mid \forall x\forall t\; M \text{ does not accept }x \text{ in }t \text{ steps.}\}$, and since the strings and natural numbers are countable then we can just condense it into a single for all that enumerates all of them.
- The set $\text{Total} := \{M \mid M \text{ is total}\}$ is in $\Pi_2^0$, since we can write it as $$\text{Total} = \{M \mid \forall x \exists t \; M\text{ halts on $x$ in $t$ steps}\}. $$
- The set $\text{Fin} := \{M \mid L(M) \text{ is finite}\}$ is in $\Sigma_2^0$, since $$\text{Fin} = \{M \mid \exists n \forall x\forall t  \text{ $|x|\le n$ or $M$ doesn't accept $x$ in $t$ steps}\}. $$
- The set is *cofinite* if its complement is finite. The set $\text{Cofinite} := \{M \mid L(M) \text{ is cofinite}\}$ is in $\Sigma_3^0$, since $$\text{Cofinite} := \{M \mid \exists n \forall x \exists t \; \text{$|x|\le n$ or $M$ accepts $x$ in $t$ steps}\}.  $$
**Def:** $\mathsf{HP}_1 := {\sf HP}$, and let $\mathsf{HP}_{n+1}$ be the halting problem for oracle Turing machines with oracle $\mathsf{HP}_n$, $n \ge 1$; that is  $$\mathsf{HP}_{n+1} := \{M \#x \mid \text{$M$ is an oracle Turing machine $\mathsf{HP}_n$, and $M$ halts on input $x$}\}. $$The oracle need not be represented in the description of the oracle machine $M$. 

**Prop:** We see that $\mathsf {HP}_n \in \Sigma_n^0\setminus \Pi_n^0$.

**Obs:** $\Sigma_n^0\cup \Pi_n^0\subseteq \Delta_{n+1}^0$, and $\Sigma_n^0 \cup \Pi_n^0\neq \Delta_{n+1}^0$. 

### Completeness

We say that a set is recursively enumerable-hard if every recursively enumerable set $\le_\text m$-reduces to it. In other words, the set $B$ is recursively enumerable-hard