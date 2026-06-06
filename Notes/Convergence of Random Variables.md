---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Random Variables]], [[Lp spaces]], [[Convergence of Measurable Functions]], [[Lp spaces]], [[Lebesgue Integral on Measure Spaces]]

Let $X_1, \dots, X_n, \dots$ be a sequence of random variables. There are a lot of types of convergence

# Types of Convergence

### Pointwise Convergence

It is the absolute simplest. Let $X_n$ be the sequence of random variables, we say that it *converges pointwise* if for all $\omega \in \Omega$, $$\lim_{n \to \infty} X_n(\omega) = X(\omega)$$
We can denote it as $X_n \to X$, or if we want to specify, $X_n \stackrel{p}{\longrightarrow}X$ 
## Almost Everywhere Convergence

The sequence of random variables $X_n$, converges *converges almost surely* to $X$ if $$\Bbb P(\{\omega \in \Omega \mid \lim_{n \to \infty} X_n(\omega) = X(\omega)\} = 1$$or $$\Bbb P(\lim_{n\to \infty} X_n = X) = 1$$We can denote is as $X_n \stackrel{a.s.} {\longrightarrow} X$, or $\lim\limits_{n \to \infty} X_n = X\; a.s.$ 

## Convergence in Probability
 
The sequence of random variables $X_n$ converges to $X$ in *probability* if for every $\varepsilon> 0$, $$\Bbb P(\{\omega\in \Omega \mid |X_n(\omega) - X(\omega)|>\varepsilon\})=0 $$
We can denote this kind of convergence by $X_n \stackrel{\Bbb P}{\longrightarrow}X$, omitting $\omega$. The condition is $$\Bbb P(\lim_{n \to \infty} |X_n-X| > \varepsilon) = 0 $$

## Convergence in Mean

The sequence of random variables $X_n$ converges to $X$ in *mean* if $$\lim_{n \to \infty} E|X_n - X| = 0$$
This type of convergence is also called $L^1$ *convergence* and it's denoted as $X_n \stackrel{L^1}{\longrightarrow}X$

## Convergence in Mean Squared

The sequence of random variables $X_n$ converges to $X$ in *mean squared* if $$\lim_{n \to \infty} E|X_n - X|^2 = 0$$
This type of convergence is also called $L^2$ *convergence* and it's denoted as $X_n \stackrel{L^2}{\longrightarrow}X$


## Convergence in $L^p$

The sequence of random variables $X_n$ converges to $X$ in $L^p$ if $$\lim_{n \to \infty} E|X_n - X|^p = 0$$
This type of convergence is also called $L^1$ *convergence* and it's denoted as $X_n \stackrel{L^p}{\longrightarrow}X$

## Convergence in distribution or Weak Convergence




# Relations between types of convergence

- Almost sure convergence $\implies$ Convergence in probability
- Convergence in probability $\centernot\implies$ Almost sure convergence (in general)
- Almost sure convergence $\centernot\implies$ Almost sure convergence in $L^1$ (in general)
- Convergence in $L^2$ $\implies$ Convergence in $L^1$
- Convergence in $L^1$ $\implies$ Convergence in probability
- Convergence in probability $\implies$ Convergence in distribution

# Important Theorems

### Monotone Convergence Theorem
Let $0 \le X_1 \le X_2 \le \cdots$ be an increasing sequence of random variables that converges almost surely to $X$. Then $$\lim_{n \to \infty} \Bbb E[X_n] = \Bbb E[X] $$
### Dominated Convergence Theorem
Let $X_1, X_2, \dots$ be a sequence of random variables, and a random variable $Y$, that $|X_n| \le Y$ , for all $n \in \Bbb N^+$. If $\lim\limits_{n \to \infty} X_n = X\; a.s.$ then $X$ and $X_n$ are integrable and $$\lim_{n \to \infty} \Bbb E[X_n] = \Bbb E[X] $$
