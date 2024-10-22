---
tags:
  - RealAnalysis
  - VectorAnalysis
  - FractionalCalculus
---
Subjects: [[Real Analysis]], [[Vector Analysis]], [[Fractional Calculus]]
Links: [[Riemann Integral in R]], [[Fubini's Theorem]], [[Riemann Integral in Rn]]
Let $f$ be a continuous function on the real line. We will define $n$th repeated integral with a basepoint $a$ as

$$ f^{(-n)}(x) = \int_a^x \int_a^{\sigma_1} \cdots \int_a^{\sigma_{n-1}} f(\sigma_n) \, d\sigma_n \cdots\, d\sigma_2 \, d\sigma_1 $$

then it can be simplified as

$$ D^{-n}_af =f^{(-n)}(x) = \frac{1}{(n-1)!}\int_a^x (x-t)^{n-1} f(t) \, dt $$

This can be used to generalize the idea to fractional integrals using the gamma function.

$$ D^{-\alpha}_af = f^{(-\alpha)}(x) = \frac{1}{\Gamma(\alpha)}\int_a^x (x-t)^\alpha f(t)\, dt $$

and thus we can actually define an the fractional derivative, this is called the Reimann-Louisville fractional derivative, let $\alpha \in (0, 1)$, then

$$ D^{\alpha}_af = \frac{1}{\Gamma (1-\alpha)} \frac{d}{dx}\int_a^x \frac{f(t)}{(x-t)^\alpha} \, dt $$