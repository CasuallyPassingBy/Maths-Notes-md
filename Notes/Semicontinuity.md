---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Topology on Metric Spaces]], [[limsup and liminf]], [[Continuity on Metric Spaces]], [[Rectifiable Curves in Rn]]

A function $f:X \to \Bbb R\cup\{ \infty\}$ is ********************_lower semicontinuous at the point $x_0 \in X$_ if given that ${c< f(x_0)}$, there’s a $\delta>0$ such that

$$ d_X(x, x_0) < \delta \implies c<f(x) $$

We say that $f$ is ********************lower semicontinuous******************** if it is at every $x_0 \in X$.

A function $f: X \to \Bbb R\cup \{-\infty\}$ is *********************************_upper semicontinuous at the point $x_0 \in X$_ if given that ${f(x_0) < c}$, there’s a $\delta>0$ such that

$$ d_X(x, x_0) \implies f(x)< c $$

We say that $f$ is ****************upper semicontinuous**************** if it is at every $x_0 \in X$.

Let $f: X \to \Bbb R\cup \{ \infty\}$, $f$ is lower semicontinuous at $x_0$ iff we have that for every sequence $(x_k)$ in $X$ that $x_k \to x$, it is satisified that

$$ f(x_0) \le \liminf _{k \to \infty} f(x_k) $$

or using the functional version, we get that

$$ f(x_0) \le \liminf_{x \to x_0}f(x) $$

Let $f:X \to \Bbb R\cup\{-\infty\}$, $f$ is lower semicontinuous at $x_0$, iff we have that for every sequence $(x_k)$ in $X$, such that $x_k \to x$, it is satisfied that

$$ f(x_0) \ge \limsup _{k \to \infty} f(x_k) $$

or using the functional version, we get that

$$ f(x_0) \ge \limsup_{x \to x_0}f(x) $$

We can have a similar idea to translate the problem of continuity of a function to thinking of the the pre-image of an open set. Doing so we get that $f:X \to \Bbb R\cup\{\infty\}$ is lower semicontinuous if

$$ f^{-1}[(r, \infty]] \text{ is open for all }r \in \Bbb R $$

Similarly get that $f: X \to \Bbb R\cup\{-\infty\}$ is upper semicontinuous if

$$ f^{-1}[[ -\infty, r)] \text{ is open for all }r \in \Bbb R $$

A function is continuous iff it is lower semicontinuous and upper semicontinuous.

Let $f: X \to \Bbb R\cup\{\infty\}$ is lower semicontinuous and if $f^{\le a}:= f^{-1}[( -\infty, a]]$ is a non empty compact set for some $a \in \Bbb R$, then $f$ reaches its minimum on $X$.

Let $f: X \to \Bbb R \cup\{-\infty\}$ is upper semicontinuous and if $f^{\ge a}:= f^{-1}[[a, \infty)]$ is a nonmepty compact set for some $a \in \Bbb R$, then $f$ reaches its maximum on $X$.