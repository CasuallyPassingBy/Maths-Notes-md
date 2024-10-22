---
tags:
  - ComplexAnalysis
---
Subjects: [[Complex Analysis]]
Links: [[Complex Numbers]]
### The $\exp$ function

********Def:******** Let $z = x+yi$, then

$$ \exp(z)=e^z := e^x(\cos y + i \sin y) $$

******************Prop:****************** Properties of $\exp(z)$

- $e^{z+w} = e^z e^w$ for all $z, w \in \Bbb C$
- $e^z$ is never $0$
- If $x$ is real, then $e^x >1$ when $x>0$, and $0< e^x<1$ when $x<0$
- $|e^{x+yi}|= e^x$
- $e^z$ is periodic; each period for $e^z$ has the form $2\pi ni$, for some integer $n$
- $e^z =1$ iff $z = 2\pi ni$ for some integer $n$

### The trigonometric functions

**********Def:********** The complex sine and cosine functions are defined by

$$ \cos z = \frac{e^{iz} + e^{-iz}}{2} \quad \text{ and } \quad \sin z = \frac{e^{iz} - e^{-iz}}{2i} $$

### Logarithm

********Prop:******** Let $A_{y_0}$ denote the set of complex numbers $x+iy$ such that $y_0\le y < y_0+2\pi$; symbolically,

$$ L_{y_0} = \{x+iy \mid x \in \R, y_0 \le y < y_0 + 2\pi\} $$

Then $\exp$ maps $L_{y_0}$ bijectively to $\Bbb C^*$

******************Def:****************** The function $\ln:\Bbb{C^* \to C}$ with range $y_0 \le \Im(\ln z) < y_0 + 2\pi$, is defned by

$$ \ln z = \ln |z| +i \arg z $$

where $\arg z$ takes values in the interval $[y_0, y_0+2\pi)$ and $\ln|z|$ is the usual logarithm of the positive number $|z|$. When we want to specify the branch of the logarithm we write as $\ln_{y_0}$

**********Prop:********** The logarithm $\ln$ is the inverse of $\exp$ in the followin sense: For any branch of $\ln$ , we have that $\exp(\ln z)=z$, and if we choose the branch lying in $y_0 \le y < y_0+2\pi$, then $\ln(\exp(z)) = z$ for $z = x+iy$ and $y_0 \le y < y_0+2\pi$

****Prop:**** Let $z_1, z_2 \in \Bbb C^*$, then $\ln(z_1 z_2) = \ln (z_1)+\ln(z_2)$ (up to the additional of integral multiples of $2\pi i$).

### Complex Exponential

**************Def:************** Let $a, b \in \Bbb C$ with $a \ne 0$. Then $a^b$ is defined to be $\exp(b\ln a)$; it is understood that some interval $[y_0, y_0 +2\pi)$, the branch of $\ln$, has been chosen within which $\arg$ function takes its value.

********Prop:******** Let $a,b \in \Bbb C$, with $a\ne 0$. Then $a^b$ is singled value iff $b$ is an integer. If $b$ is real and a rational number, $b = p/q$ is its lowest terms, than $a^b$ has exactly $q$ distinct values, namely, the $q$ roots of $a^p$. If $b$ is real an irrational or if $b$ has nonzero imaginary part, then $a^b$ has infinitely many values. When $a^b$ has distinct values, these values differ by factors of the form $\exp(2\pi nbi)$.

### The $n$th root function

**********Def:********** Let $n \in \N$, then the $n$th function is defined by

$$ \sqrt[n]{z} = z ^\frac{1}{n} = \exp \left(\frac{\ln z}{n}\right) $$

for a specific choice of branch of $\ln z$; with this choice, $\sqrt[n]{z} = \exp((\ln z)/n)$ is called a ****branch**** of the $n$th root function.

********************Prop:******************** The functions $\sqrt[n]z$ so defined so defined is an $n$th root of $z$; that is, $(\sqrt[n] z)^n =z$. It is obtained as follows. If $z = re^{i\theta}$, then

$$ \sqrt[n]z = \sqrt[n] r e^{i\theta /n} $$

Consecuently we need to define the branches of $\sqrt[n]{z}$, and let $\alpha\in \R$, then the set

$$ A_{\alpha, n} :=\{r(\cos \theta + i\sin\theta ) \in \Bbb C \mid \alpha \le \theta < \alpha +2\pi, r >0\} $$