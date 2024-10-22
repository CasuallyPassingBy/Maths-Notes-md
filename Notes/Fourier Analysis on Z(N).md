---
tags:
  - FourierAnalysis
  - GroupTheory
---
Subjects: [[Fourier Analysis]], [[Group Theory]]
Links: [[Main definitions for Fourier Analysis]], [[Cyclic Groups]], [[Integers modulo n]]

Let $N$ be a positive positive integer. A complex number $z$ is an $n$th root of unity if $z^n = 1$. The set of all roots of unity is precisely $$\left\{1, e^{2\pi i/N}, e^{2\pi i 2/N}, \dots, e^{2\pi i (n-1)/n}\right\}$$
So if $\zeta = e^{2\pi i/N}$, we find that $\zeta^k$ generates all the roots of unity and additionally, we see that $$\zeta^k = \zeta^m \iff N \mid m-k$$
The set of all $n$th roots of unity by $\Bbb Z(n)$. It is really easy to see that $(\Bbb Z(N), \cdot, 1) \cong (\Bbb Z/N \Bbb Z, +, 0)$, with the isomorphism being $\varphi: \Bbb Z/N \Bbb Z \to \Bbb Z(N)$, and defined as $$\varphi([k]) = e^{2\pi ik/N}$$Let $V$ and $W$ be the vector spaces of complex-valued functions on $\Bbb Z/ n \Bbb Z$ and $\Bbb Z(n)$, namely $\Bbb C^{\Bbb Z /\Bbb nZ}$ and $\Bbb C^{\Bbb Z(n)}$ respectively. Then, the isomorphism between $V$ and $W$ carries over, $\Phi: V \to W$, by $$\varphi(F)(e^{2\pi i k/N})= F(k)$$
Getting that $V$ and $W$ are isomorphic.

# Fourier Analysis 

On $\Bbb Z(n)$ the analogues of the exponentials of continuous Fourier analysis are: $e_0, \dots, e_{n-1}$, defined by $$e_{m}(k)= e^{2\pi i mk/N} \qquad \text{for } m, k \in \{0, 1, \dots n-1\}$$
We endow the vector space of the complex valued functions $\Bbb Z(n)$, denoted by $V$, namely $\Bbb C^{\Bbb Z(n)}$, with a inner product: $$(f, g) = \frac1{N}\sum_{k = 0}^{N-1} f(k) \overline{g(k)}$$and the associated norm $$\|f\|^2 = \frac1{N}\sum_{k = 0}^{N-1} |f(k)|^2$$
**Lemma:** The family $\{e_0, \dots, e_{N-1}\}$ is orthonormal:$$(e_m, e_k) = \delta_{m,k}$$
We define the $n$th *Fourier coefficient* of $f$ by $$a_n = \frac1{N} \sum_{k = 0}^{N-1} f(k) e^{-2\pi i k n/N} = (f, e_n)$$
**Th:** If $F$ is a function on $\Bbb Z(N)$, then $$f(k) = \sum_{n = 0}^{N-1} a_n e^{2\pi i nk/N} = \sum_{k = 0}^{N-1} (f, e_k) e_k$$Moreover, $$\sum_{n = 0}^{N-1} |a_n|^2 = \frac1{N}\sum_{k = 0}^{N-1} |F(k)|^2$$
# FFT

The [[Fast Fourier Transform]] is one of the most important algorithms in computer science.

Let $\#(M)$ denote the minimum number of operations needed to calculate all the Fourier coefficients of any function on $\Bbb Z(M)$. 

**Lemma:** If we are given $\omega_{2M} = e^{-2\pi i/2M}$, then $$\#(2M) \le 2\#(M) + 8M$$
**Th:** Given $\omega_N = e^{-2\pi i /N}$ with $N = 2^n$, it is possible to calculate the Fourier coefficients of a function on $\Bbb Z(N)$ with at most $$4\cdot 2^n n = 4N \log_2(N) = O(N\log N)$$
