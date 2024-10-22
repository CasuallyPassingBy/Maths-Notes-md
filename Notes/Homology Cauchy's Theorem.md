---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Contour Integrals in C]], [[Analytic Functions]], [[Homology in C]]

Def: Let $\Omega \subseteq\Bbb C$ be a region. We say that $\Omega$ is simply connected if $\hat{\Bbb C}\setminus \Omega$ is connected in $\hat{\Bbb C}$.

Let $\Omega \subseteq \Bbb C$ be a region. The the region $\Omega$ is simply connected iff for every $\gamma\subseteq \Omega$ closed piecewise smooth and for every $z \in \Bbb C\setminus \Omega$ we have that $n(\gamma;z)= 0$

Let $\Omega \subseteq \Bbb C$ be a region. The the region $\Omega$ is simply connected iff for every $\gamma\subseteq \Omega$ cycle and for every $z \in \Bbb C\setminus \Omega$ we have that $n(\gamma;z)= 0$ ^e7f410

Let $\Omega \subseteq \Bbb C$ be a region. We say that $\gamma\subseteq \Omega$ a cycle is homologous to $0$ in $\Omega$, which is denote as $\gamma \sim 0 \pmod \Omega$, if it satisfies that that $n(\gamma; z) =0$ for every $z\in \Bbb C\setminus \Omega$. We will also say that two cycles $\gamma, \tilde \gamma \subseteq \Omega$ are homologous in $\Omega$, denoted as $\gamma \sim \tilde \gamma \pmod \Omega$, if it satisifies that ${\gamma -\tilde\gamma \sim 0 \pmod \Omega}$, i.e., for every $z\in\Bbb C\setminus \Omega$, we have that $n(\gamma-\tilde \gamma; z) =0$.

This means that a region $\Omega\subseteq \Bbb C$, is simply connected if every cycle $\gamma\subseteq\Omega$ is homologous to $0$ in $\Omega$.

Let $f:\Omega \subseteq\Bbb C \to \Bbb C$ is continuous in $\Omega$. The following statements are equivalent:

- For every cycle $\gamma\subseteq \Omega$ such that $\gamma \sim 0 \pmod \Omega$, it satisfies that
    
    $$ \oint_\gamma f(z) \, dz =0 $$
    
- For any two cycles $\gamma, \tilde \gamma \subseteq \Omega$ such that $\gamma \sim \tilde\gamma \pmod \Omega$, it satisfies that
    
    $$ \oint_\gamma f(z)\, dz = \oint_{\tilde \gamma} f(z)\, dz $$
    

### Homology Cauchy’s Theorem
Let $\Omega \subseteq\Bbb C$ be a region, and $f:\Omega \to \Bbb C$. If $f$ is analytic in $\Omega$, then

$$ \oint_\gamma f(z)\, dz =0 $$

for every cycle $\gamma \subseteq \Omega$ such that $\gamma \sim 0\pmod \Omega$.

Let $\Omega \subseteq\Bbb C$ be a region, and $f:\Omega \to \Bbb C$ anlytic. If $\Omega$ is simply connected then

$$ \oint_\gamma f(z) \, dz =0 $$

for every piecewise smooth closed curve $\gamma \subseteq \Omega$

Let $\Omega \subseteq\Bbb C$ be a region, and $f:\Omega \to \Bbb C$ anlytic. For any two cycles $\gamma, \tilde \gamma \subseteq \Omega$ such that ${\gamma \sim \tilde \gamma \pmod \Omega}$, then

$$ \oint_\gamma f(z)\, dz = \oint_{\tilde \gamma} f(z)\, dz $$

Let $\Omega \subseteq\Bbb C$ be a simply connected region region, and $f:\Omega \to \Bbb C$ anlytic. If $f(z)\ne 0$ for all ${z\in \Omega}$, there exist, defined on $\Omega$, logarithm branches and $n$th roots of $f$