---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Infinite Products]]

**Def**: Let $f_n: A \subseteq \Bbb C \to \Bbb C$, be a sequence of function. We say that the product $f = \prod\limits_{n = 1}^\infty f_n$  **converges pointwise** on $A$, if for every $z\in A$ $\prod\limits_{n = 1}^\infty f_n(z)$ converges. If $\prod\limits_{n = 1}^\infty f_n$ converges pointwise on $A$, we can define $R_n(z) = \prod\limits_{k = n+1}^\infty f_k$, and it will converge pointwise. We say that $\prod\limits_{n = 1}^\infty f_n$ **converges uniformly** on $B\subseteq A$ if $R_n \rightrightarrows 1$ on $B$

**Prop:** Let $f_n: A \subseteq \Bbb C \to \Bbb C$, and $B\subseteq A$. Then $\prod\limits_{n = 1}^\infty (1+|f_n|)$  converges uniformly on $B$ iff $\sum\limits_{n = 1}^\infty |f_n|$ converges uniformly on $B$. 

**Cor:** Let $f_n: A \subseteq \Bbb C \to \Bbb C$, and $B\subseteq A$. If $\prod\limits_{n = 1}^\infty (1+|f_n|)$ converges uniformly on $B$, then $\prod\limits_{n = 1}^\infty (1+f_n)$ converges uniformly on $B$

If we need that $\prod\limits_{n = 1}^\infty f_n$ to converge uniformly, it suffices to that $\sum\limits_{n = 1}^\infty |f_n-1|$ converges uniformly, then $\prod\limits_{n = 1}^\infty (1+|f_n-1|)$, converges uniformly, then $\prod\limits_{n = 1}^\infty f_n$ converges uniformly.

If we restrict to continuous functions, we can get stronger results.

**Th:** Let $\{f_n\}\subseteq \mathcal C(U, \Bbb C)$ where $U$ is a region in $\Bbb C$.  Let $f = \prod\limits_{n = 1}^\infty f_n$ converges pointwise on $U$. Let $R_n = \prod\limits_{k = n+1}^\infty f_k$  and $p_n = \prod\limits_{k = 1}^n f_k$. If for all $K \subseteq U$ compact, we have that $R_n \rightrightarrows 1$ on $K$. Then 
1. For every $K \subseteq U$ compact, there's an $m\in \Bbb N$ such that for every $n \ge m$ $Z(R_n) \cap K = \varnothing$ and $Z(f_n) = \varnothing$ 
2.  For every $K \subseteq U$ compact, we have that $p_n \rightrightarrows f$ on $K$
3. $f\in \mathcal C(U, \Bbb C)$ and $p_n \stackrel{\rho}{\longrightarrow} f$ 
4. $R_n\in \mathcal C(U, \Bbb C)$ and $R_n \stackrel{\rho}{\longrightarrow} 1$ 

**Th:** Let $\{f_n\}\subseteq \mathcal H(U)$, such that $f = \prod\limits_{n = 1}^\infty f_n$ converges pointwise on $U$, and $R_n = \prod\limits_{k = n+1}^\infty f_k$, if $R_n \stackrel{\rho}{\longrightarrow} 1$, then 
1. $f\in \mathcal H(U)$
2. $R_n \in \mathcal H(U)$ 
3. $Z(f) = \bigcup\limits_{n = 1}^\infty Z(f_n)$
4. If for every $n\in \Bbb N$, we have that $f_n \not \equiv 0$, then $f \not \equiv 0$, additionally for every $a\in Z(f)$, the set $N(a) = \{n \in \Bbb N \mid f_n(a) = 0\}$ is finite and $$m(f, a) = \sum_{n \in N(a)} m(f_n, a)$$
We are getting a relationship of a product of analytic functions and looking at  their [[Zeros of Analytic Functions|zeros]]. 

We got a problem we want to solve:
Let $U \subseteq \Bbb C$ be a region, and $M=\{a_n \mid n\in \Bbb N\}$, such that $M' \cap U = \varnothing$. Is there a function $f\in \mathcal H(U)$ such that $Z(f) = M$? 

Let suppose that there's a $\{g_n\}\subseteq \mathcal H(U)$ such that $Z(g_n) = \varnothing$,  if we can make it such that $$\sum_{n = 1}^\infty |(z-a_n)g_z(a)-1|$$
to converge uniformly then $$f = \prod_{n = 1}^\infty (z-a_n)g_n(z)$$ is the solution we want to the problem. 

**Def:** For each $p \in \Bbb N$, we define $E_p:\Bbb C \to \Bbb C$, then $E_0(z) = 1-z$, and for $p \ge 1$, we get
$$E_p(z) = (1-z)\exp\left(\sum_{k = 1}^p \frac{z^k}{k}\right)$$
$E_p$ is the $p$th Weiestrass elemental function, this are the elementary factors.

**Lemma:** We get an important lemma: If $|z_n| \le 1$ then $|E_p(z) -1| \le |z|^{p+1}$, for $p \in \Bbb N$. 

### Existence of entire function with specified zeroes
**Th**: Let $\{a_n\}\subseteq \Bbb C\setminus\{0\}$ such that $\lim\limits_{n \to \infty} |a_n| = \infty$, if there exists $\{p_k \}\subseteq \Bbb N$ such that for all $R>0$, 
$$\sum_{n = 1}^\infty \left(\frac{R}{a_k}\right)^{p_k+1}$$converges, then $$f(z) = \prod\limits_{k= 1}^\infty E_{p_k}\left(\frac{z}{a_k}\right)$$ is entire, and $Z(f) = \{a_n\mid n \in \Bbb N\}$ and $m(f, a) = |\{k \in \Bbb N \mid a_k = a\}$

We can see that if $\lim\limits_{n \to \infty} |a_k| = \infty$, given $R>0$, there exists $n \in \Bbb N$ such that for all $k\ge n$, then $|a_k| \ge 2R$, then $R/|a_k| \le 1/2$, then we get that 
$$
\left(\frac{R}{|a_k|}\right)^k \le \frac{1}{2^k}
$$Thus $p_k = k$ satisfies the conditions of the of the theorem above.

**Th:** Let $M\subseteq \Bbb C$ with $M' = \varnothing$ , given $m: M \to \Bbb N⁺$, then there's $f\in \mathcal H(U)$ such that $Z(f) = M$, and every $a\in M$,  satisfies $m(f, a) = m(a)$

### Existence of analytic function with specified zeroes
Let $U \subset \Bbb C$ region, $M \subseteq U$ such that $M' \cap U = \varnothing$. If $m: M \to \Bbb N⁺$, then there's $f\in \mathcal H(U)$ such that $Z(f) = \varnothing$ and for every $a\in Z(f)$ we have that $m(f, a) = m(a)$ 

The proof of this is really nice, since we basically do a 'simple case', and the other case, we transport it into the simple case, and back. The simple case is particularly, when the region $U$ satisfies this property: there exists $R>0$ such that $$\{z \in \Bbb C \mid |z| >R \} \subseteq U \qquad \text{and} \qquad M \subseteq \overline B_R(0)$$
### Weierstrass Factorization Theorem
Let $f\in \mathcal H(U)$, with $f\not\equiv 0$. If $|Z(f)| = \aleph_0$, let $Z(f) \setminus\{0\} = \{a_k \mid k \in \Bbb N\}$, where each $a_k$ appears as many times as its multiplicity, then for every $\{p_k\}\subseteq \Bbb N$ such that for every $R>0$
$$\sum_{k = 1}^\infty \left(\frac{R}{a_k}\right)^{p_k+1}\qquad \text{converges}$$
There exists $g\in \mathcal H(\Bbb C)$ such that 
$$
f(z) = z^m e^{g(z)} \prod_{k = 1}^\infty E_{p_k}\left(\frac{z}{a_k}\right)
$$
Where $m =0$ if $0 \not \in Z(f)$ and $m = m(f, 0)$ if $0 \in Z(f)$. 

Using this theorem we get factorization for $\sin$ and $\cos$, but we need a lemma:

**Lemma:** for $a\in \Bbb C\setminus \Bbb Z$, we get that $$\frac{1}{a} + \sum_{n = 1}^\infty \frac{2a}{a²-n²} = \pi \cot(\pi a)$$
The way we prove this in class was to calculate a limit of contour integrals, over the border of a rectangles, with vertex at
- $z_1(n) = (n +1/2)-in$
- $z_2(n) =(n+1/2) +in$
- $z_3(n) = -(n+1/2) +in$
- $z_4(n) = -(n+1/2) -in$
Over a function the function
$$f(z) = \frac{\cot(\pi z)}{z(z-a)}$$
Looking at the residues we get that for big enough $n$, we get that $$\frac{1}{2\pi i}\oint_{\gamma_n} f(z) \, dz  = \sum_{m = 1}^n \frac{2}{\pi (m²-a²)}-\frac{1}{\pi a²}+\frac{\cot(\pi a)}{a} $$If we look that $$\lim_{n \to \infty} \oint_{\gamma_n}f(z)\, dz =0$$Then we get the proof of the lemma.

With this we can give a factorization for $\sin$ and $\cos$ $$ \sin(\pi z) = \pi z \prod_{n = 1}^\infty \left(1-\frac{z²}{n²}\right) = \pi z \prod_{n \ne 0} \left(1-\frac{z}{n}\right)e^{z/n}$$ and getting that $$\sin(z) = \pi z\prod_{n = 1}^\infty \left(1-\frac{z²}{n²\pi²}\right)$$ To get the factorization of the $\cos$, we use the one for the cosine and get that $$\cos(\pi z) = \prod_{n = 1}^\infty \left(1-\frac{4z²}{(2n+1)²}\right) = \prod_{n \in \mathbb{Z}, \, n \; \text{odd} } \left(1-\frac{2z}{n}\right)e^{2z/n}$$
and getting that $$\cos(z) = \prod_{n = 0}^\infty \left(1-\frac{4z²}{\pi²(2n+1)}\right)$$