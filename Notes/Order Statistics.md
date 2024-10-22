---
tags:
  - Statistics
---
Subjects: [[Statistics]]
Links: [[Statistics and Sample Distribution]]

**Def:** Let $X_1, \dots,X_n$ be a random sample. The random variables $$
\begin{align*}
X_{(1)} &= \min\{ X_1,\dots, X_n\}  \\
X_{(2)} &= \min\{X_1, \dots, X_n \}\setminus \{X_{(1)}\} \\
X_{(3)} &= \min\{X_1, \dots, X_n \}\setminus \{X_{(1)}, X_{(2)} \}\\
&\vdots \\
X_{(n)} &= \max \{X_1, \dots, X_n\}
\end{align*}
$$
are known with the name of *order statistics*. To $X_{(1)}$ is known as the as the first order statistic, to $X_{(2)}$ is called the second order statistic, and so on. To $X_{(i)}$ is called the *$i$th order statistic*, $i = 1, \dots, n$

We have the relation $X_{(1)} \le X_{(2)} \le \cdots \le X_{(n)}$. We see that $i$th order statistic is not necessarily equal to random variable in the sample, in general, is a function of all random variables

# Individual Distributions

For $n\ge 1$ 
- $f_{X_{(1)}} = nf(x)[1-F(x)]^{n-1}$
- $f_{X_{(n)}} = n f(x) [F(x)]^{n-1}$ 

The probability density function of the $i$th order statistic is $$f_{X_{(i)}} (x) = {n\choose i}i f(x) [F(x)]^{i-1} [1-F(x)]^{n-i}$$
Let $R = X_{(n)} - X_{(1)}$ is called the *range* of the sample. Then getting the pdf is $$f_R(r) = n(n-1)\int_{-\infty}^\infty f(v)f(r+v)[F(r+v)-F(v)]^{n-2}\,dv $$
# Joint Distributions

For $x_1 < \cdots < x_n$, then $$f_{X_{(1)}, \dots, X_{(n)}}(x_1, \dots, x_n;\theta) = n! \prod_{i= 1}^n f(x_i;\theta)$$
For $i < j$, and $x < y$. Then $$f_{X_{(i)}, X_{(j)}}(x, y) = {n \choose i, j-1, n-j} i (j-i) f(x) f(y)[F(x)]^{i-1}[F(y) - F(x)]^{j-i-1}[1-F(y)]^{n-j}$$
Getting the corollary that $$f_{X_{(1)}, X_{(n)}}(x, y) = n (n-1) f(x) f(y)[F(y) - F(x)]^{n-2} $$
