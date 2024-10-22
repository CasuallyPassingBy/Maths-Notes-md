---
tags:
  - RealAnalysis
---
Subjects: [[Real Analysis]]
Links: [[Improper Integrals in R]]

The *Cauchy Principal value* is a is a method for assigning values to certain improper integrals which would otherwise be undefined.
#### For a singularity at a finite number b
We can also define over singularities. Let $a < b< c$, where $b$ is a difficult point at which the behaviour of the $f$ is such that
$$
\int_a^b f(x)\, dx = \pm \infty
$$
for any $a< b$, and 
$$
\int_b^c f(x)\,dx =\mp \infty
$$
Then we can define the Cauchy Principle value for a singularity at a finite number $b$, as 
$$
\text{p.v.}\int_a^c f(x)\,dx=\lim_{\varepsilon\to 0^+} \left[\int_a^{b-\varepsilon} f(x)\ dx +\int_{b+\varepsilon}^c f(x)\right] 
$$
#### For a singularity at $\infty$

The *Cauchy principle Value* at infinity is defined as:

$$ \text{p.v.}\int_\Bbb Rf=\lim_{x\to\infty}\int_{-x}^xf $$
where 
$$
\int_{-\infty}^0 f(x)\, dx = \pm \infty
$$
and 
$$
\int_0^\infty f(x)\, dx = \mp\infty
$$In the special case that: $f:\Bbb R\to\Bbb R$, if $\int_\Bbb R f$ exists, then:

$$ \text{p.v.}\int_\Bbb R f=\int_\Bbb R f $$

In some cases it is necessary to deal simultaneously with singularities both at a finite number $b$ and at infinity. This is usually done by a limit of the form 
$$
\lim_{\;\eta \to 0^+}\, \lim_{\;\varepsilon \to 0^+} \,\left[\,\int_{b - \frac{1}{\eta}}^{b - \varepsilon} f(x)\,dx \,~ + ~ \int_{b+\varepsilon}^{b + \frac{1}{\eta}} f(x)\,dx \,\right].
$$

In those cases where the integral may be split into two independent, finite limits,
$$
\lim_{\; \varepsilon\to 0^+\;} \, \left|\,\int_a^{b-\varepsilon} f(x)\,dx \,\right|\; < \;\infty
$$
and 
$$
\lim_{\;\eta\to 0^+}\;\left|\,\int_{b+\eta}^c f(x)\,dx \,\right| \; < \; \infty
$$
According to the my Complex Analysis by Paez:
Given a function $f:\Bbb R\{x_1, \dots, x_n\} \to \Bbb R$ such that $x_k <x_{k+1}$ for $k \in\{1, \dots, n-1\}$ and $f$ is not bounded for any neighbourhood around $x_k$, and integrable over any interval $[c, d] \subseteq \Bbb R\setminus\{x_1, \dots, x_n\}$, we define the *Cauchy principal value* of the integral $\int_\Bbb R f$ as
$$
\text{p.v.} \int_{-\infty}^\infty f(x)\, dx = \lim_{\alpha\to\infty}\left(\int\limits_{-\alpha}^{x_1-1/\alpha}f(x)\,dx + \sum_{k = 1}^n\int\limits_{x_k+1/\alpha}^{x_{k+1}-1/\alpha}f(x)\,dx +\int\limits_{x_k+1/\alpha}^\alpha f(x)\, dx\right) 
$$
which can be the same from the definition from wikipedia but don't know how. 

Calculating the Cauchy principal value can be useful, since if $f$ is even and integrable over any interval in $\Bbb R$ we get that
$$
\int_{0}^\infty f(x)\,dx = \lim_{\alpha \to \infty} \int_{0}^ \alpha f(x)\,dx = \frac{1}{2}\lim_{\alpha \to \infty} \int_{-\alpha}^ \alpha f(x)\,dx= \frac{1}{2}\text{p.v.} \int_{-\infty}^\infty f(x)\, dx
$$