---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Filters and Ideals]], [[Convergence of Sequences in Metric Spaces]], [[Convergence of Sequences]], [[Stone-Čech compactification]], [[Measure]]

Let $U$ be a non-principal ultra filter on $\Bbb N$, and $\omega$ be the associated two-valued content

If $\omega(S) =0$, for some subset $S\subseteq \Bbb N$, we say that $\omega$-small. If $\omega(S)=1$, we say that $S$ contains $\omega$-almost all elements of $\Bbb N$

Let $\omega$ be the associated two-valued content to an ultrafilter $U$, and $f:\Bbb N \to \Bbb N$. If $\omega(S) \le \omega(f^{-1}[S])$ for any set $S\subseteq N$. Then $f(n) = n$ for $\omega$-almost all elements of $\Bbb N$. 
# Ultralimit of points

Assume $(x_n)_{n\in \Bbb N}$ is a sequence of points in a metric space $X$. Let us define the $U$-limit or $\omega$-limit of a sequence $(x_n)_{n\in \Bbb N}$ as the point $x_U\in X$ such that for every $\varepsilon>0$, the point $x_n$ lies in $B(x_U, \varepsilon)$ for $\omega$-almost all $n$; that is, if $$S_\varepsilon = \{n \in \Bbb N \mid d(x_U, x_n) <\varepsilon\}$$
then $\omega(S_\varepsilon) =1$ or $S_\varepsilon \in U$. In this case we will write: $$x_U = \lim_{\omega} x_n = \lim_{U} x_n$$ For example, if $U$ is a principal ultrafilter defined $\{A\subseteq \Bbb N \mid n \in A\}$ for some $n \in \Bbb N$, then $x_U = x_n$. 

The sequence $x_n$ can be thought of as a map $\Bbb N \to X$ defined by $n\mapsto x_n$. If $X$ is compact, then the map $\Bbb N \to X$ can be extended to a continuous map $\beta \Bbb N \to X$ from the Stone-Čech compactification $\beta \Bbb N$ of $\Bbb N$. Then the $U$-limit $x_U$ is the image of $U$. 

**Prop:** Let $x_n$ be a sequence of points in a metric space $X$. Assume that $\lim_U x_n = x_U$. Then $x_U$ is a partial limit of $x_n$

**Prop:** Any sequence $x_n$ of points in a compact metric space $X$ has a unique $U$-limit. In particular, a bounded sequence of real numbers has a unique $U$-limit

**Lemma:** A sequence of points in a metric space converges iff all subsequences have the same $U$-limit

**Th:** In a normed vector space, let $(x_n)$ and $(y_n)$ is be sequences with $U$-limit, then $(x_n+y_n)$ has a $U$-limit and:$$ \lim_U (x_n + y_n) = \lim_U x_n + \lim_U y_n$$
**Def**: Let $A$ be a set of natural numbers. For each $n\in \Bbb N$, let $A(n) = |A \cap \{0, \dots, n-1\}|$ denote the number of elements of $A$ that are smaller than $n$. The limit $$d(A) = \lim_{n\to\infty} \frac{A(n)}{n}$$ if it exists, is called the *density* of $A$. 

**Th:** There exists a content $m$ on $\Bbb N$ such that $m(A) = d(A)$ for every set $A$ that has a density. 

# Ultralimits of Spaces

Let $U$ be a nonprincipal filter of $\Bbb N$, $\omega$ be the corresponding 2-valued content of $U$.

Let $X_n$ be a sequence of metric spaces. Consider all the sequence of points $x_n \in X_n$. On the set of all sequences, we define an $\infty$-pseudometric by:
$$ d((x_n), (y_n)) = \lim_\omega d_n(x_n, y_n)$$
We note that the $\omega$-limit is always defined since it can take a value in $[0, \infty]$. We define the $\omega$-convergence to $\infty$, analogously to the usual convergence to $\infty$; that is $\lim x_n = \infty \iff \lim 1/x_n = 0$. 

Let $X_\omega$ be the corresponding metric space; that is the underlying set $X_\omega$ is formed by equivalence classes of sequences of points $x_n \in X_n$ defined by: $$ (x_n) \sim (y_n) \quad \iff\quad \lim_\omega d_n(x_n, y_n) = 0$$
The space $X_\omega$ is called the $\omega$-limit of $X_n$. It is also called the $\omega$-product; this term is motivated by the fact that $X_\omega$ is a quotient of the product $\prod X_n$.  Typically $X_\omega$ will denote the $\omega$-limit of the sequence $X_n$; we can also write $$X_\omega = \lim_\omega X_n$$
**Prop:** The $\omega$-limit of any sequence of metric spaces is complete

