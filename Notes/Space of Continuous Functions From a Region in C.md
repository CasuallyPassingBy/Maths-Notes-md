---
tags:
  - ComplexAnalysis
---
Links: [[Continuous Function Spaces]], [[The Riemann Sphere]], [[Equivalence of Metrics]]

We will consider $U$ a region in $\Bbb C$, being an open and connected set of $\Bbb C$. 

**Prop: $\star$:** If $U \subseteq \Bbb C$ is a region, there there's a sequence $\{K_n \mid n \in \Bbb N\}$ of compact sets such that:
- $U = \bigcup\limits_{n = 1}^\infty K_n$ 
- $K_n \subseteq \text{int}(K_n)$
- If $C\subseteq \widehat{\Bbb C}\setminus K_n$ is a connected component, then there's a $Q \subseteq \widehat{\Bbb C}\setminus U$ a connected component such that $Q \subseteq C$

This proposition will let us create a metric, on the space $\mathcal C(U, M)$ where $U$ is a region in $\Bbb C$ and $M$ is a metric. 

The obvious attempt, is to try the uniform metric. Let $U$ be a region in $\Bbb C$ and $M$ is metric space, then and $f, g\in \mathcal C(U, M)$, and the "metric" to be
$$
\rho(f, g) = \sup_{z\in U} d(f(z), g(z))
$$
We have problems since $U$ is not a compact set

By prop $\star$, we know that $U = \bigcup\limits_{n = 1}^\infty K_n$, then $U = \bigcup\limits_{n = 1}^\infty \text{int}(K_n)$. This allows us given $K \subseteq U$ a compact set, then there's a $n \in \Bbb N$ such that $K \subseteq \text{int}(K_n)$. 

**Obs:** For each $n \in \Bbb N$ let $\rho_n: \mathcal C(U, M)\times \mathcal C(U, M) \to \Bbb R$ given by
$$
\rho_n (f, g) = \sup_{z\in K_n}d(f(z), g(z))
$$
is a pseudometric on $\mathcal C(U, M)$, since if $\rho_n(f, g)=0$, then $f|_{K_n} = g|_{K_n}$.

**Prop:** We define the function $\rho: \mathcal C(U, M)\times \mathcal C(U, M) \to \Bbb R$ as 
$$
\rho(f, g) = \sum_{n = 1}^\infty \frac{1}{2^n}\frac{\rho_n(f, g)}{1+\rho_n(f, g)}
$$

$(\mathcal C(U, M), \rho)$ is a metric space

We now have metric on $\mathcal C(U, M)$, and thus a topology. Since the metric is really troublesome, we would like to try to study the topology in itself without using the metric. 

**Prop $\star\star$:** Consider the metric space $(\mathcal C(U, M), \rho)$
1. $\forall \varepsilon >0\exists \delta >0 \exists K \subseteq U$ compact, such that $\forall f, g \in \mathcal C(U, M)$ if $$ \sup_{z\in K} d(f(z), g(z)) < \delta \implies \rho(f, g) <\epsilon$$
2. $\forall \delta >0 \forall K \subseteq U$ compact, $\exists \varepsilon > 0$, such that $\forall f, g \in \mathcal C(U, M)$ if $$ \rho(f, g) < \varepsilon \implies \sup_{z \in K} d(f(z), g(z))<\delta$$
This is an incredibly technical proposition but it is the bridge to stop using the $\rho$ metric, since it gives an analogues of how the balls generated by the metric are.

**Th:** An open set $O \subseteq \mathcal C(U, M)$ is open iff for every $f \in O$ there's a $\delta >0$ and $K \subseteq U$ compact, such that $\{g \in \mathcal C(U, M) \mid \forall z \in K[d(f(z), g(z)<\delta]\}\subseteq O$.

**Cor:** the topology of $(\mathcal C(U, M), \rho)$ does **not** depend on the sequence $\{K_n\}_{n  \in \Bbb N}$ given by the prop $\star$, which is amazing.

**Th:** Let $\{f_n \mid n \in \Bbb N\}\subseteq \mathcal C(U, M)$, and $f\in \mathcal C(U, M)$:
- $f_n \stackrel{\rho}{\longrightarrow} f$ (converges on the metric $\rho$) iff $\forall K\subseteq U$ compact $f_n \rightrightarrows f$ on $K$ 
- $(f_n)$ is a Cauchy sequence in $(\mathcal C(U, M), \rho)$ iff $\forall K \subseteq U$ compact, $(f_n)$ is uniformly Cauchy on $K$

$(\mathcal C(U, M), \rho)$ is complete iff $(M, d)$ is complete

We would use normally a $(M, d)$ that is complete. 