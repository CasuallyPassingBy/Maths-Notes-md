---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Continuity on Metric Spaces]]

Let $(X, d_X)$ and $(Y, d_Y)$ be metric spaces, we can write $F(X, Y) = \{ f: X\to Y \mid f \text{ function}\} =\\^X Y = Y^X$. 

Let $\mathcal F \subseteq F(X, Y)$
- Given $x\in X$, $\mathcal F$ is **equicontinuous at** $x$, for every $\varepsilon > 0$ there's a $\delta>0$ such that for every $y\in X$ and every $f\in \mathcal F$, we have if $$d_X(x, y) < \delta \implies d_Y(f(x), f(y)) <\varepsilon$$We say that $\mathcal F$ is **equicontinuous** on $A\subseteq X$, if it is equicontinuous at every point $x \in A$.
- $\cal F$ is **uniformly equicontinuous** on $A\subseteq X$ if for every $\varepsilon >0$ there's a $\delta>0$, such that for every $x, y \in A$ and every $f\in \cal F$, $$d_X(x, y) < \delta \implies d_Y(f(x), f(y)) <\varepsilon$$

We have a couple of observations, we can make:
- If $\cal F$ is equicontinuous at $X$, then every $f\in \cal F$ is continuous at $x$
- If $\cal F$ is equicontinuous on $X$, then $\mathcal F \subseteq \mathcal C(X, Y)$ 
- If $\cal F$ is uniformly equicontinuous on $A$, then for every $f\in \cal F$, then $f|_A$ is uniformly continuous on $A$
- If $\mathcal F \subseteq \mathcal C(X, Y)$ is finite, then $\cal F$ is equicontinuous on $X$

We have that equicontinuity $\centernot \implies$  uniform equicontinuity.

We have that uniform equicontinuity $\centernot \implies$  uniform equicontinuity.

Let $\mathcal F \subseteq \mathcal C(X, Y)$ and $K \subseteq X$ compact, if $\cal F$ is equicontinuous on $K$, then $\cal F$ is uniformly equicontinuous on $K$. 

Let $(X, d_X)$ and $(Y, d_Y)$ be metric spaces and $\mathcal F\subseteq F(X, Y)$ and $X$ be locally compact. Then $\cal F$ is equicontinuous on $X$ iff $\cal F$ is uniformly equicontinuous on every $K \subseteq X$ compact.