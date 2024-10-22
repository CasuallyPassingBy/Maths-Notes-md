---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]]

**Th (Alfors):** Let $z_0 \in \Bbb C$ be an isolated singularity of the non constant function $f$. The following are equivalent:
- $z_0 \in\Bbb C$ is a removable singularity or a pole of $f$
    
- there’s $k\in \Bbb Z$ such that given $\alpha \in \Bbb R$, it is satisfied that
    
    - If $\alpha < k$
        
        $$ \lim_{z\to z_0}|z-z_0|^\alpha |f(z)| = \infty $$
        
    - If $\alpha = k$
        
        $$ \lim_{z\to z_0}|z-z_0|^\alpha |f(z)| = |l| \ne 0 $$
        
    - If $\alpha > k$
        
        $$ \lim_{z\to z_0}|z-z_0|^\alpha |f(z)| = 0 $$
        
- There’s $\alpha \in \Bbb R$ such that   $$ \lim_{z\to z_0}|z-z_0|^\alpha |f(z)| = \infty \quad \text{ or } \quad \lim_{z\to z_0}|z-z_0|^\alpha |f(z)| = 0 $$
********Def:******** Let $z_0 \in \Bbb C$ be an isolated singularity of $f$. We say that $z_0$ is a essential singularity of $f$ if $z_0$ is neither a removable singularity nor a pole of $f$

**Prop:** Let $z_0 \in \Bbb C$ is a isolated singularity of $f$. It follows that: $z_0$ is an essential singularity of $f$ iff for all $\alpha \in \Bbb R$, it has that $\lim_{z\to z_0}|z-z_0|^\alpha|f(z)|$ doesn’t exist

**Th:** Let $z_0 \in \Bbb C$ is a isolated singularity of $f$. It follows that: $z_0$ is an essential singularity of $f$ iff for all $w\in \Bbb C$, and every $\varepsilon>0$ and all $\delta> 0$, there’s $z\in B_\delta(z_0)\setminus \{z_0\}$ such that $f(z) \in B_\varepsilon(w)$

**Cor:** Let $z_0$ is an essential singularity of $f$, then for any $w \in \Bbb C$ there’s a sequence $(z_n)$ with ${z_n \ne z_0}$ for all $n \in \Bbb N$, such that $z_n \to z_0$ and $f(z_n) \to w$.
