---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Limits of a Sequence in R]]
## General Properties

Let $\lim a_n = a$ and $\lim b_n = b$ .

### **Algebraic Properties**

$$ \lim_{n\to \infty} ca_n =a\text{, for all c $\in \mathbb{R}$} $$

$$ \lim_{n\to \infty} (a_n + b_n) = a +b $$

$$ \lim_{n \to \infty}(a_nb_n) = ab $$

$$ \lim_{n \to \infty} \frac{a_n}{b_n} = \frac{a}{b} \text{ given that $b \neq 0$} $$

### **Order Properties**

If there’s a $c \in \mathbb{R}$ where $\forall n \in \mathbb{N} (c \leq b_n) \ \Rightarrow c \leq b$. Similarly if $\forall n \in \mathbb{N} (a_n \leq c) \Rightarrow a\leq c$

If $c = 0$ will be a special case of this theorem.

$\forall n \in \mathbb{N}(a_n \leq b_n) \Rightarrow a \leq b$
### The Squeeze Theorem

Given the sequences: $(x_n), (y_n)$ and $(z_n)$ where $\forall n \in \mathbb{N}(x_n \leq y_n \leq z_n)$ and $\lim x_n = L = \lim z_n$ $\Rightarrow \lim y_n = L$ 

**Def:** A sequence $(a_n)$ is said to be _increasing_ if $\forall n \in \mathbb{N} (a_n \leq a_{n+1})$. Similarly, $(a_n)$ is said to be _decreasing_ if $\forall n \in \mathbb{N} (a_{n} \geq a_{n+1})$ . In both of this cases $(a_n)$ is monotonic.

## The Monotone Convergence Theorem
If a sequence $(a_n)$ is monotonic and bounded, thus it’s convergent.

Let $f:\mathbb{N} \to \mathbb{N}$ where $f$ is strictly increasing, and the sequence $(a_n)$, a subsequence is just $(a_{f(n)})$ is a subsequence of $(a_n)$, also can be think as given a sequence of natural numbers where: $\forall k \in\mathbb{N} [n_k <n_{k+1}]$ and the sequence that runs on $k$ will be denoted as $(a_{n_k})$ is a subsequence of $(a_n)$.

Theorem: given a convergent sequence if and only if any subsequence is convergent to the same limit.

### Bolzano-Weierstrass Theorem
Given a bounded sequence, there’s a convergent subsequence.