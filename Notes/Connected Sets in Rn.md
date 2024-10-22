---
tags:
  - VectorAnalysis
---
Subjects: [[Vector Analysis]] 
Links: [[Perfect and Connected Sets in R]]

**********Def:********** Let $A \subseteq \Bbb R^n$. We say that $A$ is **************disconnected************** if there exist ${B, C \subseteq \Bbb R^n}$, nonempty such that:

- $A = B\cup C$
- $\operatorname{cl}(B) \cap C= B \cap \operatorname{cl}(C) = \varnothing$

A set is **********connected********** if it not disconnected

****Def:**** Let $x, y \in \Bbb R^n$. We define the straight line segment that joins $x$ with $y$, denoted with $[x,y]$ and defined by

$$ [x,y] :=\{x +t(y-x) = (1-t)x +ty \mid 0 \le t \le 1\} $$

********Th:******** Let $B, C \subseteq \Bbb R^n$ such that $x \in B$ and $y \in C$. If $B$ and $C$ are separated, then $[x, y] \not \subseteq B \cup C$.

**************Def:************** Let $A \subseteq \Bbb R^n$. We say that $A$ is _******convex******_ if for every pair $x, y \in A$, then $[x, y] \subseteq A$

************Th:************ Let $A \subseteq \Bbb R^n$. If $A$ is convex, then $A$ is connected

**********Def:********** Let $x=x_0, x_1, x_2, \dots, x_k= y \in \Bbb R^n$, and we will that the set $\bigcup_{i = 1}^n[x_i, x_{i-1}]$ is a polygonal curve that connects $x$ and $y$.

************Def:************ Let $A \subseteq \Bbb R^n$. $A$ is polygonally connected if for every pair of points $x, y \in A$ exists a polygonal curve that connects $x$ and $y$ and is contained in $A$.

****Th:**** Let $A\subseteq \Bbb R^n$ be a nonempty open set. $A$ is connected, iff$A$ is polygonally connected.

************Prop:************ Let $A\subseteq \Bbb R^n$. $A$ is disconnected iff there’s $U, V \subseteq \Bbb R^n$ open sets such that:

- $A \subseteq U \cup V$
- $A\cap U \ne \varnothing$ and $A\cap V \ne \varnothing$
- $A\cap U\cap V = \varnothing$

******************Cor:****************** Let $A \subseteq \Bbb R^n$. $A$ is connected iff there’s no $U,V \subseteq \Bbb R^n$ open sets such that:

- $A \subseteq U \cup V$
- $A\cap U \ne \varnothing$ and $A\cap V \ne \varnothing$
- $A\cap U\cap V = \varnothing$

### Path-Connected Sets

Def:************ A set $A \subseteq \Bbb R^n$ is path-connected if for every pair of points $x, y \in A$ there exists a [[Limits and Continuity of Vector Valued Functions of R|continuous fucntion]] ${\gamma:[0,1] \to \Bbb R^n}$ with $\gamma(0) =1$ and $\gamma(1) = b$. We call $\gamma$ a ****_path joining $a$_ and $b$.

Prop:************ A path-connected set is connected.

********Th:******** Let $A\subseteq \Bbb R^n$ an nonempty open set. $A$ is connected iff $A$ is path-connected.

********Th:******** Let $A\subseteq \Bbb R^n$ be an open connected set, and $x, y \in A$, then there’s a [[Differentiabilty of vector valued functions of R|differentiable path]] $\gamma:[0,1] \to \Bbb R^n$ with $\gamma(0) = x$ and $\gamma(1) = y$

### Path-Covering Lemma

Suppose $\gamma:[a,b] \to U$ is a continuous path from the interval into an open subset $U$ of $\Bbb R^n$. Then there are a number $\rho >0$ and a partition $P$ of the interval $[a,b]$ such that:

- $B_\rho(t_k) \subseteq U$ for $k \in \{1, \dots, m\}$
- $\gamma(t) \in B_\rho(\gamma(t_0))$ for $t_0 \le t \le t_1$
- $\gamma(t) \in B_\rho(\gamma(t_k))$ for $t_{k-1} \le t \le t_{k+1}$
- $\gamma(t) \in B_\rho(\gamma(t_m))$ for $t_{m-1} \le t \le t_m$