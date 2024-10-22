---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Analytic Functions]], [[Homology in C]], [[Isolated Singularities]], [[Laurent Series in C]]

Let $\Omega\subseteq \Bbb C$ be a region, $z_1, z_2, \dots, z_n \in \Omega$ and $f:\Omega\setminus\{z_1, \dots, z_n\} \to \Bbb C$ be a analytic, such that $z_k$ is an isolated singularity of $f$, and let choose $r_1, \dots, r_n$ positive real numbers such that 
- $\overline B(z_k, r_k) \subseteq \Omega$ 
- if $\gamma_k(t) = r_k e^{it }+z_k$ with $t\in [0, 2\pi]$, then $$
	n(\gamma_k, z_j) = \delta_{k, j}
	$$
For the rest of this section

Let $\Omega \subseteq\Bbb C$ be a region and $z_1, z_2, \dots, z_n\in \Omega$ and $r_1, r_2, \dots, r_n$ positive real numbers that satisfy that $\overline B(z_k, r_k)\setminus \{z_k\} \subseteq \Omega\setminus\{z_1, \dots, z_n\}$ for all $k \in \{1, \dots n\}$ . If $f: \Omega\setminus\{z_1, \dots, z_n\}\to \Bbb C$ is analytic, then for every cycle $\gamma \subseteq \Omega\setminus\{z_1, \dots, z_n\}$ such that $\gamma \sim 0 \pmod \Omega$ , then 
$$
\oint_\gamma f (z)\, dz = \sum_{k = 1}^n m_k \oint_{\gamma_k} f(z)\, dz 
$$
where $m_k = n(\gamma; z_k)$ and $\gamma_k (t)= r_k e^{it }+z_k$ with $t\in [0, 2\pi]$ and $k \in \{1, \dots n\}$ 

Since the integrals of the form
$$
\oint_{\gamma_k} f(z)\, dz
$$
are so important we will analyse them with a bit more care. We will denoted them as 
$$
P_k = \frac{1}{2\pi i}\oint_{\gamma_k} f(z)\, dz
$$
A couple of things to note, the value of $P_k$ is not dependent on $r_k$, since we can $0 <r<r_k$  and with $\gamma_r (t) = re^{it} +z_k$, then $\gamma = \gamma_r - \gamma_k \sim 0 \pmod \Omega$, then
$$
\oint_\gamma f(z) \, dz = 0 
$$
Meaning they must be equal. 
If we analyse the function
$$
\tilde f(z) = f(z) - \frac{P_k}{z-z_k}
$$
And we integrate this function over any closed curve $\gamma \subseteq B(z_k, r_k)\setminus \{z_k\}$, we see that $\gamma \sim n(\gamma;z_k)\gamma_{\gamma_r} \pmod {B(z_k, r_k)\setminus \{z_k\}}$, and thus 
$$
\oint_\gamma \tilde f(z)\, dz = 0
$$
And this number $P_k$ has the particularity that the function 
$$
f(z) - \frac{P_k}{z-z_k}
$$has a primitive on a perforated neighbourhood around $z_k$. 

Let $z_0\in \Bbb C$ be an isolated singularity of $f$. We say that $R \in \Bbb C$ is the residue of $f$ in $z_0$, if the function
$$
f(z)- \frac{R}{z-z_0}
$$
has a primitive in some perforated neighbourhood around $z_0$. In this case we will write it as
$$
R = \text{Res}_{z = z_0} f = \text{Res}(f, z_0)
$$
If $z_0 \in \Bbb C$ is an isolated singularity of $f$ and $r>0$ such that $f$ is analytic on $A_{0, r}(z_0)$, then 
$$
f(z) = \sum_{n \in \Bbb Z} A_{n}(z-z_0)^n
$$
for all $z \in A_{0, r}(z_0)$. Then we can get that
$$
f(z)- \frac{A_{-1}}{z-z_0} = \sum_{\substack{n \in \Bbb Z\\ n \ne 1}} A_{n}(z-z_0)^n
$$
Everything on the right hand side has a primitive in $A_{0, r}(z_0)$. Then we can conclude that
$$
\text{Res}(f, z_0) = A_{-1}
$$
Let $z_0 \in \Omega$ and $g:\Omega \to \Bbb C$ analytic. If $f:\Omega\setminus \{z_0\}\to \Bbb C$ defined as
$$
f(z) = \frac{g(z)}{(z-z_0)^k}
$$
with $k \in \Bbb N^+$, then
$$
\text{Res}(f, z_0) = \frac{g^{(k-1)}(z_0)}{(k-1)!}
$$
In the particular case that $k = 1$, we see that

$$
\text{Res}(f, z_0) = g(z_0) = \lim_{z \to z_0} (z-z_0)f(z)
$$

Let $z_0 \in \Bbb C$ be a pole of order $1$ of a function $f$, and $g$ be an analytic function in a neighbourhood around $z_0$. Then $\text{Res}(fg, z_0) = g(z_0)\text{Res}(f, z_0)$

Let $g,h :\Omega \to \Bbb C$ analytic functions such that $g$ has a $0$ of order $k$, and $h$ has a $0$ of order $k+1$ at the point $z_0 \in \Omega$. Then the function $f=g/h$
- $f$ has a pole of order $1$ at $z_0$
- $\text{Res}(f, z_0) = (k+1)\frac{g^{(k)}(z_0)}{h^{(k+1)}(z_0)}$

Let $f, g$ be analytic functions and let $z_0$ be a $k$ order $0$ of $f$, then
$$
\text{Res}\left(g\frac{f'}{f}, z_0\right) =k\cdot g(z_0)
$$
If $z_0$ is a $k$ order pole, then 
$$
\text{Res}\left(g\frac{f'}{f}, z_0\right) = -k\cdot g(z_0)
$$

We get the kinda interesting identity of
$$
\text{Res}(\pi\cot(\pi z), n) = 1
$$
for $n \in \Bbb Z$. 
#### Residue Theorem
Let $\Omega\subseteq \Bbb C$ be a region, $z_1, z_2, \dots, z_n \in \Omega$ and $f:\Omega\setminus\{z_1, \dots, z_n\} \to \Bbb C$ be a analytic, such that $z_k$ is an isolated singularity of $f$, for any cycle $\gamma \subseteq \Omega\setminus \{z_1, \dots, z_n\}$  such that $\gamma \sim 0 \pmod \Omega$, then 
$$
\oint_\gamma f(z)\, dz = 2\pi i\sum_{k = 1}^n n(\gamma, z_k) \text{Res}(f, z_k)  
$$

this can be used to prove the [[Higher Derivatives of Analytic Functions#Cauchy Integral Formula for Derivatives|Cauchy Integral formula for derivatives]], in a couple of lines.

We can extend this theorem and get that:
Let $\Omega \subseteq \Bbb C$ be a region, $\{z_1, \dots, z_n, \dots\}\subseteq \Omega$ be an infinite set such that has no accumulation point on $\Omega$, and $f: \Omega\setminus\{z_1,\dots, z_n, \dots\}\to \Bbb C$ is analytic, then for any cycle $\gamma \subseteq \Omega\setminus\{z_1, \dots, z_n, \dots\}$ such that $\gamma \sim 0 \pmod \Omega$, then
$$
\oint_\gamma f(z)\, dz = 2\pi i\sum_{k = 1}^n n(\gamma, z_k) \text{Res}(f, z_k)  
$$

### Residue at $\infty$

We can define the residue of a a function at $\infty$. Let $f$ be an analytic function for $|z|>R$. We define it as
$$
\text{Res}(f,\infty ) = -\frac{1}{2\pi i} \oint_{\gamma }f (z)\, dz
$$
where we define $\gamma$ to be the circumference of radius $r>R$ in the counterclockwise.

We define the function $g(z) = f(1/z)$ for $0 < |z| <1/R$, then 
$$
	\text{Res}(f, \infty) = \text{Res}\left(-\frac{g(z)}{z^2}, 0\right)
$$
Let $f$ be analytic on $\Bbb C$, except for a finite set of isolated singularities $z_1, \dots, z_n$, then
$$
\text{Res}(f, \infty) = -\sum_{k = 1}^n \text{Res}(f,z_k)
$$