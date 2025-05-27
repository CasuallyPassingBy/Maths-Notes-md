---
tags:
  - StochasticProcesses
---
Subjects: [[Stochastic Processes]]
Links: [[Markov Processes]], [[Simple Random Walks]]

Let us considering the symmetric random walk that in each time unit is equally likely to take a unit step either to left or the right. Now suppose that we speed up this process by taking smaller and smaller steps in smaller and smaller time intervals.

Suppose that each $\Delta t$ time units we take a step of size $\Delta x$ either to left or to the right with equal probabilities. If we let $X(t)$ denote this position at time $t$, then $$X(t):= \Delta x \sum_{n = 0}^{\lfloor t/\Delta t \rfloor}X_n $$where $Y_n \sim \text{Ber}(1/2)$ and $X_n := 2Y_n -1$. Since $\text{E}[X_n] = 0$, $\text{Var}(X_n) = \text{E}[X_n^2] = 1$, we see that $$
\begin{align*}
\text{E}[X(t)] &= 0, \\
\text{Var}(X(t)) &= (\Delta x)^2 \left\lfloor \frac{t}{\Delta t}\right\rfloor.
\end{align*}
$$
We shall now let $\Delta x$ and $\Delta t$ go to $0$. If we let $\Delta x = c \sqrt{\Delta t}$ for some $c >0$, then we see that as $\Delta t \to 0$, $$
\begin{align*}
\text{E}[X(t)] &= 0, \\
\text{Var}(X(t)) &\to c^2t. 
\end{align*}
$$
By the central limit theorem and other stuff we get that:
- $X(t)$ is normal with mean $0$ and variance $c^2 t$.
- $\{X(t) \mid t \ge 0\}$ has independent and stationary increments.

**Def:** A stochastic process $\{X(t) \mid \ge 0\}$ is said to be *Brownian motion process* if:
- $X(0) = 0$
- $\{X(t) \mid t\ge 0\}$ has stationary independent increments,
- for every $t > 0$, $X(t) \sim \mathcal N(0, c^2 t)$. 

When $c = 1$, the process is often called *standard Brownian motion*. As any Brownian motion can always be converted to the standard process by looking at $X(t)/c$, we shall suppose throughout that $c = 1$.

We know that with probability $1$, $X(t)$ is indeed a continuous function in $t$. (black magic)

We see that is a *Markov process*.

Since $X(t)$ is normal with mean $0$ and variance $t$, its density function is given by $$ f_t(x) := \frac1{\sqrt{2\pi t}} \exp\left(\frac{-x^2}{2t}\right).$$
From the stationary independent increment assumption, it easily follows that the joint density function of $X(t_1), \dots X(t_n)$ is given by $$f(x_1, \dots, x_n) = f_{t_1}(x_1) \prod_{k = 2}^n f_{t_k - t_{k-1}}(x_k - x_{k-1}) = f_{t_1}(x_1) f_{t_2-t_1}(x_2 - x_1)\cdots f_{t_n-t_{n-1}}(x_n - x_{n-1})$$
We can calculate the conditional density of $X(s)$ given that $X(t) = B$, where $s < t$: $$f_{s\mid t} (x \mid B) = \frac{f_s(x) f_{t-s}(B-x)}{f_t(B)} = \sqrt{\frac{t}{2\pi s(t-s)}} \exp\left(-\frac{t(x-Bs/t)}{2s(t-s)}\right),$$thus $$X(s) \mid X(t) = B \sim \mathcal N\left(\frac{Bs}{t}, \frac{s(t-s)}{t}\right).$$
If we let $s/t = \alpha$, then $0 <\alpha < 1$, then the conditional distribution given $X(t)$ is normal with mean $\alpha X(t)$ and variance $\alpha (1-\alpha) t$.

**Def:** A stochastic process $\{X(t) \mid t\ge 0\}$ is called a *Gaussian process* if $X(t_1), \dots X(t_n)$ has a multivariate normal distribution for all $0 \le t_1, \dots, t_n$.

Since a multivariate distribution is completely determined by the marginal mean values and the covariance values, it follows that Brownian motion could also be defined as a Gaussian process $\text{E}[X(t)] =0$, and for $s \le t$, $$ \text{Cov}(X(s), X(t)) =s.$$
Let $\{X(t) \mid t \ge 0\}$ be a Brownian motion process and consider the process of values between $0$ and $1$ conditional on $X(1) = 0$. That is consider the conditional stochastic process $\{(X(t)\mid  X(1) = 0) \mid 0\le t \le 1\}$. By the same argument as used in establishing, we can show that this process, known as the *Brownian Bridge*, is a Gaussian process. Let us compute its covariance function, since $\text{E}[X(s) \mid X(1) = 0] = 0$, for $s < 1$. We have that, for $s \le t \le 1$, $$\text{Cov}[(X(s), X(t)) \mid X(1) = 0] = s(1-t).$$Thus the Brownian Bridge can be defined as a Gaussian process with mean value $0$ and covariance function $s(1-t)$, $s \le t$. This leads to an alternative approach to obtaining such process.

**Prop:** If $\{X(t) \mid t\ge 0\}$ is Brownian motion, then $\{Z(t) \mid 0 \le t\le 1\}$ is a Brownian Bridge process when $Z(t) := X(t) - tX(1)$.

# Hitting Times, Maximum Variable and Arc Sine Laws

Let us denote $T_a$ the first time that the Brownian motion hits $a$. When $a >0$ we will compute $P(T_a \le t)$ by considering $P(X(t) \ge a)$ and conditioning on whether or not $T_a \ge t$. This gives $$P(X(t) \ge  a) = P(X(t) \ge a \mid T_a \le t) P(T_a \le t) + P(X(t) \ge a \mid T_a > t) P(T_a > t).$$Let us note that because of black magic, we know that the paths are continuous functions on $t$, so $P(X(t) \ge a \mid T_a > t) = 0$, because by the intermediate 