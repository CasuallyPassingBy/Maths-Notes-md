---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Complete Metric Spaces]], [[Metric Spaces#Metric Identification on Pseudo-metric Spaces|Metric Identification on Pseudo-metric Spaces]]
We say that a metric space $X^*$ is a *****_____completion of $X$_ if $X^*$ is complete and there’s an isometry ${\iota:X \to X^*}$ such that $\overline{\iota[X]} = X^*$ (the closure of $\iota[X]$ in $X^*$)

We can actually make explore the set of all Cauchy sequences in $X$, let $x_\bullet =(x_n)$ and $y_\bullet =(y_n)$ me Cauchy sequences, and we may refer to the distance as,

$$ d(x_\bullet, y_\bullet) = \lim_{k\to \infty}d(x_n , y_n) $$

this is actually a pseudometric. We make the Metric Identifiaction of a pseudometric:

We say that two Cauchy sequences $(x_k)$ and $(y_k)$ in $X$ are **********equivalent,********** denoted as $(x_k) \sim (y_k)$ if

$$ \lim_{k \to \infty} d(x_k, y_k) =0 $$

We have that $\sim$ is an equivalence relation in the set of all Cauchy sequences of $X$. We to generate the new space we make it as

$$ X^* := \{x_\bullet : \Bbb N \to X\mid x_\bullet \text{ is Cauchy}\}/\sim $$

and define the function $d^*: X^*\times X^* \to \Bbb R$ as, and we denote $[x_k]$ to be the equiavalence class of the Cauchy sequence $(x_k)$.

$$ d^*([x_k], [y_k]) := \lim_{k \to \infty }d(x_k, y_k) $$

$d^*$ is well-defined (it doesn’t depend on the representatives of chosen), and it is a metric on $X^*$.

We have that $(X^*, d^*)$ is a complete metric space. For this result we need a couple of lemmas:

- If $(a_n)_{n \in \Bbb N}$ is a Cauchy sequence in $X$, then every subsequence $(a_{n_k})_{k \in \Bbb N}$ is related via $\sim$ to the main sequence
- For any $\varepsilon>0$, there is a subsequence $(a_{n_k})_{k \in \Bbb N}$ such that for any $k , l \in \Bbb N$ we have that $d(a_{n_l}, a_{n_k}) < \varepsilon$

If $x \in X$, we denote for $[x]$ is the equivalence class of the constant sequence of $x$.

Then $\iota (x) = [x]$, has that $\overline {\iota [X]} = X^*$ meaning is a completion