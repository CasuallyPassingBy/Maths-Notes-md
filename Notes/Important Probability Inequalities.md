---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Convergence of Random Variables]], [[Random Variables]], [[Conditional Expected Values of Random Variables]], [[Conditional Probability]]

## Markov Inequality

Let $X \ge 0$, be a random variable with finite expected value. For any $\varepsilon > 0$, then $$P(X \ge \varepsilon) \le \frac{E[X]}{\varepsilon}$$
We can also look at the conditional version, let $\mathscr G$ be a sub-$\sigma$-algebra $$P(X \ge \varepsilon \mid \mathscr G) \le \frac{E(X \mid \mathscr G)}{\varepsilon}$$
We can also get different versions: $$P(|X| \ge \varepsilon ) \le \frac{E|X|}{\varepsilon}$$
$$P(|X|^n \ge \varepsilon ) \le \frac{E|X|^n}{\varepsilon^n}$$

## Chebyshev Inquality

Let $X$ be a random variable with finite expected value $\mu$ and finite variance $\sigma$. For any $\varepsilon >0$, $$P(|X - \mu |^2 \ge \varepsilon )  \le \frac{\sigma²}{\varepsilon^2}$$
## Extended Chebyshev Inequality

Let $X$ be a random variable, and $g \ge 0$ be a nondecreasing function such that $g(X)$ is a random variable with finite expected value. For any $\varepsilon>0$, $$P(X \ge \varepsilon) \le \frac{E[g(X)]}{g(\varepsilon)}$$
## Kolmogorov Inquality

Let $X_1, \dots, X_n$ independent random variables with expected value $0$ and finite second moment. For any $\varepsilon>0$, $$P(\max_k\{|X_1 + \dots + X_k|\} \ge \varepsilon ) \le \frac{1}{\varepsilon^2}\sum_{k = 1}^n \text{Var}(X_k)$$