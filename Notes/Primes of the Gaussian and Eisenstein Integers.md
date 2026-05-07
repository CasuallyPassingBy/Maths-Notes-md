---
tags:
  - RingTheory
  - NumberTheory/AlgebraicNumberTheory
---
Subjects: [[Ring Theory]], [[Algebraic Number Theory]]
Links: [[Quadratic Integers]], [[Integral Domains]], [[Unique Factorisation Domains]], [[Legendre Symbols]]

# Gaussian Integers

We know that the Gaussian integers are an Euclidean domain with the norm $N(z) = |z|^2$ , and in particular they are a unique factorisation domain.

**Obs:** Let $\alpha\in \Bbb Z[i]$ such that $N(\alpha) = p$ with $p$ prime in $\Bbb Z$, then $\alpha$ is a prime in $\Bbb Z[i]$. Additionally, if $\alpha \in \Bbb Z[i]$, then $N(\alpha) = \alpha \overline{\alpha}$, and in particular $\alpha \mid N(\alpha)$. 

**Lemma:** If $\alpha \in \Bbb Z[i]$ and $q$ is the smallest integer that $\alpha$ divides then $q$ is a prime in $\Bbb Z$. Additionally, if $\alpha$ can only divide a single prime $q\in\Bbb Z$.

**Obs:** The prime of $\Bbb Z[i]$ are factors of primes in $\Bbb Z$. 

**Lemma:** Let $\alpha\in \Bbb Z[i]$ and suppose that $\alpha$ divides the prime $p$. Then $$N(\alpha) \mid p^2.$$Additionally, we have two cases
- If $N(\alpha) = p^2$, then this means that $\alpha\beta = p$, with $\beta$ a unit, and $\alpha$ and $p$ are associates. Lastly, $p$ is also a prime in $\Bbb Z[i]$. 
- If $N(\alpha) = p$, then $$p = N(\alpha) = a^2+b^2,$$if $\alpha = a+bi\in \Bbb Z[i]$. 

**Obs:** The primes $p\in \Bbb Z$ are classified as:
- $2$
- $p\equiv 1 \pmod 4$
- $p\equiv 3\pmod 4$.

**Obs:** We can factorise $2$ in the ring $\Bbb Z[i]$, since it is $(1+i)(1-i)$. Notice that $(1-i)$ is associate to $(1+i)$, and $(1+i)$ is prime. 

**Obs:** If $p \equiv 3\pmod 4$ and prime $p$ in $\Bbb Z$, then $p$ cannot be written as the sum of two squares, thus $p$ must also be prime in $\Bbb Z[i]$. 

If $p \equiv 1 \pmod 4$ and prime $p$ in $\Bbb Z$, we can use the quadratic residue to show that there exists $x\in \Bbb Z$ such that $x^2 \equiv -1 \pmod p$, then $p\mid x^2 +1$ in $\Bbb Z$. Notice that $x^2+1 = (x-i)(x+i)$ in $\Bbb Z[i]$, then $$p\mid (x+i)(x-i),\quad \text{in }\Bbb Z[i].$$If $p$ was a prime in $\Bbb Z[i]$, then $p \mid x+i$ or $p\mid x-i$, which would imply that $$\frac xp \pm \frac1 pi\notin \Bbb Z[i].$$Then $p$ cannot be prime, We can prove that $\alpha = a+bi$, and $p = \alpha \overline{\alpha}$, and this means that $$\alpha^2 +\beta^2 = N(\alpha)= \alpha \overline{\alpha} = p, $$this means that $p = 4n +1\in \Bbb Z$ is a sum of squares. The divisors of $\Bbb Z[i]$ of $p=4n+1$ are $$\alpha, i\alpha, -\alpha, -i\alpha, \overline\alpha, i\overline\alpha, -\overline\alpha, -i\overline\alpha.$$
**Th:** the primes of $\Bbb Z[i]$ are
- $1+i$ and its associates.
- the primes $p = 4n+3\in \Bbb Z$, and its associates.
- the factors $\alpha = a +bi$ the prime of the integer primes of the form $p = 4n+1\in \Bbb Z$. 

The primes that are also prime in $\Bbb Z[i]$ are also called *Gaussian primes*

This actually gives us a proof of the following number theoretic question. 

**Fermat's Theorem on Sum of Squares or Fermat's Christmas Theorem:** The prime $p$ (in $\Bbb Z$) is the sum of two integer squares, $p = a^2+b^2$, $a,b\in \Bbb Z$, iff $p = 2$ or $p \equiv 1\pmod 4$. Except for interchanging $a$ and $b$ or changing the signs of $a$ and $b$, the representation of $a$ as a sum of two squares is unique.

**Cor:** Let $n$ be a positive integer and write $$n = 2^k p_1^{\alpha_1}\cdots p_r^{\alpha_r}q_1^{\beta_1}\cdots q_s^{\beta_s}$$where $p_1, \dots p_r$ are distinct primes congruent to $1$ modulo $4$ and $q_1, \dots, q_r$ are distinct primes congruent $3$ modulo $4$. Then $n$ can be written as a sum of two squares in $\Bbb Z$ iff each $\beta_i$ is even. Further, if this condition on $n$ is satisfied, the number of representation of $n$ as a sum of two squares is $4(\alpha_1+1)(\alpha_2+1)\cdots (\alpha_r+1)$. 
# Eisenstein Integers

Let $\omega = (1+\sqrt{-3})/2$. We know that the Eisenstein integers, $\Bbb Z[\omega]$, is a Euclidean domain with the norm $N(a+b\omega) = a^2 +ab +b^2 =|a+b\omega|^2$. 

We know that the units of $\Bbb Z[\omega]$ are $\{\pm 1,\pm\omega, \pm\omega^2\}$. 

**Obs:** Let $\alpha\in \Bbb Z[\omega]$ such that $N(\alpha) = p$ with $p$ prime in $\Bbb Z$, then $\alpha$ is a prime in $\Bbb Z[\omega]$. Additionally, if $\alpha \in \Bbb Z[i]$, then $N(\alpha) = \alpha \overline{\alpha}$, and in particular $\alpha \mid N(\alpha)$. 

We know that, just as in the case where the Gaussian integers not all primes of $\Bbb Z$ are primes in the Gaussian integers, not all primes of $\Bbb Z$ are again primes in $\Bbb Z[\omega]$. We know that $(3-\omega)(2+\omega) = 7$. 

**Lemma:** Let $\alpha\in \Bbb Z[\omega]$ and suppose that $\alpha$ divides the prime $p$. Then $$N(\alpha) \mid p^2.$$Additionally, we have two cases
- If $N(\alpha) = p^2$, then this means that $\alpha\beta = p$, with $\beta$ a unit, and $\alpha$ and $p$ are associates. Lastly, $p$ is also a prime in $\Bbb Z[\omega]$. 
- If $N(\alpha) = p$, then $$p = N(\alpha) = a^2+ab+b^2,$$if $\alpha = a+b\omega\in \Bbb Z[\omega]$. 

**Obs:** The primes $p\in \Bbb Z$ are classified as:
- $3$
- $p\equiv 1 \pmod 3$
- $p\equiv 2\pmod 3$.

We can check that $-(1-2\omega)^2 = 3$, and thus $3$ is not a prime. 

**Obs:** If $p$ is a rational prime, and $p\equiv 2$, then it is also a prime in $\Bbb Z[\omega]$. 

If $p \equiv 1 \pmod3$, then $-3$ is a quadratic residue $\mod p$, meaning, that there's an $x\in\Bbb Z$ such that $x^2\equiv -3 \pmod p$. With this in mind, we can find that $p\equiv 1 \pmod 3$, then $p = \alpha \overline\alpha$, then $\alpha$ is a prime of $\Bbb Z[\omega]$. 

**Th:** the primes of $\Bbb Z[\omega]$ are
- $2+\omega$ and its associates.
- the primes $p = 3n+2\in \Bbb Z$, and its associates.
- the factors $\alpha = a +b\omega$ the prime of the integer primes of the form $p = 3n+1\in \Bbb Z$. 

The primes that are also prime in $\Bbb Z[\omega]$ are also called *Eisenstein primes*. 