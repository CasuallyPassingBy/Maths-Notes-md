---
tags:
  - ProbabilityTheory
---
Subjects: [[Probability Theory]]
Links: [[Probability Functions for Random Variables]], [[Random Variables]], [[Random Vectors]], [[Probability Functions for Random Vectors]], [[Change of Variable Theorem in Rn]]

# Random Variables
## Change of Variable Theorem V.1.

Let $X$ be a continuous random variable with a probability density function $f_X$. Let $\varphi: \Bbb R \to \Bbb R$ be a strictly monotone continuous function with differentiable inverse $\varphi^{-1}$. Then probability density function of $Y = \varphi(X)$ is given by

$$ f_Y(y) = \begin{dcases} f_X(\varphi^{-1}(y))\left|\frac{d}{dy} \varphi^{-1}(y)\right| & y \in \operatorname{Im}\varphi \circ X \\ 0 & \text{otherwise} \end{dcases} $$

This result is basically the application of the chain rule and its fairly trivial

We can generalise this theorem for the transformations $\varphi$ that are piecewise strictly monotone. 

## Change of Variable Theorem V.2.

Let $X$ be continuous random variable with values inside, with a pdf of $f_X(x)$, and values inside $(a, c)$. Let $\varphi:(a, c) \to \Bbb R$ be a function such that admits this decomposition: $$\varphi(x) = \varphi_1(x) \cdot1_{(a, b)} (x)+ \varphi_2(x) \cdot1_{( b, c)} (x)$$ where $a < b< c$, and each of the functions $\varphi_1(a,b) \to \Bbb R$ and $\varphi_2:(b,c) \to \Bbb R$ be continuous, strictly monotonous, and with differentiable inverse. Then the random variable $Y = \varphi(X)$ takes values inside the set $\varphi(a, c)$, and has a density function of $$\begin{align*}
f_Y(y) &=  f_X(\varphi_1^{-1}(y))\left|\frac{d}{dy} \varphi_1^{-1}(y)\right|\cdot 1_{\varphi_1(a, b)}(x) \\ &+   f_X(\varphi_1^{-1}(y))\left|\frac{d}{dy} \varphi_2^{-1}(y)\right|\cdot 1_{\varphi_2(b, c)}(x)
\end{align*}
$$
The proof is fairly similar to the one above. A somewhat common thing to do with random variable is squaring it, so it can be useful to know how. 

Let $X$ be random variable, and $Y = X^2$. We can split $\varphi(x) = x^2$ into two pieces, both strictly monotone, and get that the density function of $Y$, is $$f_Y(y) = \begin{dcases}
	f_X(-\sqrt y) \frac{1}{2\sqrt y} + f_X(\sqrt y ) \frac{1}{2\sqrt y} & y >0 \\
	0 & y \le 0
\end{dcases}
$$
# Random Vectors

This involves involves a bit more machinery since it is quite similar to the change of variable of $\Bbb R^n$. 

## Change of Variable V.3.

Let $(X, Y)$ be a random continuous vector with values inside $I \subseteq \Bbb R^2$, with a pdf $f_{X, Y}(x, y)$. Let $\varphi:I \to \Bbb R²$ be continuous with inverse $\varphi^{-1}(u, v)$ differentiable. Then the values $(U, V) = \varphi(X, Y)$ take values in $\varphi(I)$ with a density function $$f_{U, V} (u, v) = \begin{dcases}
f_{X, Y}(\varphi^{-1}(u, v)) |J(u, v)| & (u, v) \in \varphi(I) \\
0 & \text{otherwise}
\end{dcases}$$
Where $$|J(u, v) | = |\det J_{\varphi^{-1}}(u, v)|$$
### Important Transformations
#### Sum
Let $(X, Y)$ be absolutely continuous vector with a density function $f_{X, Y}(x, y)$. Then $X+Y$ has a distribution function $$f_{X+Y} (u) = \int_{-\infty}^\infty  f_{X, Y}(u-v, v)\, dv $$
While the formula might look a bit asymmetric, we can just consider the change of variable $z = u -v$, and would get $$f_{X+Y} (u) = \int_{-\infty}^\infty  f_{X, Y}(z, u-z)\, dz $$Meaning it is completely symmetrical. 

If we look into the case where $X$ and $Y$ are independent. Then we get that $$f_{X+Y} (u) = \int_{-\infty}^\infty  f_X(u-v) f_Y(v)\, dv $$
This is related with the idea of the [[Convolution]], and can be seen as $f_{X+Y} = f_X * f_Y$

When $X$ and $Y$ are independent discrete variables with whole number values, it is fairly easy to to verify the pmf of $X+Y$, in complete analogy $$f_{X+Y}(u) = \sum_{k \in \Bbb Z} f_X(u-k) f_Y(k)$$
#### Difference

Let $(X, Y)$ be absolutely continuous vector with a density function $f_{X, Y}(x, y)$. Then $X-Y$ has a distribution function $$f_{X-Y} (u) = \int_{-\infty}^\infty  f_{X, Y}(u+v, v)\, dv $$
When $X$ and $Y$ are independent we get the $$f_{X+Y} (u) = \int_{-\infty}^\infty  f_X(u+v) f_Y(v)\, dv$$
When $X$ and $Y$ are independent discrete variables with whole number values, it is fairly easy to to verify the pmf of $X-Y$, in complete analogy $$f_{X-Y}(u) = \sum_{k \in \Bbb Z} f_X(u+k) f_Y(k)$$
#### Product

Let $(X, Y)$ be absolutely continuous vector with a density function $f_{X, Y}(x, y)$. Then $XY$ has a distribution function $$f_{XY} (u) = \int_{-\infty}^\infty  f_{X, Y}(u/v, v)\left|\frac{1}{v}\right|\, dv  $$

#### Quotient

Let $(X, Y)$ be absolutely continuous vector with a density function $f_{X, Y}(x, y)$. Then $X/Y$ has a distribution function $$f_{X/Y} (u) = \int_{-\infty}^\infty  f_{X, Y}(uv, v)\left|v\right|\,  dv  $$