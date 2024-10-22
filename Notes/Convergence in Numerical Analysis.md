---
tags:
  - NumericalAnalysis
---
Subjects: [[Numerical Analysis]]
Links: [[Error In Numerical Analysis]]
Suppose that $E_0>0$ denotes an error introduced at some stage in the calculations and $E_n$ represents the magnitud of the error after $n$ subsequent operations

- If $E_n \approx CnE_0$ where $C$ is a constant independent of $n$, then the growth of error is said to be ******linear******
- If $E_n \approx C^n E_0$ for some $C>1$, then the growth of error is called _**********exponential**********_

Linear growth is usually unavoidable and for small values of $C$ and $E_0$ it is generally accepted. Exponential growth must be avoided since $C^n$ grows fast, this leads to unacceptable inacuracies regardless the size of $E_0$. An algorithm that exhibits linear growth is ******stable******, whereas an algorithm with expoonetial error growth is ********unstable********.

## Rates of convergence

Suppose $(\beta_n) _{n \in \Bbb N}$ is a sequence that converges to $0$, and $(\alpha_n)_{n \in \Bbb N}$ converges to a number $\alpha$. If a positive constant $K$ and $N \in \Bbb N$ exist such that for all $n \ge N$

$$ |\alpha_n - \alpha| \le K |\beta_n| $$

then we say that $(\alpha_n)_{n \in \Bbb N}$ converges to $\alpha$ with ******************************rate, or order, of convergence****************************** of $O(\beta_n)$. It is indicated as $\alpha_n = \alpha + O(\beta_n)$. In nearly every situation we use

$$ \beta_n = \frac{1}{n^p} $$

with positive $p$. We are generally interested in the larges $p$ with $\alpha_n = \alpha + O(1/n^p)$

Suppose that $\lim \limits_{h \to 0} G(h) = 0$ and $\lim\limits_{h \to 0} F(h) = L$. If there’s a positive constant $K$, and $\delta$, such that if $|h |< \delta$, then

$$ |F(h) - L| \le K|G(h)| $$

then we write $F(h ) = L + O(G(h))$