---
tags:
  - SpecialNumbers
  - Combinatorics
---
Subjects: [[Special Numbers]], [[Combinatorics]]
Links: [[Falling and Rising Factorials and Pochhamer Symbols]], [[Multi-index notation]]

We define the binomial coefficient of $r$ choose $k$ as $$ {r\choose k} := \begin{cases}\dfrac{r^\underline k}{k!} & k \in \Bbb N \\
0 & \text{otherwise},\end{cases}$$where $r^\underline k$ is the $k$th falling factorial. This definition is extremely useful since, it lets us choose from more than just natural numbers, and let $r\in \Bbb C$. 

Some notable examples are $${r\choose 0} = 1, \quad {r\choose 1} = r, \quad {r\choose 2} = \frac{r(r-1)}{2}.$$
If we let $n \in \Bbb N$, then we have the following formula $${n \choose k} = \frac{n!}{k!(n-k)!}.$$This leads to a symmetric formula for the binomial coefficients when $n, k \in \Bbb N$ $${n \choose k} = {n \choose n-k}.$$By the same definition, we get a general identities $${r\choose k} = \frac{r}{k} {r-1\choose k-1}, \qquad k {r\choose k} = r{r-1\choose k-1}, \qquad (r-k){r\choose k} = r{r-1\choose k}. $$We also get the addition formula, or the recursive formula from this identities $${r\choose k} = {r-1 \choose k} + {r-1\choose k-1}.$$If we inductively apply this formula we get the a general formula: $$\sum_{k \le n} {r+k \choose k} = {r+n+1\choose n}.$$We also have another identity for $n, m\in\Bbb N$ $$\sum_{k = 0}^n {k\choose m } = {n+1\choose m+1}.$$This leads to a nice special case where $m = 1$, $$\sum_{k =0}^n k =\sum_{k =0}^n {k \choose 1} = {n+1\choose 2} = \frac{n(n+1)}{2}.$$The general result is equivalent to the result of [[Discrete Calculus]] $$\sum_{k=0}^n k^{\underline m} = \frac{(n+1)^{\underline{m+1}}}{m+1},$$which I found amusing. We can also see that $$\nabla \left({x\choose m}\right) = {x\choose m-1}, \qquad \nabla \left({x\choose m}\right) = {x-1\choose m-1}.$$
We can prove a inductively on $m$, that $$\sum_{k = 0}^m {r\choose k}\left(\frac{r}{2}- k\right) = \frac{m+1}{2} {r\choose m+1}. $$

We get the binomial theorem and the extended binomial theorem. For $x, y\in \Bbb C$ and $n \in \Bbb N$ then $$(x+y)^n = \sum_{k = 0}^n {n \choose k} x^k y^{n-k},$$if $x, y \in \Bbb C$ with $|x| > |y|$ and $r \in \Bbb C$, then $$(x+y)^r = \sum_{k = 0}^\infty {r \choose k}x^k y^{n-k}. $$
If we look for the connection to the negative binomial coefficients then we get that $${-r \choose k } =(-1)^k{r+k-1\choose k}.$$This has a nice consequence of $$\sum_{k \le m} {r\choose k}(-1)^k = (-1)^m{r-1\choose m}.$$
If we ask about the partial sums of the binomial coefficients, we know it doesn't have a closed form, but we can have a certain equality $$\sum_{k \le m} {m +r \choose k} x^k y^{n-k} = \sum_{k \le m} {-r\choose k} (-x)^k(x+y)^{m+k}, \quad \text{for $m \in \Bbb Z$}. $$Let us not that this is a more general version of the identity above, since if we let $x = -1$ and $y =1$, then we get the original identity. Now, if $x = y = 1$ and $r = m+1$, then $$2^{2m}= \sum_{k \le m} {2m+1\choose k} = \sum_{k \le m} {m+k \choose k} 2^{m-k}.$$thus $$2^m = \sum_{k \le m}{m+k\choose k} 2^{-k}.$$
Let $r\in \Bbb C$ and $k, m \in \Bbb N$, then $${r\choose m}{m \choose k} = {r\choose k}{r-k\choose m-k}.$$
We have a nice generalisation of the binomial coefficients into the *multinomial coefficients* then $$ {a_1 + a_2 + \dots + a_n \choose a_1, a_2, \dots, a_n} :=\frac{(a_1+a_2 +\dots +a_n)!}{a_1!a_2! \cdots a_n !} = {a_1 +a_2 + \dots +a_n\choose a_2 +\dots+ a_n} \cdots {a_{n-1}+a_n\choose a_n}.$$
With these tools we get the the following generalisation of the binomial theorem, called the multinomial theorem: $$\left(\sum_{k = 1}^n x_i\right)^m = \sum_{|\alpha | = m} {m \choose \alpha} x^\alpha$$where $\alpha$ is a multi-index, and $x^\alpha = \prod\limits_{k = 1}^n x_k^{\alpha_k}$. 
The following identity is called *Vandermonde's Convolution*: $$\sum_{k = 0}^n {r\choose k} {s\choose n-k} ={r+s\choose n}\quad \text{for $n \in \Bbb N$}. $$From this we get a couple of identities $$\begin{align*}
\sum_{k} {r\choose m+k} {s\choose n-k} &={r+s\choose m+n}\qquad \text{for $m,n \in \Bbb Z$}.  \\  \\
\sum_{k} {\ell \choose m+k}{s\choose n+k} &= {\ell +s \choose \ell -m+n}
\qquad \text{for $\ell \in \Bbb N$ and $n, m \in \Bbb Z$}.\\ \\
\sum_{k} {\ell \choose m+k}{s+k\choose n}(-1)^k &= (-1)^{m+1}{s-m \choose n-\ell} \qquad \text{for $\ell \in \Bbb N$ and $n, m \in \Bbb Z$}.\\ \\
\sum_{k \le \ell} {\ell-k \choose m}{s \choose k-n} (-1)^k &= (-1)^{1+m} {s-m-\ell \choose \ell -m -n} \qquad \text{for $\ell, m , n \in \Bbb Z$}. \\ \\
\sum_{k = 0}^\infty {\ell -k \choose m}{q+k\choose n} &= {\ell +q +1\choose m+n+1}\qquad  \text{for $\ell, m, n, q \in \Bbb N$ for $n \ge q$}.
\end{align*} 
$$
We have a couple of identities that involve $1/2$. $${r\choose k}{r-1/2 \choose k} = {2r\choose 2k}{2k\choose k}2^{-2k}. $$If we set $k = r = n$, where $n \in \Bbb N$, then $${n-1/2 \choose n} = {2n \choose n}2^{-2n}.$$We also have that $${-1/2\choose n} = \left(\frac{-1}{4}\right)^n {2n \choose n}.$$
