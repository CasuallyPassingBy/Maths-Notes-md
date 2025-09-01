---
tags:
  - GroupTheory
---
Subjects: [[Group Theory]]
Links: [[Groups]], [[Subgroups]], [[Lie Groups]], [[Affine Spaces]]

Let $E(n)$ denote the subgroup of $\text{GL}(n+1,\Bbb R)$ consisting of the form $$\left\{\left.\begin{pmatrix} A & b \\ 0 & 1\end{pmatrix}\; \right\rvert\; A \in \text{O}(n), b\in \Bbb R^n\right\},$$where $b$ is considered as an $n\times 1$ column matrix. We can see that $E(n)$ is an embedded Lie subgroup. If $S\subseteq \Bbb R^{n+1}$ denoted the affine subspace defined by $x^{n+1} = 1$, then a simple computation shows that $E(n)$ takes $S$ to itself. If we identify $S$ with $\Bbb R^n$ in the obvious way, this induces a smooth action of $E(n)$ on $\Bbb R^n$, in which the matrix $\begin{pmatrix} A & b \\ 0 & 1\end{pmatrix}$ sends $x$ to $Ax + b$. 

We know that it is the set of $\text E(n)$ is the subgroup of $\text{Diffeo}(\Bbb R^n)$ that preserves the Euclidean distance function. For this reason $\text E(n)$ is called the *Euclidean group*. Because any point in $\Bbb R^n$ can be taken to any other by translation, $\text E(n)$ acts transitively on $\Bbb R^n, so $\Bbb R^n$ is a homogeneous $\text E(n)$-space.

If we want to also preserve the orientation of $\Bbb R^n$, wee need to consider the *special euclidean group* $$\text{SE}(n) := \left\{\left.\begin{pmatrix} A & b \\ 0 & 1\end{pmatrix}\; \right\rvert\; A \in \text{SO}(n), b\in \Bbb R^n\right\}.$$
Lastly, we see that $\text{SE}(n)$ also acts transitively on $\Bbb R^n$, so it is a homogeneous $\text{SE}(n)$-space.

We can decompose $\text E(n)$ and $\text{SE}(n)$ into a [[Semidirect Product of Groups|semidirect product]]: $$\text{E}(n) = \Bbb R^n \rtimes \text O(n), \quad \text{SE}(n) = \Bbb R^n \rtimes \text{SO}(n). $$
From this we see that there's an embedding from $\text O(n) \hookrightarrow \text E(n)$. 

Because the group $\text E(n)$ acts smoothly and transitively on $\Bbb R^n$, and the stabiliser group of the origin is the subgroup $\text O(n)$, then $\Bbb R^n$ is diffeomorphic to $\text{E}(n)/\text{O}(n)$, and to $\text{SE}(n)/\text{SO}(n)$. This is something we can see from the algebraic point of view, but is nice to see it is also true from the topological perspective.