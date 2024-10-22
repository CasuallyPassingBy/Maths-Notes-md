---
tags:
  - Analysis
---
Subjects: [[Metric and Normed Spaces]]
Links: [[Isometries in Vector Spaces]], [[Metric Spaces]], [[Normed Spaces]]

Let $X=(X, d_X)$ and $Y =(Y, d_Y)$ be metric spaces. A function $\phi:X \to Y$ is an ********isometry******** if for any $x_1, x_2 \in X$, it satisfies that

$$ d_Y(\phi(x_1), \phi(x_2)) = d_X(x_1, x_2) $$

this implies that $\phi$ has to be injective, but not surjective. Basically like a group homomorphism but for metric spaces. If an isometry is bijective we call it a global isometry, isometric isomorphism or congruence mapping.

Similarly as we defined isometries for metric spaces, we can define a function $f: V \to W$ between normed spaces, we say that $f$ **************preserves norm************** if for any $v \in V$

$$ \|f(v)\|_W = \|v\|_V $$

where $\|\cdot\|_V$ and $\|\cdot \|_W$ are the norms of $V$ and $W$.

Let $f: W \to V$ be an injective linear map, $V$ being a normed space, and $\|\cdot \| _f : W \to \Bbb R$ be defined as $\|w\|_f = \|f(w)\|_V$, then $\|\cdot \|_f$ is a norm in $W$. Meaning we can embue a norm on $W$, using a norm in $V$

Let $W$ and $V$ be normed spaces, and $g : V\to W$ be a linear transformation, then $g$ is an isometry iff $g$ preserves norm

Let $V$ and $n$-dimensional vector space over $\Bbb R$, with a base $\{e_i\}_{i = 1}^n$. Then every $v = \sum x_i e_i$, with unique $x_i \in \Bbb R$, then we can define a $\|\cdot \|_*: V \to \Bbb R$ as

$$ \|v\|_* =\left(\sum_{i = 1}^n x_i \right)^{1/2} $$

Then $\|\cdot\|_*$ is a norm in $V$, and the function $\phi: \Bbb R^n \to V$, defined as $\phi(x_1, \dots, x_n) = \sum x_i e_i$ is a bijective isometry.

In other words every finite vector space over $\Bbb R$, can be be given a norm that is isometrically equivalent and linearly equivalent to $\Bbb R^n$. Meaning there we only need $\Bbb R^n$ for finite dimensional vector spaces over $\Bbb R$.