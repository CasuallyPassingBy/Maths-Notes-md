---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Separable, First and Second Countable Spaces]], [[Topological Covers]], [[Special Types of Collections in Topology]]

**Def:** We say sequence of open covers $\{\mathcal U_n \mid n <\omega\}$ of a topological space $X$ is a *developement* if for every point $x\in X$, the collection $\{\text{st}(x, \mathcal U_n)\mid n <\omega\}$ is a local base for $X$ at $x$. We say that $X$ is *developable* if $X$ has a development.

**Prop:** If $X$ is developable, then there's a development $\{\mathcal U_n \mid n <\omega\}$ such that $\mathcal U_n$ is refinement of $\mathcal U_m$ for any $m \le n < \omega$.

**Obs:** We see that every developable space is first countable. 

**Def:** We say sequence of open covers $\{\mathcal U_n \mid n <\omega\}$ of a topological space $X$ is a *strong developement* if for every point $x\in X$ and every $U \in \tau_X$ with $x\in U$, there's a $V\in \tau_X$  and $n <\omega$ such that $\text{st}(V, \mathcal U_n) \subseteq U$. We say that $X$ is *strongly developable* if $X$ has a strong development. 

**Prop:** If $X$ is strongly developable, then there's a strong development $\{\mathcal U_n \mid n <\omega\}$ such that $\mathcal U_n$ is refinement of $\mathcal U_m$ for any $m \le n < \omega$.

**Def:** Let $\{\mathcal U_n \mid n <\omega\}$ be a development. We say that $\{\mathcal U_n \mid n <\omega\}$ is a *point-finite development* (resp., *locally finite developement*) if each $\mathcal U_n$ is a point finite (resp., locally finite) family. Naturally, we say that $X$ is *point finite developable* (resp., *locally finite developable*) if has a point-finite development (resp., locally finite developement).

**Def:** We say sequence of open covers $\{\mathcal U_n \mid n <\omega\}$ of a topological space $X$ is a *$\cal K$-developement* if for every compact $K \subseteq X$, and any $U \in \tau_X$ with $K \subseteq U$, then there's an $n<\omega$ such that $\text{st}(K, \mathcal U_n) \subseteq U$. We say that $X$ is *$\cal K$-developable* if $X$ has a $\cal K$-developement. 

**Prop:** If $X$ is $\cal K$-developable, then there's a $\cal K$-development $\{\mathcal U_n \mid n <\omega\}$ such that $\mathcal U_n$ is refinement of $\mathcal U_m$ for any $m \le n < \omega$.

**Prop:** A topological space is $\cal K$-developable iff it is strongly developable.