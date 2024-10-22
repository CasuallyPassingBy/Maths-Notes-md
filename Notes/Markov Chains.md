---
tags:
  - StochasticProcesses
---
Subjects: [[Stochastic Processes]]
Links: [[Simple Random Walks]], [[Markov Chains with Matrices]], [[Definitions for Stochastic Processes]]

We can condense the notation of $P(X_n = x_n)$, and instead write $p(x_n)$. 

A *Markov Chain* is a discrete time stochastic process $\{X_n\mid n \in \Bbb N\}$, with a discrete state space, that satisfies the Markov property, i.e., for any $n \ge 0$ whole number, and for any states $x_0, \dots, x_{n+1}$, it follows that
$$
P(X_{n+1} = x_{n+1} \mid X_0 = x_0, \dots, X_n = x_n) = P(X_{n+1}= x_{n+1} \mid X_n = x_n)
$$

or in our new notation
$$
p(x_{n+1}\mid x_0, \dots, x_n ) = p(x_{n+1}\mid x_n)
$$
This condition is equivalent to
$$
P(X_0 = x_0, \dots, X_n = x_n) = P(X_0 = x_0)\prod_{i = 1}^n P(X_i=x_i \mid X_{i-1} = x_{i-1})
$$
Or with the new notation
$$
p(x_0, \dots, x_n) = p(x_0) \prod_{i = 1}^n p(x_i \mid x_{i-1})
$$
since the state space is discrete we can take it as the state space being $\Bbb N$, or a finite subset that has the begining terms. If the state space of a Markov chain is finite, then it is called a *finite Markov chain*.

**Transition Probabilities**. The probability $P(X_{n+1} = j \mid X_n = i)$, can be denoted as $p_{ij}(n, n+1)$, and represents the transition probability from the $i$ state at time $n$ to the $j$ state at time $n+1$. Th