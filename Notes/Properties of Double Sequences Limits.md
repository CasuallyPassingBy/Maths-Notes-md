---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Double Sequences Limits]]

### Monotone Double Sequences

_**Definition:**_ A double sequence $s_{n,m}$ can be monotone if, given $(n,m) \le (p,q)$:

- $s_{n,m} \le s_{p,q}$, being increasing or,
- $s_{n,m} \ge s_{p,q}$, being decreasing.

_**Theorem:**_ Given a _monotonic_ double sequence it _converges_ iff it is _bounded,_ and:

1. If the double sequence is increasing then:
    
    $$ \lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right) = \lim_{n\to\infty}\left(\lim_{m\to\infty} s_{n,m}\right) = \lim_{n,m\to\infty} s_{n,m} = \sup_{n,m\in\mathbb{N}}s_{n,m} $$
    
2. If the double sequence is decreasing then:
    

$$ \lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right) = \lim_{n\to\infty}\left(\lim_{m\to\infty} s_{n,m}\right) = \lim_{n,m\to\infty} s_{n,m} = \inf_{n,m\in\mathbb{N}}s_{n,m} $$

### Theorems

**Factorizing Theorems**

If the sequence $s_{n,m} = a_nb_m$, where $(a_n)$ and $(b_m)$ are sequences with limits, $\lim_{n\to\infty}a_n = l_1$, and $\lim_{m\to\infty}b_m = l_2$, then

$$ \lim_{n\to\infty}\left(\lim_{m\to\infty} s_{n,m}\right) = \lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right) = \lim_{n,m\to\infty} s_{n,m} = l_1l_2 $$

If the sequence $s_{n,m} = a_n+b_m$, where $(a_n)$ and $(b_m)$ are sequences with limits, $\lim_{n\to\infty}a_n = l_1$, and $\lim_{m\to\infty}b_m = l_2$, then:

$$ \lim_{n\to\infty}\left(\lim_{m\to\infty} s_{n,m}\right) = \lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right) = \lim_{n,m\to\infty} s_{n,m} = l_1+l_2 $$

**Sandwich Theorem**

Let $x_{n,m}, s_{n,m}$ and $y_{n,m}$ be double sequences of real numbers, where:

$$ \forall (n,m)\in\mathbb{N}^2(x_{n,m} \le s_{n,m} \le y_{n,m}) $$

If $\lim_{n,m\to\infty} x_{n,m} = \lim_{n,m\to\infty} y_{n,m}$ , then $s_{n,m}$ is _convergent_ and:

$$ \lim_{n,m\to\infty} x_{n,m}=\lim_{n,m\to\infty} s_{n,m}= \lim_{n,m\to\infty} y_{n,m} $$

### Double Subsequences

_**Definition:**_ Considering the strictly increasing sequence of pairs of natural numbers: $(k_1, r_1) <(k_2, r_2) < \cdots (k_n, r_n) < \cdots$, then the sequence $s(k_n, r_m) = s_{k_n, r_m}$ is a double subsequence of $s_{n,m}$.

_**Theorem:**_ If the sequence $s_{n,m}$ converges to $a$ iff, any subsequences of $s_{n,m}$ converges to $a$.

_**Theorem:**_ If the iterated limits of a double sequence $s_{n,m}$ exists and satisfy:

$$ \lim_{m\to\infty}\left(\lim_{n\to\infty} s_{n,m}\right) = \lim_{n\to\infty}\left(\lim_{m\to\infty} s_{n,m}\right) = a $$

Then, the iterated limits of any subsequence $(s(p_n, q_m))$ exist and satisfy:

$$ \lim_{m\to\infty}\left(\lim_{n\to\infty} s(p_n, q_m)\right) = \lim_{n\to\infty}\left(\lim_{m\to\infty} s(p_n, q_m)\right) = a $$

_**Lemma:**_ Every double sequence of real numbers has a monotonic subsequence.

_**Bolzano-Weiestrass Theorem:**_ A bounded double sequences of real numbers has a convergent subsequence.

_**Corollary:**_ Any double sequence $(s(n,m))$ has a convergent subsequence $(s(p_n, q_m))$ where the iterated limits:

$$ \lim_{m\to\infty}\left(\lim_{n\to\infty} s(p_n, q_m)\right) \text{ and }\lim_{n\to\infty}\left(\lim_{m\to\infty} s(p_n, q_m)\right) $$

_Exist_ and are _equal_ to $\lim_{n,m\to\infty} s(p_n,q_m)$ .