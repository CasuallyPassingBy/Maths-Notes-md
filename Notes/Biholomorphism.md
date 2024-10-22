---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]

**Def**: Let $U, V\subseteq \Bbb C$ be regions. We say that $U$ and $V$ are **biholomorphic** or **biholomorphically equivalent**, if there's a bijective analytic function $f:U \to V$. We write it as $U \approx V$. If we know the biholomorphism $f$, then we can write it as $U \approx_f V$

**Obs**: The $\approx$ is an equivalence relation. 

$D := B_1(0)$, for the rest of the note.

We can see that $\Bbb C \not\approx D$ since if there was a a function $f: \Bbb C \to D$, analytic then $f$ would be constant.

We see that if $f:\Bbb C \to \Bbb C$ is analytic and injective then $f(z) = az+b$, then $f$ is surjective. Meaning that if $U \approx \Bbb C$ then $U = \Bbb C$.

The goal from Riemann was to characterize all the $U \subset \Bbb C$ such that $U\approx D$ 

**Def**: Let $U\subseteq \Bbb C$ be a region. We say that $U$ satisfies the **Riemann condition** ($U \in \text{RC}$ as a shorthand), if for every $f\in \mathcal H(U)$ such that $Z(f) = \varnothing$ then $\exists g\in\mathcal H(U)$, that $g² = f$ 

We see that $D \approx D$, and we want to find all the biholomorphisms. We can use [[Maximums Modulus Theorem#Schwarz Lemma|Schwarz Lemma]] to find them all. 

Let $a \in D$, and we define
$$
\varphi_a (z) = \frac{z-a}{1-\overline a z}
$$
is a Möbius transformation. with $\varphi_a(a) =0$, and $\varphi_a[\partial D] = \partial D$. Since we can see that $\varphi_a$ has a pole at $1/\overline a$, and $|1/\overline a| >1$, we see that $\varphi_a$ is analytic on $B_{|1/\overline a|}(0)$ which contains $D$. Thus $\varphi_a:D \to D$ is a biholomorphism. 

Additionally, $\varphi_a^{-1} = \varphi_{-a}$ 

We need to look at special properties of $\varphi_a$. $$\varphi_a'(z) = \frac{(1-\overline az) +(z-a)\overline a}{(1-\overline a z)}$$
and we see that$$\varphi_a'(a) = \frac{1}{1-|a|²}, \qquad\quad \varphi_a'(0) =1-|a|²$$
**Lemma**: Let $f:D\to D$ be analytic, and $a\in D$, we call $\alpha = f(a)$, then $$|f'(\alpha)| \le \frac{1-|\alpha|²}{1-|a|^2}$$Furthermore, if $|f'(\alpha)| = \frac{1-|\alpha|²}{1-|a|^2}$, then there's $c\in \partial D$ such that $$f(z) = \varphi_{-a}(c\varphi_a(z))$$in particular, $f$ is injective.

**Th:** $D \approx_f D$, and $a\in D$, $f(a) = 0$, then there's $c\in \partial D$ such that $f = c\varphi_a$ 

### Riemann Theorem
Let $U\subset \Bbb C$ be a region. If $U$ satisfies the Riemann condition, for every $a\in U$, there exists a unique biholomorphism $f: U \to D$, such $f(a) = 0$ and $f'(a) >0$.

The proof has 3 main parts:
1. Existence of biholomorphism(the hardest), requires the use of [[Normal Families of Functions in C|Normal families]] 
2. Given that biholomorphism construct one that satisfies the additional constraints
3. Uniqueness of the biholomorphism