---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Normed Spaces]], [[Complete Metric Spaces]], [[Continuity on Metric Spaces]], [[Norm of Linear Operators for finite dimensions]], [[Space of Linear Transformations]]

If $V=(V, \|\cdot\|_V)$ and $W= (W, \|\cdot\|_W)$ be normed spaces and $L:V\to W$a linear transformation. Then all the following are equivalents:
- $L$ is continuous
- $L$ is continuous at $0$
- There’s a $c >0$ such that $\|Lv\|_W \le c\|v\|_V$ for all $v \in V$, this is called a *bounded transformation*
- $L$ is Lipschitz continuous.

We will denote ${\cal B}(V, W)$ to be
$$
	{\cal B}(V, W) :=\{T: V \to W\mid T \text{ is linear and bounded}\}
$$
and we define 
$$
\|T\|_{{\cal B}(V, W)} := \sup_{\substack{v \in V \\ v \ne 0}} \frac{\|Tw\|_W}{\|v\|_V}
$$
We can see that ${\cal B}(V, W)$ is a vector space, and $\| \cdot \|_{{\cal B}(V, W)}$ is a norm, thus, $({\cal B}(V, W), \|\cdot \|_{{\cal B}(V, W)})$ is a normed space.

We can see that, that since every $T$ is linear then we can divide by the norm of the vector and we get that $v/\|v\|_V \in S_V$
$$
\|T\|_{{\cal B}(V, W)} = \sup_{v\in S_V} \|Tv\|_W
$$
Similarly we get the, that for any $v \in V$, we get that 
$$
	\|Tv\|_W \le \|T\|_{{\cal B}(V, W)}\|v\|_V
$$
In the case that $V$ is a finite dimensional vector space, then ${\cal L}(V, W) = {\cal B}(V, W)$, since every linear map is continuous. 

If $W$ is a Banach space, then ${\cal B}(V, W)$ is a Banach space with the metric described above.

Let $S_k \to S$ in $\mathcal B(V, W)$ and $T_k \to T$ on $\mathcal B(W, Z)$, then $T_k \circ S_k \to T\circ S$. 