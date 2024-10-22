---
tags:
  - Topology
---
Subject: [[Topology]]
Links: [[Convergence of Sequences in Metric Spaces]], [[Sequences in Rn]], [[Limits of a Sequence in R]], [[Separable, First and Second Countable Spaces]], [[Continuous Functions and Homeomorphims]]

Let $X$ be a topological space
- A *sequence* on $X$ is a function from $\Bbb N$ to $X$. The sequence $n\mapsto x_n$ is represented by $(x_n)_{n \in \Bbb N}$ 
- A sequence $(x_n)_{n \in \Bbb N}$  on $X$ *converges* to a point $x_0\in X$ if for each neighborhood $N$ of $x_0$ there's a natural number $n(V)$ such that $x_m \in V$, whenever $m \ge n(V)$. The symbol $x_n\to x_0$ means that the sequence $(x_n)_{n \in \Bbb N}$  converges to $x_0$
- We say that the sequence $(x_n)_{n \in \Bbb N}$  is *finite* if the set $\{x_n \mid n \in \Bbb N\}$ is finite. In the case where $(x_n)_{n \in \Bbb N}$  is not finite, then we will say that it is *infinite*

Let $\cal B$ be a local base of neighborhoods of $X$ at the point $x_0\in X$ and the sequence $(x_n)_{n \in \Bbb N}$  on $X$, then $x_n \to x_0$ iff for every $B\in \cal B$ there's a natural number $n(B)$ such that $x_n \in B$ for $n \ge n(B)$

Let $E$ be a subset of the topological space $X$. If $(x_n)_{n \in \Bbb N}$  is an infinite sequence of points of $E$ that converges to $x$, then $x \in \text{Lim}(E)$

If $E$ is a closed subset of the space $X$ and $(x_n)_{n \in \Bbb N}$  is a sequence in $E$ that converges to the point $x_0$, then $x_0\in E$

Let $f:X\to Y$ be a continuous function. If $(x_n)_{n \in \Bbb N}$ a sequence on $X$ that converges to $x_0$, then $f(x_n)\to f(x_0)$

If $X$ is a first countable space, and $E\subseteq X$, then $x\in \text{cl}(E)$ iff there's a sequence on $E$ that converges to $x$

Let $f:X\to Y$ be a function between spaces $X$ and $Y$. If $X$ is first countable and $x\in X$, then $f$ is continuous on $x$ iff for every sequence $(x_n)_{n \in \Bbb N}$  on $X$ that converges to $x$ we have that $f(x_n) \to f(x)$

Let $X$ be a set, and $\tau_1$ and $\tau_2$ be topologies on $X$, such that $\tau_1 \subseteq \tau_2$. We see that the sequence $(x_n)_{n \in \Bbb N}$ converges to a point $x \in X$ in $(X, \tau_2)$, then $x_n \to x$, in $(X, \tau_1)$. 

