---
tags:
  - FourierAnalysis
  - "#QuantumMechanics"
---
Subjects: [[Fourier Analysis]], [[Quantum Mechanics]]
Links: [[Poisson Summation Formula]], [[Fourier Transform in R]], [[Probability Functions for Random Variables]], [[Expected Value of Random Variables]], [[Variance of Random Variables]]

The basic understanding of the law, formulated in vaguest most general form, states that a function and its Fourier transform cannot both be localised.

We need a couple of things before tackling the uncertainty principle.

First let $\psi$ is a "state function" which we can assume to be in $\mathcal S(\Bbb R)$, and which is normalized according to the requirement that $$\int_{-\infty}^\infty |\psi(x)|^2\, dx = 1$$
The position of the particle is then determined not as a definite point $x$; instead its probable location is given by the rules of Quantum Mechanics as follows: 
- The probability that the particle is located in the interval $(a,b)$ is
$$\int_a ^b|\psi(x)|^2\, dx$$
We see that the *probability density* is $|\psi(x)|^2$, meaning that there is an *expectation* of where the particle might be. Then $$\overline x = \int_{-\infty}^\infty x |\psi(x)|^2\, dx $$If we can calculate is can try to calculate its variance, which in our terminology is the *uncertainty* attached to the expectation. $$\int_{-\infty}^\infty (x-\overline x)^2 |\psi(x)|^2\, dx $$
The reason that momentum is related to the Fourier transform is because of De Broglie Hypothesis, stating that the momentum of a particles is related by its wavelength by $p = \hbar k$, where $k$ is the wave number. 

We can do the same analysis, we did with position as we did with momentum. Getting that:
- The probability that the momentum $\omega$ of the particle belongs to the interval is
$$\int_a ^b|\hat\psi(x)|^2\, dx$$
where $\hat \psi$ is the Fourier transform of $\psi$.

**Th:** Suppose $\psi$ is a function in $\mathcal S(\Bbb R)$ which satisfies the normalisation condition $$\int_{-\infty}^\infty |\psi(x)|^2\, dx = 1$$. Then $$ \left(\int_{-\infty}^\infty x^2 |\psi(x)|^2\, dx \right) \left(\int_{-\infty}^\infty \omega^2 |\hat\psi(\omega)|^2\, d\omega\right) \ge \frac1{16\pi^2}$$and the equality holds iff $\psi(x) = Ae^{-Bx^2}$ where $B>0$ and $|A|^2 = \sqrt{2B/\pi}$. In fact, we have $$ \left(\int_{-\infty}^\infty (x-x_0)^2 |\psi(x)|^2\, dx \right) \left(\int_{-\infty}^\infty (\omega-\omega_0)^2 |\hat\psi(\omega)|^2\, d\omega\right) \ge \frac1{16\pi^2}$$for every $x_0, \omega_0 \in \Bbb R$. 

Suppose $f$ is continuous on $\Bbb R$. If $f$ and $\hat f$ are compactly supported then $f = 0$. This has the same spirit as the uncertainty principle. 

From this theorem, we see that the lower bound for the product of the uncertainty of the position and the uncertainty of the momentum has a lower bound of $1/16\pi^2$. This result is actually incomplete since it has been rescaled to change the units of measurements. The proper physical conclusion is $$\sigma^2_x \sigma²_p \ge \frac{h²}{16\pi^2}$$or in more standard form: $$ \sigma_x \sigma_p \ge \frac{\hbar}{2}$$where $h$ is Planck's constant, and $\hbar$ is the reduced Planck's constant.

The heuristic assertion stated before can be made precise as follows. If $F$ is a function on $\Bbb R$, then we say that the preponderance of its mass is contained in an interval $I$ (centred at the origin) if $$\int_I x^2 |F(x)|^2 \, dx \ge \frac1{2} \int_\Bbb R x^2|F(x)|^2\, dx$$With $f\in \mathcal S(\Bbb R)$, then this inequality holds for $f$ and $\hat f$ with their respective intervals $I_1$ and $I_2$. If $L_j$ denotes the length of $I_j$, we have that $$L_1 L_2 \ge \frac1{2\pi}$$
A similar conclusion holds if the interval are not necessarily centred at the origin

# Operators

The Heisenberg uncertainty principle can be formulated in terms of the operator $L = - \frac{d^2}{dx^2}+x^2$, which acts on Schwarz functions by the formula $$L(f) = - \frac{d^2f}{dx^2} + x^2 f$$This operator, sometimes called the *Hermite operator* is the quantum analogue of the harmonic oscillator. 

We have that the Heisenberg uncertainty principle implies that for all $f\in \mathcal S$, $$(Lf, f) \ge (f, f)$$
This is usually denoted by $L \ge I$

The operators $A$ and $A^*$ defined on $\mathcal S$ by $$ A(f) = \frac{df}{dx}+xf\qquad A^*(f) = - \frac{df}{dx}+xf$$
The operators $A$ and $A^*$ sometimes called the *annihilation* and *creation* operators, respectively. They have the following properties, for all $f, g\in \mathcal S$:
- $(Af, g) = (f, A^* g)$
- $(Af, Af) = (A^* A f, f) \ge 0$
- $A^* A = L-I$
This shows again that $L \ge I$

