---
tags:
  - Analysis
  - LinearAlgebra
---
Subjects: [[Metric and Normed Spaces]], [[Linear Algebra]]
Links: [[Multilinear Transformation]], [[Bounded Linear Operators]]

If $V_i= (V_i, \|\cdot\|_{V_i})$ for $i \in \{1, \dots, n\}$ and $W= (W, \|\cdot \|_W)$ be normed spaces. Let $F\in \mathcal L(V_1, \dots, V_n;W)$. Then the following are equivalent:
- $F$ is continuous
- $F$ is continuous at $0$
- There exists $c \in \Bbb R$, $\|F(v)\|_W \le c\|v_1\|_{V_1}\cdots \|v_n\|_{V_n}$ for all $v = (v_1, \dots, v_n) \in V_1 \times \dots \times V_n$, which i guess would be the analogue to a linear map being bounded

I will use $\mathcal B(V_1, \dots, V_n;W)$ to be $$\mathcal B(V_1, \dots, V_n;W):= \{F\in \mathcal L(V_1, \dots, V_n;W)\mid F\text{ is conitnuous}\}$$ we also define 
$$\|F\|_{\mathcal B(V_1, \dots, V_n;W)} := \sup_{\substack{v_j \in V_j \setminus\{0\} \\j \in \{1, \dots, n\}}}\frac{\|F(v_1, \dots, v_n)\|_{\mathcal B(V_1, \dots, V_n;W)}}{\|v_1\|_{V_1}\cdots \|v_n\|_{V_n}}$$
is a norm on $\mathcal B(V_1, \dots, V_n;W)$, and when $n =1$ it coincides with the norm for bounded linear transformations. 

In the case where $V_1 = \cdots = V_n = V$, then we write $$\mathcal B_n(V;W) := \mathcal B(V, \dots, V; W)$$

Similarly, as we had for multilinear transformations:

If we associate each $F \in \mathcal B(V_1, \dots, V_n; W)$ and the function $\tilde F \in \mathcal B(V_1, \mathcal B(V_2, \dots, V_n; W))$ given by $$\tilde (Fv_1)(v_2, \dots, v_n) := F(v_1, v_2, \dots, v_n)$$
We a vector space isomorphism and $$\mathcal B(V_1, \dots, V_n; W) \cong \mathcal B(V_1, \mathcal L(V_2, \dots, V_n;W))$$
not only that but, this is also an isometry. Iterating over this isomorphism, we can "unpack", and get something like: $$\mathcal B(V_1, \dots, V_n; W)\cong \mathcal B(V_1, \mathcal B(V_2, \cdots, \mathcal B(V_{n-1}, \mathcal B(V_n, W))\cdots))$$
if $W$ is a Banach space, then $\mathcal B(V_1, \dots, V_n; W)$ is a Banach space