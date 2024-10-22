---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Isolated Singularities]]

**Def:** Let $\Omega\subseteq \Bbb C$ be a region, $z_0 \in \Omega$ and $f:\Omega\setminus\{z_0\} \to \Bbb C$ analytic. We say that $z_0$ is a **removable singularity** of $f$ if there’s $\tilde f:\Omega\to\Bbb C$ analytic such that $\tilde f(z) = f(z)$ for $z \in \Omega\setminus \{z_0\}$

**********Prop:********** Let $\Omega\subseteq \Bbb C$ be a region, $z_0 \in \Omega$ and $f:\Omega\setminus\{z_0\} \to \Bbb C$ analytic. The point $z_0$ is removable singularity of $f$ iff

$$ \lim_{z \to z_0}(z-z_0)f(z) = 0 $$

iff

$$ \lim_{z\to z_0}f(z) \text { exists in }\Bbb C $$

iff there’s an $>0$ such that $f$ is bounded in $B_r(z_0) \setminus \{z_0\}$