Links: [[Taylor Series in R]], [[Trigonometric Identities]], [[Useful Identities]]
# Exponential 
$$e^x  = \exp(x) = \sum_{n = 1}^\infty \frac{x^n}{n!} \quad\text{for all $x \in \mathbb{C}$} $$

$$\exp(\exp(x)-1) = \sum_{n = 1}^\infty \frac{B_n}{n!} x^n$$where $B_n$ represents the [[Bell numbers]]

We also have the Error function defined as $$\text{erf}\; x:= \frac{2}{\sqrt\pi}\int_0^x e^{-t^2}\, dt$$ getting that $$\text{erf}\; x = \frac{2}{\sqrt\pi} \sum_{n = 0}^\infty  (-1)^n \frac{1}{n! (2n+1)}x^{2n+1}$$
# Logarithm
$$\ln(1-x) = -\sum_{n= 1}^\infty \frac{x^n}{n} $$
$$\ln(1+x) = \sum_{n= 1}^\infty (-1)^{n+1}\frac{x^n}{n} $$

# Geometric Series
$$\frac1{1-x} = \sum_{n = 0}^\infty x^n$$
$$\frac1{(1-x)^2} = \sum_{n = 0}^\infty nx^{n-1}$$
$$\frac1{(1-x)^3} = \sum_{n = 0}^\infty \frac{n(n-1)}{2}x^{n-2}$$


all of them are convergent for $|x|<1$

# Binomial Series

The binomial series is the power series $$(1+x)^\alpha = \sum_{n = 0}^\infty {\alpha\choose n} x^n$$
where ${\alpha\choose n}$ are the [[Generalised Binomial Theorem|generalised binomial coefficients]], and only converge for $|x| <1$. The are special cases for $\alpha = \pm 1/2$, which are worth noting $$(1+x)^{1/2} = \sum_{n = 0}^\infty {\frac1{2}\choose n} x^n = \sum_{n = 0}^\infty (-1)^{n-1} \frac{(2n-2)!!}{(2n)!!} x^n = \sum_{n = 0}^\infty \frac{(-1)^{n-1}(2n)!}{4^n (n!)^2 (2n-1)} x^n  $$
$$(1+x)^{-1/2} = \sum_{n = 0}^\infty{-\frac{1}{2}\choose n}x^n = \sum_{n = 0}^\infty (-1)^n\frac{ (2n-1)!!}{(2n)!!}x^n = \sum_{n = 0}^\infty \frac{(-1^n)(2n)!}{4^n (n!)^2} x^n$$
Using the [[Multifactorials]] notation

# Trig Functions at $x = 0$
$$ \sin x = \sum_{k =0}^\infty \frac{(-1)^k x^{2k+1}}{(2k+1)!} \quad\text{for all $x \in \mathbb{C}$} $$

$$ \cos x = \sum_{k =0}^\infty \frac{(-1)^k x^{2k}}{(2k)!} \quad\text{for all $x \in \mathbb{C}$} $$

$$ \tan x= \sum_{k =1}^\infty B_{2k}\frac{(-4)^{k}(1-4^{k}) x^{2k-1}}{(2k)!} \quad \text{for $|x| < \frac{\pi}{2}$} $$
$$\sec x = \sum_{n = 0}^\infty \frac{(-1)^n E_{2n}}{(2n)!}x^{2n} \quad \text{for $|x| < \frac{\pi}{2}$} $$
$$\csc x = \sum_{n = 0}^\infty \frac{(-1)^{n-1}2(2^{2n-1}-1)B_{2n}}{(2n)!}x^{2n-1} \quad \text{for $0<|x| < {\pi}$}$$
$$ \cot x =  \sum_{n = 0}^\infty (-1)^n \frac{2^{2n}B_{2n}}{(2n)!}x^{2n-1}\quad \text{for $0<|x| < \pi $}$$
where $B_n$ are the [[Bernoulli numbers]], and $E_n$ are the [[Euler Numbers]]

# Inverse Trig Functions

$$\arcsin x = \sin^{-1} x = \sum_{n = 0}^\infty \frac{(2n)!}{4^n (n!)^2(2n+1)}x^{2n+1} = \sum_{n = 0}^\infty (-1)^n{{-\frac{1}{2}} \choose n} \frac{x^{2n+1}}{2n+1} \quad \text{for } |x|\le 1$$
$$\arccos x = \cos^{-1} x = \frac{\pi}{2} -\sin^{-1} x = \frac{\pi}{2}-  \sum_{n = 0}^\infty \frac{(2n)!}{4^n (n!)^2(2n+1)}x^{2n+1} \quad \text{for } |x|\le 1$$
$$\arctan x = \tan^{-1} x = \sum_{n = 0}^\infty \frac{(-1)^n}{2n+1}x^{2n+1} \quad \text{for } |x|\le 1$$
# Hyperbolic Trig Functions at $x = 0$
$$ \sinh x = \sum_{k =0}^\infty \frac{ x^{2k+1}}{(2k+1)!} \quad\text{for all $x \in \mathbb{C}$} $$

$$ \cosh x = \sum_{k =0}^\infty \frac{ x^{2k}}{(2k)!} \quad\text{for all $x \in \mathbb{C}$} $$

$$ \tanh x= \sum_{k =1}^\infty B_{2k}\frac{4^{k}(1-4^{k}) x^{2k-1}}{(2k)!} \quad \text{for $|x| < \frac{\pi}{2}$} $$
$$\text{sech}\; x = \sum_{n = 0}^\infty \frac{ E_{2n}}{(2n)!}x^{2n} \quad \text{for $|x| < \frac{\pi}{2}$} $$
$$\text{csch}\; x = -\sum_{n = 0}^\infty \frac{2(2^{2n-1}-1)B_{2n}}{(2n)!}x^{2n-1} \quad \text{for $0<|x| < {\pi}$}$$
$$ \text{coth} \;x =  \sum_{n = 0}^\infty \frac{2^{2n}B_{2n}}{(2n)!}z^{2n-1}\quad \text{for $0<|x| < \pi $}$$
where $B_n$ are the [[Bernoulli numbers]], and $E_n$ are the [[Euler Numbers]]

# Inverse Hyperbolic Trig Functions

$$\text{arcsinh}\; x = \sinh^{-1} x = \sum_{n = 0}^\infty \frac{(-1)^n (2n)!}{4^n (n!)^2(2n+1)}x^{2n+1} = \sum_{n = 0}^\infty {{\frac{1}{2}} \choose n} \frac{x^{2n+1}}{2n+1} \quad \text{for } |x|\le 1$$
$$\text{arctanh}\; x = \tanh^{-1} x = \sum_{n = 0}^\infty \frac{1}{2n+1}x^{2n+1} \quad \text{for } |x|\le 1$$

# Elliptic Integrals

The complete [[Elliptic Integrals|elliptic integral]] of the first kind $K$ has a Taylor Series of $$K(x) = \frac{\pi}{2} \sum_{n = 0}^\infty \left(\frac{(2n)!}{4^n(n!)^2}\right)^2x^{2n} = \frac{\pi}{2} \sum_{n = 0}^\infty \left(\frac{(2n-1)!!}{(2n)!!}\right)^2x^{2n}$$
The second elliptic integral of the second kind $E$ has a Taylor series $$E(x) = \frac{\pi}{2} \sum_{n = 0}^\infty \left(\frac{(2n)!}{4^n (n!)^2}\right)^2\frac1{1-2n} x^{2n} = \frac{\pi}{2} \sum_{n = 0}^\infty \left(\frac{(2n-1)!!}{(2n)!!}\right)^2\frac1{1-2n} x^{2n}$$
