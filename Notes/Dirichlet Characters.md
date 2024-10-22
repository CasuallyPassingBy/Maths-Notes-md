---
tags:
  - FourierAnalysis
  - AnalyticNumberTheory
---
Subjects: [[Elementary Number Theory]], [[Fourier Analysis]]
Links: [[Fourier Analysis on finite abelian groups]], [[Euler Totient Function]], [[Multiplicative Functions]]

We take the abelian group $\Bbb Z_q^\times$, being the units modulo $n$. We know that $|\Bbb Z_q^\times| = \varphi (q)$.

We consider the function $\delta_\ell$ on $\Bbb Z_q^\times$, which we think of the characteristic of $\ell$; if $n \in \Bbb Z_q^\times$, then $$\delta_\ell(n) = \begin{cases} 1 & n \equiv \ell \pmod q \\ 0 & n \not\equiv \ell \pmod q\end{cases}$$
This function we can expand in a Fourier series: $$\delta_\ell(n) = \sum_{e\in \widehat{\Bbb Z_n^\times}} \widehat{\delta_\ell}(e)e(n)$$
where $$\widehat{\delta_\ell(n)}(e) = \frac1{|\Bbb Z_n^\times|} \sum_{m \in \Bbb Z_n^\times} \delta_\ell(m)\overline{e(m)} = \frac1{|G|}\overline{e(\ell)}$$
Hence $$\delta_\ell(n) = \frac1{|\Bbb Z_n^\times|} \sum_{e \in \widehat{\Bbb Z_n^\times}}\overline{e(\ell)}e(n)$$
We can extend the function $\delta_\ell$ to all of $\Bbb Z$ by setting $\delta_\ell(m) = 0$ whenever $m$ and $q$ are not relatively prime. Similarly, the extension of the characters $e \in \widehat{\Bbb Z_n^\times}$ to all $\Bbb Z$ is given by the recipe $$\chi(m) = \begin{cases} e(m) & (m , q) = 1 \\ 0 & (m , q) = 0\end{cases}$$
are called the *Dirichlet characters* modulo $q$. We shall denote the extension to $\Bbb Z$ of the trivial character of $\Bbb Z_n^\times$ by $\chi_0$, so that $\chi_0(m) = 1$, whenever $m$ and $q$ are coprime, otherwise $0$. 

**Obs:** The Dirichlet character modulo $q$ are completely multiplicative on all of $\Bbb Z$.

**Lemma:** The Dirichlet characters are multiplicative. Moreover, $$ \delta_\ell(m) = \frac1{\varphi(q)}\sum_\chi \overline{\chi(\ell)}\chi(m)$$where the sum is over all Dirichlet characters.

**Def:** A Dirichlet character is said to be *real* if it takes on only real values (that is $+1$, $-1$, or $0$) and *complex* otherwise. $\chi$ is real iff $\chi(n) = \overline{\chi(n)}$

**Def:** The Dirichlet character $\chi$ is *even* if $\chi(-1) = 1$ and it si *odd* of $\chi(-1) = -1$