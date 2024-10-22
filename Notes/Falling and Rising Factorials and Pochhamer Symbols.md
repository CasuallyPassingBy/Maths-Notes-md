---
tags:
  - SpecialNotations
---
Subjects: [[Special Notations]]
We define the _******falling factorial******_ is defined as

$$ (x)_n = x^{\underline n} = \prod_{k = 0}^{n-1} (x-k) = \prod_{k = 1}^n (x-k+1) $$

Similarly we define the rising factorial as

$$ x^{(n)} = x^{\overline n} = \prod_{k = 0}^{n-1} (x+k) = \prod_{k = 1}^n (x+k-1) $$

### Properties

- $(x)_n = (x-n+1)^{(n)} =(-1)^n(-x)^{(n)}$
- $x^{(n)} = (x+n-1)_{n} =(-1)^n(-x)_{n}$

We get that the special case of the rising factorial of $1/2$, we get

$$ \left(\frac{1}{2}\right)^{(n)} = \frac{(2n-1)!!}{2^n} $$

which is sometimes used in the Taylor series of $\sqrt{1+x}$.

We get some really nice properties namely, with this we can define the generalized binomial coefficients as

$$ {x \choose n } = \frac{(x)_n}{n!} = \frac{x^{\underline n}}{n!} $$

and

$$ {x+n-1 \choose n} = \frac{x^{(n)}}{n!} = \frac{x^{\overline n}}{n!} $$

which brings more of a symmetric idea to the negative binomial coefficients. 
Since 
$$
	{-x \choose n} = (-1)^n\frac{x^{(n)}}{n!} = (-1)^n {x+n-1\choose n}
$$

The falling factorial can be extended to real values of $x$ using the gamma function provided $x$ and $x+n$ are real numbers that are not negative integers

$$ (x)_n = \frac{\Gamma(x+1)}{\Gamma(x-n+1)} $$

and the rising factorials as

$$ x^{(n)} = \frac{\Gamma(x+n)}{\Gamma(x)} $$

Falling factorials appear in multiple differentiation of simple power function

$$ \left(\frac{d}{dx}\right)^n x^a = (a)_n x^{a-n} $$

They also appear in the [[Hypergeometric Function|hypergeomtric fucntions]] as

$$ {}_2F_1(a,b;c;z) = \sum_{n=0}^\infty \frac{a^{(n)} b^{(n)}}{c^{(n)}} \frac{z^n}{n!}

$$

but the assholes use the wrong notation, when they are studying it.

### Relation to the Stirling Numbers

We can make a connection to the powers using the Stirling numbers of the first kind

$$ \begin{align*}(x)_n & = \sum_{k=0}^n \begin{bmatrix} n \\ k \end{bmatrix} (-1)^{n-k}x^k \\x^{(n)} & = \sum_{k=0}^n \begin{bmatrix} n \\ k \end{bmatrix} x^k \\\end{align*} $$

and similarly, using the Stirling numbers of the second kind we get that

$$ \begin{align*}x^n & = \sum_{k=0}^{n} \begin{Bmatrix} n \\ k \end{Bmatrix} (x)_{k} \\ & = \sum_{k=0}^n \begin{Bmatrix} n \\ k \end{Bmatrix} (-1)^{n-k} x^{(k)} .\end{align*} $$

We know that the rising and falling factorials are polynomials sequences of binomial type, bringing us to a connection to umbral calculus.

# Pochhammer $k$-symbol

We can define the Pochammer $k$-symbol $(x)_{n,k}$ is defined as

$$ (x)_{n,k}= \prod_{i = 0}^{n-1} (x+i k) = k^n \left(\frac{x}{k}\right)_n $$

which makes that $(x)_{n,1} = x^{(n)}$ which is dumb, and $(x)_{n,-1} =(x)_n$ which is dumber still

We can define the $k$-gamma function as:

$$ \Gamma_k (x) = \lim_{n \to \infty}\frac{n! k^n(nk)^{x/k -1}}{(x)_{n,k}} $$

when $k =1$, then $\Gamma_k = \Gamma$, the [[Gamma Function|usual gamma function]]