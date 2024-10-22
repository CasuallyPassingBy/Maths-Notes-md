---
tags:
  - StochasticProcesses
---
Subjects: [[Stochastic Processes]]
Links: [[Random Variables]]

A *stochastic process* is a collection of random variables $\{X_t \mid t \in T\}$ parameterised by $T$, called a *parametric space*, and with values of the set $S$ called *the state space*.

It is common to consider the parameter space to be a discrete set $T= \Bbb N$, or a continuous set $T = \Bbb R^{\ge 0}$, and this set is interpreted as the time. The first case we call that the process is said to be in *discrete time*, and this kind of process is denoted as $\{X_n \mid n \in \Bbb N\}$, while the other case it is sad to be in *continuous time*, and it will be denoted as $\{X_t \mid t\ge 0\}$. 

We can think that a stochastic process is a function of two inputs of the form $X:T \times \Omega \to S$ such that that pair $(t, \omega)$ is associated to the state $X(t, \omega)$, which it can be written as $X_t(\omega)$. If we have $t\in T$ fixed, then the mapping $\omega \mapsto X_t(\omega)$ is a random variable, and if we have $\omega \in \Omega$ fixed, then the mapping $t \to X_t(\omega)$ is called a *trajectory or a realisation* of the process. This is the reason that sometimes a stochastic process is called a *random funciton*. 