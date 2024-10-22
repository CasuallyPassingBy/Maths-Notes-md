---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[Zeros of Analytic Functions]], [[Poles of Analytic Functions]], [[Homology in C]]

### Argument Principle (Local Ver)

Let $\Delta \subseteq \Bbb C$ be an open ball and $a_1, \dots, a_n, b_1, \dots, b_m \in \Delta$. If $f$ is a meromorphic on $\Delta$ such that $a_j$ is a zero of order $k_j \in \Bbb N^+$, for each $j \in \{1, \dots, n\}$ and $b_l$ is a pole of $f$ of order $h_l$ for ${l \in \{1, \dots, m\}}$, then

$$ \frac{1}{2\pi i }\oint_\gamma \frac{f'(z)}{f(z)}\, dz = \sum_{j =1}^n k_j \cdot n(\gamma, a_i)- \sum_{l = 1}^m h_l\cdot n(\gamma, b_l) $$

for all $\gamma \subseteq \Delta \setminus \{a_1, \dots, a_n, b_1, \dots, b_m\}$ that is piecewise smooth closed curve

**********Cor:********** Let $\Delta \subseteq \Bbb C$ be an open ball and $a_1, \dots, a_n, b_1, \dots, b_m \in \Delta$. If $f$ is a meromorphic on $\Delta$ such that $a_j$ is a zero of order $k_j \in \Bbb N^+$, for each $j \in \{1, \dots, n\}$ and $b_l$ is a pole of $f$ of order $h_l$ for ${l \in \{1, \dots, m\}}$. If $\gamma \subseteq \Delta \setminus \{a_1, \dots, a_n, b_1, \dots, b_m\}$ that is piecewise smooth closed curve and ${\tilde \gamma = f\circ \gamma}$, then

$$ n(\tilde \gamma; 0) = \frac{1}{2\pi i }\oint_\gamma \frac{f'(z)}{f(z)}\, dz = \sum_{j =1}^n k_j \cdot n(\gamma, a_i)- \sum_{l = 1}^m h_l\cdot n(\gamma, b_l) $$

**********Cor:********** Let $\Delta \subseteq \Bbb C$ be an open ball and $a_1, \dots, a_n, b_1, \dots, b_m \in \Delta$. If $f$ is a meromorphic on $\Delta$ such that $a_j$ is a zero of order $k_j \in \Bbb N^+$, for each $j \in \{1, \dots, n\}$ and $b_l$ is a pole of $f$ of order $h_l$ for ${l \in \{1, \dots, m\}}$. If $\gamma \subseteq \Delta \setminus \{a_1, \dots, a_n, b_1, \dots, b_m\}$ that is piecewise smooth closed curve such that $n(\gamma; z)$ can only take the values of $0$ or $1$ and $\tilde \gamma = f\circ \gamma$ , then

$$ n(\tilde \gamma;0) = (\#\text{ of zeros} - \# \text{ of poles })\text{ of }f \text{ trapped by }\gamma $$

******Th (Ahlfors):****** Let $f:\Omega \to\Bbb C$ analytic, $z_0 \in \Delta \subseteq \Omega$, $\Delta$ an open ball, and $w_0 = f(z_0)$. If $z_0$ is a zero of order $k$ of the function $g(z) =f(z) -w_0$ for all $z \in \Delta$, then there exist $\varepsilon, \delta >0$ such that $w\in B_\varepsilon(w_0) \setminus \{w_0\}$ the identity $f(z) = w$ has exactly $k$ solutions in $B_\delta(z_0) \setminus\{z_0\}$. Additionally, we can find $\delta>0$ such that all the soltions of the identity $f(z) = w$ are different from each other.

********Cor:******** Let $f:\Omega \to \Bbb C$ analytic and $U \subseteq \Omega$ be an open subset. If $f$ is nonconstant, then $f[U]\subseteq\Bbb C$ is an open set.

********Cor:******** Let $f:\Omega \to \Bbb C$ analytic. If $f$ is injective in the region $\Omega$, $f'(z) \ne 0$ for all $z \in \Omega$

******Prop:****** Let $f:\Omega \to \Bbb C$ analytic. If $f$ injective in the region $\Omega$, then the inverse function ${f^{-1}:f[\Omega] \to \Omega}$ is analytic in $f[\Omega]$ (is also a region) and additionally $(f^{-1})'(w)\ne0$ for all ${w\in \Omega}$

************Prop:************ Let $f:\Omega \to \Bbb C$ analytic and injective in $\Omega$. If $z_0 \in \Omega$ and $R>0$ such that $B_R(z_0) \subseteq \Omega$ and $\gamma_r(t)= re^{it} +z_0$, with $t \in [0, 2\pi]$ and $0<r<R$, then

$$ f^{-1}(w) = \frac{1}{2\pi i}\oint_{\gamma_r} \zeta \frac{f'(\zeta)}{f(\zeta)-w}\, d\zeta $$

**********************************************************************************************Inverse Function Theorem for Analytic Functions**********************************************************************************************

Let $f:\Omega \to \Bbb C$ analytic. If $z_0 \in \Omega$ is such that $f'(z_0) \ne 0$, then there’s $r>0$ such that $f$ is injective on $B_r(z_0)$, $f[B_r(z_0)]$ is open, $f^{-1}$ is analytic on $f[B_r(z_0)]$ and

$$ (f^{-1})'(w) = \frac{1}{f'(f^{-1}(w))}\ne 0 $$

for all $w \in f^{-1}[B_r(w_0)]$

### Rouché-Gliksberg Theorem
Let $f$ and $g$ be meromorphic functions on the disk $\Delta\subseteq \Bbb C$ and $\gamma\subseteq \Delta$ be a piecewise smooth closed curve such that $n(\gamma; z) =0$ or $n(\gamma; z) =1$ for all $z \in \Delta \setminus \gamma$. Let $Z_f$ be the number of zeros of $f$ enclosed by $\gamma$ counted with multiplicities, $P_f$ the number of poles of $f$ enclosed by $\gamma$ counted with multiplicities, and $Z_g$ and $P_g$ be the corresponding ones for the function $g$. If $f$ and $g$ are such that

$$ |f(z) +g(z) | <|f(z)|+|g(z)| $$

for all $z \in \gamma$, then

$$ Z_f -P_f = Z_g-P_g $$

### Rouché Theorem
Let $f$ and $g$ be analytic functions on the disk $\Delta\subseteq \Bbb C$ and $\gamma\subseteq \Delta$ be a piecewise smooth closed curve such that $n(\gamma; z) =0$ or $n(\gamma; z) =1$ for all $z \in \Delta \setminus \gamma$. Let $Z_f$ be the number of zeros of $f$ enclosed by $\gamma$ counted with multiplicities, $P_f$ the number of poles of $f$ enclosed by $\gamma$ counted with multiplicities, and $Z_g$ and $P_g$ be the corresponding ones for the function $g$. If $f$ and $g$ are such that

$$ |f(z) -g(z) | <|g(z)| $$

for all $z \in \gamma$, then

$$ Z_f = Z_g $$
### Hurwitz's Theorem
Let $f_n , f:\Delta \to\Bbb C$ analytics on the disk $\Delta$ and $\gamma\subseteq \Delta$ be a piecewise smooth closed curve such that $n(\gamma; z) =0$ or $n(\gamma; z) =1$ for all $z \in \Delta \setminus \gamma$. If the the sequence $f_n$ converges uniformly to $f$ over $\gamma$ and $f(z) \ne 0$ for all $z \in \gamma$, then there exists $N\in \Bbb N$ such that for all $n \ge N$ the functions $f_n$ and $f$ have the same amount of zeros enclosed by $\gamma$

**Prop:** Let $f_n: \Omega \to \Bbb C$ be a sequence of analytic functions such that it converges uniformly to $f$ over any compact set $K \subseteq \Omega$. If $f_n (z) \ne 0$ for all $n \in \Bbb N$ and for all $z \in \Omega$, then $f$ is the constant $0$ or $f(z) \ne0$ for all $z \in \Omega$

## Argument Principle
Let $\Omega \subseteq \Bbb C$ be an region and $a_1, \dots, a_n, b_1, \dots, b_m \in \Omega$. If $f$ is a meromorphic on $\Omega$ such that $a_j$ is a zero of order $k_j \in \Bbb N^+$, for each $j \in \{1, \dots, n\}$ and $b_l$ is a pole of $f$ of order $h_l$ for ${l \in \{1, \dots, m\}}$, then

$$ \frac{1}{2\pi i }\oint_\gamma \frac{f'(z)}{f(z)}\, dz = \sum_{j =1}^n k_j \cdot n(\gamma, a_i)- \sum_{l = 1}^m h_l\cdot n(\gamma, b_l) $$

for any cycle $\gamma \subseteq \Omega \setminus \{a_1, \dots, a_n, b_1, \dots, b_m\}$ that is $\gamma \sim 0 \pmod \Omega$. This can be done using the [[Residue Theorem]]

**Cor:** Let $\Omega \subseteq \Bbb C$ be an open ball and $a_1, \dots, a_n, b_1, \dots, b_m \in \Omega$. If $f$ is a meromorphic on $\Omega$ such that $a_j$ is a zero of order $k_j \in \Bbb N^+$, for each $j \in \{1, \dots, n\}$ and $b_l$ is a pole of $f$ of order $h_l$ for ${l \in \{1, \dots, m\}}$. If $\gamma \subseteq \Omega \setminus \{a_1, \dots, a_n, b_1, \dots, b_m\}$ that cycle that $\gamma \sim 0 \pmod \Omega$ and ${\tilde \gamma = f\circ \gamma}$, then

$$ n(\tilde \gamma; 0) = \frac{1}{2\pi i }\oint_\gamma \frac{f'(z)}{f(z)}\, dz = \sum_{j =1}^n k_j \cdot n(\gamma, a_i)- \sum_{l = 1}^m h_l\cdot n(\gamma, b_l) $$

**********Cor:********** Let $\Omega \subseteq \Bbb C$ be an open ball and $a_1, \dots, a_n, b_1, \dots, b_m \in \Omega$. If $f$ is a meromorphic on $\Omega$ such that $a_j$ is a zero of order $k_j \in \Bbb N^+$, for each $j \in \{1, \dots, n\}$ and $b_l$ is a pole of $f$ of order $h_l$ for ${l \in \{1, \dots, m\}}$. If $\gamma \subseteq \Omega \setminus \{a_1, \dots, a_n, b_1, \dots, b_m\}$ that is cycle such that $\gamma \sim 0 \pmod \Omega$ and $n(\gamma; z)$ can only take the values of $0$ or $1$ and $\tilde \gamma = f\circ \gamma$ , then

$$ n(\tilde \gamma;0) = (\#\text{ of zeros} - \# \text{ of poles })\text{ of }f \text{ trapped by }\gamma $$

We can extend this to get that:

Let $\Omega \subseteq \Bbb C$ be an region and $a_1, \dots, a_n, b_1, \dots, b_m \in \Omega$. If $f$ is a meromorphic on $\Omega$ such that $a_j$ is a zero of order $k_j \in \Bbb N^+$, for each $j \in \{1, \dots, n\}$ and $b_l$ is a pole of $f$ of order $h_l$ for ${l \in \{1, \dots, m\}}$, and let $g$ be analyctic on $\Omega$

$$ \frac{1}{2\pi i }\oint_\gamma g(z)\frac{f'(z)}{f(z)}\, dz = \sum_{j =1}^n k_j \cdot n(\gamma, a_j)\cdot g(a_j)- \sum_{l = 1}^m h_l\cdot n(\gamma, b_l)\cdot g(b_l) $$

for any cycle $\gamma \subseteq \Omega \setminus \{a_1, \dots, a_n, b_1, \dots, b_m\}$ that is $\gamma \sim 0 \pmod \Omega$