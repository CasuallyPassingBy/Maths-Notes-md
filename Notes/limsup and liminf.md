---
tags:
  - RealAnalysis
  - Analysis
  - Topology
---
Subjects: [[Real Analysis]], [[Metric and Normed Spaces]], [[Topology]]
Links: [[Properties of Limits of Sequences in R]] [[Limits of a Sequence in R]], [[Functional Limits in R]]

The concept of $\limsup$ and $\liminf$ of a sequence , is to put a long term upper bound and lower bound of a sequence. The $\limsup$ of a sequence as: given the sequence $(y_n)$ defined as follow: $$ y_n = \sup\{x_k \mid k \geq n \} \text{ and } \lim_{n \to\infty} y_n := \limsup x_n = a $$
For some $a$ , or as the following:
$$ \forall\varepsilon>0\exists N \in\mathbb{N}[\forall n \geq N(x_n - \varepsilon < a)] $$

And the $\liminf$ is defined similarly with a sequence $(z_n)$ defined as: $$ z_n = \inf \{x_k \mid k \geq n \} \text{ and } \lim_{n \to\infty} z_n := \liminf x_n =b $$
for some $b$, or as the following:$$ \forall\varepsilon > 0\exists N\in\mathbb{N}[\forall n\geq N(x_n < b +\varepsilon) ] $$

The good thing is that $\limsup$ and $\liminf$ of a sequence exist with weaker conditions, as long as the sequence is bounded, both must exist, and even if it’s not bounded one of them can exist.

### Algebraic Properties
Given a bounded sequence $(a_n)$ $$ \liminf a_n \leq \limsup a_n $$
The sequence $(a_n)$ converges to a limit if and only if $\liminf a_n = \limsup a_n$

Given two sequences bounded $(a_n)$ and $(b_n)$ then, the following properties hold:

- $\limsup(a_n + b_n) \leq \limsup a_n + \limsup b_n$
- $\liminf(a_n +b_n) \geq \liminf a_n+\liminf b_n$
- $\limsup(a_nb_n)\leq (\limsup a_n)(\limsup b_n)$
- $\liminf(a_n b_n) \geq (\liminf a_n)(\liminf b_n)$
- If a constant $c \in \mathbb{R}^+$ then, $\limsup{ca_n} = c\limsup a_n$ and $\liminf ca_n = c\liminf a_n$
- If a constant $c \in \mathbb{R}^-$ then, $\limsup ca_n = c\liminf a_n$ and $\liminf ca_n = c\limsup a_n$

# Metrics Spaces

The following versions of $\limsup$ and $\liminf$ can be also be expressed for [[Topology of Metric Spaces|Metric Spaces]]

Let $f: E \to\Bbb R$ and $a$ a limit point of $E$. Then we can define
$$ \limsup_{x \to a} f(x) := \lim_{\varepsilon \to 0}(\sup\{ f(x)\mid x \in E \cap B_\varepsilon(a)\setminus a\}) $$
and
$$ \liminf_{x\to a}f(x) := \lim_{\varepsilon \to 0}(\inf\{f(x) \mid x \in E \cap B_{\varepsilon}(a) \setminus a\}) $$

We see that $\varepsilon$ shrinks, the supremum of the function over the ball is monotone decreasing, so we have that
$$ \limsup_{x \to a} f(x) := \inf_{\varepsilon >0}(\sup\{ f(x)\mid x \in E \cap B_\varepsilon(a)\setminus a\}) $$
and, similarly
$$ \liminf_{x\to a}f(x) := \sup_{\varepsilon > 0}(\inf\{f(x) \mid x \in E \cap B_{\varepsilon}(a) \setminus a\}) $$
I think that we can think we can use similar to a definition using arbitrary sequences such that $x_n \to x_0$ and $x_n \ne x_0$ for all $n\in \Bbb N$, then it has the property that
$$ \limsup_{k \to \infty} f(x_k) = \limsup_{x\to x_0} f(x) \qquad \liminf_{k \to \infty} f(x_k) = \liminf_{x\to x_0} f(x) $$

# Topological Spaces

We can extend this even further when to extend to [[topological spaces]]. Let $(X, \tau)$ be a topological space, and $E\subseteq X$. 

Let $f: E \to\Bbb R$ and $a$ a point in the closure of $E$. Then we can define
$$ \limsup_{x \to a} f(x) := \inf\{\sup\{ f(x) \mid x\in E\cap U\} \mid U \in \tau \land a\in U\} = \inf_{a\in U} \sup_{x\in U} f(x)$$
and
$$ \liminf_{x\to a}f(x) := \sup\{\inf\{ f(x) \mid x\in E\cap U\} \mid U \in \tau \land a\in U\} =  \sup_{a\in U} \inf_{x\in U} f(x) $$
