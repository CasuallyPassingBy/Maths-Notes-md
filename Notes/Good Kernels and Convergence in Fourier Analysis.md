---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Main definitions for Fourier Analysis]], [[Convolution]]

**Def:** A family of kernels $\{K_n(x)\}_{n = 1}^\infty$ on the circle is said to be a family of *good kernels* if it satisfies the following properties:
- For all $n \ge 1$, $$\frac{1}{2\pi}\int_\pi^\pi K_n(x)\, dx = 1$$
- There exists $M>0$ such that for all $n \ge 1$, $$\int_{-\pi}^\pi |K_n(x)|\, dx \le M $$
- For every $\delta>0$, $$\int_{\delta\le |x| \le \pi} |K_n(x)| \, dx \to 0 \quad \text{as} \quad n\to \infty$$
**Th:** Let $\{K_n\}_{n = 1}^\infty$ be a family of good kernels, and $f$ an integrable function on the circle. Then $$\lim_{n\to \infty} (f*K_n)(x) = f(x) $$whenever $f$ is continuous at $x$. If $f$ is continuous everywhere, then the above limit is uniform. 

Because of this result, the family $\{K_n\}_{n = 1}^\infty$ is sometimes referred to as an *approximation to the identity*. 

**Th:** Let $\{K_n\}_{n = 1}^\infty$ be a family of good kernels that are even, and $f$ an integrable function on the circle. If $f$ has jump discontinuity at $x$, then $$\lim_{n \to\infty} (f*K_n)(x) = \frac{f(x^+)+f(x^-)}{2}$$
Given this theorem, we would like to check that $D_N$ is a good kernel, since it would be really comfy to imply that the Fourier series of $f$ converges to $f(x)$  whenever $f$ is continuous at $x$. Unfortunately, we have that $D_N$ violates the second property; $$\int_{-\pi}^\pi |D_N(x)|\, dx \ge c \ln N \quad \text{as }N \to \infty$$
# Cesàro and Abel summability
Since a Fourier series may fail to converge at individual points, we are led to try to overcome this failure by interpreting the limit $$\lim_{N\to \infty} S_N(f) = f$$in a different sense

### [[Cesàro Convergence]]
Since the Dirichlet kernels fail to belong to the family of good kernels, but we can create another kernel that is well behaved using the Dirichlet kernels

**Def:** The $N$-th *Fejér kernel* is given by $$F_N(x) = \frac{1}{N} \sum_{k = 0}^{N-1} D_k(x) $$
**Prop:** We have that $$F_N(x) =\frac{1}{N} \frac{\sin^2(Nx/2)}{\sin^2(x/2)} $$and the Fejér kernel is a good kernel

#### Fejér Theorem
If $f$ is integrable on the circle, then the Fourier series of $f$ is Cesàro summable to $f$ at every point of continuity of $f$. Moreover, if $f$ is continuous on the circle, then the Fourier series of $f$ is uniformly Cesàro summable to $f$.

Additionally, we get that if $f$ has a jump discontinuity at $x$, then $$\lim_{n \to\infty} (f*F_n)(x) = \frac{f(x^+)+f(x^-)}{2}$$

**Cor:** If $f$ is integrable on the circle and $\hat f(n)$ for all $n$, then $f = 0$ at all points of continuity of $f$

**Cor:** Continuous functions on the circle can be uniformly approximated by trigonometric polynomials. This last one can be prove using [[Stone-Weierstrass Theorem]]

## [[Abel's Summability]]
To adapt the idea of Abel's summability to the context of Fourier series, we define the Abel's means of the function $f(\theta) \sim \sum\limits_{n = -\infty}^\infty a_n e^{in\theta}$ by $$A_r(f)(\theta) = \sum_{n = -\infty}^\infty r^{|n|}a_n e^{in\theta}$$$
Since $n$ takes values over all the integers, then it is natural to write it as $c_0 = a_0$, and $c_n = a_n e^{in\theta} + a_{-n}e^{-in\theta}$, for $n> 0$. 

We note that since $f$ in integrable $|a_n|$ is uniformly bounded in $n$, so $A_r(f)$ converges absolutely and uniformly for each $0\le r <1$. Just as the case of Cesàro means, the key fact is that these Abel means can be written as convolutions $$A_r(f)(\theta) = (f*P_r)(\theta)$$where $P_r(\theta)$ is a the *Poisson kernel*.

**Def:** A family of kernels can be indexed by a continuous parameter $0\le r <1$. In the definition of good kernels, we simply replace $n$ by $r$ and the take the limit in the third property appropriately, as $r \to 1^-$, for example

**Lemma:** The Poisson kernel is a good kernel as $r$ tends to $1$ from below, and it is even.

**Th:** The Fourier series of an integrable function on the circle is Abel summable to $f$ at every point of continuity. Moreover, if $f$ is continuous on the circle, then the Fourier series of $f$ is uniformly Abel summable to $f$

Additionally, we get that if $f$ has a jump discontinuity at $x$, then $$\lim_{r \to 1^-} (f*P_r)(x) = \frac{f(x^+)+f(x^-)}{2}$$
Using [[Abel's Summability#Littlewood's Tauberian Theorem|Littlewood's Tauberian Theorem]], then we get that: if $f$ is an integrable function that satisfies $\hat f(n) = O(1/|n|)$, then:
- if $f$ is continuous at $\theta$, then $$S_n(f)(\theta) \to f(\theta) \quad \text{as }n \to \infty$$
- If $f$ has a jump discontinuity at $\theta$, then $$S_n(f)(\theta) \to \frac{f(\theta^+)+f(\theta^-)}{2} \quad \text{as } n \to \infty$$
- If $f$ is continuous, then $S_n(f) \rightrightarrows f$. 
