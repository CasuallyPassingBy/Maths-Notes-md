---
tags:
  - Topology
---
Subjects: [[Topology]]
Links: [[Convergence of Filters]], [[Convergence of Sequences]], [[Directed Sets]], [[Cofinal and Coinitial Subsets]], [[Hausdorff Spaces]]

**Def:** A *net* on a set $X$ is a function $r: \Lambda \to X$, where $\Lambda$ is a directed set. To the point $r(\lambda)$ is denoted frequently as $x_\lambda$, and the expression "$r: \Lambda \to X$ is a net" is also written as "$(x_\lambda)_{\lambda \in \Lambda}$ is a net". 

**Obs:** Every sequence on $X$ is a net on $X$.

**Def:** A point $x$ is called a *limit of a net* $(x_\lambda)_{\lambda\in \Lambda}$ is for every neighbourhood $U$ of $x$ there exists a $\lambda_0 \in \Lambda$ such that $x_\lambda \in U$ for every $\lambda \ge \lambda_0$, we say that the net $(x_\lambda)_{\lambda\in \Lambda}$ *converges to $x$*. A net can converge to many points; the set of all limit points of the net $(x_\lambda)_{\lambda\in \Lambda}$ is denoted as $\lim_{\lambda \in \Lambda}x_\lambda$. 

**Def:** A point $x$ is called a *cluster point of a net $(x_\lambda)_{\lambda\in \Lambda}$* if for every neighbourhood $U$ of $x$ and every $\lambda_0 \in \Lambda$ there exists a $\lambda \ge \lambda_0$ such that $x_\lambda \in U$.

**Def:** We say that a net $(x_\sigma)_{\sigma \in \Sigma}$ is *finer* than the net $(x_\lambda)_{\lambda\in \Lambda}$ if there is a function $\phi: \Sigma \to \Lambda$ with the following properties:
- For every $\lambda_0 \in \Lambda$ there exists a $\sigma_0 \in \Sigma$ such that $\phi(\sigma) \ge \lambda_0$ whenever $\sigma \ge \sigma_0$.
- $x_{\phi(\sigma)} = x_\sigma$  for $\sigma \in \Sigma$.
We just make the observation that a non-decreasing function $\phi: \Sigma \to \Lambda$ such that $\phi[\Sigma]$ is cofinal in $\Lambda$. 

**Prop:** If $x$ is a cluster point of the net $(x_\sigma)_{\sigma\in \Sigma}$  that is finer than the net $(x_\lambda)_{\lambda\in \Lambda}$, then $x$ is a cluster point of $(x_\lambda)_{\lambda\in \Lambda}$. If $x$ is a limit point of the net $(x_\lambda)_{\lambda\in \Lambda}$, then $x$ is also a limit point of every net $(x_\sigma)_{\sigma\in \Sigma}$ finer than $(x_\lambda)_{\lambda\in \Lambda}$. If $x$ is a cluster point of the net $(x_\lambda)_{\lambda\in \Lambda}$, then $x$ is a limit point of a net $(x_\sigma)_{\sigma\in \Sigma}$  that is finer than $(x_\lambda)_{\lambda\in \Lambda}$. 

**Prop:** Let $A$ be subset of a topological space $X$. For any $x\in X$, $x \in \text{cl}_X(A)$ iff there's a net  $(x_\lambda)_{\lambda \in \Lambda}$ on $A$ that converges to $x$.

**Cor:** A set $A$ is closed iff if together with any net it contains its limit points.

**Cor:** the point $x \in \text{Lim}(A)$ iff there exists a net $(x_\lambda)_{\lambda\in \Lambda}$ that converges to $x$, such that $x_\lambda \in A$, and $x_\lambda \neq x$ for all $\lambda \in \Lambda$. 

**Prop:** Let $X$ and $Y$ be topological spaces, and $f: X \to Y$ be a function. $f$ is a continuous function iff $$f[\lim_{\lambda \in \Lambda} x_\lambda] \subseteq \lim_{\lambda \in \Lambda} f(x_\lambda)$$for every net $(x_\lambda)_{\lambda\in \Lambda}$ in the space $X$.
 
**Prop:** A topological space $X$ is a $T_2$ space iff every net in $X$ has at most one limit.

**Th:** For every net $(x_\lambda)_{\lambda\in \Lambda}$ in a topological space, the family $\mathcal F((x_\lambda)_{\lambda\in \Lambda})$ consisting of all sets $A \subseteq X$ with the property that there exists a $\lambda_0\in \Lambda$ such that $x_\lambda \in A$ whenever $\lambda \ge \lambda_0$ is f filter in the subspace and $\lim\mathcal F((x_\lambda)_{\lambda\in \Lambda}) = \lim_{\lambda\in \Lambda_0} x_\lambda$. If the net $(x_\sigma)_{\sigma\in \Sigma}$ is finer than the net $(x_\lambda)_{\lambda\in \Lambda}$, then the filter $\mathcal F ((x_\sigma)_{\sigma\in \Sigma})$ is finer than the filter $\mathcal F((x_\lambda)_{\lambda\in \Lambda})$. 

**Th:** Let $\mathcal F$ be a filter in a topological space $X$; let us denote $\Lambda$ the set of all pairs $(x, A)$, where $x\in A \in \cal F$ and let us define $(x_1, A_1) \le (x_2, A_2)$ if $A_2 \subseteq A_1$. The set $\Lambda$ is directed by $\le$, and for the net $(x_\lambda)_{\lambda\in \Lambda}$ is defined as $x_\lambda = x$ for $\lambda = (x, A) \in \Lambda$, we have that $\mathcal F = \mathcal F (\Lambda(\mathcal F))$ and $\lim_{\lambda \in \Lambda} x_\lambda = \lim \cal F$. 