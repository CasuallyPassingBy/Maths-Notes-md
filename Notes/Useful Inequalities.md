Links: [[Useful Identities]]
### Weiestrass

let $(a_i)_{i\in I}$ be finite collection of real numbers in $[0,1]$ then:

$$ 1+\sum_{i\in I}a_i \le\prod_{i\in I}(1+a_i)\le\left(1-\sum_{i\in I}a_i\right)^{-1} $$

$$ 1-\sum_{i\in I}a_i\le\prod_{i\in I}(1-a_i) \le \left(1-\sum_{i\in I} a_i \right)^{-1} $$

### Hölder

When $p + q = 1$, then:

$$ \sum_{i=1}^n|x_iy_i|\le \left(\sum_{i=1}^n|x_i|^p\right)^{1/p} \left(\sum_{i=1}^n|y_i|^q\right)^{1/q} $$

### Minkowski

When $p\ge 1$, then:

$$ \left(\sum_{i=1}^n|x_i+y_i|^p\right)^{1/p}\le\left(\sum_{i=1}^n|x_i|^p\right)^{1/p}+\left(\sum_{i=1}^n|y_i|^p\right)^{1/p} $$

### Cauchy-Schwarz

$$ \left(\sum_{i=1}^nx_iy_i\right)^{1/2}\le\left(\sum_{i=1}^nx_i^2\right)^{1/2}\left(\sum_{i=1}^ny_i^2\right)^{1/2} $$

### The Mean Inequality

$$ \frac{n}{\sum_{i}x_i^{-1}}\le\left(\prod_ix_i\right)^{\frac{1}{n}}\le\frac{1}{n}\sum_i x_i \le\left(\frac{1}{n}\sum_ix_i^2\right)^{\frac{1}{2}}\le\frac{\sum_i x_i^2}{\sum_i x_i} $$

We define numbers, $p, q \in (1,\infty)$ that satisfy $\dfrac{1}{p} +\dfrac{1}{q} = 1$, are called harmonic conjugates. We can extend the definition with $p = 1$, and $q = \infty$, as long as we define $\dfrac{1}{\infty} = 0$. This DOESN’T MEAN, that $1 = \infty \cdot 0$.

### Young’s Inequality

Let $p, q \in (1, \infty)$ such that $\dfrac{1}{p} +\dfrac{1}{q} =1$. Then, for any real numbers $a, b\ge0$ it follows that

$$ ab \le \frac{1}{p}a^p+\frac{1}{q}b^q $$

### Hölder’s Inequality in $\Bbb R^n$

Let $p, q$ harmonic conjugates. Then for any $x, y \in \Bbb R^n$, it follows that with ${(xy)_i = x_i y_i}$ (Hadarmard product) for $1 \le i \le n$

$$ \sum_{i = 1}^n|x_iy_i | \le \left(\sum_{i = 1}^n |x_i|^p \right)^{1/p}\left(\sum_{i = 1}^n |y_i|^q \right)^{1/q} $$

or equivalently,

$$ \|xy\|_1 \le \|x\|_p \|y\|_q $$

### Minkowski Inequality in $\Bbb R^n$

Let $p \in [1, \infty]$, then for any $x, y \in \Bbb R^n$ we have that

$$ \|x+y\|_p \le \|x\|_p +\|y\|_p $$

This finally gives us that $\|\cdot \|_p$ is a norm in $\Bbb R^n$. Then we can see that $(\Bbb R^n, \|\cdot\|_p)$ is a normed space, and we can denote it simply as $\Bbb R^n _p$.

We can compare different $p$-metrics, and get the following results:
- $\|x \|_r \le \|x\|_s$ for $1 \le s\le r\le\infty$
- $\|x\|_s \le n^{\frac{r-s}{sr}} \|x\|_r$ for $1 \le s\le r<\infty$
- $\|x\|_s \le n^{\frac{1}{s}} \|x\|_\infty$ for $1 \le s < \infty$
    
- For any $x \in \Bbb R^n$, we have that
    $$ \|x\|_\infty = \lim_{r \to \infty} \|x\|_r $$