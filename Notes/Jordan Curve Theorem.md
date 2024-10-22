---
tags:
  - Topology
---
Subject: [[Topology]]

We define a Jordan Curve $\Gamma$ as the image of a continuous and injective function $\gamma$, from $\Bbb S^1$ to $\Bbb R^2$. Meaning is a simple closed curve. The Jordan Curve Theorem states that $\Bbb R^2 \setminus \Gamma$ *is disconnected and consists of two components*. 

We know that $\Gamma$ is compact, and we have that two compact sets are disjoint iff $\text{dist}(A, B)> 0$, and that $\gamma^{-1}$ is continuous

A Jordan curve is said to be a *Jordan polygon* if $\Bbb S^1$ can be covered by finitely many arcs on each of which $\gamma$ has the form 
$$
\gamma(\cos t, \sin t)= (\lambda t+\mu, \rho t +\sigma)
$$
with constants $\lambda, \mu, \rho, \sigma$. Thus $\Gamma$ is a closed curve without intersections.

**Lemma 1**
The Jordan curve theorem holds for every Jordan polygon $\Gamma$.
The proof of this lemma makes it as to consider $\Gamma$ as a bunch of edges $E_1, \dots, E_n$, and vertices $v_1, \dots, v_n$. 
Then we take the minimum distance from the edges to each other that are not neighbouring each other
$$
\delta = \min\{\text{dist}(E_i, E_j) \mid 1 < j-i<n-1\}
$$
And we consider the "ball" around each edge,
$$
N_i := \{ q\in \Bbb R^2 \mid \text{dist}(q, E_i)<\delta\}
$$
We can see that for each $N_i$, we get that, $N_i \cap \Gamma \subseteq E_{i-1}\cup E_i \cup E_{i+1}$, ($E_0 = E_n$)this is because we are looking at the part of the path that is in this "ball", since we chose $\delta$ that way, then we only touch the adjacent edges of each edge $E_i$. We can see that actually $N_i \setminus \Gamma$ is actually composed of two components, the proof calls them $N_i'$ and $N_i''$, i will do the same. Then we can create two connected sets. 

And we can see that $N_i'\cap N_{i+1}' \ne \varnothing$ and $N_i''\cap N_{i+1}'' \ne \varnothing$, for $i = 1, \dots n$. 

Then $\bigcup\limits_{i = 1}^n N_i'$ and $\bigcup\limits_{i = 1}^n N_i''$ are both connected sets and for any $p \in \Bbb R^2\setminus \Gamma$ there's is a line segment in $\Bbb R^2\setminus \Gamma$ connecting $p$ to one of them.

We are going to split the points of $\Bbb R^2\setminus \Gamma$ into two types: evens and odds. This is so that we can actually say that $\Bbb R^2\setminus \Gamma$ has at least two connected components

We need to choose a coordinate system such that each vertex $v_i=(x_i, y_i)$ has a different $x_i$ value. The partition is made as such: let $p\in \Bbb R^2\setminus \Gamma$, let $m(p)$ be the number of points in which the upward vertical ray from $p$ meets $\Gamma$. We make the exception however, when the ray either touches one vertex $v_i$, or when $v_{i-1}$ and $v_{i+1}$ lie on the same side vertically through $p$. If $m(p)$ is odd (even) then $p$ is odd (even)

We can see that for every $p$ there's an $\varepsilon>0$ such that if $d(q, p)< \varepsilon$, then $q$ and $p$ have the same parity. Lastly we need to check that this partition is actually path-connected, and it is. Then we get the first lemma: The Jordan curve theorem holds for Jordan polygons.

**Lemma 2:** Every Jordan curve $\Gamma$ can be approximated arbitrarily well by a Jordan polygon $\Gamma'$

The way this works is by abusing the hell out of the continuity of $\gamma$ and $\gamma^{-1}$, and we make a fine enough grid such that $\Gamma$ only touches a a finite number of squares in the grid and we begin making approximations, like the points that touch the grid make a linear interpolation. If the grid is fine enough we can make it arbitrarily good

**Lemma 3:** Let $\Gamma$ be a Jordan polygon. Then the bounded component of $\Bbb R^2\setminus \Gamma$ contains a disc, on the boundary of the circle of which are two points $\gamma(a)$ and $\gamma(b)$, with $|a-b|\ge \sqrt{3}$

**Lemma 4:** Let $\Gamma$ be Jordan polygon, and $a$ and $b$ points belonging to the same connected component, $X$, $\Bbb R^2\setminus\Gamma$ . Let the distance from $\Gamma$ and $\{a, b\}$ be at least $1$, and for every chord $S$, that starts and ends in $\Gamma$, but contained in $X$, that has length less than $2$, $a$ and $b$ are in the same component of $X\setminus S$. Then we have that there is a continuous path $\Pi$ from $a$ to $b$ such that $\text{dist}(\Pi, \Gamma) \ge 1$. 
### Jordan Curve Theorem
Let $\Gamma$ be a Jordan curve in $\Bbb R^2$. Then $\Bbb R^2\setminus \Gamma$ has exactly two connected components. One of this components is bounded (the interior), and the other one is unbounded (the exterior), and the curve $\Gamma$ is the boundary of each component. 

Let $\Gamma$ be a Jordan arc, i.e., the image of a continuous mapping of $[0,1]$ under an injective continuous map, also known a simple open curve. Then $\Bbb R^2\setminus \Gamma$ is connected

Apparently there's a generalisation called, [[Jordan-Brouwer Separation Theorem]]