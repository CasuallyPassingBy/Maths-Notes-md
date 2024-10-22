---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Residue Theorem]], [[Riemann Integral in R]], [[Contour Integrals in C]], [[Cauchy Principal Value in R]]

# Strategy 1
The first type we will analyse are of a certain form: $R(x, y)$ which is a rational function on the real variables $x$ and $y$, which is defined for any pair $(x, y)\in \Bbb R^2$  such that $x^2+y^2 =1$. Meaning we will solve  integrals of the form
$$
\int_0^{2\pi} R(\cos(\theta), \sin(\theta))\, d\theta
$$
If we make $\gamma(\theta) = \exp(\theta i)$, we can actually get that
$$
\frac{1}{\gamma(\theta)} = \exp(-\theta i)
$$
Meaning that
$$
\cos(\theta ) = \frac{1}{2}\left(\gamma(\theta)+\frac{1}{\gamma(\theta)}\right) \qquad \text{ and } \qquad 
\sin(\theta ) = \frac{1}{2i}\left(\gamma(\theta)-\frac{1}{\gamma(\theta)}\right)
$$
and 
$$
\gamma'(\theta) = i \exp(\theta i) = i\gamma(\theta)
$$
with this we can actually get that
$$
\int_0^{2\pi }R(\cos(\theta), \sin(\theta))\, d\theta = \int_0^{2\pi} R\left(\frac{1}{2}\left(\gamma(\theta)+\frac{1}{\gamma(\theta)}\right),\frac{1}{2i}\left(\gamma(\theta)-\frac{1}{\gamma(\theta)}\right) \right)\frac{1}{i\gamma(\theta)}\gamma'(\theta)\, d\theta
$$

This can be simplified as
$$
\oint_\gamma R\left(\frac{1}{2}\left(z+\frac{1}{z}\right), \frac{1}{2i}\left(z-\frac{1}{z}\right)\right)\frac{1}{iz}\, dz
$$
With this in mind, we can make a substitution, and define
$$
f(z) = R\left(\frac{1}{2}\left(z+\frac{1}{z}\right), \frac{1}{2i}\left(z-\frac{1}{z}\right)\right)\frac{1}{iz}
$$
Then
$$
\int_0^{2\pi} R(\cos(\theta), \sin(\theta))\, d\theta = \oint_\gamma f(z)\, dz = 2\pi i\sum_{k = 1}^n \text{Res}(f, z_k)
$$where $z_1, \dots, z_n$ are the poles of $f$ inside of $B(0,1)$.

# Strategy 2
The other type of integral are of the type
$$
\int_{-\infty}^\infty R(x)\, dx
$$
where $R = p/q$ is a rational function such that the degree of $q$ is at least two times the degree of $p$, $R$ has a $0$ at $\infty$ of order $2$ or equal, and doesn't has any poles in the real line. From this hypothesis we can assure that $r>0$ is sufficiently big, there's $M>0$ such that
$$|R(z)|\le \frac{M}{|z|^2}$$
if $|z| \ge r|$. With this we can assure that
$$
\int_{-\infty}^\infty R(x)\, dx < \infty 
$$
then we can calculate this as
$$
\int_{-\infty}^\infty R(x)\, dx = \lim_{r\to \infty}\int_{-r}^r R(x)\, dx
$$
Now we will consider $\gamma$ a piecewise smooth closed curve formed by the pieces $\gamma_1(x)= x$, with $x\in[-r, r]$ and the semicircle parametrized by $\gamma_2(t) = re^{it}$ with $t\in [0, \pi]$. We can choose $r>0$ sufficiently big such that all the poles of $R$ are contained in the disk $B(0, r)$. 
![[Pasted image 20240118183035.png]]

With this we can use the Residue Theorem
$$
\int_{\gamma_1} R(z)\, dz +\int_{\gamma_2} R(z)\, dz=\oint_\gamma R(z)\, dz = 2\pi i \sum_{k =1}^n \text{Res}(R, z_k)
$$
where $z_1, \dots, z_n$ are the poles of $R$ contained in the upper semiplane, i.e. $\Im (z)>0$ for $k \in \{1, \dots, n\}$.  Calculating the first integrals we get that
$$
\int_{\gamma_1} R(z)\,dz +\int_{\gamma_2}R(z)\, dz = \int_{-r}^r R(x)\, dx + \int_0^\pi R(re^{it})ire^{it}\, dt
$$
If we prove that 
$$
\lim_{r\to \infty} \int_{0}^\pi R(re^{it}) ire^{it}\, dt = 0
$$
Then we can calculate the integral. 
Since 
$$
\left|\int_{0}^\pi R(re^{it})ire^{it}\, dt\right| \le \int_0^\pi |R(re^{it})|r \, dt \le \frac{M}{r}\pi
$$
Thus 
$$
\lim_{r\to \infty} \int_{0}^\pi R(re^{it}) ire^{it}\, dt = 0
$$
And finally we see that
$$
\int_{-\infty}^\infty R(x)\, dx = \lim_{r\to \infty} \oint_\gamma f(z)\, dz = 2\pi i \sum_{\Im (z_k) >0} \text{Res}(R, z_k)
$$
where $z_1, \dots, z_n$ are the poles on the upper semiplane of $R$
# Strategy 3
A type of integral that is related to the the type above, are of the form
$$
\int_{-\infty}^\infty R(x)\cos(x)\, dx \qquad \text{ and } \qquad \int_{-\infty}^\infty R(x)\sin(x)\,dx
$$
where we need that $R$ has a $0$ at $\infty$ of at least order $2$, and without any poles in the real line. Then we can calculate both integrals by calculating
$$
\int_{-\infty}^\infty R(x) e^{ix}\, dx
$$
We can call $f(z) = R(z)e^{iz}$
Since the real part has the $\cos$ and the imaginary part has the $\sin$. This integral always exists since $|R(x) e^{ix}| = |R(x)|$ for all $x\in \Bbb R$, and we have that
$$
\int_{-\infty}^\infty f(x)\, dx = \lim_{r\to \infty} \int_{-r}^r f(x)\, dx
$$
Then we can use the same contour as the one above. Let $\gamma$ a piecewise smooth closed curve formed by the pieces $\gamma_1(x)= x$, with $x\in[-r, r]$ and the semicircle parametrized by $\gamma_2(t) = re^{it}$ with $t\in [0, \pi]$, and get
$$
\int_{\gamma_1} f(z)\, dz + \int_{\gamma_2} f(z)\, dz = \oint_{\gamma} f(z)\, dz = 2\pi i \sum_{\Im (z_k)> 0} \text{Res}(f, z_k)
$$
where $z_1, \dots, z_n$ are the poles on the upper semiplane of $f$

With basically the same argument as above we can check that
$$
\lim_{r\to \infty} \int_{\gamma_2}f(z)\, dz =0
$$
with this we get that
$$
\int_{-\infty}^\infty f(x)\, dx = \lim_{r\to \infty} \int_{-r}^r f(x)\, dx = 2\pi i \sum_{\Im(z_k)>0 } \text{Res}(f, z_k)
$$
where $z_1, \dots, z_n$ are the poles on the upper semiplane of $f$
# Strategy 4
Given a function $f:\Bbb R\{x_1, \dots, x_n\} \to \Bbb R$ such that $x_k <x_{k+1}$ for $k \in\{1, \dots, n-1\}$ and $f$ is not bounded for any neighbourhood around $x_k$, and integrable over any interval $[c, d] \subseteq \Bbb R\setminus\{x_1, \dots, x_n\}$, we define the *Cauchy principal value* of the integral $\int_\Bbb R f$ as
$$
\text{p.v.} \int_{-\infty}^\infty f(x)\, dx = \lim_{\alpha\to\infty}\left(\int\limits_{-\alpha}^{x_1-1/\alpha}f(x)\,dx + \sum_{k = 1}^n\int\limits_{x_k+1/\alpha}^{x_{k+1}-1/\alpha}f(x)\,dx +\int\limits_{x_k+1/\alpha}^\alpha f(x)\, dx\right) 
$$

We will now use the residue theorem to to calculate 
$$
\text{v.p.}\int_{-\infty}^\infty R(x)\sin(ax)\, dx \quad \text{and}\quad \text{v.p.}\int_{-\infty}^\infty R(x)\cos(ax)\, dx 
$$

With $a>0$ and $R$ being a rational function that has a $0$ of degree at least $1$ at $\infty$, and poles of order $1$ in the real line. for this method we will suppose that $R$ only has a pole of order $1$ at $z=0$.  

We are going to integrate over this contour. We are going to integrate over $\gamma_\alpha$, that goes from $[1/\alpha, \alpha]$, $[\alpha, \alpha+i\alpha]$, $[\alpha+i\alpha, -\alpha+i\alpha]$, $[-\alpha, -1/\alpha]$ and then the lower semi circle joining $-1/\alpha$ and $1/\alpha$, for $\alpha>1$.

![[Pasted image 20240118182937.png]]
We can actually choose a sufficiently large $\alpha$ such that we can have all poles of $R$ are contained inside the contour, that lie inside the upper semiplane. Let $f(z) = R(z)e^{iaz}$ . Then
 $$
 \oint_{\gamma_\alpha} f(z)\, dz = 2\pi i \left(\sum_{\Im(z_k)>0} \text{Res}(f, z_k) + \text{Res} (f, 0)\right)
 $$
where $z_1, \dots, z_n$ are the poles of $f$ in the upper semiplane. If we calculate
$$
 \begin{align*}
	 \oint_{\gamma_\alpha}f(z)\,dz =& \int_{1/\alpha}^\alpha f(x)\, dx + \int_0^\alpha f(\alpha+ix )i\, dx - \int_{-{\alpha}}^\alpha f(x+i\alpha)\, dx \\
	 &-\int_0^\alpha f(-\alpha +ix)i\, dx +\int_{-\alpha}^{1/\alpha}f(x)\, dx +\int_{\tilde \gamma_\alpha} f(z)\, dz
 \end{align*}
$$
By the restrictions we have in $R$, we know there are $M, r>0$, such that if $|z|\ge r$
 $$
 |R(z)| \le \frac{M}{z}
 $$
If $r\le \alpha$, we can actually bound the integral along the edges by terms that go to $0$ as $\alpha \to \infty$. Meaning we only only need to take care of the integral along the lower semicircle.

Here we use the fact that, that the pole at $z= 0$ is only of order $1$. Then we can actually use Laurent Series, and make the decomposition
$$
f(z) = \frac{B}{z} + \phi(z)
$$
where $\phi$ is analytic. This is true for some neighbourhood, and we just take $\alpha$ big enough such that $\tilde \gamma_\alpha$ is inside that neighbourhood. With $\tilde \gamma_\alpha(t) = (1/\alpha)e^{it}$, with $t\in [\pi, 2\\pi]$. Then we get that:
$$
\int_{\tilde \gamma_\alpha} f(z)\, dz = \int_{\tilde \gamma_\alpha} \frac{B}{z}\, dz + \int_{\tilde \gamma_\alpha} \phi(z)\,dz 
$$
From the first integral we get the value of $B\pi i$, and for the second one we can actually bound it, since by being analytic it is bounded in a smaller neighbourhood. Then we get that 
$$
\begin{align*}
\left|\int_{\tilde \gamma_\alpha} \phi(z)\, dz\right| &\le \int_{\tilde \gamma_\alpha} |\phi(z)|\, |dz| \\
&\le M' \int_{\tilde \gamma_\alpha}\, |dz| = M' \pi(1/\alpha)
\end{align*}
$$
Which we can see that tends to $0$ as $\alpha \to \infty$. Then we get that we get that
$$
\begin{align*}
	2\pi i \left(\sum_{\Im(z_k)>0}\text{Res}(f, z_k) + \text{Res}(f, 0)\right) &= \\
	&= \lim_{\alpha\to \infty } \oint_{\gamma_\alpha} f(z)\,dz \\
	=& \left(\text{v.p.}\int_{-\infty}R(x)\cos(ax)\, dx\right) +\\
	&i\left(\text{v.p.}\int_{-\infty}R(x)\sin(ax)\, dx\right) +\\
	&+\pi i\text{Res}(f, 0)
\end{align*}
$$
Finally we get that
$$
\begin{align*}
	\left(\text{v.p.}\int_{-\infty}R(x)\cos(ax)\, dx\right) +i \left(\text{v.p.}\int_{-\infty}R(x)\sin(ax)\, dx\right)  \\
	=2\pi i \sum_{\Im(z_k)>0} \text{Res}(f, z_k) + \pi i \text{Res}(f, 0)
\end{align*}
$$

We get that in general, we get that if $R$ has poles of order $1$ at $x_1< x_2 < \dots < x_n$, and a $0$ of order at least $1$ at $\infty$, Then 
$$
\begin{align*}
	\left(\text{v.p.}\int_{-\infty}R(x)\cos(ax)\, dx\right) +i \left(\text{v.p.}\int_{-\infty}R(x)\sin(ax)\, dx\right)  \\
	=2\pi i \sum_{\Im(z_k)>0} \text{Res}(f, z_k) + \pi i \sum_{k = 1}^n\text{Res}(f, x_k)
\end{align*}
$$
where $f(z) = R(z)e^{iaz}$.
Lastly we If we have that $R$ has no real poles, and a $0$ at $\infty$, then 
$$
\begin{align*}
	\left(\text{v.p.}\int_{-\infty}R(x)\cos(ax)\, dx\right) +i \left(\text{v.p.}\int_{-\infty}R(x)\sin(ax)\, dx\right) 
	=2\pi i \sum_{\Im(z_k)>0} \text{Res}(f, z_k) 
\end{align*}
$$
# Strategy 5
The last type of integral we will solve are of the form
$$
\int_0^\infty x^aR(x)'\, dx
$$
with $0 < a <1$ and $R$ is a rational function that has a $0$ of at least order $2$ at $\infty$, without any poles in the real axis, except possibly a pole of order $1$ at $x=0$.

We will use different branches of logarithm to define $z^a$, in particular
$$
z^a=\exp(a\ln_0(z))
$$
where 
$$
\ln_0(z) = \ln|z| + i\theta
$$
with $0 < \theta(z) < 2\pi$ and $z \in \Bbb C\{x  \in \Bbb R\mid x \ge 0\}$

We will know take the piecewise smooth closed curve $\gamma$ given by $\gamma = \gamma_1-\gamma_2-\gamma_3+\gamma_4$, in which, $\gamma_1(t)= re^{it}$, with $t \in [1/n, 2\pi -1/n]$ and $n \in \Bbb N$; $\gamma_2(t) = te^{i(2\pi 1/n)}$, with $t\in [\delta, r]$, and $0 <\delta < r$; $\gamma_3(t)= \delta e^{it}$ with $t\in [1/n, 2\pi -1/n]$ and $\gamma_4(t) = te^{i/n}$. 

![[Pasted image 20240118230317.png]]
This picture is wrong since $\gamma_1$ and $\gamma_3$ are wrongly directed according to the parametrization above.

We can choose $r$ and $n$, sufficiently big and $\delta$ sufficiently small, that we can assure that all the poles of $R$ trapped by $\gamma$, then by the Residue Theorem we get, with $f(z) = z^aR(z)$
$$
\oint_\gamma f(z)\, dz = 2\pi i \sum_{k =1}^n \text{Res}(f, z_k)
$$
where $z_1, \dots, z_n$ are poles of $R$ contained in $\Bbb C\setminus \Bbb R^{\ge 0}$. 

We need to explore what happens when $r, n\to \infty$ and $\delta\to 0^+$. We can actually bound the integrals over $\gamma_1$ and $\gamma_3$ with things that tend to $0$ as $r\to \infty$ and $\delta\to 0^+$. Then we only need to see what happens with $\gamma_2$ and $\gamma_4$. 

We can look at the function 
$$
g(x,y)= x^a \exp(ia (2\pi -y))R(xe^{i(2\pi-y)})
$$
is continuous on $[\delta, r] \times [-\eta, \eta]$ for some $\eta >0$. Then it is uniformly continuous and the functions
$$
h_n(x) = x^a\exp(ia(2\pi -1/n))R(xe^{i(2\pi -1/n)})
$$
converges uniformly to the function
$$
h(x) = x^ae^{2\pi i a} R(x)
$$
Then we get that
$$
\lim_{n \to \infty}\int_{\gamma_2}z^a R(z)\, dz  = \lim_{n \to \infty}\int_\delta ^r h_n (x)\, dx = \int_\delta ^r h(x)\, dx
$$
Similarly we get that
$$
\lim_{n \to \infty} \int_{\gamma_4} f(z)\, dz = \lim_{n \to \infty} \int_{\delta}^r t^a\exp(i a/n)R(te^{i/n})\, dt = \int_\delta ^r t^aR(t)\, dt 
$$
Then we get the equation, as the $r\to \infty$ and $\delta\to 0^+$. 
$$
	2\pi i \sum_{k = 1}^n \text{Res}(f, z_k) = (1-e^{2\pi i a}) \int_0^\infty x^aR(x)\,dx
$$
The we get that
$$
\int_0^\infty x^aR(x)\,dx = \frac{2\pi i}{1-e^{2\pi i a}} \sum_{k = 1}^n \text{Res}(f, z_k)
$$
where $f(z) = z^aR(z)$ and $z_1,\dots, z_n$ are the poles of $R$. 