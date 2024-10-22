---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Homotopy in C]]

**Def**: Let $\gamma:[a, b] \to \Bbb C$ continuous, we say that $\sigma:[a, b] \to \Bbb C$ is a logarithm if
- $\sigma$ is continuous
- $e^{\sigma(t)} = \gamma(t)$ for all $t \in [a,b]$

We see that if $\gamma$ has a logarithm, then $Z(\gamma) = \varnothing$. 

If $\sigma_1$ and $\sigma_2$ are logarithms of $\gamma$, then there exists $n \in \Bbb Z$ such that $\sigma_1 -\sigma_2 \equiv 2 n \pi i$ 

**Prop**: If $\gamma$ has a logarithm over $[a, c]$ and $[c, b]$, then it has logarithm over $[a,b]$

**Th**: We get the following result: Let $\gamma:[a,b] \to \Bbb C$ continuous. Then $\gamma$ has a logarithm iff $Z(\gamma) = \varnothing$. The first implication is trivial, and the second actually uses techniques similar to [[Contour Integration over Continuous Curves#Shabat's Technique|Shabat's Technique]] to integrate over continuous paths, which i find endearing.

# Index of continuous curves

Let $\gamma$ be a closed piecewise smooth curve that is never $0$, and let $\sigma_1, \sigma_2 :[a,b] \to \Bbb C$ be logarithms that means that $e^{\sigma_1(b)} = \gamma(b) = \gamma(a) = e^{\sigma_1(a)}$. Meaning that $\sigma_1(b) = \sigma_1(a) + 2n\pi i$, for some $n \in \Bbb Z$. For $\sigma_2(t) = \sigma_1(t) + 2m \pi i$ for some $m \in \Bbb Z$. Thus
$\sigma_1(b) - \sigma_1(a) = \sigma_2(b) - \sigma(a) = 2n \pi i$. Meaning that this last quantity doesn't depend on the choice of logarithm. 

Let $\varphi = \Im (\sigma)$, with $\sigma$ being a logarithm of $\gamma$, then $\varphi(t) \in \text{Arg}(\gamma(t))$, and $2n \pi i = \sigma(b) -\sigma(a) = \varphi(b) - \varphi(a)$ 

Another way to have the same result, is to consider to integrate over $\gamma$, meaning
$$\oint_\gamma \frac{1}{z} \, dz$$
which by [[Contour Integration over Continuous Curves#Shabat's Technique|Shabat's Technique]] we would find that both $\sigma_1$ and $\sigma_2$ are both be antiderivatives of $1/z$ along $\gamma$. 

**Def**: Let $\gamma:[a, b] \to \Bbb C$ be a closed continuous curve, and given $z \in \Bbb C \setminus \gamma$, we can define the index of $\gamma$ on $z$ as$$ n(\gamma;z) = \frac{1}{2\pi i}(\sigma(b) -\sigma(a))$$
with $\sigma$ being a logarithm of $\gamma - z$. Similarly we can make a similar definition to the index using [[Cauchy's Integral Formula]], and [[Contour Integration over Continuous Curves#Shabat's Technique|Shabat's Technique]] we can define it as $$ n(\gamma;z) = \frac{1}{2\pi i } \oint_\gamma \, \frac{1}{\zeta-z}\, d\zeta  = \frac{1}{2\pi i } \int_{\gamma-z} \frac{1}{\zeta}\, d\zeta$$
We see that $n(\gamma;z ) = n(\gamma -z; 0)$, with $\gamma$ piecewise smooth. 

**Prop**: We get this lemma, let $\gamma_0, \gamma_1: [a, b] \to \Bbb C\setminus \{0\}$ be closed curves 
- $n(\gamma_0 \gamma_1; 0) = n(\gamma_0; 0)+n(\gamma_1;0)$
- If for all $t\in [a, b]$ it satisfies that $|\gamma_0(t)-\gamma_1(t)| \le |\gamma_1(t)|$, then $n(\gamma_0; 0) = n(\gamma_1; 0)$

**Th**: Let $\gamma$ be a closed curve. Let $\varphi: \Bbb C\setminus \gamma \to \Bbb Z$ $\varphi(z) = n(\gamma;z)$. Then $\varphi$ is continuous at each connected component and if $V \subseteq \Bbb C\setminus \gamma$ is the unbounded connected component, then $\varphi|_V \equiv 0$ 

### Connection to Homology

Let $\gamma_0, \gamma_1:[a,b]\to U$ be closed piecewise smooth curves. If $\gamma_0 \simeq \gamma_1 \pmod U$, then $\gamma_0 \sim \gamma_1 \pmod U$ 

**Cor**: Let $\gamma:[a,b]\to U$ be a piecewise smooth curve. If $\gamma \simeq 0 \pmod U$, then $\gamma \sim 0 \pmod U$. 