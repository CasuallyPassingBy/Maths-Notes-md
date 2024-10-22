---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
# Partitions and Tagged Partitions

Given the interval $I = [a, b]$, then a _partition_ $\mathcal{P}$ is a finite, ordered set, $\mathcal{P} := (x_k )_{k= 0}^n$, where $a = x_0$, $b= x_n$ and $x_{i-1} < x_i$ for $1\le i \le n$. This partition cuts the interval $I$ into distinct non overlapping subintervals:

$$ I_k =[x_{k-1}, x_k] $$

Commonly, it also denoted as $\mathcal{P} = \{ [x_{i-1}, x_i]\}_{i=1}^n= \{I_i\}_{i=1}^n$.

We can define a norm or mesh of $P$ as follows: $\|\mathcal{P}\|=$ $\max\{\Delta x_k: 1\leq k\leq n\}$ , where each $\Delta x_k$ is defined as: $\Delta x_k = x_{k} - x_{k-1}$. The set of all partitions of is denoted as: $\wp_I$

A _tagged partition_ is just a partition where at each $I_i$ you can pick a _tag $t_i \in I_i$,_ and a tagged partition is denoted as: $\dot{\mathcal{P}} = \{(I_i, t_i)\}_{i=1}^n$, and the set of all partitions of I is denoted as $\dot{\wp}_I$.

## Definition of Riemann Sums

A _**Reimann Sum**_ of a function $f:I \to \mathbb{R},$ is just:

$$ R(f, \dot{P})=\sum_{i=1}^nf(t_i)\Delta x_i $$
## Definitions of Darboux Sums

A lower or upper sum of a function $f:I \to \mathbb{R}$, is dependant on a partition $\mathcal{P}$, and on each subinterval of $\mathcal{P}$:

$$ m_k = \inf_{x\in I_k} f(x) \text{ and, } M_k = \sup_{x\in I_k} f(x) $$

The lower and upper sums are defined as follows:

$$ L(f,\mathcal{P}) := \sum_{k=1}^nm_k\Delta x_k \text{ and, } U(f;\mathcal{P}) :=\sum_{k=1}^nM_k\Delta x_k $$

In general it’s obvious that $L(f;\mathcal{P}) \leq U(f; \mathcal{P})$

_**Definition:**_ A _refinement_ of a partition $\mathcal{P}$, is a partition $\mathcal{Q}$, such that $\mathcal{P} \subseteq \mathcal{Q}$.

_**Lemma:**_ If $\mathcal{P}'$ is a refinement of a partition $\mathcal{P}$, and has the corresponding relation with the lower and upper sums:

$$ L(f,\mathcal{P}) \leq L(f,\mathcal{P}')\leq U(f,\mathcal{P}') \leq U(f, \mathcal{P}) $$

_**Lemma:**_ For any two partitions $\mathcal{P}_1$ and $\mathcal{P}_2$, then: $L(f, \mathcal{P}_1) \leq U(f, \mathcal{P}_2)$

Since the sets $\{L(f,\mathcal{P}) : \mathcal{P}\in\wp_I \}$ and $\{U(f,\mathcal{P}) : \mathcal{P}\in\wp_I \}$ are bounded thus, there exists their supremum and infimum.

The lower integral of $f$ is:

$$ L(f) =\underline{\int_I}f= \sup\{L(f;\mathcal{P}) : \mathcal{P}\in\wp_I \} $$

The upper integral of $f$ is:

$$ U(f) =\overline{\int_I}f= \inf\{U(f;\mathcal{P}) : \mathcal{P}\in\wp_I \} $$

In general, $L(f) \leq U(f)$