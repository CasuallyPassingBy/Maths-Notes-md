---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Contour Integrals in C]], [[Analytic Functions]]

Let $\Omega \subseteq \Bbb C$ be a region and $\gamma_i:[a_i, b_i]\to\Omega$ a piecewise smooth closed curve for $i \in \{1, \dots, n\}$. The union of the curves $\text{Im } \gamma_i$ along with their corresponding parametrizations $\gamma_i$ we will call it a cycle and we will denote it as

$$ \gamma_1+\gamma_2+\dots+\gamma_n $$

In the special case where we want to have reverse the direction of a cycle we have that

$$ -(\gamma_1+\gamma_2+\dots+\gamma_n) := (-\gamma_1)+(-\gamma_2)+\dots+(-\gamma_n) $$

Let $f:\Omega \subseteq \Bbb C \to \Bbb C$ be a continuous function and $\gamma$ be a cycle made out of closed piecewise smooth curves $\gamma_1, \gamma_2, \dots, \gamma_k$. We define the integral of $f$ over the cycle $\gamma$, denoted as $\int_\gamma f(z)\, dz$, as

$$ \oint_\gamma f(z)\, dz = \oint\limits_{\gamma_1+\gamma_2+\dots+\gamma_k} f(z)\, dz := \sum_{j =1}^k \oint_{\gamma_j} f(z)\, dz $$

Let $\gamma$ be a cycle made out of closed piecewise smooth curves $\gamma_1, \gamma_2, \dots, \gamma_k$, and $z_0 \in\Bbb C\setminus \gamma$. We define the index of the point $z_0$ with respect to $\gamma$, denoted as

$$ n(\gamma;z_0)= n( \gamma_1+\gamma_2+\dots+\gamma_n; z_0) $$

as

$$ n(\gamma;z_0) := \oint_\gamma \frac{1}{z-z_0}\, dz $$

We can use the definition of the integral to get that

$$ n(\gamma; z_0) = \sum_{j = 1}^k n(\gamma_j;z_0) $$

Let $\gamma$ be a cycle made out of closed piecewise smooth curves $\gamma_1, \gamma_2, \dots, \gamma_k$.

- If $z_0 \in \Bbb C$ and $\delta>0$ such that $\gamma \subseteq B_\delta (z_0)$, then $n(\gamma; w) =0$ for all $w \not \in B_\delta(z_0)$
- If $z, w\in \Bbb C$ belong to the same connected component of $\Bbb C\setminus \gamma$, then $n(\gamma; z) = n(\gamma;w)$
- If $z \in \Bbb C$ belongs to the unbounded connected component of $\Bbb C\setminus \gamma$, then $n(\gamma; z) = 0$

We can extend further the "cycle arithmetic", and we can multiply a closed curve by number $m \in \Bbb Z$. 
Let $\gamma$ be a piecewise smooth closed curve, and $m \in \Bbb N$, then we can define 
$$
m \cdot \gamma := \underbrace{\gamma + \gamma + \dots + \gamma}_{m \text{ times}}
$$
and if $m \in \Bbb Z^-$, we can define it as
$$
m \cdot \gamma := \underbrace{(-\gamma)+ (-\gamma) + \dots +(-\gamma)}_{|m|\text{ times}}
$$
Let $\Omega \subset \Bbb C$ be a region, and $z_1, z_2, \dots, z_n \in \Omega$. Let $\gamma_k$ be a piecewise smooth closed curve for $k \in \{1, \dots, n\}$ such that
$$
n(\gamma_k, z_j) = \delta_{k, j}
$$
Where this is a Kronecker delta. 

With this we can make $\gamma \subseteq \Omega\setminus\{z_1, \dots, z_n\}$, and $n(\gamma, z_k) = m_k$, then
$$
\gamma\sim \sum_{k = 1}^n m_k \cdot \gamma_k \pmod {\Omega\setminus\{z_1, \dots, z_n\}}
$$
In this way we can get that if $f:\Omega\setminus\{z_1, \dots, z_n\} \to \Bbb C$ is analytic then
$$
\oint_\gamma f (z)\, dz = \sum_{k = 1}^n m_k \cdot \oint_{\gamma_k} f(z)\, dz
$$
using [[Homology Cauchy's Theorem|Cauchy's Theorem]]. 

We can extend the theorem above:
Let $\Omega \subseteq \Bbb C$ be a region, $\{z_1, \dots, z_n, \dots\}\subseteq \Omega$ be an infinite set such that has no accumulation point on $\Omega$, and $r_1, \dots, r_n, \dots$ be positive real numbers that satisfies $\overline B(z_k, r_k)\setminus \{z_k\} \subseteq \Omega$ for $k\in \Bbb N$. If $f: \Omega\setminus\{z_1,\dots, z_n, \dots\}\to \Bbb C$ is analytic, then for any cycle $\gamma \subseteq \Omega\setminus\{z_1, \dots, z_n, \dots\}$ such that $\gamma \sim 0 \pmod \Omega$, then
$$
\oint_\gamma f (z)\, dz = \sum_{k = 1}^n m_k \cdot \oint_{\gamma_k} f(z)\, dz
$$

Lastly we can define what happens to a cycle under the image of a continuous function. Let 
$$
\gamma = \gamma_1 +\gamma_2 +\dots+\gamma_n 
$$
with $\gamma \subseteq \Omega$, and $f:\Omega \to \Bbb C$, then we denote the cycle $f \circ \gamma$ formed by the closed curves 
$$
f\circ \gamma := f\circ \gamma_1 +f\circ \gamma_2 +\dots + f\circ \gamma_n
$$
