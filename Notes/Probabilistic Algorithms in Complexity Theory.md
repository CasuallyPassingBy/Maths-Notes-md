---
tags:
  - ComputationTheory
---
Subjects: [[Theory of Computation]]
Links: [[Turing Machines]], [[Random Variables]]

A *probabilistic algorithm* is an algorithm designed to use the outcome of random process. Typically, such an algorithm would contain an instructions to "flip a coin" and the result of that coin flip would influence the algorithm's subsequent executions and output. Certain types of problems seem to be more easily solvable by probabilistic algorithms than by deterministic algorithms. 

How can making a decision by flipping a coin ever be better than actually calculating, or even estimating, the best choice in a particular situation? Sometimes, calculating the best choice may requiere excessive time and estimating it may introduce bias that invalidates the result. 

**Def:** A *probabilistic Turing machine* $M$ is a type of nondeterministic Turing machine in which each nondeterministic step is called *coin-flip step* and has two legal moves. We assign a probabilisty to each branch $b$ of $M$'s computation on input $w$ as follows. Define the probability of branch $b$ to be  $$P(b) := 2^{-k},$$where $k$ is the number of coin-flips steps that occur on branch $b$. Define the probability that $M$ accepts $w$ to be $$P(M \text{ accepts }w) = \sum_{\substack{b \text{ is an } \\ \text{accepting branch}}} P(b). $$
In other words, the probability that $M$ accepts $w$ is the probability that we would reach an accepting configuration if we simulated $M$ on $w$ by flipping a coin to determine which move to follow at each coin-flip step. We let   $$P(M \text{ rejects }w) = 1-P(M \text{ accepts }w).$$
There is an analogue to [[the complexity class P]], called [[The Complexity Class BPP|BPP]]. 

We can consider the $\sf NP$ analogue to BPP which is [[Interactive Proof Systems|IP]]. 