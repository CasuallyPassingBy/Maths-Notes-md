---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Normal Families]], [[Compactness in Metric Spaces]], [[Relative Compactness in Metric Spaces]]

Let $(M, d)$ be a complete metric space, and $U \subseteq \Bbb C$ a region, and the topology of $\mathcal C(U, M)$ given in [[Space of Continuous Functions From a Region in C]]

**Def:** A family $\mathcal F \subseteq \mathcal C(U, M)$ is called **normal** if every sequence $\{f_n\}\subseteq \mathcal F$ there's an $f\in \mathcal C(U, M)$, and there's $\{f_{n_k}\}$ is a subsequence of $\{f_n\}$, such that $f_{n_k}\stackrel{\rho}{\longrightarrow} f$ 

**Prop:** We get that $\mathcal F \subseteq \mathcal C(U, M)$ is normal iff $\cal F$ is relatively compact iff $\overline{\cal F}$ is compact

**Th:** Let $\mathcal F \subseteq \mathcal C(U, M)$. Then $\mathcal F$ is normal iff $\forall \delta >0 \forall K \subseteq U$ compact, there's $A \subseteq \mathcal F$  such that for any $f\in \mathcal F$, there's $g\in A$ such that
$$
\sup_{z\in K} d(f(z), g(z)) <\delta
$$
Using the prop $\star\star$ of [[Space of Continuous Functions From a Region in C]], we can see that a ball of $(\mathcal C(U, M), \rho)$ is basically the same as looking for a compact set $K$ and a $\delta>0$, such that it behaves really closely to being in the ball. So this proposition is basically a reformulation of $\mathcal F$ being [[Total Boundedness|totally bounded]].

## Arzelà–Ascoli Theorem
$\mathcal F\subseteq \mathcal C(U, M)$, where $\mathcal C(U, M)$ is complete, $\mathcal F$ is normal iff it satisfies:
- for every $z \in U$ the set $A_z = \{f(z) \mid z \in \mathcal F\}$ is relatively compact
- $\cal F$ is equicontinuous on $U$. 

Which is probably related to the [[Arzelà–Ascoli Theorem]] from Analysis.

**Def:** Let $U \subseteq \Bbb C$ be a region, and $\mathcal H(U) := \{f : U \to \Bbb C \mid f \text{ is holomorphic}\}$, and $\mathcal H(U) \subseteq \mathcal C(U, \Bbb C)$. 

**Prop:** Using the [[Analytic Convergence#Weiestrass Convergence Theorem|Weierstrass Convergence Theorem]], we can see a couple of things:
Let $\{f_n\}\subseteq \mathcal H(U)$ be a sequence, such that $f_n \rightrightarrows f$ on every $K\subseteq U$ compact.
- $f \in \mathcal H(U)$ 
- $\forall k \in \Bbb N$, we have that $f_n^{(k)} \stackrel{\rho}{\longrightarrow} f^{(k)}$  

Thus $(\mathcal H(U), \rho)$ is complete
The operator $D: \mathcal H(U) \to \mathcal H(U)$ given by $D(f) = f'$, is continuous.

### Montel Theorem
Let $\mathcal F\subseteq \mathcal H(U)$. Then $\cal F$ is normal iff $\cal F$ is [[Uniform Boundedness|locally bounded]] on $U$.

We can reformulate [[Argument Principle#Hurwitz Theorem|Hurwirtz Theorem]] 
### Hurwitz's Theorem
Let $\{f_n\} \subseteq \mathcal H(U)$, such that $f_n \stackrel{\rho}{\longrightarrow} f$, if there's an $a\in U$ and there's $r>0$ with $\overline{B_r(a)} \subseteq U$ such that for all $\forall z \in \partial B_r(a)$, $f(z) \ne 0$, then there's $N\in \Bbb N$ such that if $n \ge N$ then $f_n$ and $f$ have the same number of zeros on $B_r(a)$, counting multiplicity

**Prop:** Let $\{f_n\} \subseteq \mathcal H(U)$, such that $f_n \stackrel{\rho}{\longrightarrow} f$. If $Z(f_n) = \varnothing$ for all $n \in \Bbb N$ , then $Z(f) = \varnothing$ or $f\equiv 0$. 

**Prop**: Let $\{f_n\} \subseteq \mathcal H(U)$, such that $f_n \stackrel{\rho}{\longrightarrow} f$. If every $f_n$ injective, then $f$ is injective or $f$ is constant

