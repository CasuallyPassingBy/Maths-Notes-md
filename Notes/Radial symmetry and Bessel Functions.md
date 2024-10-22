---
tags:
  - FourierAnalysis
---
Subjects: [[Fourier Analysis]]
Links: [[Fourier Transform in Rn]], [[Bessel Functions]]

An important property of the Fourier transform, being that the Fourier transform of a radial function is radial. In other words, if $f(x) = f_0(\|x\|)$ for some $f_0$, then $\hat f(\omega) = F_0(\omega)$ for some $F_0$. A natural problem is to determine a relation between $f_0$ and $F_0$

For $n = 1$,  we get the formula $$F_0(x) = 2 \int_0^\infty \cos(2\pi x r) f_0
(r)\, dr$$
and for $n = 3$, the relation between $f_0$ and $F_0$ is also quite simple and given by the formula: $$F_0(\rho) = 2\rho^{-1} \int_0^\infty \sin(2\pi \rho r)f_0(r)\, dr $$
As for the case of $n = 2$, we get the relation between $f_0$ and $F_0$ being given by the not so simple formula: $$F_0(\rho) = 2\pi \int_0^\infty J_0(2\pi r\rho)f_0(r)r\, dr$$
Getting the general formula for $n$ dimensional, is a bit more complicated and i found out that can be obtained using [[Change of Variable Theorem in Rn#In $ Bbb R n$|hyperspherical coordinates]], We get the formula $$F_0 (\rho) = 2\pi \rho^{-(n/2)+1} \int_0^\infty J_{(n/2)-1}(2\pi \rho r) f_0(r) e^{n/2}\, dr $$
Using the $(n/2)-1$ order Bessel function of the first kind.
