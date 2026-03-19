---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Oracle Machines and Relative Computation]]

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
- The set $\text{Empty} := \{ M \mid L(M ) = \varnothing\}$ is in $\Pi_1^0$, since we can write it as $$\text{Empty} = \{M \mid \forall x\forall t\; M \text{ does not accept }x \text{ in }t \text{ steps.}\}$$, and since the strings and natural numbers are countable then we can just condense it into a single for all that enumerates all of them.
- The set $\text{Total} := \{M \mid M \text{ is total}\}$ is in $\Pi_2^0$, since we can write it as $$\text{Total} = \{M \mid \forall x \exists t \; M\text{ halts on $x$ in $t$ steps}\}. $$
- The set $\text{Fin} := \{M \mid L(M) \text{ is finite}\}$ is in $\Sigma_2^0$, since $$\text{Fin} = \{M \mid \exists n \forall x\forall t  \text{ $|x|\le n$ or $M$ doesn't accept $x$ in $t$ steps}\}. $$
- The set is *cofinite* if its complement is finite. The set $\text{Cofinite} := \{M \mid L(M) \text{ is cofinite}\}$ is in $\Sigma_3^0$, since $$\text{Cofinite} := \{M \mid \exists n \forall x \exists t \; \text{$|x|\le n$ or $M$ accepts $x$ in $t$ steps}\}.  $$
**Def:** $\mathsf{HP}_1 := {\sf HP}$, and let $\mathsf{HP}_{n+1}$ be the halting problem for oracle Turing machines with oracle $\mathsf{HP}_n$, $n \ge 1$; that is  $$\mathsf{HP}_{n+1} := \{M \#x \mid \text{$M$ is an oracle Turing machine $\mathsf{HP}_n$, and $M$ halts on input $x$}\}. $$The oracle need not be represented in the description of the oracle machine $M$. 

**Prop:** We see that $\mathsf {HP}_n \in \Sigma_n^0\setminus \Pi_n^0$.

**Obs:** $\Sigma_n^0\cup \Pi_n^0\subseteq \Delta_{n+1}^0$, and $\Sigma_n^0 \cup \Pi_n^0\neq \Delta_{n+1}^0$. 

### Completeness

**Def:** We say that a set is recursively enumerable-hard if every recursively enumerable set $\le_\text m$-reduces to it. In other words, the set $B$ is recursively enumerable-hard if all recursively enumerable sets $A\le_\text m B$. 

A set $B$ is said to be recursively enumerable-complete if it is both an recursively enumerable set and recursively enumerable-hard.

**Def:** If $\cal C$ is a class of sets, we say that a set is $\le_\text m$-hard for $\cal C$, or just $\cal C$-hard, if $A\le_\text m B$ for all $A\in \cal C$. We say that $B$ is $\le_\text m$-complete for $\cal C$, or just $\cal C$-complete, if $B$ is $\le_\text m$-hard for $\cal C$ and $B\in\cal C$. 

**Th:** If $A\le_\text m B$ and $B\in \Sigma_n^0$, then $A\in \Sigma_n^0$. 

**Th:** If $A\le_\text m B$ and $B\in \Delta_n^0$, then $A\in \Delta_n^0$. 

If $B$ is $\le_\text m$-complete of $\Sigma_n^0$,  then $B\notin \Pi_n^0, \Delta_n^0, \Sigma_{n-1}^0$. 

**Examples:**
- $\sf HP$ is $\le_\text m$-complete for $\Sigma_1^0$,
- $\sf MP$ is $\le_\text m$-complete for $\Sigma_1^0$,
- $\text{Empty}$ is $\le_\text m$-complete for $\Pi_1^0$,
- $\text{Total}$ is $\le_\text m$-complete for $\Pi_2^0$,
- $\text{Fin}$ is $\le_\text m$-complete for $\Sigma_2^0$,
- $\text{Cofinte}$ is $\le_\text m$-complete for $\Sigma_3^0$.

