---
tags:
  - NumberTheory
  - AnalyticNumberTheory
---
Subjects: [[Analytic Number Theory]]
Links: [[Dirichlet Characters]], [[Riemann Zeta Function]], [[Dirichlet Series]], [[Prime Numbers]], [[Infinite Products]], [[Infinite Product of Functions]]

We know that the zeta function $\zeta(s) = \sum\limits_{n \ge 1} 1/n^s$ can be expressed as a product, namely $$\sum_{n = 1}^\infty \frac1{n^s} = \prod_p \frac1{1-p^{-s}}$$
**Def:** The function $$L(s, \chi) = \sum_{n = 1}^\infty\frac{\chi(n)}{n^s}$$where $\chi$ is a Dirichlet character with $\Re(s) > 1$, is called a *Dirichlet $L$-function*. 

We would like to have a similar product formula for Dirichlet $L$-functions as we have for Riemann. Then a piece that might seem interesting might be $$\log\left(\frac1{1-z}\right) = \sum_{k = 1}^\infty \frac{z^k}{k} \qquad |z| < 1$$
**Prop:** The logarithm function satisfies the following properties:
If $|z| <1$, then $$\exp\left(\log\left(\frac1{1-z}\right)\right)= \frac1{1-z}$$
If $|z| <1$, then $$\log\left(\frac1{1-z}\right) = z + E_1(z)$$where the error $E_1$ satisfies $|E_1(z) \le |z|^2$ if $|z| <1/2$

If $|z| <1/2$, then $$\left|\log\left(\frac1{1-z}\right) \right| \le 2|z|$$

**Th:** If $\Re(s)>1$, then $$\sum_{n = 1}^\infty \frac{\chi(n)}{n^s} = \prod_p \frac1{(1-\chi(p)p^{-s})}$$where the product is over all primes

**Prop:** Suppose $\chi_0$ is the trivial Dirichlet character, $$\chi_0(n) = \begin{cases}
1 & (n ,q ) = 1 \\
0 & (n ,q ) \ne 1
\end{cases}$$
Then $$L(s, \chi_0) = \zeta(s) \prod_{p \mid q} (1-p^{-s})$$
Therefore $L(s, \chi_0) \to \infty$ as $s \to 1^+$. Moreover, $$L(s,\chi_0)= \frac{\varphi(q)}{q}\frac1{s-1}+ O(1) \qquad \text{as } s\to 1^+$$

**Th:** The Dirichlet $L$-functions $$L(s, \chi) = \sum_{n= 1}^\infty \frac{\chi(n)}{n^s} = \prod_p \frac1{1-\chi(p)p^{-s}}$$have meromorphic continuations fo $\Re(s)>0$. For $\chi$ non-trivial, $L(s, \chi)$ is *holomorphic* on that half-plane. For $\chi_0$ the trivial character, $L(s, \chi_0)$ has a *simple pole* at $s = 1$ and is holomorphic otherwise. 

**Lemma:** If $\chi$ is a non-trivial character, then  $$\left|\sum_{n = 1}^k \chi(n) \right| \le q \qquad \text{for any } k$$**Prop:** If $\chi$ is a non-trivial Dirichlet character, then the series $$ \sum_{n = 1}^\infty\frac{\chi(n)}{n^s}$$ converges for $s>0$, and we denote its sum by $L(s, \chi)$. Moreover: 
- The function $L(s, \chi)$ is continuously differentiable for $0<s<\infty$.
- There exists constants $c, c'>0$ so that 
$$ \begin{align*}
L(x, \chi) = 1+O(e^{-cs}) \qquad &\text{as } s\to \infty \\
L'(s, \chi) = O(e^{-c's}) \qquad &\text{as } s\to \infty
\end{align*}
$$

With the facts we have gathered so far we can define the logarithm of the $L$-functions. 

**Def:** If $\chi$ is a non-trivial Dirichlet character and $s>1$ we define $$\log L(s,\chi) = -\int_s^\infty \frac{L'(t, \chi)}{L(t, \chi)}\, dt $$
By the product formula, we see that $L(t, \chi) \ne 0$ when $t > 1$, and the integral is convergent since $$\frac{L'(t, \chi)}{L(t, \chi)} = O(e^{-ct})$$

**Prop:** If $s>1$, then $$\exp(\log L(s, \chi)) = L(s, \chi)$$Moreover, $$\log L(s, \chi) = \sum_p \log\left(\frac1{1-\chi(p)p^{-s}}\right)$$
Putting everything together we see that $$\sum_p \log\left(\frac1{1-\chi(p)p^{-s}}\right) = \sum_p \frac{\chi(p)}{p^s} + O\left(\sum_p \frac1{p^{2s}}\right)$$
Which we can see that the sum at converges meaning that it can be bounded, then getting that $$\sum_p \log\left(\frac1{1-\chi(p)p^{-s}}\right) = \sum_p \frac{\chi(p)}{p^s} + O\left(1\right)$$
The goal is to get: that $\chi \ne \chi_0$, then $L(1, \chi) \ne 0$

### Complex Dirichlet Characters

**Lemma:** $\Re(s)> 1$, then $$\prod_{\chi\mod q} L(s,\chi) \ge 1$$where the product is taken over all Dirichlet characters modulo $q$. In particular the product is real-valued.

**Lemma:** Let $a$ be relatively prime to $q$, $k$ be the order of $a$ in $\Bbb Z^\times(q)$, then we know that $k \mid \phi(q)$, and $$\prod_{\chi\mod q} (x-\chi(a)) = (x^k-1)^{\phi(q)/k}$$where the product is over all Dirichlet characters modulo $q$.

**Prop:** If $p$ is relatively prime to $q$, then $$\prod_{\chi\mod q} \left(1 - \frac{\chi(p)}{p^s}\right) = \left(1-\frac1{p^{fs}}\right)^g$$where $g = \varphi(q)/f$, and $f$ is the order of $p$ in $\Bbb Z^* (q)$, and the product is taken over all Dirichlet characters modulo $q$. 

**Prop:** We have that $$\prod_{\chi\mod q}  L(s, \chi) = \sum_{n = 1}^\infty \frac{a_n}n$$where $a_n \ge0$, and the product is over all Dirichlet characters modulo $q$

**Lemma:** The following properties hold:
- If $L(1, \chi) = 0$, then $L(1, \overline \chi) =0$
- If $\chi$ is a non-trivial and $L(1, \chi) = 0$, then 
$$ |L(s, \chi)| \le C|s-1| \qquad \text{when } 1\le s\le 2$$
- For the trivial Dirichlet character $\chi_0$, we have 
$$ |L(s, \chi_0)| \le \frac{C}{|s-1|} \qquad \text{when } 1\le s\le 2$$
**Th:** If $\chi$ is a non-trivial complex Dirichlet character, then $L(1, \chi) \ne 0$

### Real Dirichlet Characters

The way to get this result, is to sum along hyperbolas, something Dirichlet himself did but not for this problem. Let $\chi$ be a non-trivial Dirichlet character. Given this character, let $$F=(m,n) = \frac{\chi(n)}{(nm)^{1/2}}$$and define $$S_N = \sum \sum F(m,n) = \sum_{\substack{1 \le n , m \\ nm \le N }} F(m,n)$$
where the sum is over all integers $m,n\ge 1$ that satisfy $mn \le N$

**Lemma:** $$\sum_{n \mid k} \chi(n) \ge \begin{cases} 1 & k = \ell^2 \text{ for some } \ell \in \Bbb Z \\
0 & \text{otherwise}\end{cases}$$
**Lemma:** For all integers $0<a<b$ we have that $$\sum_{n = a}^b \frac{\chi(n)}{n^{1/2}} = O(a^{-1/2})$$and $$\sum_{n = a}^b \frac{\chi(n)}{n} = O(a^{-1})$$**Th:** The following statements are true:
- $S_N \ge c\log N$ for some constant $c>0$
- $S_N = 2 N^{1/2}L(1, \chi)+O(1)$

**Th:** If $\chi$ is a non-trivial real Dirichlet character, then $L(1, \chi) \ne 0$. We can get that $L(1, \chi) >0$

**Th:** If $\chi$ is a non-trivial Dirichlet character, then $L(1, \chi) \ne 0$.

**Cor:** If $\chi$ is a non-trivial Dirichlet character, then $\log L(s, \chi)$ is bounded as $s\to 1^+$, and we can conclude that the sum $$\sum_p \frac{\chi(p)}{p^s}$$is bounded as $s\to 1^+$. 

**Th:** Let $a$ be relatively prime with $q$,  $$\sum_{\substack{p \\ p \equiv a \pmod q}} \frac1{p^s} = \frac1{\varphi(q)} \sum_{p \not\mid q}  \frac1{p^s} + \frac1{\varphi(q)} \sum_{\chi \ne \chi_0} \overline{\chi(\ell)} \sum_p \frac{\chi(p)}{p^s}$$
# Dirichlet's Theorem for Arithmetic Progressions

Let $a, q$ be coprime numbers, then $$\sum_{\substack{p \\ p \equiv a \pmod q}} \frac1{p^s} = \frac1{\varphi(q)} \log\left(\frac1{s-1}\right) + O(1) \qquad \text{as }s\to 1^+$$and as a result, we get that$$\sum_{\substack{p \\ p \equiv a \pmod q}} \frac1{p} = \infty$$**Cor:** There are infinitely many primes of the form $$p \equiv a \pmod q$$for $a, q$ corprimes 

# Calculating Series using Dirichlet $L$-functions

**Prop:** Let $\{a_n\}_{n = 1}^\infty$ be a sequence of complex numbers such that $a_n = a_m$ iff $n \equiv m \pmod q$. We have that $$\sum_{n = 1}^\infty \frac{a_n}{n}$$converges iff $\sum_{n= 1}^q a_n = 0$

**Reminder:** The series $$F(\theta) = \sum_{|n|\ne 0} \frac{e^{in\theta}}{n}, \qquad \text{for } |\theta| < \pi $$converges for every $\theta$ and is the Fourier series of the function defined on $[-\pi, \pi]$ by $F(0) = 0$ and $$F(\theta) = \begin{cases}i(-\pi-\theta) & \pi \le\theta < 0 \\0 & \theta = 0 \\ i (\pi-\theta) &0 < \theta \le \pi\end{cases}$$and extended by periodicity ($2\pi$ period) to all $\Bbb R$. 

**Prop:** If $\theta\not\equiv0 \pmod {2\pi}$, then the series $$E(\theta) = \sum_{n = 1}^\infty \frac{e^{in\theta}}{n}$$converges and that $$E(\theta) = \frac12 \log \left(\frac1{2-2\cos\theta}\right)+\frac1{2}F(\theta)$$
To sum series $\sum_{n= 1}^\infty a_n/n$ with $a_n = a_m$ iff $n \equiv m \pmod q$ and $\sum_{n = 1}^q a_n = 0$. We define $$A(m) = \sum_{n = 1}^q a_n \zeta^{-mn} \qquad \text{where } \zeta = e^{2\pi i /q}$$We see that $A(q) = 0$, and with the using the $E(\theta)$ function defined as above, we get the result $$\sum_{n = 1}^\infty \frac{a_n}n = \frac1q \sum_{m = 1}^{q-1} A(m) E(2\pi m/q)$$
If $\{a_n\}$ is odd, $a_{-m} = -a_m$ for $m\in \Bbb Z$, then $$A(m) ) \sum_{1\le n < q/2} a_n(\zeta^{-mn}-\zeta^{mn})$$
If $\{a_n\}$ is odd then $$\sum_{n = 1}^\infty \frac{a_n}n = \frac1{2q} \sum_{m = 1}^{q-1} A(m) F(2\pi m/q)$$where $F$ is as defined above. 

With this let $\chi$ be the non-trivial Dirichlet character modulo $3$, then $$L(1, \chi) = \frac\pi{3\sqrt 3} = 1 - \frac12 +\frac14 -\frac15+\frac17-\frac18 +\cdots$$Let $\chi$ be the non-trivial Dirichlet character modulo $6$ then $$L(1, \chi) = \frac\pi{2\sqrt 3} = 1 -\frac15 + \frac17 -\frac1{11} + \frac1{13} + \cdots$$Let $\chi$ be the odd Dirichlet character modulo $8$ then $$L(1, \chi) = \frac\pi{2\sqrt 2} =1-\frac13-\frac15-\frac17+\frac19+\frac1{11}+\cdots$$Let $\chi$ be the real odd Dirichlet character modulo $7$ then $$L(1, \chi) = \frac\pi{\sqrt 7 }= 1+\frac12 -\frac13+\frac14-\frac15-\frac16 +\cdots$$For the even real Dirichlet character modulo $8$, then $$L(1, \chi) = \frac{\ln(1+\sqrt 2)}{\sqrt2} = 1-\frac13-\frac15+\frac17+\frac19-\frac1{11}+\cdots $$For the even real Dirichlet character modulo $5$, then $$L(1, \chi) = \frac2{\sqrt 5} \log \varphi = 1-\frac12-\frac13+\frac14-+\frac16-\frac17-\frac18+\frac19+\cdots $$where $\varphi$ is the golden ratio. 