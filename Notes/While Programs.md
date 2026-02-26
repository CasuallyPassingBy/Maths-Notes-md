---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Other Formalisms Equivalent to General Computation]], [[Turing Machines]], [[Gödel Recursive Functions]]

We can relate the primitive and $\mu$-recursive and functions of Gödel to more modern concepts. Consider a simple programming language with variables $\text{Var} := \{x, y,\dots\}$ ranging over $\Bbb N$ containing the following constructs:
1. *simple assignments*: $x := 0\quad x := y+1 \quad x:= y$
2. *sequential composition:* $p\; ; q$
3. *conditional:*  $\text{if }x <y \text{ then } p \text{ else }q$
4. *for loop:* $\text{for }y \text{ do }p$
5. *while loop:* $\text{while }x <y \text{ do } p$

In $3.$ and $5.$, the relation $<$ can be replaced by any of $>, \ge, \le, =$, or $\ne$. In $2.$ we can parenthesise using $\text{begin}\dots \text{end}$ if necessary.

Programs built inductively from these constructs are called the $\text{while}$ programs. Programs built without the $\text{while}$ construct $5.$ are called *for programs*. 

The intuitive operation of the for loop is as follows: upon entering the loop $\text{for }y \text{ do }p$, the current value of variable $y$ is determined, and the program $p$ is executed that many times. Assignment to the variable $y$ within the body of the loop does not change the number of times the loop is executed, nor does execution of the body of the loop alone decrement or change its value in any way except by explicit assignment. 

The intuitive operation of the while loop is as follows: upon entering the loop $\text{while }x <y \text{ do }p$, then the condition $x<y$ is tested with the current values of the variables $x, y$. If the condition is false, then the body of the loop is not executed, and control passes through to the statement following the $\text{while loop}$. If the condition is true, then the body $p$ of the loop is executed once, and then the procedure is repeated with the new values of $x, y$. If the condition always test true, then the $\text{while}$ loop never halts. 

In the presence of the $\text{while loop}$, the $\text{for loop}$ is redundant: $\text{for }y \text{ do }p$ is simulated by the $\text{while program}$ $$z := 0; w:= y; \text{ while }z < w \text{ do begin } p; z= z+1\text{ end}  $$where $z$ and $w$ are variables not occurring in $p$. However, note that for programs shall always halt. The the only source of potential nontermination is the $\text{while}$ loop.

# Semantics of $\text{While}$ Programs

**Def:** A *state* or *environments* $\sigma$ is an assignment of a nonnegative integer to each variables in $\text{Var}$; that is $\sigma:\text{Var}\to\Bbb N$. The set of all such environments is denoted $\text{Env}$. If a program started in the initial environment $\sigma$, then in the course of the execution, the values of the variables will be changed, so that if and when the program halts, the final environment will in general be different from $\sigma$. We thue interpret programs $p$ as *partial functions* $[\![p]\!]: \text{Env}\to \text{Env}$. The value $[\![p]\!](\sigma)$ is the final environment after executing the program $p$ with initial environment $\sigma$, provided $p$ halts. If $p$ doesn't halt when started in initial environment $\sigma$, then $[\![p]\!](\sigma)$ is undefined. Thus $[\![p]\!]: \text{Env}\to \text{Env}$ is an partial function; its domain is the set of $\sigma$ causing $p$ to halt. 

Formally, the meaning $[\![p]\!]$ of a while program $p$ is defined inductively as follows. For $\sigma\in \text{Env}$, $x\in \text{Var}$, and $a \in\Bbb N$, let $\sigma[x← a]$ denote the environment that is identical to $\sigma$ except to $\sigma$ for the value of $x$, which is $a$. Formally, $$\begin{align*}
\sigma[x←a](y) &:= \sigma(y), \qquad \text{ if $y$ is not $x$}, \\
\sigma[x←a](x) &:= a.
\end{align*}   $$Let $[\![p]\!]^n$ denote the $n$-fold composition of the partial function $[\![p]\!]$. Formally, $$\begin{align*}[\![p]\!]^0(\sigma) &:= \sigma, \\
[\![p]\!]^{n+1}(\sigma)&= [\![p]\!]([\![p]\!]^n(\sigma)).\end{align*}$$We now define $$\begin{align*}
[\![x := 0]\!] (\sigma) &:= \sigma[x←0], \\
[\![x := y]\!] (\sigma) &:= \sigma[x←y], \\
[\![x := y+1]\!] (\sigma) &:= \sigma[x←\sigma(y)+1], \\
[\![p\;; q]\!] (\sigma) &:= [\![q]\!]([\![p]\!](\sigma)) , \\
[\![p\;; q]\!]  &:= [\![q]\!]\circ [\![p]\!], \\ \\
[\![\text{if }x < y \text{ then }p \text{ else }q]\!](\sigma) &:= \begin{cases}
	[\![p]\!](\sigma) & \text{if }\sigma(x) <\sigma(y), \\
	[\![q]\!] & \text{otherwise,}
\end{cases}
\\ \\
[\![\text{for $y$ do }p]\!](\sigma) &:= [\![p]\!]^{\sigma(y)}(\sigma),
\end{align*}$$
and $$
[\![\text{while $x<y$ do }p]\!](\sigma) := 
\begin{cases}
	[\![p]\!]^n(\sigma) & \text{if $n$ is the least number such that $[\![p]\!]^n(\sigma)$ is defined and $[\![p]\!]^n(\sigma)(x)\ge [\![p]\!]^n(\sigma)(y)$} \\
	\text{undefined} & \text{if no $n$ exists.}
\end{cases}
$$
**Th:** 
- For every $\mu$-recursive function $f: \Bbb N^n \to \Bbb N$, there is a $\text{while}$ program $p$ such that for any environment $\sigma$, $[\![p]\!]^n(\sigma)$ is defined iff $f(\sigma(x_1),\dots, \sigma(x_n))$ is defined; and if both are defined, then $$[\![p]\!]^n(\sigma)(x_0) = f(\sigma(x_1),\dots, \sigma(x_n)).$$
- For every $\text{while}$ program $p$ with variables $x_1,\dots, x_n$ only there are $\mu$-recursive functions $f_i: \Bbb N^n\to \Bbb N$, $1\le i \le n$, such that for any environment $\sigma$, $[\![p]\!]^n(\sigma)$ is defined iff $f_i(\sigma(x_1),\dots, \sigma(x_n))$ is defined, $1\le i \le n$; and if all are defined then  $$f_i(\sigma(x_1),\dots, \sigma(x_n)) = [\![p]\!]^n(\sigma)))(x_i),\qquad 1\le i\le n.$$

**Th:** 
- For every primitive recursive function $f: \Bbb N^n \to \Bbb N$, there is a $\text{for}$ program $p$ such that for any environment $\sigma$, $[\![p]\!]^n(\sigma)$ is defined iff $f(\sigma(x_1),\dots, \sigma(x_n))$ is defined; and if both are defined, then $$[\![p]\!]^n(\sigma)(x_0) = f(\sigma(x_1),\dots, \sigma(x_n)).$$
- For every $\text{for}$ program $p$ with variables $x_1,\dots, x_n$ only there are primitive recursive functions $f_i: \Bbb N^n\to \Bbb N$, $1\le i \le n$, such that for any environment $\sigma$, $[\![p]\!]^n(\sigma)$ is defined iff $f_i(\sigma(x_1),\dots, \sigma(x_n))$ is defined, $1\le i \le n$; and if all are defined then  $$f_i(\sigma(x_1),\dots, \sigma(x_n)) = [\![p]\!]^n(\sigma)))(x_i),\qquad 1\le i\le n.$$

This proves that almost every single programming language is equivalent to a Turing machine (given infinite memory). 

**Note:** This equivalence is about _computability_ (what can be computed), not _complexity_ (how fast). While a While-program can simulate a TM, the translation often involves an exponential blow-up in steps if not handled carefully.