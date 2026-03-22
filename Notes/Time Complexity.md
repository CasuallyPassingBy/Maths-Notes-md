---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Asymptotic Notation]], [[Decidable and Undecidable Problems]], [[Models Equivalent to Turing Machines]]

Even when a problem is decidable and thus computationally solvable in principle, it may not be solvable in practice if the solution requires an inordinate amount of time or memory.

The number of steps that an algorithm uses on a particular input may depend on several parameters. For simplicity we compute the running time of an algorithm purely as a function of the length of the parameters of the string representing the input and don't consider any other parameters. In *worst-case analysis*, the form we consider here, we consider the longest running time of all inputs of a particular length. In *average-case analysis*, we consider the average of all running times of inputs of a particular length.

**Def:** Let $M$ be a deterministic Turing machine that halts on all inputs. The *running time* or *time complexity* of $M$ is the function $f:\Bbb N \to\Bbb N$, where $f(n)$ is the maximum number of steps that $M$ uses on any input of length $n$. if $f(n)$ is the running time of $M$, we say that $M$ runs in $f(n)$ and that $M$ is an $f(n)$ time Turing machines. Customarily we use $n$ to represent the length of the input. 

**Def:** Let $t:\Bbb N \to \Bbb R^+$ be function. Define the *time complexity class*, $\text{TIME}(t(n))$, to be the collection of all languages that decidable by an $O(t(n))$ time Turing machine.

# Complexity Relations Among Models

**Th:** Let $t(n)$ be a function, where $t(n) \ge n$. Then every $t(n)$ time multitape Turing machines has an equivalent $O(t^2(n))$ time single-tape Turing machine.

**Def:** Let $N$ be a nondeterminisric Turing machine that is a decider. The *running time* of $N$ is the function $f:\Bbb N \to \Bbb N$, where $f(n)$ is the maximum number of steps that $N$ uses on any branch of its computation on any length $n$. 

**Th:** Let $t(n)$ be a function, where $t(n) \ge n$. Then every $t(n)$ time nondeterministic single-tape Turing machine has an equivalent $2^{O(t(n))}$ time deterministic single tape Turing machine.

There are a lot classes important classes of problems
- [[The Complexity Class P]]
- [[The Complexity Class NP]]
	- [[The Difference Hierarchy]]
	- [[The Complexity Class coNP]]
- [[Polynomial Time Hierarchy]]