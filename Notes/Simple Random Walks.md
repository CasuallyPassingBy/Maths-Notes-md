---
tags:
  - StochasticProcesses
---
Subjects: [[Stochastic Processes]]
Links: [[Definitions for Stochastic Processes]]

A simple random walk over the whole number $\Bbb Z$ is a discrete time stochastic process  $\{X_n \mid n \in \Bbb N\}$. The value of $X_n$ is the state of the process at time $n$. The process changes form a state to another in consecutive times, according to the *transition probabilities*, given as

$$
P(X_{n+1}= j \mid X_n = 1) = 
\begin{cases}
p & j = i+1 \\
q & j = i-1 \\
0 & \text{otherwise}
\end{cases}
$$
We can consider auxiliary random variables $\{Y_n\}$ , defined as
$$
P(Y_n = i) = \begin{cases}p & i = 1 \\
q & i = -1 \\
0 & \text{otherwise}\end{cases}
$$
These random variables are identically distributed, independent and  with the property that
$$
X_{n+1} = X_n +Y_n
$$
 and we have that
 $$
 X_n = X_0 +\sum_{i = 1}^n Y_n
 $$
 Since $Y_n \sim 2\text{Ber}(p) -1$. We can suppose that $X_0 = 0$, without loss of generality, and calculate the expected values and variance.
 
For any $n \ge 0$, we have that
- $E[X_n] = n(p-q) = n(2q-1)$ 
- $\text{Var}[X_n] = 4npq = 4np(1-p)$

With the added assumption of $X_0 = 0$, we get that $X_n = \sum_{i = 1}^n Y_n$, and the that the moment generating function of $X_n$ is 
$$
M(t) = (pe^t +qe^{-t})^n
$$

We now can calculate the probability of the random walk be in a given position after $n$ steps:

For any $n \in \Bbb N$ and $x \in \Bbb Z$, such that $|x| \le n$, and $x \equiv n \pmod 2$, we know that
$$
P(X_n = x \mid X_0 = 0) = {n \choose \frac{1}{2}(n+x)} p^{\frac{1}{2}(n+x)}q^{\frac{1}{2}n-x}
$$
for the values of $x$ that don't satisfy this conditions the probability is $0$.

For the numbers $n$ and $x-y$ have the same parity, and $|x-y| \le n$, we have that
$$
P(X_n = x \mid X_0 = y) = {n \choose \frac{1}{2}(n+x-y)} p^{ \frac{1}{2}(n+x-y)} q^{ \frac{1}{2}(n-x+y)}
$$

$(*)$For a random walk over $\Bbb Z$, the probability of an eventual return to the initial point is 
$$
1-|p-q|
$$
Meaning, only when $p=1/2$, we know for certain that we will return to the original point, but it might take infinite time.

# Gambler's Ruin

We have a gambler $A$ that successively bets one monetary unit to a gambler $B$. Initially, $A$ has $k$ units, and $B$ has $N-k$ units. At each bet $A$ has the probability of winning being $p$ and the probability of losing of $q = 1-p$, and no draws. The bets stop only when a player has $0$ units, meaning that either the capital $A$ is $0$ (lost everything) or $N$ (won everything). 

If we model, this with a random walk $\{X_n \mid n \in \Bbb N\}$, where $X_n$ represents the capital of $A$ at time $n$. We see that the state state is $\{0, 1, \dots, N\}$, in which the states $0$ and $N$ are absorbing. We can ask what's the probability that the walk gets absorbed into the $0$ state rather than the $N$ state. 

To solve this problem, we define the first moment where we visit an absorbing state, let $\tau = \{ n \in \Bbb N \mid X_n = 0, N\}$, and we can check that this is a random variable that is finite almost all the time. Then we can translate when will the game stop into the probability question
$$
u_k = P(X_\tau =0\mid X_0 = k)
$$
From the total probabilty theorem we have that 
$$
u_k = pu_{k+1}+qu_{k-1}
$$
for $k = 1, \dots, N-1$, and the boundary conditions for the recurrence relation being $u_0 = 1$ and $u_N= 0$. We get the equation
$$
u_{k+1} - u_k = (q/p)(u_k-u_{k-1})
$$
Back solving the equation we get that
$$
u_{k+1} - u_{k} = (q/p)^{k-1}(u_1-1)
$$
If we sum to get a telescoping sum we get that, and we call $S_k = \sum_{i = 0}^k (q/p)^k$, then
$$
u_k = 1+(u_1-1)S_k
$$
If we check this formula with our boundary conditions, we get that 
$$
u_1 = 1- \frac{1}{S_{N-1}}
$$
and substituting back we get the equation
$$
u_k = 1-\frac{S_{k-1}}{S_{N-1}}
$$
Thus we get the formula
$$
u_k = \begin{dcases}
\frac{N-k}{N} & p =1/2 \\ \\
\frac{(q/p)^N-(q/p)^k}{(q/p)^N-1} & p \ne 1/2
\end{dcases}
$$

We can calculate what is the ruin probability for the other player as
$$
u_{N-k} = \begin{dcases}
k /N & q =1/2 \\ \\ 
\frac{(q/p)^k-1}{(q/p)^N-1} & q\ne 1/2
\end{dcases}
$$

$(*)$ The expected number of bets before the ruin is
$$
m_k = \begin{dcases}
k (N-k) & p = q \\ \\
\frac{1}{q-p}\left(k-N \frac{(q/p)^k-1}{(q/p)^N-1}\right) & p \ne q
\end{dcases}
$$
